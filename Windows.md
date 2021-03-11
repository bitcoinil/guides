# BitcoinIL Windows Setup

Download the installation file: [bitcoinil-0.21.0-win64-setup.exe](https://github.com/bitcoinil/guides/raw/main/assets/binaries/windows/bitcoinil-0.21.0-win64-setup.exe).

The Browser or Windows might warn you that the file is not from a known origin and you should be careful - that's a great suggestion at all times especially when it comes to Bitcoin and crypto! That being said do be careful and make sure you only down from verified sources and do not download from uncomfirmed links or publications.

We're working on having all the binaries code-signed before downloading, until then download with caution and adhear to public announcements, and use all the available precautions.

After running the installer, for testnet activate the BitcoinIL Test. 

![Installation Wizard](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-1.png)

Follow the installation guide and if you're a first-timer it's recommended to install as the wizard suggests - this will make it easier in the following steps.

![Installation Wizard Progress](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-2.png)

Once the installation is complete, if you're going to run Testnet make sure to *Uncheck* the option `Run BitcoinIL Core` on the final step.

![Installation Wizard Complete](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-3.png)

A window will show up similar to this:

__placeholder for the running wallet screenshot__

Click on `Windows -> Console` which will open a simple console window which has an input box at the bottom of it, in that input box type in:

```
addnode 178.238.226.217 onetry
``` 

If you've installed BitcoinIL without changing any of the default settings, such as the installation directory, navigate your file browser to: `C:\Users\[YourUsername]\AppData\Roaming\BitcoinIL`

__placeholder for files screenshot__

