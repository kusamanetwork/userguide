# Secure Validator Setup

Over the last year, we have started to see a number of projects moving from PoW to PoS, which creates a whole new industry for running a staking business. In some sense, running a validator is like operating a cryptocurrency exchange because the underlying staked asset could potentially be worth millions of dollars. Thus, as a node operator you have to maintain a heightened security level for your validator, as well as have a robust network architecture to make sure that the value at stake is not at risk of being lost. 

There are many different ways to architect your network infrastructure. The two common slashing situations are server downtime and equivocation (i.e., double signing). The amount of effort spent to achieve these goals is dependent on what level of security you need - someone with a few thousand dollars behind their validator is going to have a different threat model to someone with several million. It also encourages everyone to come up with their own designs to avoid being hacked in the same way as other validators.

That being said, there are some common tips and techniques that will be useful for anyone interested in running a validator. We will first go through some existing validator architecture designs and then look into each area individually.

## Existing approaches (Cosmos, Tezos, etc.)

We will focus on the design of the network architecture in this section. No matter what kind of validators you are trying to run, they will have a similar network design, so we will take Cosmos as a reference. 

The simplest approach would have only a validator node running without any firewall, with the p2p port accessible from the internet. This means that anyone can know the IP address of the node, which is not ideal and opens additional attack vectors.

The second approach is to include a firewall in front of the validator. This means that it can use the firewall to do deep package inspection, which can prevent attacks on the level of e.g. SYN-Floods. One disadvantage of this setup is that validators always have a possibility to go down, so when your node has an outage or is otherwise unreachable, it could cause the validator to be slashed. Another problem is that it does not have Denial-of-Service (DoS) resistance, which means that it could easily be attacked in this manner. You can read more about this layered network architecture [here](#layered-network-architecture).

Another approach would be to separate the network architecture into two layers; the first having "sentry" nodes facing the Internet that hides the validator entirely to the public, and the second consisting of the validator sitting in a firewalled private network only accessible by the sentry nodes. This approach is an effective way to mitigate DDoS attacks by deploying multiple sentry nodes on different cloud environments. You can also add an additional layer of private sentry nodes as a middle layer, in order to increase separation between the public sentry nodes and validators.

Unfortunately, this design still has an availability problem when the validator is down. One can mitigate this by deploying an additional validator to support the [High Availability (HA)](#high-availability-(optional)) feature. This way, even if one of your validators goes down, there is a backup validator that can replace it, thus mitigating potential slashing from unresponsiveness. Of course, if both your primary and secondary validators are nonresponsive, you will still be slashed. Thus, your primary and secondary validators should be, at a minimum, geographically separate, but you can vary other aspects (e.g. operating system, hardware, service provider) to help ensure that both validator nodes are unlikely to go down at the same time.

Besides these architectural decisions, there are some approaches to improve key management by making it unavailable to potential intrusions in the validator servers. These approaches include using Hardware Security Modules (HSM) for Cosmos' suggested list of HSMs that support ed25519). Cosmos also introduced a Key Management System (KMS) which has a unified API to support validators that manage their key from different sources like HSM and have double signing protection. It is recommended to host the KMS on another machine to have better security and risk management. This helps to ensure that your system does not have a single point of failure. Remember that an active validator must be up and running 24/7 in order to avoid slashing; this means that malicious users can attempt to attack your validator at all times!

There is a great article about a [Cosmos validator's architecture](https://iqlusion.blog/a-look-inside-our-validator-architecture) written by Tony Arcieri and Shella Stephens.

## Layered Network Architecture

The concept of a layered network architecture is discussed in a post in the [Cosmos forum](https://forum.cosmos.network/t/sentry-node-architecture-overview/454). The goal is to mitigate the effect of a DDoS attack by running multiple public full nodes on different cloud providers, and making those nodes the only way to talk to the validator. The validator itself is secured behind a firewall or private network.

The public "sentry" nodes can run on cloud providers; they won't have any stake at risk, and if they are down for a while they can be replaced shortly without any disruption to the validator's work. It would also be interesting to run the public nodes in different providers/availability regions, so that the validator is not affected by any individual provider outages. That said, there are other solutions to mitigate DDoS attack - we encourage everyone to build up their own designs, to avoid homogeneity.

## High Availability (Optional)

A validator node must be up and running 24/7, with as close as possible to 100% uptime. If an active validator becomes unreachable, then it would cause a portion of that validator's stake to be slashed.

By setting up HA, you could make your validator more robust than a single validator node. Even if one of your validators fails to connect, you still have another to participate in the validation process.

Below are two examples of a high availability set-up:

### Active - Standby
Imagine there are two validators, one is active and the other one would be on standby (failover). We can keep track of the heartbeat of the active one, and in the case of a problem, the standby will take over immediately. It is important to make sure these two are configured in the same way. Whatever you change in the active, must also be changed in the standby.

### Active - Active
Imagine we add a load balancer to connect these two validators, and it has an algorithm to decide which validator should execute an operation. It may use a round-robin algorithm or some other algorithm, but it should very carefully ensure that there is no equivocation (double signing), as two validators are running simultaneously with the same validator key.

Either of these approaches is valid; choosing one depends entirely on what you want to achieve.

## Hardware Security Module (HSM)

An [HSM](https://en.wikipedia.org/wiki/Hardware_security_module) is a hardware component for storing your keys inside a tamper-proof, secure element that is never exposed to the file system of your machine during signing. This makes it extremely hard for an attacker to extract the private key. If your validator stores the secret keys in a plain-text format on the same machine, your keys would be easily exposed if your validator is hacked. At this point, the attacker can perform double signing to cause your validator's stake to be slashed. It is important to find a hardware component that is dedicated to storing your keys.

Currently, there are a few types of HSMs available on the market. [YubiHSM2](https://www.yubico.com/products/yubihsm/) is the most widely used in Cosmos validators because it supports the Ed25519 curve. VBefore choosing a CloudHSM, you should check whether the necessary curve is available or not. For example, at the time of writing, the only CloudHSM that supports Ed25519 is Microsoft Azure.

That said, validators are managing millions of dollars worth of assets, and so storing your keys on a CloudHSM is not recommended. When you use a CloudHSM, you trust the solution provider, so consider how much you support the provider when you decide to set up a secure validator with CloudHSM. Moreover, compared with YubiHSM2, it costs more than $3,000 per month, which is relatively expensive if you are using [Azure](https://azure.microsoft.com/en-in/pricing/details/azure-dedicated-hsm/).

Another possibility is to use a custom remote signing server, which offers a similar level of security. With this setup, a separate server is set up that acts as the single system that does the signing.

If you want to verify that your architecture and general setup are secure, you can also have a third party audit your setup and publish the result.

### "Hacking" HSM PEM keys for Tezos

[https://blog.polychainlabs.com/tezos/2019/05/28/encoding-tezos-ec-keys.html](https://blog.polychainlabs.com/tezos/2019/05/28/encoding-tezos-ec-keys.html)

## Monitoring Tools

- [Telemetry](https://github.com/paritytech/substrate-telemetry) This tracks your node details including the version you are running, block height, CPU & memory usage, block propagation time, etc.  

- [Prometheus](https://prometheus.io/) based monitoring stack, including [Grafana](https://grafana.com) for dashboards and log aggregation. It includes alerting, querying, visualization, and monitoring features, and works for both cloud and on-premise systems. The data from substrate-telemetry can be made available to Prometheus through exporters like [this](https://github.com/w3f/substrate-telemetry-exporter).

## Linux Best Practices

- Never use the root user.
- Always update the security patches for your OS.
- Enable and set up a firewall.
- Never allow password-based SSH, only use key-based access.
- Disable non-essential SSH subsystems (banner, motd, scp, X11 forwarding) and harden your SSH configuration ([reasonable guide to begin with](https://stribika.github.io/2015/01/04/secure-secure-shell.html)).
- Back up your storage regularly.

## Conclusions

* We should not expose validators to the public internet, they should only be accessible by allowed parties. Therefore, we propose a layered approach in which the validators are isolated from the internet and connect to the Polkadot network via an intermediate layer of public-facing nodes.

* At the moment, Polkadot/Substrate can't interact with HSM/SGX, so we need to provide the signing key seeds to the validator machine. This key is kept in memory for signing operations and persisted to disk (encrypted with a password).

* Given that HA setups would always be at risk of double-signing and there's currently no built-in mechanism to prevent it, we propose having a single instance of the validator to avoid slashing. Slashing penalties for being offline are much less than those for equivocation.

### Validators 

* Validators should only run the Polkadot binary, and they should not listen on any port other than the configured p2p port.

* Validators should run on bare-metal machines, as opposed to VMs. This will prevent some of the availability issues with cloud providers, along with potential attacks from other VMs on the same hardware. The provisioning of the validator machine should be automated and defined in code. This code should be kept in private version control, reviewed, audited, and tested.

* Signing and node keys should be provided in a secure way.

* Polkadot should be started at boot and restarted if stopped for any reason (supervisor process).

* Polkadot should run as non-root user.

* Each validator should connect to the Polkadot network through a set of at least 2 public-facing nodes. The connection is done through a VPN and the machine can't access the public internet, thus the only possible connection is through the VPN.

### Public Facing Nodes

* At least two nodes associated with each validator run on at least two different cloud providers and they only publicly expose the p2p port.

* They can run as a container on Kubernetes and we can define the desired state (number of replicas always up, network and storage settings); the connection between the validator and the public-facing nodes is done through a VPN. They have the common kubernetes security setup in place (restrictive service account, pod security policy and network policy).

* Node keys should be provided in a secure way.

* Only run the Polkadot container, no additional services. The VPN agent should run on a sidecar in the same pod (sharing the same network stack).

### Monitoring

* Public-facing nodes and the validator should be monitored and alerts set for several failure conditions defined.

* There should be an on-call rotation for managing the alerts.

* There should be a clear runbook with actions to perform for each level of each alert and an escalation policy.

## References

[https://medium.com/figment-networks/full-disclosure-figments-cosmos-validator-infrastructure-3bc707283967](https://medium.com/figment-networks/full-disclosure-figments-cosmos-validator-infrastructure-3bc707283967)

[https://kb.certus.one/](https://kb.certus.one/)

[https://github.com/slowmist/eos-bp-nodes-security-checklist](https://github.com/slowmist/eos-bp-nodes-security-checklist)

[https://forum.cosmos.network/t/sentry-node-architecture-overview/454](https://forum.cosmos.network/t/sentry-node-architecture-overview/454)

[https://medium.com/loom-network/hsm-policies-and-the-importance-of-validator-security-ec8a4cc1b6f](https://medium.com/loom-network/hsm-policies-and-the-importance-of-validator-security-ec8a4cc1b6f)
