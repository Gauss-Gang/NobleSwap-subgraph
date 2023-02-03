# NobleSwap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Gauss Chain and NobleSwap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.

## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/blocks)**: Tracks all blocks on Gauss Chain.

2. **[Exchange](https://pancakeswap.medium.com/pancakeswap-info-relaunch-in-partnership-with-150-000-bounty-winner-streamingfast-f7892559d388)**: Tracks all NobleSwap Exchange data with price, volume, liquidity, ...

3. **[Farm Auctions](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/farm-auctions)**: Tracks all NobleSwap Farm Auctions with auctions and bids.

4. **[NFT Market (v1)](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/nft-market)**: Tracks all NobleSwap NFT Market for ERC-721.

5. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/pairs)**: Tracks all NobleSwap Pairs and Tokens.

6. **[Profile](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/profile)**: Tracks all NobleSwap Profile with teams, users, points and campaigns.

7. **[SmartChef](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/smartchef)**: Tracks all NobleSwap SmartChef (a.k.a. Syrup Pools) with tokens and rewards.

8. **[Timelock](https://thegraph.com/legacy-explorer/subgraph/pancakeswap/timelock)**: Tracks all NobleSwap Timelock queued, executed, and cancelled transactions.

## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.
