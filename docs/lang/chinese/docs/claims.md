# 领取 KSM

Kusama 在发布之前和之后也有不同的方式来领取 KSMs。

Kusama 经已在 2019 年 8 月 23 日非正式发布。

现在你能使用持有 DOT 的以太坊地址直接通过 Kusama 网络上换取 KSM 到你的 Kusama 帐号，过程只需要简单签署信息。

### 一. 生成 Kusama 地址

你可以通过几种方法创建 Kusama 地址。对于大多数用户，我们建议使用Polkadot UI，因为它允许储密钥到电脑。

> 注意：不幸的是，现时 Kusama 没有硬件钱包支持。希望这会很快改变！

你可以考虑使用的另一个选项 `subkey` 命令行程序，它允许你采取额外步骤来保护密钥的安全。此外，另外两个选项包括 Enzyme 钱包浏览器扩展和 Polkawallet 移动钱包，虽然这些需要额外的步骤来生成 Kusama 地址。

使用 Polkadot UI

1. 打开 [Polkadot UI](https://polkadot.js.org/apps) 并前往到 `Settings` 选项，在 `address network prefix` 选择 Kusama（canary)。再按下 "Save & Reload"。

2. 前往 [Polkadot UI Accounts](https://polkadot.js.org/apps/#/accounts) 选项，然后按下 `Add account` 按钮。

![polkadotui-find-the-accounts-page](../../../../img/polkadotui-find-the-accounts-page.png)

3. 输入帐户名称 并 設定密码。 此密码将用于解鎖你的帐號。

![polkadotui-create-your-account](../../../../img/polkadotui-create-your-account.png)

4. 忽略高级选项，除非你想更改密钥的加密类型（我们建议使用 "Schnorrkel（sr25519)")。

5. 按下 `Save` 并且 `Create and backup account`。

6. 保存你的密钥在本地。

7. 该帐户现在显示在 "Accounts" 标签。

8. 按下 DOT 图标将地址复制到剪贴板。

![polkadotui-copy-account-address](../../../../img/polkadotui-copy-account-address.png)

### 二. 使用 MyCrypto

首先前往 [MyCrypto](https://download.mycrypto.com/) 下载你使用的操作系统版本。之后再前往 Polkadot JS [Claims 程序](https://polkadot.js.org/apps/#/claims)，选择你在第一步创建好的帐号。

![Claim Step 1](../../../../img/claim/claim-1.png)

然后你会一个信息（`Pay KSMs to the Kusama account: .......`，你只需要复制这个信息，再通过 MyCrypto 使用你拥有 DOT 的以太坊地址签名这个信息。

![Claim Step 2](../../../../img/claim/claim-2.png)

当你按 "Sign Message"，你将获得如下所示的 JSON 输出:

![Claim Step 3](../../../../img/claim/claim_3.png)

最后把签名信息贴回 Claims 程序，按下 `Confirm claim` 即可完成。

![Claim Step 4](../../../../img/claim/claim-3.png)]

按下 "Redeem"，此时，如果一切正常，你将看到成功消息，并且你的 KSM 将在你的帐户中。 恭喜你现在可以参与 Kusama 网络，例如[治理](./governance.md)和[抵押](./staking.md)。另外在非正式发布期间，转帐 KSM 将不能使用。

![Claim Step 4](../../../../img/claim/claim-4.png)]

### 核对

當你领取 KSM 后，Polkadot UI 余额將會立即更新。

### 需要协助？

请加入 [Claim Support](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders) Riot 频道。

### 使用第三方领取

**我们不建议使用第三方应用程序或流程来领取 KSM**

使用第三方程序可能会导致你的分配丢失，因此我们不建议你使用任何第三方应用程序。







