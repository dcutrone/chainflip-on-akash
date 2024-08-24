## What is Chainflip?
Chainflip is a decentralised, trustless protocol that enables native cross chain swaps between different blockchains.

## What is Akash?
Akash is an open network that lets users buy and sell computing resources securely and efficiently. 

## How to deploy Chainflip RPC node on Akash?
1. Fund your wallet with AKT tokens
2. Open [Akash Console](https://console.akash.network/)
3. Use SDL from this repository to deploy Chainflip RPC node

## How to use RPC?
Example RPC request:
```
curl -H "Content-Type: application/json" -d '
{
   "id":1,
   "jsonrpc":"2.0",
   "method":"cf_pool_info",
   "params":{
      "base_asset":{
         "chain":"Ethereum",
         "asset":"ETH"
      },
      "quote_asset":{
         "chain":"Ethereum",
         "asset":"USDC"
      }
   }
}' http://localhost:9944
```

Replace http://localhost:9944 with forwarded port from Akash Console.

Method cf_pool_info returns the fees percentages LP's earn in the given pool.

More useful RPCs in [Chainflip Docs](https://docs.chainflip.io/lp/integrations/lp-rpcs).
