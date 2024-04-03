# example-subgraph

Example Subgraph for Baobab ERC20 contract.
The Subgraph tracks `n_transfers`, the number of transfers made by each address.

## Prerequisites

- [pnpm](https://pnpm.io/)
- Running [Graph Node](https://github.com/graphprotocol/graph-node)
- Running [IPFS Node](https://github.com/ipfs/kubo)

## Simple Start

1. Install dependencies

```
pnpm i
```

2. Generate the subgraph.yaml file

```
pnpm run codegen
```

Rerun when `abis/*`, `schema.graphql` or `subgraph.yaml` changes

3. Build the subgraph

```
pnpm run build
```

Rerun when `src/*` changes

4. Create a subgraph on the graph node

```
export GRAPH_ADMIN_URL=<Graph Node Admin URL>
pnpm run create
```

5. Deploy the subgraph

```
export GRAPH_ADMIN_URL=<Graph Node Admin URL>
export IPFS_ADMIN_URL=<IPFS Node Admin URL>
pnpm run deploy
```

6. Query the subgraph

A GraphQL UI & API should be exposed at `<Graph Node Query URL>/subgraphs/name/example-subgraph`

- **QUERY** URL, not Admin URL!
