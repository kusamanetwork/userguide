# How to get KSMA

The Kusama network is Polkadot's R&D network. This guide will walk you through how to proceed with claiming KSMA (Kusama tokens).

In order to align Kusama with the existing DOT holders and community, if you are a DOT allocation holder you can claim the equivalent amount of Kusama tokens (ticker: KSMA). There are two ways to claim either before genesis by sending a transaction on Ethereum or after genesis by signing a message using your allocation key and making a transaction on Kusama.

## Step 1. Create a Kusama account

You will need a Kusama account to claim the KSMA. There are a few ways you can create one. For most users, we recommend using the [Polkadot UI](https://polkadot.js.org/apps/#/explorer) since it will allow you to store your encrypted keyfile locally.

> NOTICE: Unfortunately at this time Kusama and Substrate chains do not have hardware wallet support using the Ledger or Trezor products. Hopefully soon this will change!

Another option you may consider using are `subkey` commandline utility which will allow you to be extra secure and generate your key on an air-gapped device. A couple other options include using Enzyme in-browser wallet (like MetaMask) or the Polkawallet mobile wallet.


### Using polkadot{.js} extension (Chrome or Firefox)

1. Install the polkadot{.js} extension from the [Chrome store](//TODO) or [Firefox store](https://addons.mozilla.org/en-US/firefox/addon/polkadot-js-extension/).
1. Create a new account by clicking on `I want to create a new account with a new seed`.
1. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or want to import your account again.
1. Enter a name for the account and type a strong password (at least 6 characters).
1. Click on `Add the account with the generated seed`.
1. You can copy the account's address to the clipboard by clicking on its identicon.

### Using `subkey`

1. Follow the build instructions for [Substrate](https://github.com/paritytech/substrate#6-building).
2. When building, instead of building all of the binaries only build `subkey` by typing `cargo build subkey`.
3. You can build / use the subkey on a computer that is not connected to the internet for added security.
4. The command `subkey generate` will generate a new keypair.

### Using Polkadot UI

1. Navigate to the [Polkadot UI Account's Tab](https://polkadot.js.org/apps/#/accounts) and click on the `Add account` button.
2. Enter a name for your account and create a secure password. This password will be used to decrypt your account.
3. Ignore the advanced options unless you want to change the type of cryptography used for your keys (either sr25519 or ed25519 works).
4. Click `Save` and `Create and backup account`.
5. Save your encrypted keystore locally.
6. The account now appears in your Accounts tab and is backed up to the keystore you just saved.
7. Click on the DOT identicon to copy the address to the clipboard.

### Using Enzyme browser wallet (Chrome only)

1. Install the Enzyme browser wallet from the [Chrome store](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh). Click `Add to Chrome` and confirm by clicking `Add extension` in the popup window.
2. Accept the Terms of Use.
3. Make a strong password and make sure to write it down in another place, then click `Create`.
4. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.
5. Click `Dashboard`.
6. Click the DOT identicon to copy your address to clipboard.

### Polkawallet

TODO


## Step 2. Get KSMA tokens

There are two methods to claim KSMA.

**1. Dot Holders:**
Those who participated in the Polkadot sales can claim a proportional amount of KSMA prior to the launch of the network. 

You can do this through [this claims process](https://claims.kusama.network/).

You can refer to [this detailed guide](./method1.md) for a step by step walk through for how to do so.

Having trouble? Get support in the KSMA [Claims chat](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders).

**2. Faucet:**
For those who didn’t participate in the Polkadot sale, KSMA are publicly available upon genesis through a faucet. Find out more [here](./method2.md).

Public projects that need more KSMA can request them by emailing projects@kusama.network.
