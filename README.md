# Hydro Protocol V1 Smart Contracts.
These contracts are created and owned by The Hydro Protocol Foundation (not me).

## Before you deploy:
- These contracts are very expensive the deploy, so consider testing on a test net first.
- The HybridExchange contract uses alot of gas, try a gas limit of `5000000` or more.
- **Should use solidity compilier version `0.4.24`;** *commit.e67f0147*

## How to deploy:
1. First Deploy `Proxy.sol` 
2. Deploy `HybridExchange.sol`, passing the `Proxy` contract address and the address of the discount token (`0x9af839687f6c94542ac5ece2e317daae355493a1`) to the constructor.
3. Call addAddress on the `Proxy` contract with the address of your relayer account (Any ethereum account which you have the private key for).