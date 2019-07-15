# Participating in Kusama Governance

This guide will help you participate in Kusama governance by  voting on referenda, and voting for council members. Before being able to participate, you will need to create a KSMA account and acquire KSMA tokens. 

## Viewing active referenda

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Democracy tab](https://polkadot.js.org/apps/#/democracy) to see currently active proposals.

Proposals currently last 28,800 blocks which equates to approximately 48 hours. You can find out more details on proposals in the [Kusama forum](https://forum.kusama.network/).

## Voting on active referenda

Prerequisites:
- Have a KSMA account
- Have KSMA tokens
- Note that KSMA tokens will be **locked** during the duration of the referendum
- If you vote `aye` for a proposal and it passes, your tokens will be **locked** until the proposal has been enacted

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Democracy tab](https://polkadot.js.org/apps/#/democracy) to see currently active proposals.
3. Note the proposal index number, and find out more details about the proposal in the [Kusama forum](https://forum.kusama.network/). 
4. Head over to the (Extrinsics tab)[https://polkadot.js.org/apps/#/extrinsics], select the account you wish to vote with, and select `democracy` under "submit the following extrinsic." Choose `vote(ref_index,vote)` in the second column, enter the proposal index you noted down in step 3 and vote `aye` to support the proposal, and `nay` to vote against it.

All the tokens in the account you selected will be **locked** until the referendum ends. If you voted `aye` and the proposal has passed, your tokens will be locked until the proposal has been enacted. It is recommended that you do **not** vote with the entirety of your KSMA, as your tokens will be locked up for some time, so you should create a voting account and transfer the amount of KSMA you want to vote with before voting. 

## Voting for council members

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Council tab](https://polkadot.js.org/apps/#/council) to see current council candidates.
3. In the [Kusama forum](https://forum.kusama.network/), you will find a thread dedicated to council members proposing their candidacy and find out more information.
4. Head over to the [Extrinsics tab](https://polkadot.js.org/apps/#/extrinsics), select the account you wish to vote with, and select `council` under "submit the following extrinsic." Choose `setApprovals(votes, index)` in the second column, enter the council index of the candidate you wish to vote for, and select `yes` to support the candidate, and `nay` to vote against it.
5. Click `Submit transaction` and sign the transaction.

## Submit oneself as a council candidate

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Council tab](https://polkadot.js.org/apps/#/council) to see current council candidates.
3. In the [Kusama forum](https://forum.kusama.network/), you will find a thread dedicated to council members proposing their candidacy and find out more information. Add your account number, reasons for being a suitable council member and any further information you want to share.
4. Head over to the (Extrinsics tab)[https://polkadot.js.org/apps/#/extrinsics], select the account you wish to vote with, and select `council` under "submit the following extrinsic." Choose `submitCandidacy(slot)` in the second column and select the slot you prefer to be in.
5. Click `Submit transaction` and sign the transaction.
