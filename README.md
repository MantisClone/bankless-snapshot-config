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
https://snapshot.org/#/playground/multichain?query=eyJwYXJhbXMiOnsiZ3JhcGhzIjp7IjEzNyI6Imh0dHBzOi8vYXBpLnRoZWdyYXBoLmNvbS9zdWJncmFwaHMvbmFtZS9zYW1lZXBzaS9tYXRpY2Jsb2NrcyJ9LCJzeW1ib2wiOiJCQU5LIiwic3RyYXRlZ2llcyI6W3sibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoiYmFsYW5jZXIiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJkZWNpbWFscyI6MTh9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJiYWxhbmNlciIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoic3Rha2VkLWJhbGFuY2VyIiwicGFyYW1zIjp7InRva2VuQWRkcmVzcyI6IjB4ZGI3Y2I0NzFkZDBiNDliMjljYWI0YTFjMTRkMDcwZjI3MjE2YTBhYiIsImJhbGFuY2VyUG9vbElkIjoiMHg1YTZhZTFmZDcwZDA0YmE0YTI3OWZjMjE5ZGZhYmM1MzgyNWNiMDFkMDAwMjAwMDAwMDAwMDAwMDAwMDAwMjBlIiwic3Rha2luZ0NvbnRyYWN0IjoiMHhjNDhjM2ExOWJjNzliOWQ2YWM0MzkxNzIzMDQxNTg0MTE0YTQyNzJkIiwic3ltYm9sIjoiQkFOSyJ9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InN1c2hpc3dhcCIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsIm1hc3RlcmNoZWZWZXJzaW9uIjoidjIiLCJ1c2VTdGFrZWRCYWxhbmNlcyI6InRydWUifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJ1bmlzd2FwIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJhZGRyZXNzIjoiMHgyZDk0YWEzZTQ3ZDlkNTAyNDUwM2NhODQ5MWZjZTlhMmZiNGRhMTk4In0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InVuaXN3YXAtdjMiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsInBvb2xBZGRyZXNzIjoiMHgxYTgwYWZlMTQxNDM2MzdjMGI3NjA5ZTZlMjc2NDY0ZTRmNzQ4MDE0IiwidG9rZW5SZXNlcnZlIjowfSwibmV0d29yayI6MX0seyJuYW1lIjoiYXJyYWtpcy1maW5hbmNlIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJkZWNpbWFscyI6MTgsInRva2VuQWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsInBvb2xBZGRyZXNzIjoiMHg0NzJEMEIwRERGRTBCQzAyQzI3OTI4YjhCY2JENjdFNjVEMDdkNDhhIn0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InJhcmktZnVzZSIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwidG9rZW4iOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJmVG9rZW4iOiIweDI1MDMxNkIzRTQ2NjAwNDE3NjU0YjEzYkVhNjhiNWY2NEQ2MUU2MDkifSwibmV0d29yayI6MX1dLCJzdGFydEJsb2NrcyI6eyIxMzciOjEzMDAwMDAwfX0sIm5ldHdvcmsiOjEsInNuYXBzaG90IjoiMTU0MTY1NzAiLCJhZGRyZXNzZXMiOlsiMHgxRUMxQ2NFRjNlMTczNWJkQTNGNEJBNjk4ZThhNTI0QUE3YzkzMjc0Il19
