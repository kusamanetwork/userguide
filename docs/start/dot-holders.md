# KSM Claims

If you participated in the DOT sale and have received your DOT indicator tokens, you can claim the corresponding amount of KSM. 

Make sure to use your original Ethereum key during this process.

*Note: DOT holders who do not wish to participate in Kusama are encouraged to donate their KSM to the community. You can do so in the faucet. You may even get some swag as a token of appreciation!*

## Claiming before Kusama genesis

Claiming before the Kusama genesis block means that you will start the network with the balance already in your account. It is really easy to do this using the KSM claims DApp.

### Generate a Kusama address

If you haven't already done so, you will need to generate a Kusama address. See [this page](./claims.md) first!

### Claiming your KSM with MyCrypto

The DApp helps you send a transaction from MyCrypto. MyCrypto is good to use in case you have stored the keys to your DOT allocation on a hardware device like a Ledger Nano S or a Trezor, and it also supports private keys, mnemonics and parity signer.

**NOTICE**: It is much more secure to download and use the MyCrypto app locally. Please make sure to download the latest version for your operating system. You can always find the most up-to-date releases of the desktop app on their [releases page](https://github.com/MyCryptoHQ/MyCrypto/releases).

Once you've downloaded the MyCrypto app and run it locally (run it on an airgapped computer for maximum security), head over to the [claiming DApp](https://claim.kusama.network) and select `Claim on Ethereum (before genesis)` from the dropdown. The DApp will display the address and ABI to the Claims contract and an input asking for you to enter your Kusama address. When you paste your Kusama address in the input it will display a hex-encoded public key. 

**NOTE**: If you used `subkey` to generate your address, you should already have your public key.

Go to the MyCrypto application and click on the Contract tab. Choose the Custom selection for the contract and copy the address and ABI and address of the Claims contract. The mainnet Claims contract address is `0x9a1B58399EdEBd0606420045fEa0347c24fB86c2`. Click `Access`.

Select the `claim` function from the dropdown and enter the address of the Ethereum account that holds the balance of DOT allocation for which you would like to claim KSM. Usually this should be the same address that you are planning to send the transaction from, in exceptional cases it would be from a different key known as the amendment key (but don't worry about this if it sounds strange to you). 

Next enter in the hex encoded public key that the claims DApp outputted for you.

Unlock your wallet using your preferred method and click "Sign and Send."

You can click on the link to view your transaction on Etherscan, when the transaction is mined to the network then you are finished! When the Kusama network starts you will already have the balance of KSM in your Kusama address.

## Claiming after Kusama genesis
This section will become available upon Kusama network launch.
