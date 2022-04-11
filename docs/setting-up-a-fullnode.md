# How to run a Gravity Bridge mainnet full node

A Gravity chain full node is just like any other Cosmos chain.
Unlike the validator flow no external software is required.

## What do I need

A Linux server with any modern Linux distribution, 4gb of ram and at least 320gb storage.

### Download Gravity chain software

```bash
wget https://github.com/Gravity-Bridge/Gravity-Bridge/releases/download/v1.5.0/gravity-linux-amd64
mv gravity-linux-amd64 gravity

chmod +x gravity
sudo mv gravity /usr/bin/
```

### Init the config files

```bash
cd $HOME
gravity init <MYMONIKER> --chain-id gravity-bridge-3
```

### Copy the genesis file

```bash
wget https://raw.githubusercontent.com/Gravity-Bridge/gravity-docs/main/genesis.json
cp genesis.json $HOME/.gravity/config/genesis.json
```

### Add seed node

Change the seed field in ~/.gravity/config/config.toml to contain the following:

```text

seeds = "2b089bfb4c7366efb402b48376a7209632380c9c@65.19.136.133:26656,63e662f5e048d4902c7c7126291cf1fc17687e3c@95.211.103.175:26656"

```

### Return To The Gravity Toolbox

[SkyNet | Validators Gravity Bridge Toolbox](https://gravity-snapshot01.skynetvalidators.com/index.nginx-debian.html)
