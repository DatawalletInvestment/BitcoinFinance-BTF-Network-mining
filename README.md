# BitcoinFinance-BTF-Network-mining
Bitcoin Finance forked chain mining
# Solo Mining BitcoinFinance-BTF Tutorial
This tutorial provides instructions for setting up a BitcoinFinance BTF Network Node and a mining pool. For this tutorial, I used an bitcoin finance node for guide.

:donate: BitcoinFinance BTF address: 1EaEtsRk4sHs1sD1FJhj5AybcdKjmsCcCf

:electric_plug: Will get you set up and provide support/training for just 1 BTF!



## Definitions
**BitcoinFinance Node:** A server running [BitcoinFinance Core](https://www.doji.today/) that maintains it's own blockchain. Bitcoin Finance nodes make up the backbone of the BTF network. By running your own node, you serve as a peer in the peer-to-peer network that is BitcoinFinance Core.

**Mining Pool:** A server running [Stratum protocol](https://en.bitcoin.it/wiki/Stratum_mining_protocol) that can be connected to by mining rigs (e.g. A4+ LTC S9I S9J T9+,S19, Antminer ,avalon 1346) using HTTP(S). The Stratum pool used in this tutorial is [Bitforce Pool](https://www.bitforcepool.com) you can also using [IEpool](https://www.iepool.com).

## Prerequisites
You should be comfortable working on the command line and using Linux / windows. For this tutorial, we will use a Ubuntu 16 virtual machine (I'm use Google Cloud Engine).

You will need to install and configure the BitcoinFinance daemon running on Ubuntu /windows. You will also need to install and configure Node cmd / sh.

Understanding networking will help as well. Since you'll be running a few services that heavily depend on a reliable network connection.

You don't need to be a developer but to support this setup and solo mine for a long enough time to actually mine a block, you need system admin skills (might be wise to find a techie friend who can help admin this setup if this is something new to you)

## Getting Started

:information_source: If you're doing this on AWS or GCP, use a large instance with good network connection then after you finish, dial it down to a smaller instance.

First, begin by setting up a Ubuntu server. You will need to have enough disk space for the blockchain. I'm using these specs on Google Cloud Engine:

* Ubuntu 16.04
* 1 vCPU
* 2.5 GB memory
* 20 GB disk

:star: Once you have your server all setup just do an update before we get going:
```
sudo apt-get update
```

## Step 1: Installing BitcoinFinance Core
You will need to install and configure BitcoinFinance  Core on your server. You will need to be running BitcoinFinance Core (BitcoinFinance Daemon) as well. BitcoinFinance Daemon needs to run 24/7/365 while mining is happening. Here's how I recommend to install it.

1. Change to `/opt` since that's where software should be install on Linux OSs:
```
cd /opt
```
2. Get BitcoinFinance Core (double check you're getting the latest, at the time of writing 0.14.2 was the latest):
```
wget https://www.doji.today/DojiNode/released_unix_x86_x64_dcr_ver1.5.1.tar.gz
```
3. Uncompress Litecoin Core and remove the compressed file:
```
tar -xvzf released_unix_x86_x64_dcr_ver1.5.1.tar.gz
rm -rf released_unix_x86_x64_dcr_ver1.5.1.tar.gz
```
4. At this point, you've got Litecoin Core software in `/opt/released_unix_x86_x64_dcr_ver1.5.1`. Next, we need to configure the BitcoinFinance Daemon

## Step 2: Starting BitcoinFinance Daemon
First we will configure the BitcoinFinance Daemon then we'll start it. BitcoinFinance Daemon looks for a `bitcoin.conf` file. If you go to `/opt/released_unix_x86_x64_dcr_ver1.5.1` and try running the daemon without a config you can see where it's looking for you configuration file:
```
cd /opt/released_unix_x86_x64_dcr_ver1.5.1

```
Before runing a bitcoinFinance node you should install dependency of bitcoin Finance:
here some helpful link:
## Dependency Build Instructions
Linux Distribution Specific Instructions
Ubuntu & Debian
Dependency Build Instructions

Build requirements:
```
sudo apt-get install build-essential cmake pkg-config python3
```
Now, you can either build from self-compiled depends or install the required dependencies:
```
sudo apt-get install libevent-dev libboost-dev
```
SQLite is required for the descriptor wallet:
```
sudo apt install libsqlite3-dev
```
Berkeley DB is only required for the legacy wallet. Ubuntu and Debian have their own libdb-dev and libdb++-dev packages, but these will install Berkeley DB 5.3 or later. This will break binary wallet compatibility with the distributed executables, which are based on BerkeleyDB 4.8. Otherwise, you can build Berkeley DB yourself.

To build Bitcoin Core without wallet, see Disable-wallet mode

Optional port mapping libraries (see: -DWITH_MINIUPNPC=ON and -DWITH_NATPMP=ON):
```
sudo apt install libminiupnpc-dev libnatpmp-dev
```
ZMQ dependencies (provides ZMQ API):
```
sudo apt-get install libzmq3-dev
```
User-Space, Statically Defined Tracing (USDT) dependencies:
```
sudo apt install systemtap-sdt-dev
```
GUI dependencies:

Bitcoin Core includes a GUI built with the cross-platform Qt Framework. To compile the GUI, we need to install the necessary parts of Qt, the libqrencode and pass -DBUILD_GUI=ON. Skip if you don't intend to use the GUI.
```
sudo apt-get install qtbase5-dev qttools5-dev qttools5-dev-tools
```
Additionally, to support Wayland protocol for modern desktop environments:
```
sudo apt install qtwayland5
```
The GUI will be able to encode addresses in QR codes unless this feature is explicitly disabled. To install libqrencode, run:
```
sudo apt-get install libqrencode-dev
```
Otherwise, if you don't need QR encoding support, use the -DWITH_QRENCODE=OFF option to disable this feature in order to compile the GUI.



**Step 1: Sample BitcoinFinance BTF Daemon Configuration**
```
./bitcoin-qt -maxtipage=100000000000000  -gen -datadir=.\chaindata\  -rpcuser=btf  -rpcpassword=abc123   -rpcport=3333  -rpcallowip=192.168.1.0/24  -rpcbind=192.168.1.102   -printtoconsole

```

## Step 2: Creating your mining account in bitforce or iepool (BitcoinFinance Mining Pool)
Now that we have BitcoinFinance Daemon running, we can setup out Stratum server where we can connect our mining rig and start working.
 [Bitforce Pool](https://www.bitforcepool.com)
 [Iepool ](https://www.iepool.com)



## Step 3: Connect your ASICS
Open you asic's panel
configure as follow:
stratum:    stratum+tcp://miner.bitforcepool.com:3333
worker:     Your_BTF_ADDRESS.Your_Worker_Name       eg.  1EaEtsRk4sHs1sD1FJhj5AybcdKjmsCcCf.MYASIC3
Password:  BTF

It takes about 24 Hours to get BTF in your Bitcoin Finance Daemon balance.



