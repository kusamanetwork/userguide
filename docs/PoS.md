# Kusama transition to PoS

Kusama network started as a Proof-of-Authority network and was transitioned to Proof-of-Stake on 28 October 2019 at approximately 18:43 Zurich time (CET). The first successful validator set rotation took place at 22:45 CET.

## Rollout plan

The rollout of full functionality of Kusama is staggered to allow for a safe transition. The first PoS phase will begin with 20 validators. Of the 20, the Web3 Foundation will run nine and Parity Technologies will run six. Five will be run by highly staked community members as voted in by the phragmen election.

When the initial transition is successful, additional validator spots will be opened 10 at a time
in order to allow for more validators to enter the active set.

When the first transition to PoS takes place, the full functionality of Kusama is not fully available. Notably,
the Sudo key will still exist and be used to initiate further upgrades, and balance transfers will still be disabled
for a short while. It is expected that the full functionality of Kusama will be enabled shortly, granted that no issues
arise and a smooth transition takes place.

## For Validators

For validators, it is important that you ensure you're running the latest client code in archive mode. You will need to
resync your node with the `--pruning=archive` flag on and ensure that your session keys have been properly configured.
If you need any guidance, please see the [validator guide](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-validate-kusama)
for full details.
