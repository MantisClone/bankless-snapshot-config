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
    },
    {
      "name": "contract-call",
      "network": "1",
      "params": {
        "symbol": "BANK",
        "address": "0xeaEAb9f1B25fa00FC01a3fcE521b47E88527Aa02",
        "decimals": 18,
        "methodABI": {
          "name": "delegatedBalances",
          "type": "function",
          "inputs": [
            {
              "name": "delegate",
              "type": "address",
              "internalType": "address"
            }
          ],
          "outputs": [
            {
              "name": "delegatedBalance",
              "type": "uint256",
              "internalType": "uint256"
            }
          ],
          "stateMutability": "view"
          }
        }
      }
  ],
  "startBlocks": {
    "137": 13000000
  }
}
```

# Playground Link
https://snapshot.org/#/playground/multichain?query=eyJwYXJhbXMiOnsiZ3JhcGhzIjp7IjEzNyI6Imh0dHBzOi8vYXBpLnRoZWdyYXBoLmNvbS9zdWJncmFwaHMvbmFtZS9zYW1lZXBzaS9tYXRpY2Jsb2NrcyJ9LCJzeW1ib2wiOiJCQU5LIiwic3RyYXRlZ2llcyI6W3sibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImVyYzIwLWJhbGFuY2Utb2YiLCJwYXJhbXMiOnsiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsImRlY2ltYWxzIjoxOH0sIm5ldHdvcmsiOjEzN30seyJuYW1lIjoiZXJjMjAtYmFsYW5jZS1vZiIsInBhcmFtcyI6eyJhZGRyZXNzIjoiMHgyOUZBRjU5MDViZkY5Q2ZjYzdDRjU2YTVlZDkxRTBmMDkxRjg2NjRCIiwiZGVjaW1hbHMiOjE4fSwibmV0d29yayI6MTB9LHsibmFtZSI6ImJhbGFuY2VyIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJhZGRyZXNzIjoiMHgyZDk0QUEzZTQ3ZDlENTAyNDUwM0NhODQ5MWZjRTlBMmZCNERBMTk4IiwiZGVjaW1hbHMiOjE4fSwibmV0d29yayI6MX0seyJuYW1lIjoiYmFsYW5jZXIiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweERCN0NiNDcxZGQwYjQ5YjI5Q0FCNGExQzE0ZDA3MGYyNzIxNmEwQWIiLCJkZWNpbWFscyI6MTh9LCJuZXR3b3JrIjoxMzd9LHsibmFtZSI6InN0YWtlZC1iYWxhbmNlciIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwidG9rZW5BZGRyZXNzIjoiMHhkYjdjYjQ3MWRkMGI0OWIyOWNhYjRhMWMxNGQwNzBmMjcyMTZhMGFiIiwiYmFsYW5jZXJQb29sSWQiOiIweDVhNmFlMWZkNzBkMDRiYTRhMjc5ZmMyMTlkZmFiYzUzODI1Y2IwMWQwMDAyMDAwMDAwMDAwMDAwMDAwMDAyMGUiLCJzdGFraW5nQ29udHJhY3QiOiIweGM0OGMzYTE5YmM3OWI5ZDZhYzQzOTE3MjMwNDE1ODQxMTRhNDI3MmQifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJzdXNoaXN3YXAiLCJwYXJhbXMiOnsic3ltYm9sIjoiQkFOSyIsImFkZHJlc3MiOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJtYXN0ZXJjaGVmVmVyc2lvbiI6InYxIiwidXNlU3Rha2VkQmFsYW5jZXMiOiJ0cnVlIn0sIm5ldHdvcmsiOjF9LHsibmFtZSI6InN1c2hpc3dhcCIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4REI3Q2I0NzFkZDBiNDliMjlDQUI0YTFDMTRkMDcwZjI3MjE2YTBBYiIsIm1hc3RlcmNoZWZWZXJzaW9uIjoidjIiLCJ1c2VTdGFrZWRCYWxhbmNlcyI6InRydWUifSwibmV0d29yayI6MTM3fSx7Im5hbWUiOiJ1bmlzd2FwLXYzIiwicGFyYW1zIjp7InN5bWJvbCI6IkJBTksiLCJwb29sQWRkcmVzcyI6IjB4MWE4MGFmZTE0MTQzNjM3YzBiNzYwOWU2ZTI3NjQ2NGU0Zjc0ODAxNCIsInRva2VuUmVzZXJ2ZSI6MH0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImFycmFraXMtZmluYW5jZSIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiZGVjaW1hbHMiOjE4LCJwb29sQWRkcmVzcyI6IjB4NDcyRDBCMERERkUwQkMwMkMyNzkyOGI4QmNiRDY3RTY1RDA3ZDQ4YSIsInRva2VuQWRkcmVzcyI6IjB4MmQ5NEFBM2U0N2Q5RDUwMjQ1MDNDYTg0OTFmY0U5QTJmQjREQTE5OCJ9LCJuZXR3b3JrIjoxfSx7Im5hbWUiOiJyYXJpLWZ1c2UiLCJwYXJhbXMiOnsidG9rZW4iOiIweDJkOTRBQTNlNDdkOUQ1MDI0NTAzQ2E4NDkxZmNFOUEyZkI0REExOTgiLCJmVG9rZW4iOiIweDI1MDMxNkIzRTQ2NjAwNDE3NjU0YjEzYkVhNjhiNWY2NEQ2MUU2MDkiLCJzeW1ib2wiOiJCQU5LIn0sIm5ldHdvcmsiOjF9LHsibmFtZSI6ImNvbnRyYWN0LWNhbGwiLCJuZXR3b3JrIjoiMSIsInBhcmFtcyI6eyJzeW1ib2wiOiJCQU5LIiwiYWRkcmVzcyI6IjB4ZWFFQWI5ZjFCMjVmYTAwRkMwMWEzZmNFNTIxYjQ3RTg4NTI3QWEwMiIsImRlY2ltYWxzIjoxOCwibWV0aG9kQUJJIjp7Im5hbWUiOiJkZWxlZ2F0ZWRCYWxhbmNlcyIsInR5cGUiOiJmdW5jdGlvbiIsImlucHV0cyI6W3sibmFtZSI6ImRlbGVnYXRlIiwidHlwZSI6ImFkZHJlc3MiLCJpbnRlcm5hbFR5cGUiOiJhZGRyZXNzIn1dLCJvdXRwdXRzIjpbeyJuYW1lIjoiZGVsZWdhdGVkQmFsYW5jZSIsInR5cGUiOiJ1aW50MjU2IiwiaW50ZXJuYWxUeXBlIjoidWludDI1NiJ9XSwic3RhdGVNdXRhYmlsaXR5IjoidmlldyJ9fX1dLCJzdGFydEJsb2NrcyI6eyIxMzciOjEzMDAwMDAwfX0sIm5ldHdvcmsiOiIxIiwic25hcHNob3QiOiIxNzYzNTY3MyIsImFkZHJlc3NlcyI6WyIweGI2YWMwMzQxRmNmM0ZCNTA3QTgyMDhEMzRhOTdmMTM3NzllMTM5M0QiXX0.
