# KSMA claims

The Kusama network is Polkadot's R&D network. This guide will walk you through how to proceed with claiming KSMA.

In order to align Kusama with the existing DOT holders and community, if you are a DOT allocation holder you can claim the equivalent amount of Kusama tokens (ticker: KSMA). There are two ways to claim either before genesis by sending a transaction on Ethereum or after genesis by signing a message using your allocation key and making a transaction on Kusama.

## Create a Kusama account

You will need a Kusama account to claim the KSMA. There are a few ways you can create one. For most users, we recommend using the [Polkadot UI](https://polkadot.js.org/apps/#/explorer) since it will allow you to store your encrypted keyfile locally.

> NOTICE: Unfortunately at this time Kusama and Substrate chains do not have hardware wallet support using the Ledger or Trezor products. Hopefully soon this will change!

Another option you may consider using are `subkey` commandline utility which will allow you to be extra secure and generate your key on an air-gapped device. A couple other options include using Enzyme in-browser wallet (like MetaMask) or the Polkawallet mobile wallet.

### Using Polkadot UI

1. Navigate to the [Polkadot UI Account's Tab](https://polkadot.js.org/apps/#/accounts) and click on the `Add account` button.
2. Enter a name for your account and create a secure password. This password will be used to decrypt your account.
3. Ignore the advanced options unless you want to change the type of cryptography used for your keys (either sr25519 or ed25519 works).
4. Click `Save` and `Create and backup account`.
5. Save your encrypted keystore locally.
6. The account now appears in your Accounts tab and is backed up to the keystore you just saved.
7. Click on the DOT identicon to copy the address to the clipboard.

### Using `subkey`

1. Follow the build instructions for [Substrate](https://github.com/paritytech/substrate#6-building).
2. When building, instead of building all of the binaries only build `subkey` by typing `cargo build subkey`.
3. You can build / use the subkey on a computer that is not connected to the internet for added security.
4. The command `subkey generate` will generate a new keypair.

### Using Enzyme browser wallet (Chrome only)

1. Install the Enzyme browser wallet from the [Chrome store](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh). Click `Add to Chrome` and confirm by clicking `Add extension` in the popup window.
2. Accept the Terms of Use.
3. Make a strong password and make sure to write it down in another place, then click `Create`.
4. Copy the seed phrase and store it somewhere safe. Don't share the seed phrase with anyone, you can use it to access your account if you forget your password or otherwise lose your keystore.
5. Click `Dashboard`.
6. Click the DOT identicon to copy your address to clipboard.

### Polkawallet

TODO

## Claiming before Kusama genesis

Claiming before the Kusama genesis block means that you will start the network with the balance already in your account. It is really easy to do this using the KSMA claims DApp.

### Claim your KSMA with MyCrypto

MyCrypto is the option you will use if you have stored the keys to your DOT allocation on a hardware device like a Ledger Nano S or a Trezor.

> NOTICE: It is much more secure to download and use the MyCrypto app locally, You can always find the most up-to-date releases of the desktop app on their [releases page](https://github.com/MyCryptoHQ/MyCrypto/releases).

Once you've downloaded the MyCrypto app and run it locally (run it on an airgapped computer for maximum security), head over to the [claiming DApp](https://claims.kusama.network) and enter your Kusama address and select if you are claiming for an amendment (if this sounds strange to you, it means you should NOT click the checkbox). The DApp will generate some transaction data.

Head back to the MyCrypto application and click on the Contract tab. Choose the Custom selection for the contract and copy the ABI and address of the Claims contract. The mainnet Claims contract address is 0xXXXXXXXXXXX. Click `Access`.

Select the `claim` function and enter the address of the Ethereum account that holds the balance of DOT allocation for which you would like to claim KSMA.

Next enter in the information that the claims DApp outputted for you. For the curious ones, this is the hex representation of your Kusama public key which is how your chosen address is derived.

Unlock your wallet using your preferred method and click "Sign and Send."

You can click on the link to view your transaction on Etherscan, when the transaction is mined to the network then you are finished! When the Kusama network starts you will already have the balance of KSMA in your Kusama address.

## Claiming after genesis

This section of the guide will go live after Kusama's genesis block.
