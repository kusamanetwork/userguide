# KSM Claims

If you participated in the DOT sale and have received your DOT indicator tokens, you can claim the corresponding amount of KSM. 

Make sure to use your original Ethereum key during this process.

*Note: DOT holders who do not wish to participate in Kusama are encouraged to donate their KSM to the community. You can do so in the faucet. You may even get some swag as a token of appreciation!*

## Claiming after Kusama genesis

Claiming after the Kusama genesis block means that the network has already started and you now want to claim a balance of KSMs to your Kusama account. It's very easy to do by signing a simple message.

### Generate a Kusama address

If you haven't already done so, you will need to generate a Kusama address. See [this page](./claims.md) first!

### Claiming your KSM with MyCrypto

The Polkadot JS [Claims app](https://polkadot.js.org/apps/#/claims) helps you sign a message from MyCrypto. MyCrypto is good to use in case you have stored the key to the Ethereum account holding your DOT indicator tokens on a hardware device like a Ledger Nano S or a Trezor. It also supports raw private keys, mnemonics and the Parity signer. 

**NOTICE**: It is much more secure to download and use the MyCrypto app locally. Please make sure to download the latest version for your operating system. You can always find the most up-to-date releases of the desktop app on their [releases page](https://github.com/MyCryptoHQ/MyCrypto/releases).

Once you've downloaded MyCrypto and have it running locally (we recommend an air-gapped computer for maximum security), you can start by navigating to the Claims app on the Polkadot JS UI. Select the account you would like to claim the KSMs into and click the blue "Continue" button to proceed. Your screen should look something like this:

![Claim Step 1](../../img/claim/claim-1.png)

The hex encoded string that follows the sentence: "Pay KSMs to the Kusama account:" is the hex-encoded public key of your Kusama account, minus the `0x` prefix. To verify that the public key is correct you can use the `subkey` tool to inspect your address.

The next step is to go to the MyCrypto application and click on "Sign & Verify Message" tab. This will prompt you to select a method for unlocking your wallet. After unlocking your wallet, you will copy and paste the outputted sentence into the input box. 

![Claim Step 2](../../img/claim/claim-2.png)

When you click "Sign Message" you will get a JSON output like the below:

![Claim Step 3](../../img/claim/claim_3.png)

Copy and paste the JSON output of the signed message from MyCrypto into the input box on the Polkadot JS UI and click "Confirm Claim."

![Claim Step 3](../../img/claim/claim-3.png)

At this point you will see a success message if everything went right and your KSMs will now be in the account that you claimed to. Congratulations you can now participate in aspects of the Kusama network such as [governance](../try/governance) and [staking](../try/staking). During the soft launch period balance transfers will not be enabled.

![Claim Step 4](../../img/claim/claim-4.png)]

### Verifying your Claim

After you make an on-chain claim for KSMs, your balance should be updated on the Polkadot UI immediately.

### Need Help?

Please join the [Claim Support](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders) channel.

### Third Party Claims Processes

**We do not recommend using a third-party app or process to perform your claim or acquire KSM**

Claiming using a third-party process can lead to the loss of your allocation, therefore we cannot recommend using any third party apps to do so. Manually specifying your transaction data, as specified in our claims process, is the only way to be certain you will receive your allocation. 
