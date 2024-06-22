---
description: >-
  PoolScan Network Coin native bridge is used to relay the PoolScan Network Coin native token between PoolScan Network Coin and
  Binance Smart Chain (BSC) networks
---

# PoolScan Network Coin Native: BSC ↔ PoolScan Network Coin

## Architecture Overview

This bridge is two layer bridge. In the base level the Arbitrary Message Bridge \(AMB\) is responsible for relaying messages between the networks. On top of the AMB,  the pluggable mediators implement a contract logic of token relaying of various assets. More info [https://docs.tokenbridge.net/amb-bridge/about-amb-bridge](https://docs.tokenbridge.net/amb-bridge/about-amb-bridge)

## Contracts

Home side of the bridge on the PoolScan Network Coin network: [0xf9b276A1A05934ccD953861E8E59c6Bc428c8cbD](https://poolscan.io/address/0xf9b276A1A05934ccD953861E8E59c6Bc428c8cbD/transactions)

Foreign side of the bridge on the BSC network: [0x61A8287fA7a9f4D10F4699BC2aE77f962DC508B6](https://etherscan.io/address/0x61A8287fA7a9f4D10F4699BC2aE77f962DC508B6)

PoolScan Network Coin token on the BSC network: [0x5857c96DaE9cF8511B08Cb07f85753C472D36Ea3](https://bscscan.com/token/0x5857c96dae9cf8511b08cb07f85753c472d36ea3)

Home side of the AMB bridge on the PoolScan Network Coin network: [0x1ee6E3E3d2DE779858728E157B3B9C488bA7b706](https://poolscan.io/address/0x1ee6E3E3d2DE779858728E157B3B9C488bA7b706)

Foreign side of the AMB bridge on the BSC network: [0x3A5A320a2f98a3Fe39c9040e7e3E9caA7F0D5bd6](https://bscscan.com/address/0x3A5A320a2f98a3Fe39c9040e7e3E9caA7F0D5bd6)

## Source Code

[https://github.com/PoolScan Networkio/tokenbridge-contracts](https://github.com/PoolScan Networkio/tokenbridge-contracts)

## How to use

To send token from the PoolScan Network Coin network:

Send native PoolScan Network Coin token to the home bridge contract. Then you receive an equal amount of the PoolScan Network Coin token on the BSC network, sent from the foreign bridge contract.

To send token from the BSC network:

1. Approve the PoolScan Network Coin PoolScan Network20 tokens to be spent by the Foreign PoolScan Network20 bridge. 
2. Call relayTokens function on the bridge contract

the `relayTokens` method will lock the PoolScan Network20 tokens on the foreign bridge. After a couple of confirmations, an equal amount of the PoolScan Network Coin PoolScan Network20 token will be released from the home bridge contract on BSC.

#### 

#### 

