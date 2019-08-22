# 通过水龙头(Faucet)里取Kusama(KSM)代币
## 获取 KSM 简介

任何人也可以在 Kusama 正式发布后通过水龙头获取KSM。与测试网络代币不同的是，我们希望 KSM 成为一种稀缺资源和水龙头旨在有限地分配代币给每个人。
 
为了被免女巫攻击，水龙头只会向在2019年6月21日之前注册的Github帐户发送。如果你没有在该日期前注册，请使用[此表格](https://docs.google.com/forms/d/e/1FAIpQLSfGAqjXY3xLokwl7A-R4JZAnrBnSI3BVXKMKDLCKVtHaxgs-w/formResponse)提交申请获取 KSM 代币。

### 要求:

- Github 帐号需要在 2019 年 6 月 21 日之前注册
- 用户使用该地址必须是之前没有接收过 KSM
- 每24小时只能获取一次
- 地址需要含`ksma` (不用区分大小写)

### 第一步: 生成地址

水龙头只会发送到含有 `ksma` 字串的地址 (不用区分大小写 `KSMA` 或 `kSmA` 也没有问题)。它不会发送 KSM 到同一个地址两次，所以每次用户要求 KSM 代币时，必须使用新地址。

取得有效地址需要生成大量地址，直到找到一个符合要求。你可以想象是个细小的工作量证明。你可以使用[Subkey](#使用-Subkey)，[PolkadotJS Dashboard](#使用-PolkadotJS-Dashboard)或任何其他能够生成任意地址的程序。如果你喜欢，你可以自己编写。

#### 使用 PolkadotJS Dashboard

1. 前往 [Settings](https://polkadot.js.org/apps/#/settings) 并在 "address network prefix" 选单中选择 `Kusama (canary)`，再按下 `Save & Reload`。
![](https://i.imgur.com/ABFP18c.png)

2. 在 [Accounts](https://polkadot.js.org/apps/#/accounts) 页面，选择`Vanity Address` 标签。
![](https://i.imgur.com/tiGnTzS.png)

3. 之后在 "search for" 栏输入 `ksma` 并使用 "keypair crypto type" 的预设值，之后再按下 `Start generation`。这样大概需要10分钟生成你想要的地址格式。
![](https://i.imgur.com/M9L1cIS.png)

#### 使用 Subkey

#### 安裝

你可以使用以下指令安装 `subkey`:
```
cargo install --force --git https://github.com/paritytech/substrate subkey
```
或者编译源代码`subkey`。

1. 按照 [Substrate](https://github.com/paritytech/substrate#6-building) 说明进行操作.
2. 编译時，只需要输入 `cargo build -p subkey` 编译 `subkey`
3. 可执行档案在  `./target/debug/subkey`

#### 使用方法

执行 `subkey --network kusama vanity "ksma"` 会生成新的钥匙对地址并含有 `ksma`。

具体时间取决于你的计算机硬件配置和运气，运算可能需要几秒到大约10分钟。

```
$ subkey --network kusama vanity "ksma"
  Generating key containing pattern 'ksma'
  100000 keys searched; best is 190/237 complete
  200000 keys searched; best is 201/237 complete
  300000 keys searched; best is 207/237 complete
  ...
  1000000 keys searched; best is 225/237 complete
  2000000 keys searched; best is 225/237 complete
  best: 237 == top: 237
  Secret Key URI `0x6262bcafcf6e6abbea102a2dbafecb81c28e9737e2cbce3d3ead7bde47806ac4` is account:
  Public key (hex): 0xe6a979d75da9241c491f12b7e7c2cf015ba9202a4be4649a15b72a3a60e0e730
  Address (SS58): Hnksmako1TfL4rsVMnT798syHFdF8rtFQT3tNF4jqLdswZD
```

`Address (SS58)` 是将用来获取 KSM 的 Kusama 地址。请注意，字串`ksma`从第三个字元开始，由于 `Secret Key` 掌控你的资金，所以请永远不要把它分享给其它人。

查看 [`subkey` 文档](https://substrate.dev/docs/en/ecosystem/subkey)或输入`subkey --help` 了解更多用法例子。

### 第二步: 提交 Issue

当你生成好含有 `ksma` 的 Kusama 地址后，你可以在水龙头里获取 KSM。

1. 登入 Github，并前往 Kusama 网络的[水龙头库](https://github.com/kusamanetwork/faucet/issues)
2. 按下 Issues 标签，再按下 "New Issue"。
3. 在 "Title" 上输入任何文字也可以，它会被忽略。
4. 在 "Leave a comment" 输入你在第一步生成的 Kusama 地址(必须含有 "ksma")。只需填下地址，没有其他。再按下 "Submit new issue"。 
5. 现在你只需要等待水龙头处理你的请求。
具体时间取决于网络因素和服务器负载，有可能需要数分钟，但是普遍能在30秒内完成。
8. 你会在 "Issue" 里看到是否成功或失败的留言。成功指 0.1 KSM 经已发送到你填下的地址，而失败是指有错误发生和没有发送 KSM 到该地址 (例如水龙头短缺、地址错误等等)。
9. 当你看到回覆后，不论成功与否，"Issue" 会自动关闭。

### 注意:

- 每个 Github 帐号在24小时内只能获取 0.1 KSM
- 记住只填上 _地址_，没有其它文字及绝对不會是你的种子或助记词
- 一开始每日最多发放的(_所有用戶_) KSM 数量是 10 KSM (*这可能将来會更改*)

### 捐助:

如果你想支持水龙头，欢迎发送 KSM 到以下地址 ****EFWaoKxTJ5kJvjNDytcXqPZKHXPc6NhTYZXmYczNZdw2Auf****
我们将会利用这些捐助定期充值水龙头钱包。

### 支援:

如果你有技术问题，请前往[Kusama Watercooler chat](https://riot.w3f.tech/#/room/#kusamawatercooler:polkadot.builders)发问并将会有人帮助你。