# How to get KSM

The Kusama network is Polkadot's R&D network. This guide will walk you through how to proceed with claiming KSM (Kusama tokens).

In order to align Kusama with the existing DOT holders and community, if you are a DOT allocation holder you can claim the equivalent amount of Kusama tokens (ticker: KSM). There are two ways to claim either before genesis by sending a transaction on Ethereum or after genesis by signing a message using your allocation key and making a transaction on Kusama.

## Step 1. Create a Kusama account

You will need a Kusama account to claim the KSM. There are a few ways you can create one. For most users, we recommend using the [Polkadot UI](https://polkadot.js.org/apps/#/explorer) since it will allow you to store your encrypted keyfile locally.

> NOTICE: Unfortunately at this time Kusama and Substrate chains do not have hardware wallet support using the Ledger or Trezor products. Hopefully soon this will change!

Another option you may consider using are `subkey` commandline utility which will allow you to be extra secure and generate your key on an air-gapped device. A couple other options include using Enzyme in-browser wallet (like MetaMask) or the Polkawallet mobile wallet.

### Using Polkadot UI

1. Navigate to the [Polkadot UI Account's Tab](https://polkadot.js.org/apps/#/accounts) and click on the `Add account` button.

<img src="../img/polkadotui-find-the-accounts-page.png" width=50% />

2. Enter a name for your account and create a secure password. This password will be used to decrypt your account.

<img src="../img/polkadotui-create-your-account.png" width=50% />

3. Ignore the advanced options unless you want to change the type of cryptography used for your keys (either sr25519 or ed25519 works).

4. Click `Save` and `Create and backup account`.

5. Save your encrypted keystore locally.

6. The account now appears in your Accounts tab and is backed up to the keystore you just saved.

7. Click on the DOT identicon to copy the address to the clipboard.
<img src="../img/polkadotui-copy-account-address.png" width=50% />

### Using `subkey`

1. Follow the build instructions for [Substrate](https://github.com/paritytech/substrate#6-building).
2. When building, instead of building all of the binaries only build `subkey` by typing `cargo build subkey`.
3. You can build / use the subkey on a computer that is not connected to the internet for added security.
4. The command `subkey generate` will generate a new keypair.

### Using Enzyme browser wallet (Chrome only)

1. Install the Enzyme browser wallet from the [Chrome store](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh). Click `Add to Chrome` and confirm by clicking `Add extension` in the popup window.

2. Accept the Terms of Use.

<img src="../img/enzyme-open-the-extension.png" width=50% />

3. Make a strong password and make sure to write it down in another place, then click `Create`.

<img src="../img/enzyme-choose-a-password.png" width=50% />

4. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../img/enzyme-generate-seed-phrase.png" width=50% />

5. Click `Dashboard`.

6. Click the DOT identicon to copy your address to clipboard.

<img src="../img/enzyme-copy-your-address.png" width=50% />

### Using Polkawallet

1. Install [Polkawallet](https://polkawallet.io). Click Download and select the link corresponding to the platform you are using. On android you may need to allow installing apps from external sources. On iOS, you may need to "trust" Polkawallet in the General>Profiles & Device Management > Enterprise App Section before running the app.

2. Once opening the app, copy the seed phrase and store it in a safe place, don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../img/polkawallet-create-account.jpg" width=50% />

3. Name your account and make a strong password, make sure to write it down in another place, then click Save.

4. You will be asked to confirm your seed phrase - this is to make sure you have copied it somewhere safe.

5. Click on the pink QR Code symbol, and select Copy address to copy your address to clipboard.

<img src="../img/polkawallet-accounts-page.jpg" width=50% />
<img src="../img/polkawallet-copy-address.jpg" width=50% />


## Step 2. Get KSM tokens

There are two methods to claim KSM.

**1. Dot Holders:**
Those who participated in the Polkadot sales can claim a proportional amount of KSM prior to the launch of the network. 

You can do this through [this claims process](https://claim.kusama.network/).

You can refer to [this detailed guide](./dot-holders.md) for a step by step walk through for how to do so.

Having trouble? Get support in the KSM [Claims chat](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders).

**2. Faucet:**
For those who didn’t participate in the Polkadot sale, KSM are publicly available after genesis through a faucet. Find out more [here](./faucet.md).

Public projects that need more KSM can request them by emailing projects@kusama.network.
