# Kusama transition to PoS

Kusama network started as a Proof-of-Authority network and will be transitioned to Proof-of-Stake on 28 October, 2019 at approximately 18:43 Zurich time (CET) with the first validator set rotation happening at approximately 22:43 CET.

## Rollout plan

The rollout of full functionality of Kusama is staggered to allow for safe transition. The first PoS phase will
begin with 20 validators. Nine of the initial validators will be ran by Web3 Foundation, six will be ran by Parity Technologies and five will be ran by highly staked
community members as voted in by the phragmen election.

When the initial transition is successful, additional validator spots will be opened 10 at a time
in order to allow for more validators to enter the active set.

When the first transition to PoS takes place, the full functionality of Kusama is not fully available. Notably,
the Sudo key will still exist and be used to initiate further upgrades, and balance transfers will still be disabled
for a short while. It is expected that the full functionality of Kusama will be enabled shortly, granted that no issues
arise and a smooth transition takes place.

## For Validators

For validators, it is important that you ensure you're running the latest client code in archive mode. You will need to
resync your node with the `--pruning=archive` flag on, and ensure that your session keys have been properly configured.
If you need any guidance, please see the [validator guide](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-validate-kusama)
for full details.
