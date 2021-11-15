# Collateral Manager ERC1155 NFT Server

## Outstanding Task

- Implement metadata Python server for OpenSea, etc. to query


## References

- Good [Flask example](https://github.com/ProjectOpenSea/metadata-api-python/blob/master/app.py) for ERC-721 metadata from OpenSea
- [OpenSea standards](https://docs.opensea.io/docs/metadata-standards)
- [ERC-1155 spec](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1155.md#erc-1155-metadata-uri-json-schema)
- Our [`OverlayV1OVLCollateral.sol`](https://github.com/overlay-market/overlay-v1-core/blob/main/contracts/collateral/OverlayV1OVLCollateral.sol) contract from `overlay-v1-core`
- OpenZeppelin's [ERC-1155 implementation](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC1155/extensions/ERC1155Supply.sol) which our collateral manager's inherit from
- [Forum post](https://forum.openzeppelin.com/t/create-an-erc1155/4433) from OpenZeppelin on creating an ERC-1155 token and validating associated metadata



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


- Existing boilerplate [FastAPI](https://github.com/tiangolo/fastapi) server in [`overlay-market/markets-api`](https://github.com/overlay-market/markets-api)

- Example image of metadata displayed on UI for an ETH/USDC market:

![Position Metadata](../assets/images/erc1155-position-metadata.jpeg)
