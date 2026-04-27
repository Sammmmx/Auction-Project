# Auction Contract

## Overview
A decentralized auction system built in Solidity that supports multiple simultaneous auctions. Users can create auctions, place bids, and cancel auctions. Gas optimized with custom errors and mapping-based state management.

## Contract
- `Auction.sol` — Core auction contract

## Features
- Create multiple auctions with unique item numbers
- Time-based auction duration
- Bidding with exact payment enforcement
- Owner can cancel active auctions
- Check auction status, highest bidder and active bid price
- Gas optimized — no array loops, mapping based lookups
- Custom errors throughout
- Events on every state change

## Tech Stack
- Solidity ^0.8.26
- Hardhat
- Ethers.js
- Chai

### Installation
npm install

### Run Tests
npx hardhat test

### Deploy
npx hardhat ignition deploy ignition/modules/Auction.js --network sepolia

## Deployed Contract
- Network: Sepolia Testnet
- Address: 0x772eAeC1C8d996f8C8B8F56E6F8485935DbA44A8
- Verified on: Etherscan - https://sepolia.etherscan.io/address/0x772eAeC1C8d996f8C8B8F56E6F8485935DbA44A8

## Test Coverage
Tests passing covering:
- createAuction access control and validations
- Bidding with correct and incorrect amounts
- Auction cancellation
- checkAuctionActive status
- checkHighestBidder after bids
- checkActiveBidPrice validations
- Event emission for all functions

## License
MIT
