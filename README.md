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
https://snapshot.org/#/playground/multichain?query=eyJwYXJhbXMiOnsiZ3JhcGhzIjp7IjEzNyI6Imh0dHBzOi8vYXBpLnRoZWdyYXBoLmNvbS9zdWJncmFwaHMvbmFtZS9zYW1lZXBzaS9tYXRpY2Jsb2NrcyJ9LCJzeW1ib2wiOiJCQU5LIiwic3RyYXRlZ2llcyI6W3sibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoiYmFsYW5jZXIiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweERCN0NiNDcxZGQwYjQ5YjI5Q0FCNGExQzE0ZDA3MGYyNzIxNmEwQWIiLCJkZWNpbWFscyI6MTh9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InN0YWtlZC1iYWxhbmNlciIsInBhcmFtcyI6eyJ0b2tlbkFkZHJlc3MiOiIweGRiN2NiNDcxZGQwYjQ5YjI5Y2FiNGExYzE0ZDA3MGYyNzIxNmEwYWIiLCJiYWxhbmNlclBvb2xJZCI6IjB4NWE2YWUxZmQ3MGQwNGJhNGEyNzlmYzIxOWRmYWJjNTM4MjVjYjAxZDAwMDIwMDAwMDAwMDAwMDAwMDAwMDIwZSIsInN0YWtpbmdDb250cmFjdCI6IjB4YzQ4YzNhMTliYzc5YjlkNmFjNDM5MTcyMzA0MTU4NDExNGE0MjcyZCIsInN5bWJvbCI6IkJBTksifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJzdXNoaXN3YXAiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweERCN0NiNDcxZGQwYjQ5YjI5Q0FCNGExQzE0ZDA3MGYyNzIxNmEwQWIiLCJtYXN0ZXJjaGVmVmVyc2lvbiI6InYyIiwidXNlU3Rha2VkQmFsYW5jZXMiOiJ0cnVlIn0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoidW5pc3dhcCIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4MmQ5NGFhM2U0N2Q5ZDUwMjQ1MDNjYTg0OTFmY2U5YTJmYjRkYTE5OCJ9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJ1bmlzd2FwLXYzIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJwb29sQWRkcmVzcyI6IjB4MWE4MGFmZTE0MTQzNjM3YzBiNzYwOWU2ZTI3NjQ2NGU0Zjc0ODAxNCIsInRva2VuUmVzZXJ2ZSI6MH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImFycmFraXMtZmluYW5jZSIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiZGVjaW1hbHMiOjE4LCJ0b2tlbkFkZHJlc3MiOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJwb29sQWRkcmVzcyI6IjB4NDcyRDBCMERERkUwQkMwMkMyNzkyOGI4QmNiRDY3RTY1RDA3ZDQ4YSJ9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJyYXJpLWZ1c2UiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsInRva2VuIjoiMHgyZDk0QUEzZTQ3ZDlENTAyNDUwM0NhODQ5MWZjRTlBMmZCNERBMTk4IiwiZlRva2VuIjoiMHgyNTAzMTZCM0U0NjYwMDQxNzY1NGIxM2JFYTY4YjVmNjRENjFFNjA5In0sIm5ldHdvcmsiOjF9XSwic3RhcnRCbG9ja3MiOnsiMTM3IjoxMzAwMDAwMH19LCJuZXR3b3JrIjoiMSIsInNuYXBzaG90IjoiMTU1NTU1NzciLCJhZGRyZXNzZXMiOlsiMHgxRUMxQ2NFRjNlMTczNWJkQTNGNEJBNjk4ZThhNTI0QUE3YzkzMjc0Il19
