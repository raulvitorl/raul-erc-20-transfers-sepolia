# USDC Transfers Subgraph (Sepolia)

Subgraph que indexa eventos **Transfer** e **Approval** do contrato USDC na rede Sepolia Testnet, além de eventos administrativos do proxy.

## Tecnologias
- The Graph (Subgraph Studio & decentralized network)
- AssemblyScript (mappings)
- GraphQL schema & event handlers
- Proxy handling (FiatTokenProxy + implementation)

## Query URL (Development - rate-limited)
https://api.studio.thegraph.com/query/1743097/raul-erc-20-transfers-sepolia/version/latest

## Exemplos de Queries
```graphql
{
  transfers(first: 10, orderBy: timestamp, orderDirection: desc) {
    id
    from
    to
    value
    timestamp
  }
}