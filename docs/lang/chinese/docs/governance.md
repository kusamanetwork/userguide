# 治理

Kusama 的治理遵循与 [Polkadot 治理的计划](https://polkadot.network/a-walkthrough-of-polkadots-governance/)有着相同的基本理念。

## Kusama 创世纪治理

最初 Kusama 的治理由三个部份组成：

1）**The Referendum Chamber** - Kusama 治理最广泛，最强大的机构。它由 KSM 持有人组成，按持有的代币数量和自愿[锁定承诺加权](https://wiki.polkadot.network/en/latest/polkadot/node/governance/#voluntary-locking)。

2）**The Council** - 成员通过 KSM 持有人 [approval voting](https://wiki.polkadot.network/en/latest/polkadot/node/governance/#how-to-be-a-council-member) 选出，并按受控代币的数量加权。

3）**The Technical Committee** - @TODO

## 参与 Kusama 治理

你可以通过提出建议，对公投进行投票以及为议会成员投票来参与 Kusama 治理。Kusama 目前有一个基本的治理界面，你可在 [polkadot.js.org/apps/#/democracy](https://polkadot.js.org/apps/#/democracy) 找到，并需要 KSM 参与 Kusama 的治理。

### 公开讨论

在[论坛](https://forum.kusama.network/)上讨论治理提案

### 我在哪里可以看到当前和过去的提案？

你可以在 [Polkadot UI](https://polkadot.js.org/apps/#/democracy) 看到生效中的提案和投票。目前暂时不支持查看过去的提案，但当我们添加该功能时并会对其进行更新。

### 查看生效中的公投

1. 使用 [Polkadot UI](https://polkadot.js.org/apps/)，确保你拥有一个帐号并在[设置选项](https://polkadot.js.org/apps/#/settings)下选择 Kusama 网络
2. 前往 [Democracy 选项](https://polkadot.js.org/apps/#/democracy)查看当前生效中的提案。

目前提案将持续 28,800 区块，相当于约 48 小时。 你可以在 [Kusama 论坛](https://forum.kusama.network/)上找到有关提案的更多详细资料。

### 在生效中的提案上投票

The Referendum Chamber 的投票将会持续 28 天，如果获得批准，则在变更生效前等待 30 天。

条件:  
- 拥有 KSM 帐号。  
- 拥有 KSM 代币。  
- 请注意，KSM 代币将在公投期间被**锁起**。
- 如果你投票赞成提案并且通过，你的代币将被**锁起**，直到提案實行(Kusama 创世纪定为30天)。

1. 使用 [Polkadot UI](https://polkadot.js.org/apps/)，确保你拥有一个帐號并在[设置选项](https://polkadot.js.org/apps/#/settings)下选择 Kusama 网络
2. 前往到 [Democracy 选项](https://polkadot.js.org/apps/#/democracy)查看当前生效中的的提案。
3. 请注意提案索引编号，并在 [Kusama 论坛](https://forum.kusama.network/)中查找有关该提案的更多详细信息。
4. 前往 [Extrinsics tab](https://polkadot.js.org/apps/#/extrinsics)，选择你要投票的帐號，并在 "submit the following extrinsic." 下选择 `democracy`。 在第二列中选择投票 `vote(ref_index,vote)`，输入你在步骤3中记下的提案索引，并投票 `aye` 支持该提案，或投票 `nay` 反对该提案 。

你选择帐号中的所有代币将被**锁起**，直到公投结束。如果你投 `aye` 并且提案已通过，则你的代币将被锁起，直到该提案在 30 天内生效。建议你不要对整个 KSM 进行投票，因为你的代币将被锁起一段时间，因此你应该在投票前创建一个投票账户并转移你想投票的 KSM 数量。

### 为议会成员投票

1. 使用 [Polkadot UI](https://polkadot.js.org/apps/)，确保你拥有一个帐号并在[设置选项](https://polkadot.js.org/apps/#/settings)下选择了 Kusama 网络。
2. 前往到 [Council 选项](https://polkadot.js.org/apps/#/council)以查看当前的议会候选人。
3. 在 [Kusama 论坛](https://forum.kusama.network/)，你会找到一个致力于议会成员提出候选资格并找到更多资料的主题。
4. 前往 [Extrinsics 选项](https://polkadot.js.org/apps/#/extrinsics)，选择你要投票的帐号，然后在 "submit the following extrinsic" 下选择 `council`。 在第二列中选择 `setApprovals(votes, index)`，输入你希望投票的候选人的议会索引，并选择 `aye` 以支持该候选人，或选择 `nay` 反对该候选人。
5. 点击 `Submit transaction` 并签署交易。

### 提交自己作为议会候选人

1. 使用 [Polkadot UI](https://polkadot.js.org/apps/)，确保你拥有一个帐号并在[设置选项](https://polkadot.js.org/apps/#/settings)下选择了 Kusama 网络。
2. 前往 [Council 选项](https://polkadot.js.org/apps/#/council)以查看当前的议会候选人。
3. 在 [Kusama 论坛](https://forum.kusama.network/)，你会找到一个致力于议会成员提出候选资格并找到更多资料的主题。 添加你的帐号，为什么你合适成为议会成员的理由以及你想分享任何进一步的资料。
4. 前往 [Extrinsics 选项](https://polkadot.js.org/apps/#/extrinsics)，选择你要投票的帐號，然后在 "submit the following extrinsic." 下选择 `council`。 在第二列中选择 `submitCandidacy(slot)`，然后选择你喜欢的插槽。
5. 點击 `Submit transaction` 并签署交易。