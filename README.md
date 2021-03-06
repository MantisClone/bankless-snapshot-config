# BanklessDAO Snapshot Configuration

The Snapshot strategy configuration used by BanklessDAO

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
https://snapshot.org/#/playground/multichain?query=eyJwYXJhbXMiOnsiZ3JhcGhzIjp7IjEzNyI6Imh0dHBzOi8vYXBpLnRoZWdyYXBoLmNvbS9zdWJncmFwaHMvbmFtZS9zYW1lZXBzaS9tYXRpY2Jsb2NrcyJ9LCJzeW1ib2wiOiJCQU5LIiwic3RyYXRlZ2llcyI6W3sibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoiYmFsYW5jZXIiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJkZWNpbWFscyI6MTh9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJiYWxhbmNlciIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoic3Rha2VkLWJhbGFuY2VyIiwicGFyYW1zIjp7InRva2VuQWRkcmVzcyI6IjB4ZGI3Y2I0NzFkZDBiNDliMjljYWI0YTFjMTRkMDcwZjI3MjE2YTBhYiIsImJhbGFuY2VyUG9vbElkIjoiMHg1YTZhZTFmZDcwZDA0YmE0YTI3OWZjMjE5ZGZhYmM1MzgyNWNiMDFkMDAwMjAwMDAwMDAwMDAwMDAwMDAwMjBlIiwic3Rha2luZ0NvbnRyYWN0IjoiMHhjNDhjM2ExOWJjNzliOWQ2YWM0MzkxNzIzMDQxNTg0MTE0YTQyNzJkIiwic3ltYm9sIjoiQkFOSyJ9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InN1c2hpc3dhcCIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsIm1hc3RlcmNoZWZWZXJzaW9uIjoidjEiLCJ1c2VTdGFrZWRCYWxhbmNlcyI6InRydWUifSwibmV0d29yayI6MX0seyJuYW1lIjoic3VzaGlzd2FwIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJhZGRyZXNzIjoiMHhEQjdDYjQ3MWRkMGI0OWIyOUNBQjRhMUMxNGQwNzBmMjcyMTZhMEFiIiwibWFzdGVyY2hlZlZlcnNpb24iOiJ2MiIsInVzZVN0YWtlZEJhbGFuY2VzIjoidHJ1ZSJ9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InVuaXN3YXAiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweDJkOTRhYTNlNDdkOWQ1MDI0NTAzY2E4NDkxZmNlOWEyZmI0ZGExOTgifSwibmV0d29yayI6MX0seyJuYW1lIjoidW5pc3dhcC12MyIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwicG9vbEFkZHJlc3MiOiIweDFhODBhZmUxNDE0MzYzN2MwYjc2MDllNmUyNzY0NjRlNGY3NDgwMTQiLCJ0b2tlblJlc2VydmUiOjB9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJhcnJha2lzLWZpbmFuY2UiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImRlY2ltYWxzIjoxOCwidG9rZW5BZGRyZXNzIjoiMHgyZDk0QUEzZTQ3ZDlENTAyNDUwM0NhODQ5MWZjRTlBMmZCNERBMTk4IiwicG9vbEFkZHJlc3MiOiIweDQ3MkQwQjBEREZFMEJDMDJDMjc5MjhiOEJjYkQ2N0U2NUQwN2Q0OGEifSwibmV0d29yayI6MX0seyJuYW1lIjoicmFyaS1mdXNlIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJ0b2tlbiI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImZUb2tlbiI6IjB4MjUwMzE2QjNFNDY2MDA0MTc2NTRiMTNiRWE2OGI1ZjY0RDYxRTYwOSJ9LCJuZXR3b3JrIjoxfV0sInN0YXJ0QmxvY2tzIjp7IjEzNyI6MTMwMDAwMDB9fSwibmV0d29yayI6MSwic25hcHNob3QiOjE1MTgwNTI5LCJhZGRyZXNzZXMiOltdfQ..
