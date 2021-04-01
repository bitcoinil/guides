# BitcoinIL Windows Setup

## Step 1 - Download & Install

Download the installation file: [bitcoinil-0.21.0-win64-setup.exe](https://guides.bitcoinil.org/assets/downloads/binaries/windows/bitcoinil-0.21.0-win64-setup.exe).

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

![Wallet Synchronizing](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-synchronizing.png)

If you don't see the wallet synchronizing after a few minutes, go to the `Window -> Peers` screen to verify that your wallet is discovering BitcoinIL peers to sync with.

![Wallet Peers](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-peers.png)

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

## Step 4 - JSON-RPC and Mining


The last piece of the puzzle is start mining BTCIL - to acheive that we'll have to do download a dedicated software, as Bitcoin's source code has disabled the built-in miner at some point, and we'll need to generate a `Legacy` address for that miner to be able to generate a payout on this new network.

### 4.1 JSON-RPC Support

First we'll need to configure the wallet to support external access via `JSON-RPC` so that the miner can communicate with it, to do that we'll need to edit the `bitcoinil.conf` file which resides in (if you followed the installations steps as suggested and didn't change anything in the setup stage) "`C:\Users\[YourUsername]\AppData\Roaming\BitcoinIL`".

![Wallet Settings](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-settings.png)

The easiest way to edit the configuration file is to go to `Settings -> Options`, and there clicking on `Open Configuration File`.

![Wallet Options - Open Configuration File](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-config-file.png)

Clicking on this button will show a warning message cautioning you from modifying the configuration file - this is an excellent warning that should be noted, our changes in the next steps will allow your wallet to be controlled via external software (such as a miner), if you're using a shared computer you might need to take additional precautionary measures to properly secure your wallet from unwanted activity.

![Wallet Configuration File Warning](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-config-file-warning.png)

Click on `OK`, and at this stage you might be prompted to select how to open the configuration file - mind you that this file is a simple text file, so you might choose simple `Notebook` to edit it, or if you prefer to use a dedicated code editor like I do, you can select that option as well:

![Open With Dialog for Configuration File](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-config-open-with.png)

In my case I chose `Visual Studio Code` and I left the `Always use this app to open .conf files` so I don't have to go through this process next time I want to edit the config file.

Once you've opened the file, it's most likely will be empty and without any content. That's ok - we'll fill it in with our settings so that we can run the miner locally.

Add the following to the file:

```conf
# Expose the RPC/JSON API
server=1

# Activate the wallet in Testnet mode
testnet=1

# Allow only local machine to access bitcoind
rpcallowip=127.0.0.1

# RPC Port to use - comment out for Testnet
# rpcport=8332

# RPC Username and password
rpcuser=bitcoinil
rpcpassword=talisawesome

# Testnet configuration
[test]
server=1
rpcallowip=127.0.0.1
rpcuser=bitcoinil
rpcpassword=talisawesome
```

Save and close the file, and shut down the wallet by going to `File -> Exit` (or by tapping `CTRL+Q`), and start the wallet again (make sure to run Testnet wallet during testing and not the mainnet wallet!).

Your wallet should now open again and quickly sync any missing blocks, it should now be ready to accept JSON-RPC calls by the miner we're about to run.

### 4.2 Legacy Address

We'll need a `Legacy` address for our miner to be able to send us the block rewards, to do that we'll once again open the wallet console by going to `Window -> Console`, and input the command `getnewaddress "miner" "legacy"` like so:

![Wallet Legacy Address in Console](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-legacy-address.png)

The console will output a new legacy address that you need to copy to a safe place as we'll need it in a moment to configure our miner.

![Wallet Created Legacy Address](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-legacy-address-created.png)

In my case the wallet created the following address: `moVw1tzfSDudWSBJS75zoGoMVVjtRXrAQP`

### 4.3 The Miner

Download the latest CPUMiner-OPT: [cpuminer-opt-3.15.7-windows.zip](https://github.com/JayDDee/cpuminer-opt/releases/download/v3.15.7/cpuminer-opt-3.15.7-windows.zip)

Or download the miner from the official release channel: [JayDDee/cpuminer-opt/releases](https://github.com/JayDDee/cpuminer-opt/releases/) and click on the `cpuminer-opt-3.15.7-windows.zip` link (circled in red below:)

![CPUMiner-OPT Releases](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/miner-releases.png)

Once the download is complete extract the files to a dedicated folder (I created the folder `E:\Apps\CPUMiner` and extracted all the files):

![CPUMiner Files Extracted](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/cpuminer-extracted.png)

Create a new file named `run-testnet.bat` and place it alongside the other CPUMiner files:

![Added run-testnet.bat file](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/run-testnet-bat.png)

Edit the file (Right click on the file and click Edit) and add the following text to the file:

```bash
cpuminer-aes-sse42.exe --coinbase-addr=YOUR_ADDRESS_HERE --algo=x17 -o http://127.0.0.1:18223 -u bitcoinil -p talisawesome --no-stratum --no-longpoll -t 10 --debug
```

Replace the string `YOUR_ADDRESS_HERE` with the address generated in the previous step, in my case it's: `moVw1tzfSDudWSBJS75zoGoMVVjtRXrAQP`, and my `run-testnet.bat` file looks like this once properly edited:

```bash
cpuminer-aes-sse42.exe --coinbase-addr=moVw1tzfSDudWSBJS75zoGoMVVjtRXrAQP --algo=x17 -o http://127.0.0.1:18223 -u bitcoinil -p talisawesome --no-stratum --no-longpoll -t 10 --debug
```

![run-testnet.bat contents](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/run-testnet-bat-contents.png)

Save and close the file, and now you can double-click it to run your miner.

> **Note**: You can download the file from this repository and save it as-is, make sure to update the wallet address with yours! Download by right-clicking and 'Save As': [run-testnet.bat](https://raw.githubusercontent.com/bitcoinil/guides/main/docs/assets/downloads/binaries/exapmle-conf/testnet/run-testnet.bat)

A new command line window will open similar to this:

![CPUMiner Initial Run](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/run-testnet-initial.png)

After a few minutes your miner should begin to find blocks and you will see the miner providing you with some relevant information:

![CPUMiner Mining](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/run-testnet-mining.png)

If you leave your computer for a few hours mining you wallet should display the block reward transactions like this:

![CPUMiner Mining](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/miner/wallet-mined.png)

## Mining Survey

Hopefully following this guide you've managed to both setup a wallet and a miner for BitcoinIL on your windows machine!

We're conducting a global open survey until the launch of the mainnet of testnet miners - if you'd like to participate simply send 1 Test BTCIL to: [`ti1qls36j7mg5fdsyg38c5rwtfvslx6qasvypphlfa`](https://testexplorer.bitcoinil.org/address/ti1qls36j7mg5fdsyg38c5rwtfvslx6qasvypphlfa), Thank you!

## Faucet

If you'd like to receive a few testnet BTCIL coins give us a shoutout on the [platform of your choosing](/#social-networks) with your address and we'll send some your way to get you started!