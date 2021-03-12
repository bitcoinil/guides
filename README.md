# BitcoinIL

BitcoinIL Is a direct clone of the [Bitcoin Core](/bitcoin/bitcoin) bitcoin with two minor changes: Modificationn to the addresses format to distringuish BTCIL addresses from BTC addresses, and a change to the mining hashing function from the Bitcoin's prefered SHA256 to the somewhat less popular X17 function.

The purpose of this clone is to experiment scaling Bitcoin and bitcoin sideways, and as opoosed to changing the block size or interval, as few other currencies have already implemented, BitcoinIL chooses to simply create a new instance of the Bitcoin blockchain from the first block.

Read below for a more detailed description of the motivation behind BTCIL.

## Installation

### Windows

Wallet Binaries: [bitcoinil-0.21.0-win64-setup.exe](https://github.com/bitcoinil/guides/raw/main/assets/binaries/windows/bitcoinil-0.21.0-win64-setup.exe)

Guide: [BitcoinIL Windows Wallet and Miner Installation Guide](https://github.com/bitcoinil/guides/blob/main/Windows.md)

### Mac OSX

Wallet Binaries: [BitcoinIL-Qt.dmg](https://github.com/bitcoinil/guides/raw/main/assets/binaries/osx/BitcoinIL-Qt.dmg)

### Linux - Ubuntu

Wallet Binaries: [btcil-ubuntu20.zip](https://github.com/bitcoinil/guides/raw/main/assets/binaries/Linux/btcil-ubuntu20.zip)

## Motivation

Bitcoin as we know it today is a respectable piece of software that performs a single function very well, it performs that function so well that it’s value keeps climbing	over the years, but with that value the desire to own and therefore the need to transact bitcoin create a sellers market with TX fees rising to tens of dollars for standard transactions in times of growth.

Many solutions have been suggested, tried, and some are still operational to this day to “remedy” this situation - the problem of the limited capacity of the bitcoin network, the apparently low transactions throughput of the current bitcoin blockchain.

I personally always took the Bitcoin Core path - can’t say why exactly but extending the blocks always seemed wrong to be like implemented by BCH. I see value in the “It works? Don’t break it!” approach, especially considering how easy and simple it is to simply try it on a new network.

Litecoin, Namecoin, Ripple, Ethereum, Dogecoin, and many others took “something” from bitcoin and made it their own, they’ve seen the beauty that is bitcoin’s core idea, and some even used the original code as their baseline. The open source nature of bitcoin not only enables it, it demands it. It demands us to explore and experiment, as we have from the very first moments we’ve realized what we’re dealing with.

I’m proposing a simple and novel approach to the scaling issue, to scale the existing bitcoin consensus sideways. If bitcoin’s Blockchain is comparable to a physical notebook, and each page in that notebook represents a block, and each row a transaction, and our current bitcoin blockchain is limited to a single page per hour, then I simply propose to make another notebook with the same rules and codebase as the one we know and love.

The incentive is simply to explore the vast space of possible options, but unlike all the predecessors that took something from bitcoin and added something of their own, I favor the path of not adding or modifying anything. Well, almost.

There’s another issue with bitcoin’s current model, current blockchain - it’s miners are heavily centered in China. They’re essentially fortified their position by leapfrogging the entire mining industry in ASIC production and the local mining industry that has access to plentiful power supplies needed for mining.

With the new network I’m proposing to changing the mining algorithm from the existing ASIC dominated function to a less-popular hashing function that has no significant ASIC presence, which will allow the network to be both mined initially by the users who put their faith in to this network and potentially allow for a new ASIC development from gen 1, effectively leveling the playing field.

It’s a simple and effective experiment to conduct in an attempt to remedy the two issues mentioned. The way I see things bitcoin in general and Bitcoin Core specifically have proven over a decade that it can deliver on a simple promise: it will continue to function the same way tomorrow as it does today. The might sound like a promise to brush off, but it’s more than a trillion dollar economy, you can’t brush that off that easily.

That promise is huge, it’s the core of what I believe in Bitcoin. I’m a developer, I understand that if I write code a certain way the computer will interpret that a certain way, it makes sense to me. Bitcoin uses clever maths and crypto to make sure that simple commands are executed well and according to an agreed upon standard which cannot be forged or counterfeited using any known methods or techniques.

By creating a new network based on the existing consensus and codebase of Bitcoin Core we effectively double the capacity of the blockchain space the Bitcoin Core consensus commands - without altering a single line of code in the original bitcoin codebase.

We can show others that this path is possible by simply taking it and building the new network, and as others will see this network grow they will too join and create yet new Bitcoin Core based networks, extending the consensus’s reach even further, and extending the capacity and throughput along the way. Solidifying the resiliency of the core idea in both standard and implementation.

It’s a perfect way to scale giving no-man power over the individual networks as they’re all bound to the original code by design, and as with Bitcoin itself, any deviation from that binding will simply result in yet-another-blockchain which defeats the purpose, and yet it empowers those who garner and nourish it, as Bitcoin does.

I choose to name it Bitcoin Israel (BTCIL), or Bitcoin IL, because I am Israeli, I’ve lived here all my life, and I love this place and the people in it. Israel has been an amazingly fertile ground for the adoption of Bitcoin specifically and crypto in general and is a huge exporter of crypto technologies, products, and experts. Because like Dogecoin have shown us Bitcoin can be a tool for a community to rally around and Israel has a huge community of bitcoin and cryptocurrencies lovers.

Some of us have been “bitcoin crazy” since as early as 2011, and we’re proud of our bitcoin heritage, and while we’ve contributed substantially thus far, some want to go even further, and explore new grounds still, and make sure that Bitcoin prospers and proliferates as an idea and as living code.

Israel has a rich history in mining technology and operations, the change of the mining function will allow the local industry to develop new ASIC hardware from first generation, and if others follow a similar path it will allow Israel to become an industry leader in ASIC design and development in the future by providing early experience advantage, furthering the decentralization of bitcoin in general and it’s mining specifically.

Israelis are international in their travels and very hospitable and welcoming at home, and Bitcoin Israel embraces the open nature (and source) of Bitcoin and as such is a fully open network that anyone is welcome to participate in - while the name does imply affiliation, no man, governmental organization, or for-or-non-profit organization has any preference in this network, as we believe any such network should be.

We hope that this experiment will prove successful and will provide a reasonable effective method of scaling the bitcoin network and improve the bitcoin ecosystem both locally in Israel and globally.

## Social Networks

Follow us on social networks:

- Follow us on Twitter: https://twitter.com/il_bitcoin
- Join us via Facebook group: https://www.facebook.com/groups/bitcoinli
- Follow our Telegram official announcements channel: https://t.me/itsbtcil
- Join our Telegram Group: https://t.me/bitcoinilnetwork
- Join our Subreddit: https://www.reddit.com/r/bitcoinli/