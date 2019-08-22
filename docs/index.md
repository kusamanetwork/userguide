# Kusama Network: User Guide
![Expect Chaos](./img/Kusama-expect-chaos.png)

## What is Kusama?
Kusama is a canary network for developers to run experiments in a Polkadot-like environment. Think of Kusama as an early proving ground for things like upgradeable runtimes, on-chain governance, and parachains. 

Have fun on Kusama! Explore the politics, hone your validator setup, campaign for the council, or vie for a parachain spot. And most of all... expect chaos.

Kusama is owned by the folks who hold Kusama tokens (KSM). There’s no central kill switch. The community rules the network through on-chain governance. 

Security caveat: Kusama is experimental! There are no guarantees. 

## Who can participate in Kusama?

Everyone!

Those who participated in the Polkadot sales can claim a proportional amount of KSM through [this claims process](https://kusama.network/newsletter).

For those who didn’t participate in the Polkadot sale, KSM are publicly available after genesis through a faucet. Find out more here.

Public projects that need more KSM can request them by emailing projects@kusama.network.

As a KSM holder, you will be able to interact with all the features of Kusama network such as staking (validating and nominating), participating in governance, voting for council members, parachain auctions and all other interactions.

## What's the Kusama timeline?
*The following launch timeline features approximate dates, [sign up for the newsletter](https://kusama.network/) to get updated on the latest.*

### Phase 0: Pre-launch Claims
`Ending: 23 August, 2019 9:30 am Zurich time`

During this period you can pre-claim your KSMs via [this Ethereum DApp](https://claim.kusama.network).

After this period, you will no longer be possible to claim KSM via Ethereum, i.e. after Ethereum block `8405350` (approx 9:30 am Zurich time).

### Phase 1: Soft Launch (PoA)
`Approximate date: 23 August, 2019`

Kusama will initially launch as a Proof of Authority (PoA) network by Web3 Foundation. During this period, most network functionality will be disabled. This period  ensures further internal testing and development of logic.

#### Validating
During this period, validators should signal their intent to validate on Kusama by bonding KSM or by nominating.

#### Claiming
Additionally, Dot holders who have not claimed their KSM yet, can do so via the on-chain [claims](https://github.com/paritytech/polkadot/blob/3b54276ee02bc2451749dc3d64e586303989b34f/runtime/src/claims.rs) module (instructions coming soon).

**Note**: You will NOT be able to most other on-chain activities like `transfer balance`, `earn block rewards`, `participate in governance`, etc. at this time.

### Phase 2: Public Network (PoS)
`Approximate date: 1-4 weeks after Soft Launch`

The Web3 Foundation will issue a final runtime upgrade to take Kusama from PoA into a decentralised PoS network. 

After this, all features will be enabled. Most importantly, validating, governance and balance transfers will be functionally live on Kusama. There will also be a public faucet to distribute KSM at this point.
