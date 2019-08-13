# Governance

Governance of Kusama follows the same basic philosophy as the [planned governance for Polkadot](https://polkadot.network/a-walkthrough-of-polkadots-governance/).

## Kusama Genesis Governance

The original governance of Kusama is composed of three bodies:

1) **The Referendum Chamber** - The broadest and most powerful body of Kusama governance. It is composed of an assembly of KSM holders, weighted by amount of tokens held and voluntary [lock-commitment](https://wiki.polkadot.network/en/latest/polkadot/node/governance/#voluntary-locking).  
2) **The Council** - Members of this body are elected through [approval voting](https://wiki.polkadot.network/en/latest/polkadot/node/governance/#how-to-be-a-council-member) of KSM holders, weighted by the number of tokens controlled.
3) **The Technical Committee** - Membership is composed according to a single vote for all teams that have successfully and independently implemented or formally specified one of the two halves of the Polkadot/Kusama protocol. A majority vote of the council controls membership of the technical committee.

## Participating in Kusama Governance

You can participate in Kusama governance by making proposals, voting on referenda, and voting for council members. Kusama currently has a basic governance UI, found at [polkadot.js.org/apps/#/democracy](https://polkadot.js.org/apps/#/democracy). You will need KSM to participate in Kusama governance.

### Public Discussion

Discuss governance proposals on the [forum](https://forum.kusama.network/). 

### Where can I see current and past proposals?

You can see active proposals you can vote on the [Polkadot UI](https://polkadot.js.org/apps/#/democracy). Viewing past proposals is not currently supported, but we will update this when we add that feature. 

### Viewing active referenda

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Democracy tab](https://polkadot.js.org/apps/#/democracy) to see currently active proposals.

Proposals currently last 28,800 blocks which equates to approximately 48 hours. You can find out more details on proposals in the [Kusama forum](https://forum.kusama.network/).

### Voting on active referenda

Voting on proposals in the Referendum chamber lasts 28 days and, if approved, then a further 30 days are waited before the change comes into force.

Prerequisites:
- Have a KSM account.
- Have KSM tokens.
- Note that KSM tokens will be **locked** during the duration of the referendum.
- If you vote `aye` for a proposal and it passes, your tokens will be **locked** until the proposal has been enacted (30 days for Kusama Genesis Governance).

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings)
2. Navigate to the [Democracy tab](https://polkadot.js.org/apps/#/democracy) to see currently active proposals.
3. Note the proposal index number, and find out more details about the proposal in the [Kusama forum](https://forum.kusama.network/). 
4. Head over to the (Extrinsics tab)[https://polkadot.js.org/apps/#/extrinsics], select the account you wish to vote with, and select `democracy` under "submit the following extrinsic." Choose `vote(ref_index,vote)` in the second column, enter the proposal index you noted down in step 3 and vote `aye` to support the proposal, and `nay` to vote against it.

All the tokens in the account you selected will be **locked** until the referendum ends. If you voted `aye` and the proposal has passed, your tokens will be locked until the proposal has been enacted in thirty days. It is recommended that you do **not** vote with the entirety of your KSM, as your tokens will be locked up for some time, so you should create a voting account and transfer the amount of KSM you want to vote with before voting. 

### Voting for council members

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings).
2. Navigate to the [Council tab](https://polkadot.js.org/apps/#/council) to see current council candidates.
3. In the [Kusama forum](https://forum.kusama.network/), you will find a thread dedicated to council members proposing their candidacy and find out more information.
4. Head over to the [Extrinsics tab](https://polkadot.js.org/apps/#/extrinsics), select the account you wish to vote with, and select `council` under "submit the following extrinsic." Choose `setApprovals(votes, index)` in the second column, enter the council index of the candidate you wish to vote for, and select `yes` to support the candidate, and `nay` to vote against it.
5. Click `Submit transaction` and sign the transaction.

### Submit oneself as a council candidate

1. Using the [Polkadot UI](https://polkadot.js.org/apps/), make sure you have an account and selected the Kusama network under the [settings tab](https://polkadot.js.org/apps/#/settings).
2. Navigate to the [Council tab](https://polkadot.js.org/apps/#/council) to see current council candidates.
3. In the [Kusama forum](https://forum.kusama.network/), you will find a thread dedicated to council members proposing their candidacy and find out more information. Add your account number, reasons for being a suitable council member and any further information you want to share.
4. Head over to the [Extrinsics tab](https://polkadot.js.org/apps/#/extrinsics), select the account you wish to vote with, and select `council` under "submit the following extrinsic." Choose `submitCandidacy(slot)` in the second column and select the slot you prefer to be in.
5. Click `Submit transaction` and sign the transaction.
