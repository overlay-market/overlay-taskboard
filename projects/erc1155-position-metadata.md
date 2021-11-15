# Collateral Manager ERC1155 NFT Server

## Outstanding Task

- Implement metadata Python server for OpenSea, etc. to query

## Requirements

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

![Position Metadata](../assets/images/erc1155-position-metadata.jpeg)
