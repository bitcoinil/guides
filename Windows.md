# BitcoinIL Windows Setup

## Step 1 - Download & Install

Download the installation file: [bitcoinil-0.21.0-win64-setup.exe](https://github.com/bitcoinil/guides/raw/main/assets/binaries/windows/bitcoinil-0.21.0-win64-setup.exe).

The Browser or Windows might warn you that the file is not from a known origin and you should be careful - that's a great suggestion at all times especially when it comes to Bitcoin and crypto! That being said do be careful and make sure you only down from verified sources and do not download from uncomfirmed links or publications.

We're working on having all the binaries code-signed before downloading, until then download with caution and adhear to public announcements, and use all the available precautions.

After running the installer, for testnet activate the BitcoinIL Test. 

![Installation Wizard](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-1.png)

Follow the installation guide and if you're a first-timer it's recommended to install as the wizard suggests - this will make it easier in the following steps.

![Installation Wizard Progress](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-2.png)

Once the installation is complete, if you're going to run Testnet make sure to *Uncheck* the option `Run BitcoinIL Core` on the final step.

![Installation Wizard Complete](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-3.png)

After the installation is complete you can start the Testnet wallet by going to **Start** -> `BitcoinIL Core (testnet)`, You will have two different options to run the BitcoinIL Core wallet - make sure to pick the `testnet` option.

![Start Menu BitcoinIL Core Options](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-testnet.png)

## Step 2 - Synchrnonizing The Blockchain

Once you've launched the wallet the first screen you'll see is most likely a firewall request by the wallet app to access the internet, like so:

![Firewall Request](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-0.png)

You should click `Allow Access` so that the wallet app can synchronize via the internet.

You'll now see a screen notifying you that the wallet is not synchronized and that you shouldn't perform any actions (e.g. sending coins) until you've reached full synchronization.

![Unsynchronized Wallet](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-1.png)

You'll now want to allow you wallet to connect to its first node to synchronize, to do that click on `Window` and select `Console`.

![Wallet Console](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-addnode.png)

In the bottom-end of the window there's a text input, use it to provide the following command to your wallet:

```
addnode 178.238.226.217 onetry
``` 

In some cases the console will reply with `null` and in others nothing will happen - both cases are good for our case.


You can now navigate to the `Peers` tab and see if the wallet started communicating with the recently added node and if it's discoving additional nodes.

![Wallet Console](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-peers.png)

You can now safely close this window and return back to the main wallet interface - at this point your wallet should begin synchronizing with the network.

![Wallet Synchronizing](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-synchronizing.png)

It should quickly sync and you'll see the wallet showing you the following message:

![Wallet Synchronized](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-synced.png)

You can now create your first address to receive BTCIL.

## Step 3 - Wallet and Addresses

Clicking on `Create a new wallet` will open a new wallet creation dialog - provide a meaningful name and potentially select `Encrypt Wallet` to fully encrypt your wallet with a passphere.

![Wallet Create](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-create.png)

Once the wallet is created, you can now generate new addresses to receive BTCIL.

![Wallet Ready](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-ready.png)

Navigate to the 'Receive' tab, and fill in a suitable label for your new addres, you can leave the rest of the fields unchanged.

Once you click `Create new receiving address` a small window with a QR code will display all the relevant information you need for the address you've created.

![Wallet Address Created](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-address.png)

In my case the generated address is shown above - click on `Copy Address` and your clipboard should now be populated with the address you've generated.

> **Note**: Testnet addresses will start with `ti1` while Mainnet addresses start with `il1` (for bech32 addresses)

You can now share that address with others and receive payments.

![Wallet No Transactions](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-no-txs.png)

In the above image my wallet shows that there are no transactions associated with my wallet. Bellow I've received a single transaction of 120BTCIL:

![Wallet Received Transaction](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-tx.png)

And if I open the transaction details by double clicking on the transaction, the wallet will provide me with some basic information regarding that transaction:

![Wallet Transaction Details](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-tx-details.png)

My main wallet page will now display the assets held by the wallet:

![Wallet With Assets](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-with-assets.png)



If you've installed BitcoinIL without changing any of the default settings, such as the installation directory, navigate your file browser to: `C:\Users\[YourUsername]\AppData\Roaming\BitcoinIL`

__placeholder for files screenshot__

