---
description: Hatchr's permanent 4.2 WETH market-maturity milestone.
---

# Graduation

A Hatchr token graduates when its indexed Uniswap V3 pool reaches **4.2 WETH** in WETH liquidity.

Graduation is a product and discovery milestone. It is not a liquidity migration.

## What changes

- Hatchr permanently marks the token as graduated.
- The progress indicator becomes a graduated state.
- Hatchr retires its integrated swap form for that token.
- The token page directs users to the Uniswap interface.

## What does not change

- The token contract does not change.
- Supply does not change.
- The LP NFT does not move or unlock.
- A replacement pool is not deployed.
- Existing Uniswap trading does not stop.
- Graduation does not guarantee a particular market cap.

## Progress

```text
progress = min(indexedPoolWeth / 4.2 WETH, 100%)
```

Once the threshold is observed after the indexer's confirmation policy, graduation is permanent in Hatchr's database.

{% hint style="warning" %}
WETH liquidity and market capitalization are different measurements. Concentrated-liquidity inventory and token price change as swaps execute.
{% endhint %}

