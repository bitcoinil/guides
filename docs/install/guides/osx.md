# BitcoinIL OSX Setup

## Step 1 - Download & Install

Download the installation file: [BitcoinIL-Qt.dmg](https://guides.bitcoinil.org/assets/binaries/osx/BitcoinIL-Qt.dmg).

The Browser might warn you that the file is not from a known origin and you should be careful - that's a great suggestion at all times especially when it comes to Bitcoin and crypto! That being said do be careful and make sure you only down from verified sources and do not download from uncomfirmed links or publications.

We're working on having all the binaries code-signed before downloading, until then download with caution and adhear to public announcements, and use all the available precautions.


![Copying The App](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-install.png)

Drag the `BitcoinIL` app to your `Applications` folder as the installer suggested.

After running the installer we'll need to modify the `bitcoinil.conf` file to launch the wallet in Testnet mode.

> **Note**: This step is not needed once the mainnet launched

Launch the BitcoinIL app 

![Copying The App](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/bitcoinil-launch.png)

You might receive a message from OSX saying the application from untrusted source - again, this warning is approriate and you should be careful when dealing with software from untrusted source.

Until BitcoinIL sorts out code signing on all binaries you'll have to explicitly allow the wallet to be activated by going to the `System Preferences` and navigating to `Security & Privacy`:

![OSX Preferences](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/osx-preferences.png)

![OSX Security & Privacy](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/osx-security-and-privacy.png)

Inside `Security & Privacy` click on the little lock icon that says `Click the lock to make changes` on the bottom left of the screen to allow modifications to this screen, and authenticate yourself.

![OSX Security & Privacy Authorized](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/osx-security-authorized.png)

Now click on the button `Open Anyway` next to where it says `"BitcoinIL Core" was blocked from use because it is not from an identified developer.`.

![OSX Allow BitcoinIL Core to Open](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/osx-open-bitcoinil-core.png)

The BitcoinIL Wallet should now launch and you'll see a similar screen:

![Wallet First Time Launch](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-first.png)

## Step 2 - Configuring for Testnet

At this point we'll need to edit the `bitcoinil.conf` file to be able to launch the wallet in Testnet mode, for that click on `BitcoinIL Core` next to the  symbol at the top left of your screen:

![Open Wallet Preferences](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-open-preferences.png)

This will open the wallet preferences screen:

![Wallet Preferences](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-preferences.png)

Click on the `Open Configuration File` on the bottom left portion of the window, this will open the `bitcoinil.conf` in edit mode, but before that it will warn you the making modifications to this file is dangerous:

![Wallet `bitcoinil.conf` Warning](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-bitcoinil-conf-warning.png)

Once again a well placed warning - make sure to adhear to these warning and any changes you make to this file are from a trusted source espeially if you're not familiar with this stuff.

Click on `OK` which will open a blank text file named `bitcoinil.conf`:

![Blank `bitcoinil.conf` File](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/bitcoinil-conf.png)

Enter the following in the file:

```
testnet=1
```

Save and close the file, and exit the wallet by going to `BitcoinIL Core` and selecting `Quick BitcoinIL Core`:

![Quit Wallet](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/quit-wallet.png)

And launch the wallet again the same way you did last time.

This time around a similar but different screen should appear and the icon should be purple of color and not the light blue of BTCIL.

![Testnet Wallet](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-testnet.png)

![Testnet Icon](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/bitcoinil-core-testnet-icon.png)

Now we need our wallet synchronized with the network, to do that we'll need to manually add a node to our wallet to kickstart the peer discovery process (this will be fixed in upcoming versions). Navigate to `Window -> Console` which will open the wallet console:

![Wallet Console](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-console.png)

![Wallet Empty Console](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-console.png)

At the bottom of this screen there's a text input which we will use to issue commands to the wallet - enter the command:

```
addnode 178.238.226.217 onetry
```

![Wallet Console - `addnode`](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-console-addnode.png)

The console might or might not respond with `null` - in any case the wallet should quickly begin to synchronize in the background as it downloads the block from the newly added peer. You can navigate to the `Peers` tab and see detailed information about the peer you've added and any other peers that connected since.

Close the `Console` or `Peers` window and you should see the wallet synchronizing it's blockchain, and once it's done your wallet should show a similar screen:

![Wallet Ready](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-ready.png)

## Step 3 - Creating a Wallet

Click on `Create a new wallet` as the screen suggests to create your first BitcoinIL wallet and name it as you see appropriate and make sure `Encrypt Wallet` if you're using a shared computer!.

![Wallet Ready](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-create.png)

You'll now see your newly created wallet screen:

![New Wallet](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-new-wallet.png)

You can navigate to the `Receive` section and create a new address to begin receiving BTCIL coins:

![Wallet Receive Screen](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-receive.png)

Add an optional label to your new address, I named `Test Address` as can be seen below, and click on the `Create new receiving address` button, leaving all the other fields unchanged.

This will create a new address in your wallet and will open the address details window where you'll be able to copy the address and save the QR code image:

![Wallet Address Details](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-address-info.png)

In my case it was the address `ti1qu6s2g22lp7326j8qy2t9qg98f630cn8veqnc4v` I generated. After closing the details window you'll see the newly created address in the `Requested payments history` section:

![Wallet Address Created](https://github.com/bitcoinil/guides/raw/main/assets/images/osx/wallet/wallet-address-created.png)


At this point you should have fully functional wallet and at least one address you can share with other to begin receiving BTCIL coins.


## Faucet

If you'd like to receive a few testnet BTCIL coins give us a shoutout on the [platform of your choosing](/#social-networks) with your address and we'll send some your way to get you started!