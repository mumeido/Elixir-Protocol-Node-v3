# Elixir Protocol V3 Validator
# How to run Elixir Protocol V3 Validator

![1](https://raw.githubusercontent.com/mumeido/Elixir-Protocol-Node-v3/main/Elixir_1.jpeg)


To learn more about Elixir Protocol, you can go here and read about their Blog [here](https://docs.elixir.xyz).

[Elixir](https://elixir.xyz) is a modular DPoS network built to power liquidity on orderbook exchanges. The cross-chain and composable nature of Elixir allows orderbook DEXs to seamlessly incorporate Elixir Protoco, a decentralized protocol, into their core infrastructure. This opens up fascinating new use cases, such as retail liquidity for pairs. The decentralized network provides the essential foundational support that enables protocols and exchanges to quickly add liquidity to their books.


## Hardware Requirements
Most hardware is capable of running a validator node. However, it is recommended that you have a system that can be run 24 hours a day, with 8GB of memory and a reliable 100Mbit internet connection. Disk usage is minimal; in most cases, 100GB of storage should be enough.

## Step 1: Update System

### Update System
```bash
sudo apt update && sudo apt upgrade -y
```
### Install Prerequisites & Docker
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```
If the response is “Docker not found” then go to [Docker](https://www.docker.com/products/docker-desktop/) for setting it up on your device.

## Step 2: Verify Docker Installation

### Verify Docker Installation
```bash
docker --version
```

## Step 3: Install Docker Pull

```bash
docker pull elixirprotocol/validator:v3
```
## Step 4: Create accuser directory

```bash
mkdir /home/elixir
cd /home/elixir
nano validator.env
```
## Step 5: Edit .ENV File

```bash
ENV=testnet-3

STRATEGY_EXECUTOR_IP_ADDRESS= Ip Vps
STRATEGY_EXECUTOR_DISPLAY_NAME=  Nama validator
STRATEGY_EXECUTOR_BENEFICIARY= Address validator
SIGNER_PRIVATE_KEY= Privat key
```
## Step 6: Run the docker

```bash
docker run -d --env-file /home/elixir/validator.env --name elixir --restart unless-stopped elixirprotocol/validator:v3
```
[2](https://raw.githubusercontent.com/mumeido/Elixir-Protocol-Node-v3/main/elixir_2.PNG)

After that, go to [Tesnet](https://testnet-3.elixir.xyz/) page and claim $MOCK with Epolia ETH and then delegate to your validator by clicking Custom Validator







