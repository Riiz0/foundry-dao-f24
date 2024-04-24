# Foundry DAO Governance

## About

1. We are going to have a contract controlled by a DAO
2. Every transaction that the DAO wants to send has to be voted on
Please note: ERC20 based voting is not always recommended, and I encourage you to explore other forms of governance like reputation based or "skin-in-the-game" based.
Plutocracy is bad! Don't default to ERC20 token voting!!

- [Foundry DAO Governance](#foundry-dao-governance)
  - [About](#about)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Quickstart](#quickstart)
- [Usage](#usage)
  - [Test](#test)
  - [Deploy](#deploy)
  - [Deploy - Other Network](#deploy---other-network)
  - [Testing](#testing)
  - [Estimate Gas](#estimate-gas)
- [Formatting](#formatting)
  - [Foundry](#foundry)
  - [Documentation](#documentation)
  - [Usage](#usage-1)
    - [Build](#build)
    - [Test](#test-1)
    - [Format](#format)
    - [Gas Snapshots](#gas-snapshots)
    - [Anvil](#anvil)
    - [Deploy](#deploy-1)
    - [Cast](#cast)
    - [Help](#help)

# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You'll know you did it right if you can run `forge --version` and you see a response like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`

## Quickstart

```
git clone https://github.com/Riiz0/foundry-dao-f24.git
cd foundry-defi-stablecoin-f23
forge build
```

# Usage

## Test

```
forge test
```

## Deploy

I did not write deploy scripts for this project, you can if you'd like!

This will default to your local node. You need to have it running in another terminal in order for it to deploy.

```
make deploy
```

## Deploy - Other Network

[See below](#deployment-to-a-testnet-or-mainnet)

## Testing

We talk about 4 test tiers in the video.

1. Unit
2. Integration
3. Forked
4. Staging

```
forge test
```

```
forge coverage
```

and for coverage based testing:

```
forge coverage --report debug
```

## Estimate Gas

You can estimate how much gas things cost by running:

```
forge snapshot
```
And you'll see and output file called `.gas-snapshot`

# Formatting

To run code formatting:

```
forge fmt
```

## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
