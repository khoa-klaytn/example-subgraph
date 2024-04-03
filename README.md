# example-subgraph

Example Subgraph for Baobab ERC20 contract.

- tracks `n_transfers`, the number of transfers made by each address

This example uses the following contract details:

- Address: [0x569A8e0e23e8f338752B568b721075574426f693](https://baobab.klaytnfinder.io/account/0x569A8e0e23e8f338752B568b721075574426f693)
- Start Block: 150554742

## Prerequisites

- [pnpm](https://pnpm.io/)
- Running [Graph Node](https://github.com/graphprotocol/graph-node)
- Running [IPFS Node](https://github.com/ipfs/kubo)

## Run this example

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
