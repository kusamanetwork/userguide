# How to get KSM

The Kusama network is Polkadot's experimental community-focused R&D network. If you hold the DOT indicator token you are entitled to claim an equivalent amount of KSM on the Kusama network. This is so that the Kusama network is aligned with the existing DOT holders and community.

The two ways to claim the KSM depends on whether you are claiming before or after the Kusama genesis. Since Kusama has not launched at the time of writing this guide, it will only cover the first case: claiming by sending a transaction on Ethereum with the key holding  DOT indicator tokens. After Kusama genesis, it will be updated to cover the second case: claiming by signing a message with the key holding DOT indicator tokens.

## Step 1. Create a Kusama account

You will need to generate a Kusama account to claim KSM. There are a few ways you can create one. 

For most users, we recommend using the [Polkadot UI](https://polkadot.js.org/apps/#/explorer) since it will allow you to store your encrypted keystore locally.

> NOTICE: Unfortunately at this time Kusama does not have hardware wallet support using the Ledger or Trezor products. Hopefully soon this will change!

Another option you may consider using is the `subkey` commandline utility which will allow you to be extra secure and generate your key on an air-gapped device. Additional two other options include the Enzyme browser extension wallet or the Polkawallet mobile wallet. But these require an extra step to make into Kusama addresses.

### Using Polkadot UI

1. Open up the [Polkadot UI](https://polkadot.js.org/apps) and navigate to the `Settings` tab. Find the configuration dropdown for `address network prefix` and select `Kusama (canary)`. Click `Save and reload`.

1. Navigate to the [Polkadot UI Account's Tab](https://polkadot.js.org/apps/#/accounts) and click on the `Add account` button.

<img src="../../img/polkadotui-find-the-accounts-page.png" width=50% />

2. Enter a name for your account and create a secure password. This password will be used to decrypt your account.

<img src="../../img/polkadotui-create-your-account.png" width=50% />

3. Ignore the advanced options unless you want to change the type of cryptography used for your keys (either sr25519 or ed25519 works).

4. Click `Save` and `Create and backup account`.

5. Save your encrypted keystore locally.

6. The account now appears in your Accounts tab and is backed up to the keystore you just saved.

7. Click on the DOT identicon to copy the address to the clipboard.
<img src="../../img/polkadotui-copy-account-address.png" width=50% />

### Using `subkey`

#### Installation

You can install `subkey` with this one-line command:

```
cargo install --force --git https://github.com/paritytech/substrate subkey
```

Alternatively, you can build `subkey` from the source code.

1. Follow the build instructions for [Substrate](https://github.com/paritytech/substrate#6-building).
2. When building, instead of building all of the binaries, only build `subkey` by typing `cargo build -p subkey`.

#### Usage

You can use subkey on a computer that is not connected to the internet for added security.

The command `subkey generate` will generate a new keypair. If you want to be more secure, use 24 words, `subkey generate --words 24`.

```
$ subkey generate
Secret phrase `robust mass coconut rocket mean runway wall check tennis update mixed raise` is account:
  Secret seed: 0x8152195386e1add616700e1d55e1ac1e63f68bd4bbcd6228ffca3da284db3f40
  Public key (hex): 0xf8fb1fe5040e3ee3d8ab4b444e2124498cf932d6b5c9544b2e86bec19507532f
  Address (SS58): 5HhALDcW6EabKJoXMPV6RdhDzSXiMiUrh1qnjQbVufqAHg3z
```

The `Public key (hex)` field is what you should use to claim your KSM tokens. Never share your `Secret phrase` or `Secret seed`, as these can both control your funds. (NOTE: Your Kusama address will be different than the one display by `subkey`. To see your Kusama address see the section [Getting Kusama address from Substrate or Polkadot address](#kusama-from-substrate-address)).

See the [`subkey` documentation](https://substrate.dev/docs/en/ecosystem/subkey) for more usage examples.

### Using Enzyme browser wallet (Chrome only)

1. Install the Enzyme browser wallet from the [Chrome store](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh). Click `Add to Chrome` and confirm by clicking `Add extension` in the popup window.

2. Accept the Terms of Use.

<img src="../../img/enzyme-open-the-extension.png" width=50% />

3. Make a strong password and make sure to write it down in another place, then click `Create`.

<img src="../../img/enzyme-choose-a-password.png" width=50% />

4. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../../img/enzyme-generate-seed-phrase.png" width=50% />

5. Click `Dashboard`.

6. Click the DOT identicon to copy your address to clipboard.

<img src="../../img/enzyme-copy-your-address.png" width=50% />

7. [Get the Kusama address from the Substrate address.](#kusama-from-substrate-address)

### Using Polkawallet

1. Install [Polkawallet](https://polkawallet.io). Click Download and select the link corresponding to the platform you are using. On android you may need to allow installing apps from external sources. On iOS, you may need to "trust" Polkawallet in the General>Profiles & Device Management > Enterprise App Section before running the app.

2. Once opening the app, copy the seed phrase and store it in a safe place, don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../../img/polkawallet-create-account.jpg" width=50% />

3. Name your account and make a strong password, make sure to write it down in another place, then click Save.

4. You will be asked to confirm your seed phrase - this is to make sure you have copied it somewhere safe.

5. Click on the pink QR Code symbol, and select Copy address to copy your address to clipboard.

<img src="../../img/polkawallet-accounts-page.jpg" width=50% />
<img src="../../img/polkawallet-copy-address.jpg" width=50% />

6. [Get the Kusama address from the Substrate address.](#kusama-from-substrate-address)

### Kusama from Substrate address

If you used one of the generation methods that gave you a generic Substrate address (begins with a `5`), then you will need to take an extra step to turn this into the properly encoding Kusama address.

1. Copy your Substrate generic address to clipboard. 
2. Go to the [Polkadot UI](https://polkadot.js.org/apps). 
3. Go to the `Settings` tab and find the configuration for `address network prefix`.
4. Select `Substrate (development)` and click `Save and reload`.
5. Go to the `Address book` and click the `Add contact` button.
6. Enter your address and give it a name like "My Address".
7. Go back to the `Settings` tab and select the `Kusama (canary)` option in `address network prefix` and click `Save and reload`.
8. Go back to the `Address book` and find the account you just added (it will have the same name).
9. The address is now formatted to be a Kusama address.

## Step 2. Get KSM tokens

There are two methods to claim KSM.

**1. Dot Holders:**
Those who participated in the Polkadot sales and have been allocated DOT indicator tokens can claim a proportional amount of KSM prior to the launch of the network.

You can do this through [this claims process](https://claim.kusama.network/).

You can refer to [this detailed guide](./dot-holders.md) for a step by step walk through for how to do so.

Having trouble? Get support in the KSM [Claims chat](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders).

**2. Faucet:**
For those who didn’t participate in the Polkadot sale, KSM are publicly available after genesis through a faucet. Find out more [here](./faucet.md).

Public projects that need more KSM can request them by emailing projects@kusama.network.
