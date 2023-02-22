# BanklessDAO Snapshot Configuration

The Snapshot strategy configuration used by BanklessDAO

It uses a `multichain` top-level strategy which contains multiple sub-strategies.

# Params

```
{
  "graphs": {
    "137": "https://api.thegraph.com/subgraphs/name/sameepsi/maticblocks"
  },
  "symbol": "BANK",
  "strategies": [
    {
      "name": "erc20-balance-of",
      "params": {
        "address": "0x2d94AA3e47d9D5024503Ca8491fcE9A2fB4DA198",
        "decimals": 18
      },
      "network": 1
    },
    {
      "name": "erc20-balance-of",
      "params": {
        "address": "0xDB7Cb471dd0b49b29CAB4a1C14d070f27216a0Ab",
        "decimals": 18
      },
      "network": 137
    },
    {
      "name": "erc20-balance-of",
      "params": {
        "address": "0x29FAF5905bfF9Cfcc7CF56a5ed91E0f091F8664B",
        "decimals": 18
      },
      "network": 10
    },
    {
      "name": "balancer",
      "params": {
        "symbol": "BANK",
        "address": "0x2d94AA3e47d9D5024503Ca8491fcE9A2fB4DA198",
        "decimals": 18
      },
      "network": 1
    },
    {
      "name": "balancer",
      "params": {
        "symbol": "BANK",
        "address": "0xDB7Cb471dd0b49b29CAB4a1C14d070f27216a0Ab",
        "decimals": 18
      },
      "network": 137
    },
    {
      "name": "staked-balancer",
      "params": {
        "tokenAddress": "0xdb7cb471dd0b49b29cab4a1c14d070f27216a0ab",
        "balancerPoolId": "0x5a6ae1fd70d04ba4a279fc219dfabc53825cb01d00020000000000000000020e",
        "stakingContract": "0xc48c3a19bc79b9d6ac4391723041584114a4272d",
        "symbol": "BANK"
      },
      "network": 137
    },
    {
      "name": "sushiswap",
      "params": {
        "symbol": "BANK",
        "address": "0x2d94AA3e47d9D5024503Ca8491fcE9A2fB4DA198",
        "masterchefVersion": "v1",
        "useStakedBalances": "true"
      },
      "network": 1
    },
    {
      "name": "sushiswap",
      "params": {
        "symbol": "BANK",
        "address": "0xDB7Cb471dd0b49b29CAB4a1C14d070f27216a0Ab",
        "masterchefVersion": "v2",
        "useStakedBalances": "true"
      },
      "network": 137
    },
    {
      "name": "uniswap",
      "params": {
        "symbol": "BANK",
        "address": "0x2d94aa3e47d9d5024503ca8491fce9a2fb4da198"
      },
      "network": 1
    },
    {
      "name": "uniswap-v3",
      "params": {
        "symbol": "BANK",
        "poolAddress": "0x1a80afe14143637c0b7609e6e276464e4f748014",
        "tokenReserve": 0
      },
      "network": 1
    },
    {
      "name": "uniswap-v3",
      "params": {
        "symbol": "BANK",
        "poolAddress": "0x25Bd78d2189a19Ce1742c252D5C5b1cC4864Fea9",
        "tokenReserve": 0
      },
      "network": 10
    },
    {
      "name": "arrakis-finance",
      "params": {
        "symbol": "BANK",
        "decimals": 18,
        "tokenAddress": "0x2d94AA3e47d9D5024503Ca8491fcE9A2fB4DA198",
        "poolAddress": "0x472D0B0DDFE0BC02C27928b8BcbD67E65D07d48a"
      },
      "network": 1
    },
    {
      "name": "rari-fuse",
      "params": {
        "symbol": "BANK",
        "token": "0x2d94AA3e47d9D5024503Ca8491fcE9A2fB4DA198",
        "fToken": "0x250316B3E46600417654b13bEa68b5f64D61E609"
      },
      "network": 1
    }
  ],
  "startBlocks": {
    "137": 13000000
  }
}
```

# Playground Link
https://snapshot.org/#/playground/multichain?query=eyJwYXJhbXMiOnsiZ3JhcGhzIjp7IjEzNyI6Imh0dHBzOi8vYXBpLnRoZWdyYXBoLmNvbS9zdWJncmFwaHMvbmFtZS9zYW1lZXBzaS9tYXRpY2Jsb2NrcyJ9LCJzeW1ib2wiOiJCQU5LIiwic3RyYXRlZ2llcyI6W3sibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoiZXJjMjAtYmFsYW5jZS1vZiIsInBhcmFtcyI6eyJhZGRyZXNzIjoiMHgyOUZBRjU5MDViZkY5Q2ZjYzdDRjU2YTVlZDkxRTBmMDkxRjg2NjRCIiwiZGVjaW1hbHMiOjE4fSwibmV0d29yayI6MTB9LHsibmFtZSI6ImJhbGFuY2VyIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJhZGRyZXNzIjoiMHgyZDk0QUEzZTQ3ZDlENTAyNDUwM0NhODQ5MWZjRTlBMmZCNERBMTk4IiwiZGVjaW1hbHMiOjE4fSwibmV0d29yayI6MX0seyJuYW1lIjoiYmFsYW5jZXIiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweERCN0NiNDcxZGQwYjQ5YjI5Q0FCNGExQzE0ZDA3MGYyNzIxNmEwQWIiLCJkZWNpbWFscyI6MTh9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InN0YWtlZC1iYWxhbmNlciIsInBhcmFtcyI6eyJ0b2tlbkFkZHJlc3MiOiIweGRiN2NiNDcxZGQwYjQ5YjI5Y2FiNGExYzE0ZDA3MGYyNzIxNmEwYWIiLCJiYWxhbmNlclBvb2xJZCI6IjB4NWE2YWUxZmQ3MGQwNGJhNGEyNzlmYzIxOWRmYWJjNTM4MjVjYjAxZDAwMDIwMDAwMDAwMDAwMDAwMDAwMDIwZSIsInN0YWtpbmdDb250cmFjdCI6IjB4YzQ4YzNhMTliYzc5YjlkNmFjNDM5MTcyMzA0MTU4NDExNGE0MjcyZCIsInN5bWJvbCI6IkJBTksifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJzdXNoaXN3YXAiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJtYXN0ZXJjaGVmVmVyc2lvbiI6InYxIiwidXNlU3Rha2VkQmFsYW5jZXMiOiJ0cnVlIn0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InN1c2hpc3dhcCIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsIm1hc3RlcmNoZWZWZXJzaW9uIjoidjIiLCJ1c2VTdGFrZWRCYWxhbmNlcyI6InRydWUifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJ1bmlzd2FwIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJhZGRyZXNzIjoiMHgyZDk0YWEzZTQ3ZDlkNTAyNDUwM2NhODQ5MWZjZTlhMmZiNGRhMTk4In0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InVuaXN3YXAtdjMiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsInBvb2xBZGRyZXNzIjoiMHgxYTgwYWZlMTQxNDM2MzdjMGI3NjA5ZTZlMjc2NDY0ZTRmNzQ4MDE0IiwidG9rZW5SZXNlcnZlIjowfSwibmV0d29yayI6MX0seyJuYW1lIjoidW5pc3dhcC12MyIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwicG9vbEFkZHJlc3MiOiIweDI1QmQ3OGQyMTg5YTE5Q2UxNzQyYzI1MkQ1QzViMWNDNDg2NEZlYTkiLCJ0b2tlblJlc2VydmUiOjB9LCJuZXR3b3JrIjoxMH0seyJuYW1lIjoiYXJyYWtpcy1maW5hbmNlIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJkZWNpbWFscyI6MTgsInRva2VuQWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsInBvb2xBZGRyZXNzIjoiMHg0NzJEMEIwRERGRTBCQzAyQzI3OTI4YjhCY2JENjdFNjVEMDdkNDhhIn0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InJhcmktZnVzZSIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwidG9rZW4iOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJmVG9rZW4iOiIweDI1MDMxNkIzRTQ2NjAwNDE3NjU0YjEzYkVhNjhiNWY2NEQ2MUU2MDkifSwibmV0d29yayI6MX1dLCJzdGFydEJsb2NrcyI6eyIxMzciOjEzMDAwMDAwfX0sIm5ldHdvcmsiOiIxIiwic25hcHNob3QiOiIxNjY4MDAwMCIsImFkZHJlc3NlcyI6WyIweDFFQzFDY0VGM2UxNzM1YmRBM0Y0QkE2OThlOGE1MjRBQTdjOTMyNzQiLCIweGI2YWMwMzQxRmNmM0ZCNTA3QTgyMDhEMzRhOTdmMTM3NzllMTM5M0QiXX0.