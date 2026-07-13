---
description: Current Hatchr mainnet parameters and protocol invariants.
---

# Protocol at a Glance

| Parameter | Current mainnet behavior |
| --- | --- |
| Network | Robinhood Chain, chain ID `4663` |
| Native gas token | ETH |
| Token standard | ERC-20 with 18 decimals |
| Supply | `1,000,000,000` tokens per launch |
| Trading pair | token/WETH |
| Venue | Uniswap V3 |
| Pool fee | 1% (`10000`) |
| Launch fee | `0.0005 ETH` |
| Creator allocation | 0% |
| Launch supply in LP | 100%, less unavoidable tick-rounding dust |
| Creator LP-fee share | 40% of collected position fees |
| Platform LP-fee share | 60% of collected position fees |
| Launch tick | `202200` |
| Graduation target | `4.2 WETH` indexed pool liquidity |
| Token address pattern | Ends in `e99` |
| Metadata | Public IPFS URI stored by the token |

{% hint style="info" %}
The launch fee, creator fee percentage, launch tick, minimum ETH requirement and platform fee wallet are owner-configurable. Integrations should read live values from the factory.
{% endhint %}

## Mainnet factory

```text
0x99bf0f2f7de390225738bb21847086a9cd6826a2
```

See [Mainnet Contracts](developers/mainnet-contracts.md) for the complete deployment registry.

