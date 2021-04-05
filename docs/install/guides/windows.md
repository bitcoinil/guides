# BitcoinIL Windows Setup

## Step 1 - Download & Install

Download the installation file: [bitcoinil-0.21.0-win64-setup.exe](https://guides.bitcoinil.org/assets/downloads/binaries/windows/bitcoinil-0.21.0-win64-setup.exe).

The Browser or Windows might warn you that the file is not from a known origin and you should be careful - that's a great suggestion at all times especially when it comes to Bitcoin and crypto! That being said do be careful and make sure you only down from verified sources and do not download from uncomfirmed links or publications.

We're working on having all the binaries code-signed before downloading, until then download with caution and adhear to public announcements, and use all the available precautions.

After running the installer, for testnet activate the BitcoinIL Test. 

![Installation Wizard](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-1.png)

Follow the installation guide and if you're a first-timer it's recommended to install as the wizard suggests - this will make it easier in the following steps.

![Installation Wizard Progress](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-2.png)

![Installation Wizard Complete](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/install-3.png)

## Step 2 - Synchrnonizing The Blockchain

Once you've launched the wallet the first screen you'll see is most likely a firewall request by the wallet app to access the internet, like so:

![Firewall Request](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-0.png)

You should click `Allow Access` so that the wallet app can synchronize via the internet.

You'll now see a screen notifying you that the wallet is not synchronized and that you shouldn't perform any actions (e.g. sending coins) until you've reached full synchronization.

![Unsynchronized Wallet](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-1.png)

![Wallet Synchronizing](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-synchronizing.png)

If you don't see the wallet synchronizing after a few minutes, go to the `Window -> Peers` screen to verify that your wallet is discovering BitcoinIL peers to sync with.

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

> **Note**: BitcoinILaddresses start with `il1` (for bech32 addresses) and the same as in Bitcoin for `legacy` addresses (starts with 1)

You can now share that address with others and receive payments.

And if I open the transaction details by double clicking on the transaction, the wallet will provide me with some basic information regarding that transaction:

If you've installed BitcoinIL without changing any of the default settings, such as the installation directory, navigate your file browser to: `C:\Users\[YourUsername]\AppData\Roaming\BitcoinIL`

> Note: You can go to `Start -> Run` and type in `%AppData% which will open the relevant folder where the `BitcoinIL` data folder resides

### 3.1 Legacy Address

We'll need a `Legacy` address for our miner to be able to send us the block rewards, to do that we'll create a new address and make sure the `Generate native segwit (Bech32) address is **Unchecked**:

![Wallet Legacy Address in Console](https://github.com/bitcoinil/guides/raw/main/assets/images/windows/wallet/wallet-legacy-address.png)

The wallet will generate a new legacy address which you can copy and use with miners and other legacy-address-requiring software.

In my case the wallet created the following address: `1PjhY1SqVgUbxmu4CdN5L7FBzzKLJBxeqY`

## 4 The Miner

Mining is somewhat involved process but extremly rewarding once you start seeing the coins fillig up your wallet.

Mining performance is measure in `Hashes per Second` and is most often written in the short-hand form of `KH/s`, or `MH/s`, or even `GH/s`, `TH/s`, and in some cases `PH/s` - all of which refer to `Kilo-Hash per Second` or `Mega-Hash per Second` and so on.

The better hardware you have the better performance, or coins-per-minute, you can expect from your miner.

Different crypto-currencies utilize different mining techniques, Bitcoin Israel is a clone of Bitcoin and is mined using the Proof-of-Work method, while some other cyrptocurrencies utilize other methods like Proof-of-Stake or hybrid methods in certain cases.

Additionally cryptocurrencies differ by the type of mining function they implement which results in different performance for different mining functions as some are easier for the computer (SHA256 - Bitcoin), while others are more complex (X17 - BitcoinIL). Bitcoin Israel is utilizing the less-popular function X17 which is considered ASIC resistent and can be currently mined using standard CPUs and GPUs.

There are several ways to mine BitcoinIL using standard consumer-grade hardware:

### Mining Type

There are several miners you can choose from to mine BitcoinIL - most modern miners support the X17 mining function and can be configured rather easily to mine BTCILs.

The main difference is the type of miner - or rather what kind of hardware it is designed to utilize to mine the coins:

#### Browser Mining

Browser mining is the slowest but the easiest way to mine crypto-currency. Currently there's no known browser miner for BitcoinIL.

A browser miner can be expected to produce annywhere between 50h/s to 500kh/s - depends on the type and quality of the miner and the device it's being used on. 

#### CPU Mining

CPU Mining is the original method of mining Bitcoins and it simply utilizes the general purpose CPU to compute hashes.

CPU mining is suitable for everyone with an access to a computer

A modern CPU can generate roughly 50-500KH/s.

#### GPU Mining

GPU Minning is a modern advanced form of crypto currency mining and it utilizes the advanced capabilities of dedicated GPU (Graphics cards) that vastly outperform CPUs. It is highly recommended to mine using a GPU if you have a graphics card, as even with the lowest-performing cards the output will be far significant than using even the most advanced CPUs.

A modern GPU can generate roughly 2-50MH/s.

#### ASIC Mining

ASIC (Application Specific Integrated Circuit) Mining is considered the most advanced form for mining cryptocurrency and is mostly prevelant on the original Bitcoin network that utilizes the popular mining function SHA256 with gen 7 ASIC currently in operation.

ASIC miners are far superior to every other form of mining and modern Bitcoin miners can produce upwards of 100TH/s (that's Tera-Hash per Second). They're expensive and highly specialized devices used only for mining Bitcoin and similar crypto currencies.

### Mining Styles

#### Solo Mining

Solo-Mining is the simplest and oldest form of crypto-currency mining - you simply connect to a bitcoin node (the wallet with an exposed JSON-RPC server) using the mining software and every time you mine a block you get the full reward (currently 50 btcil per block).

#### Pooled Mining

Pool-Mining is easier than solo-mining as it doesn't require any local server to configure, and unlike solo-mining there's no need to solve an entire block - in a pooled mining scheem all the miners split the revenues according to their relative hash-rate compared to the overall hashrate of the pool.

It's recommended to mine BitcoinIL using the pool especially if you are planning to mine using CPU or if you're a newcomer to the mining scene.

The onyl currently known Bitcoin Israel supporting pool is the first Bitcoin Israel pool - [btcilpool.com](https://btcilpool.com).


### Mining Software

There is a wide variety of mining software available depending on the type and style of your desired mining setup.

The following are some of the tested software that were confired to work with Bitcoin Israel both in solo mining and pooled mining. Below we'll describe how to mine using the pool - if you'd like to mine solo please consult with previous versions of this guide or contact us via telegram.

In most cases you will need to download the appropriate version for your OS and GPU/CPU make and model, and provide a `configuration` or `launch` file - the configuration files are usually in JSON format or similar, while the `launch` files are usually BAT Executables that simply contain execution instruction for the miner executable.

You'll need to download the miner software, extract it somewhere convenient (such as `C:\btcil` folder - you will need to create this folder!) in it's own folder (e.g. if the miner is named `T-Rex Miner` extract it's contents to `C:\btcil\T-Rex Miner` so that you'll have the `t-rex.exe` file inside the dedicated directory: `C:\btcil\T-Rex Miner\t-rex.exe`), and add (or in some cases edit existing) configuration/launch file named `BTCIL-Pool.bat` which will contain the relevant configuration for your mining setup.

In all configuration and launch files replace `__YOUR_ADDRESS__` string with your actual address (you previously generated in the above section - _use_ the `legacy` address (non-Bech32), they start with `1` and not `il`!!!).

> Note: In all configuration and launch files the `Username` (often referred to as `-u VALUE` in launch files) should be Your Bitcoin Israel Legacy address, and the `Password` field can be used to identify individual miners you own and can contain any string you'd like
#### CPUMiner-OPT

- Github: [JayDDee/cpuminer-opt](https://github.com/JayDDee/cpuminer-opt/releases/)
- Download: [github.com/JayDDee/cpuminer-opt/releases/](https://github.com/JayDDee/cpuminer-opt/releases/)
- Suitable for: Any CPU
- Create `run-btcil.bat`:

```sh
cpuminer-aes-sse42.exe -a x17 -o stratum+tcp://btcilpool.com:8228 -u __YOUR_ADDRESS__ -p talisawesome
```

#### T-Rex Miner

- Github: [trexminer/T-Rex](https://github.com/trexminer/T-Rex/)
- Download: [https://github.com/trexminer/T-Rex/releases/](https://github.com/trexminer/T-Rex/releases/)
- Suitable for: Nvidia GPU

- Create `run-btcil.bat`:

```sh
  t-rex.exe -a x17 -o stratum+tcp://btcilpool.com:8228  -u __YOUR_ADDRESS__ -p talisawesome -d 0
```

Note:
You might want to consider the following parameters for your GPU health.
All details at https://github.com/trexminer/T-Rex/ welcome page.
Each GPU has its own recommended max temperature, so refer to your GPU vendor information.
```
  --temperature-limit        GPU shutdown temperature. (default: 0 - disabled)
  --temperature-start        GPU temperature to enable card after disable. (default: 0 - disabled)
```

#### CCMiner KlausT

- Github: [nemosminer/ccminer-KlausT](https://github.com/nemosminer/ccminer-KlausT-8.21-mod-r14/)
- Download: [https://github.com/nemosminer/ccminer-KlausT-8.21-mod-r14/releases/](https://github.com/nemosminer/ccminer-KlausT-8.21-mod-r14/releases/)
- Suitable for: Nvidia GPU
- Create `run-btcil.bat`:

```sh
ccminer.exe -a x17 --segwit -o stratum+tcp://btcilpool.com:8228 -u __YOUR_ADDRESS__ -p talisawesome -t 10 -i 20 -d 0 --debug
```


#### Geekminer

- Github: [quasars84/geekminer](https://github.com/quasars84/geekminer/)
- Download: [https://github.com/quasars84/geekminer/releases/](https://github.com/quasars84/geekminer/releases/)
-Suitable for: Nvidia GPU
- Create `run-btcil.bat`:

```sh
geekminer.exe --algo=x17 -o stratum+tcp://btcilpool.com:8228 --segwit -p talisawesome -u __YOUR_ADDRESS__ -t 10 --debug
```


#### SGMiner GM

- Github: [genesismining/sgminer-gm](https://github.com/genesismining/sgminer-gm)
- Download: [https://github.com/genesismining/sgminer-gm/releases](https://github.com/genesismining/sgminer-gm/releases)
- Suitable for: AMD GPU
- Create `sgminer-btcil.conf`:

```json
{
  "pools" : [
    {
      "url" : "stratum+tcp://btcilpool.com:8228",
      "user" : "__YOUR_ADDRESS__",
      "pass" : "talisawesome"
    },
  ],
  "intensity" : "18",
  "worksize" : "256",
  "kernel" : "x17",
  "lookup-gap" : "2",
  "thread-concurrency" : "8192",
  "shaders" : "0",
  "gpu-threads" : "2",
  "gpu-engine" : "0-0",
  "gpu-fan" : "0-0",
  "gpu-memclock" : "0",
  "gpu-memdiff" : "0",
  "gpu-powertune" : "0",
  "gpu-vddc" : "0.000",
  "temp-cutoff" : "95",
  "temp-overheat" : "85",
  "temp-target" : "75",
  "api-mcast-port" : "4028",
  "api-port" : "4028",
  "expiry" : "28",
  "failover-switch-delay" : "60",
  "gpu-dyninterval" : "7",
  "gpu-platform" : "0",
  "log" : "5",
  "no-pool-disable" : true,
  "queue" : "1",
  "scan-time" : "7",
  "tcp-keepalive" : "30",
  "temp-hysteresis" : "3",
  "shares" : "0",
  "kernel-path" : "/usr/local/bin"
}
```
- Create `start-btcil.bat`:

```sh
@echo off

setx GPU_FORCE_64BIT_PTR 0
setx GPU_MAX_HEAP_SIZE 100
setx GPU_MAX_USE_SYNC_OBJECTS 1
setx GPU_MAX_ALLOC_PERCENT 100
setx GPU_MAX_SINGLE_ALLOC_PERCENT 100

:loop
sgminer -c sgminer-btcil.conf --gpu-reorder
echo restart miner...
goto loop
```

## Mining Survey

Hopefully following this guide you've managed to both setup a wallet and a miner for BitcoinIL on your windows machine!

We're conducting a global open survey until the launch of the mainnet - if you'd like to participate simply send 0.0001 BTCIL to: [`il1qxk00fvuu3t8kug2d3fnd4p7gydyr6ja8wu9540`](https://explorer.bitcoinil.org/address/il1qxk00fvuu3t8kug2d3fnd4p7gydyr6ja8wu9540), Thank you!

## Faucet

If you'd like to receive a few testnet BTCIL coins give us a shoutout on the [platform of your choosing](/#social-networks) with your address and we'll send some your way to get you started!
