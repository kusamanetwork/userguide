# Dot Holders KSM Claims

If you participated in the Polkadot sales, and have received your DOT indicator tokens, you can claim the corresponding amount of KSM. 

Make sure to use your original Ethereum key during this process.

*Note: DOT holders who do not wish to participate in Kusama are encouraged to donate their KSM to the community. You can do so in the faucet. You may even get some swag as a token of appreciation!*

## Claiming before Kusama genesis

Claiming before the Kusama genesis block means that you will start the network with the balance already in your account. It is really easy to do this using the KSM claims DApp.

### Claim your KSM with MyCrypto

MyCrypto is the option you will use if you have stored the keys to your DOT allocation on a hardware device like a Ledger Nano S or a Trezor.

> NOTICE: It is much more secure to download and use the MyCrypto app locally, You can always find the most up-to-date releases of the desktop app on their [releases page](https://github.com/MyCryptoHQ/MyCrypto/releases).

Once you've downloaded the MyCrypto app and run it locally (run it on an airgapped computer for maximum security), head over to the [claiming DApp](https://claim.kusama.network) and enter your Kusama address and select if you are claiming for an amendment (if this sounds strange to you, it means you should NOT click the checkbox). The DApp will generate some transaction data.

Head back to the MyCrypto application and click on the Contract tab. Choose the Custom selection for the contract and copy the ABI and address of the Claims contract. The mainnet Claims contract address is `0x9a1B58399EdEBd0606420045fEa0347c24fB86c2`. Click `Access`.

Select the `claim` function and enter the address of the Ethereum account that holds the balance of DOT allocation for which you would like to claim KSM.

Next enter in the information that the claims DApp outputted for you. For the curious ones, this is the hex representation of your Kusama public key which is how your chosen address is derived.

Unlock your wallet using your preferred method and click "Sign and Send."

You can click on the link to view your transaction on Etherscan, when the transaction is mined to the network then you are finished! When the Kusama network starts you will already have the balance of KSM in your Kusama address.


## Claiming after Kusama genesis
This section will become available upon Kusama network launch.
