# Overlay Task Board

## Projects

- [ ] Python server for collateral manager ERC-1555 NFTs
- [ ] Balancer V2 core market implementation
- [ ] Developer documentation for `overlay-v1-core`
- [ ] PFP Planck cat NFT smart contracts
- [ ] IPFS for PFP NFTs
- [ ] Deployment scripts
- [ ] Liquidator bots in Python
- [ ] Basis trade bots


## Collateral Manager ERC1155 NFT Server

- Implement metadata server for OpenSea, etc. to query
- Queries collateral manager contract
- Should return static position information for `positionId`:

1. Market
2. Side (long/short)
3. Leverage
4. Debt
5. Cost
6. Maintenance

- Should return dynamic position information for `positionId`:

1. Value (in OVL)
2. PnL (in OVL)
3. Notional (in OVL)
4. Collateral (in OVL)
5. Entry price
6. Current price
7. Liquidation price (est)


- Existing boilerplate [FastAPI]() server in [`overlay-market/markets-api`](https://github.com/overlay-market/markets-api)

- Example image of metadata displayed on UI for an ETH/USDC market:

![Position Metadata](assets/images/erc1155-position-metadata.jpeg)


## PFP Planck cat NFT smart contracts
