## Pool Proxy - RustMinerSystem(Not Support Pump,Nginx Forward Only )

## Install RustMinerSystem for Bitcoin Finance BTF Network(a new BTC forked chain) in Linux

```
wget  https://github.com/EvilGenius-dot/RustMinerSystem/raw/main/install.sh;
sudo chmod 777 ./install.sh;
sudo ./install.sh
```

## Install RustMinerSystem for Bitcoin Finance BTF Network(a new BTC forked chain) in ARM
```
wget  https://github.com/EvilGenius-dot/RustMinerSystem/raw/main/arm-install.sh;
sudo chmod 777 ./arm-install.sh;
sudo ./arm-install.sh
```



## Install RustMinerSystem for Bitcoin Finance BTF Network(a new BTC forked chain) in Windows

1.Download Rustminersystem
[RustminerSystem](https://www.bitforcepool.com/farmproxy/bitforce-farmproxy.zip)

2.Open control panel of rustminersystem
For the Windows version, simply double-click to start it.


## Using RustMinerSystem for Bitcoin Finance BTF Network
The default username and password for the backend are:
http://localhost:<PORT>
UserName:qzpm19kkx  
Password:xloqslz913

Create a new line for NGINX FORWORD and configure with follow stratum lines:
```

Bitforce Pool:
HiveOS-GPU
stratum+tcp://hiveos1.bitforcepool.com:3335
stratum+tcp://hiveos2.bitforcepool.com:3335
stratum+tcp://hiveos3.bitforcepool.com:3335
HiveOS-CPU
stratum+tcp://cpu1.bitforcepool.com:3335
stratum+tcp://cpu2.bitforcepool.com:3335
Asics
stratum+tcp://asic1.bitforcepool.com:3333
stratum+tcp://asic1.bitforcepool.com:3335
stratum+tcp://asic2.bitforcepool.com:3335
stratum+tcp://asic2.bitforcepool.com:3333
stratum+tcp://asic3.bitforcepool.com:3335
stratum+tcp://asic3.bitforcepool.com:3333

Global pool:
Pro Line(best):
stratum+tcp://btf.bitforcepool.com:3334
stratum+tcp://btf.bitforcepool.com:3335
Global1:
stratum+tcp://miner.bitforcepool.com:3334
Global2:
stratum+tcp://pool.bitforcepool.com:3334
US:
stratum+tcp://us.bitforcepool.com:3333
Japan:
stratum+tcp://jp.bitforcepool.com:3333
Europe:
stratum+tcp://eur.bitforcepool.com:3333
Asia:
stratum+tcp://asia.bitforcepool.com:3333
Africa:
stratum+tcp://af.bitforcepool.com:3333
Canada:
stratum+tcp://ca.bitforcepool.com:3333
Finland:
stratum+tcp://fin.bitforcepool.com:3333
Singapore:
stratum+tcp://sin.bitforcepool.com:3333
Australia:
stratum+tcp://au.bitforcepool.com:3333

```
