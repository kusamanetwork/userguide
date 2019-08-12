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

Go to the MyCrypto application and click on "Interact with Contracts" under the Tools tab. Choose the Custom selection for the contract and copy the address and ABI of the Claims contract. The mainnet Claims contract address is `0x9a1B58399EdEBd0606420045fEa0347c24fB86c2`. Click `Access`.

Select the `claim` function from the dropdown and enter the address of the Ethereum account that holds the balance of DOT allocation for which you would like to claim KSM. Usually this should be the same address that you are planning to send the transaction from, in exceptional cases it would be from a different key known as the amendment key (but don't worry about this if it sounds strange to you). 

Next enter in the hex encoded public key that the claims DApp outputted for you.

Uncheck the box that says `Automatically Calculate Gas Limit` and instead use `150000` as the inputted gas limit. Feel free to change the gas price to whatever you like or keep it at the default, you can view the network average gas price [here](https://www.ethgasstation.info/).

Click `Write` in MyCrypto and unlock your wallet using your preferred method. Afterward click "Sign Transaction" and finally send it to the network.

You can click on the link to view your transaction on Etherscan, when the transaction is mined to the network then you are finished! When the Kusama network starts you will already have the balance of KSM in your Kusama address.

### Verifying your Claim

The KSM will not be available to you until Kusama launches. If you would like to verify your claim, the best place to do it is on the info box at the bottom of the Kusama [claim DApp](https://claim.kusama.network). At the bottom of the page, you will see an input asking for the Ethereum address holding the DOT Allocation Indicator token that you claimed. After inputting this Ethereum addres you will see the registered Kusama address, public key, index, and balance of your claim. If all of this data looks right then your claim was a success! After the Kusama genesis launches, the KSM will be available automatically in your Kusama address for you to use.  

### Third Party Claims Processes

**We do not recommend using a third-party app or process to perform your claim or acquire KSM**

Claiming using a third-party process can lead to the loss of your allocation, therefore we cannot recommend using any third party apps to do so. Manually specifying your transaction data, as specified in our claims process, is the only way to be certain you will receive your allocation. 

## Claiming after Kusama genesis
This section will become available upon Kusama network launch.
