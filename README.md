# learn-blockchain
Notes from a PDD day on Blockchain

## Pluralsight Course

URL: https://app.pluralsight.com/library/courses/ethereum-blockchain-developing-applications/table-of-contents

## Notes

### Background / Introduction

Banks have a number of downsides: 

  1. require you to have total trust 
  2. Slow at processing.
  3. High fees for transactions.

With bitcoin ... don't need to trust as the system is decentralised. 
The network is/has:

  1. A public registry of assets and transactions.
  2. Its autonomous - controlled by software.
  3. Permisionless - anyone can join.
  4. Cryptographically secure. Cannot modify or forge entries.

A Blockchain - has a first block the "genesis" block. 
From here on the entries contain the id, the previous hash, the current hash (and nounce) and the payload.
Important to note that you cannot update or delete blocks on the chains - in this way its immutable.

### Ethereum

Ethereum is like a platform for applications / currencies. Other blockchain based applications needed to develop the blockchain from sratch.
It has its own currency ETH. It also has its own Turing complete language (solidity?)

Ethereum Projects:
  * Augur
  * Grid+
  * MERIDIO
  * VIANT

Types are of network are: Private, Consortium, Public

*Ethereum Wallet* - A key store, does not contain money.
*Test Networks* - Ropsten, Rinkeby, create your own.
*Faucet* - Get test ether to for a test network.


### Smart Contracts

These can be written in the following languages:
  * Solidity - javascript like
  * Serpent - python-like
  * Vyper - new python-like security oriented

Using solidity there is a web based IDE at remix.ethereum.io

There are 3 different sorts of node:
  * Miners - execute transaction, genereate blocks, get rewards.
  * Full nodes - verify transactions, store full chain, don't get rewards.
  * Light clients - only proces some transactions, rely on full nodes for validation.

Ethereum denominations are (in terms of 1 ether)
finney = 0.001
szabo = 0.000001
wei = 0.000000000000000001

# Worked Example
Most of this is taken from:
https://gist.github.com/cryptogoth/10a98e8078cfd69f7ca892ddbdcf26bc

This is the installation for Ubuntu only:
```
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install ethereum
```

Run on the Rinkeby test network:
```
geth --rinkeby
```

in another terminal run the console:
```
geth --datadir=$HOME/.ethereum/rinkeby attach ipc:$HOME/.ethereum/rinkeby/geth.ipc console
```

```
geth account new
```
