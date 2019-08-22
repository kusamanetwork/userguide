**Important:**

Kusama will launch around 23 August, 2019.

This means you will no longer be able to use the following instructions to claim KSMs. [This Ethereum DApp](https://claim.kusama.network) will be disabled after block `8405350` of Ethereum (approx 9:30 am Zurich time).

You will only be able to claim directly on the Kusama network, via your original Ethereum address that you used to procure Dots. Updated instructions for this coming soon. 

# How to get KSM (After Kusama Genesis)

The Kusama network is Polkadot's experimental, community-focused R&D network. If you hold the DOT indicator token, you are entitled to claim an equivalent amount of KSM on the Kusama network. This is so that the Kusama network is aligned with the existing DOT holders and community.

You can claim KSMs by signing a message with the Ethereum that holds your DOT indicator tokens.

## Step 1. Create a Kusama account

You will need to generate a Kusama account to claim KSM. There are a few ways you can create one.

For most users, we recommend using the [Polkadot UI](https://polkadot.js.org/apps/#/explorer) since it will allow you to store your encrypted keystore locally.

> NOTICE: Unfortunately, at this time Kusama does not have hardware wallet support. Hopefully this will change soon!

Another option you may consider using is the `subkey` command line utility, which will allow you to take extra steps to protect the security of your key. Additionally, two other options include the Enzyme browser extension wallet and the Polkawallet mobile wallet, although these require an extra step to generate Kusama addresses.

### Using polkadot{.js} extension (Chrome/Brave or Firefox)

1. Install the polkadot{.js} extension from the [Chrome store](https://chrome.google.com/webstore/detail/polkadot%7Bjs%7D-extension/mopnmbcafieddcagagdcbnhejhlodfdd?hl=en) or [Firefox store](https://addons.mozilla.org/en-US/firefox/addon/polkadot-js-extension/).
1. Create a new account by clicking on `I want to create a new account with a new seed`.
1. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or want to import your account again.
1. Enter a name for the account and type a strong password (at least 6 characters).
1. Click on `Add the account with the generated seed`.
1. You can copy the account's address to the clipboard by clicking on its identicon.

### Using `subkey`

#### Installation

You can install `subkey` with this one-line command:

```
cargo install --force --git https://github.com/paritytech/substrate subkey
```

Note that you will already have had to install the proper Rust version and dependencies.  If you have not done so, or experience problems installing using that command, run the following commands first, and then re-try the previous command:

```
curl https://sh.rustup.rs -sSf | sh

rustup update nightly
rustup target add wasm32-unknown-unknown --toolchain nightly
rustup update stable
cargo install --git https://github.com/alexcrichton/wasm-gc
```

Alternatively, you can build `subkey` from the source code.

1. Follow the build instructions for [Substrate](https://github.com/paritytech/substrate#6-building).
2. When building, only build `subkey` by typing `cargo build -p subkey`.
3. The executable is `./target/debug/subkey`.

#### Usage

You can use subkey on a computer that is not connected to the internet for added security.

The command `subkey --network kusama generate` will generate a new key-pair. If you want to be more secure, use 24 words, `subkey --network kusama generate --words 24`.

```
$ subkey --network kusama generate
Secret phrase `lobster flock few equip connect boost excuse glass machine find wonder tattoo` is account:
  Secret seed: 0x95b90eb1344e3aea40f4a6dc81622901a2ac39efb331c41db10c311bb9b46927
  Public key (hex): 0xfe7fce341ff73e1db537daa4cc8c539997a8b0654b06cb81c47e4f067f55a65a
  Address (SS58): JL1eTcbzuZP99FjeySkDrMygNREPdbhRyV7iD5AsV4fDRcg
```

The `Address (SS58)` field is what you should use to claim your KSM tokens. Never share your `Secret phrase` or `Secret seed`, as these can both control your funds.

NOTE: Previous versions of `subkey` only generated Substrate addresses. If you do not want to generate a new seed, you can convert the Substrate address to a Kusama address by following [this section](#kusama-from-substrate-address).

See the [`subkey` documentation](https://substrate.dev/docs/en/ecosystem/subkey) or enter `subkey --help` for more usage examples.

### Using Polkadot UI

1. Open up the [Polkadot UI](https://polkadot.js.org/apps) and navigate to the `Settings` tab. Find the configuration dropdown for `address network prefix` and select `Kusama (canary)`. Click `Save and reload`.

1. Navigate to the [Polkadot UI Accounts Tab](https://polkadot.js.org/apps/#/accounts) and click on the `Add account` button.

<img src="../../img/polkadotui-find-the-accounts-page.png" width=50% />

2. Enter a name for your account and create a secure password. This password will be used to decrypt your account.

<img src="../../img/polkadotui-create-your-account.png" width=50% />

3. Ignore the advanced options unless you want to change the type of cryptography used for your keys (we recommend "Schnorrkel (sr25519)").

4. Click `Save` and `Create and backup account`.

5. Save your encrypted keystore locally.

6. The account now appears in your Accounts tab and is backed up to the keystore you just saved.

7. Click on the DOT identicon to copy the address to the clipboard.
<img src="../../img/polkadotui-copy-account-address.png" width=50% />

### Using Enzyme browser wallet (Chrome or Brave only)

1. Install the Enzyme browser wallet from the [Chrome store](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh)(for Brave as well). Click `Add to Chrome` and confirm by clicking `Add extension` in the popup window.

2. Accept the Terms of Use.

<img src="../../img/enzyme-open-the-extension.png" width=50% />

3. Make a strong password and make sure to write it down in another place, then click `Create`.

<img src="../../img/enzyme-choose-a-password.png" width=50% />

4. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone; you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../../img/enzyme-generate-seed-phrase.png" width=50% />

5. Click `Dashboard`.

6. Click the DOT identicon to copy your address to clipboard.

<img src="../../img/enzyme-copy-your-address.png" width=50% />

7. [Get the Kusama address from the Substrate address.](#kusama-from-substrate-address)

### Using Polkawallet

1. Install [Polkawallet](https://polkawallet.io). Click `Download` and select the link corresponding to the platform you are using. On Android you may need to allow installing apps from external sources. On iOS, you may need to "trust" Polkawallet in the `General > Profiles & Device Management > Enterprise App` section before running the app.

2. Once the app is open, copy the seed phrase and store it in a safe place. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.

<img src="../../img/polkawallet-create-account.jpg" width=50% />

3. Name your account and make a strong password, make sure to write it down in another place, then click `Save`.

4. You will be asked to confirm your seed phrase - this is to make sure you have copied it somewhere safe.

5. Click on the pink QR Code symbol and select `Copy address` to copy your address to clipboard.

<img src="../../img/polkawallet-accounts-page.jpg" width=50% />
<img src="../../img/polkawallet-copy-address.jpg" width=50% />

6. [Get the Kusama address from the Substrate address.](#kusama-from-substrate-address)

### Kusama from Substrate address

If you used one of the generation methods that gave you a generic Substrate address (begins with a `5`), then you will need to take an extra step to turn this into the properly encoded Kusama address.

1. Copy your Substrate generic address to the clipboard.
2. Go to the [Polkadot UI](https://polkadot.js.org/apps).
3. Go to the `Settings` tab and find the configuration for `address network prefix`.
4. Select `Substrate (development)` and click `Save and reload`.
5. Go to the `Address book` and click the `Add contact` button.
6. Enter your address and give it a name like "My Address".
7. Go back to the `Settings` tab and select the `Kusama (canary)` option in `address network prefix` and click `Save and reload`.
8. Go back to the `Address book` and find the account you just added (it will have the same name).
9. The address is now formatted as a Kusama address.

## Step 2. Get KSM tokens

There are two methods to claim KSM.

**1. DOT Holders:**

Those who participated in the Polkadot sales and have been allocated DOT indicator tokens can claim a proportional amount of KSMs on the Kusama Network.

To do this you must sign a message containing the address of your Kusama account. There are two ways to do this:

1. Using the Polkadot UI [Claims app](https://polkadot.js.org/apps/#/claims).
2. Using the updated [Claims website](https://claim.kusama.network).

Refer to [this detailed guide](./dot-holders.md) for a step-by-step walk-through of the post-genesis claims process.

Having trouble? Get support in the KSM [Claims Support](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders) channel.

**2. Faucet:**

For those who didn’t participate in the Polkadot sale, KSMs are publicly available after genesis through a faucet. Find out more [here](./faucet.md).

Public projects that need more KSMs can request them by applying [here](https://docs.google.com/forms/d/1-JxlJqt8DA0E3K0QX0Gc20rF02-aqDn6r_rzkB4LaMk/edit).
