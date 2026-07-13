---
description: How Hatchr creates direct, single-sided Uniswap V3 liquidity.
---

# Uniswap V3 Liquidity

Hatchr creates a standard token/WETH Uniswap V3 pool for every launch.

## Single-sided position

The factory contributes the fixed launch supply and zero WETH at the configured launch boundary. The position is concentrated over the protocol's selected tick range.

As buyers swap WETH into the pool:

- token inventory is released to buyers;
- WETH accumulates in the pool position;
- the pool price moves along the Uniswap V3 range; and
- swap fees accrue to the position.

{% hint style="info" %}
The starting market cap is an implied valuation from pool price and fixed supply. It does not represent ETH deposited into the pool at launch.
{% endhint %}

## Pool parameters

| Parameter | Current value |
| --- | --- |
| Pair | token/WETH |
| Fee tier | 1% |
| Launch tick | `202200` |
| Token amount | Fixed launch supply, less tick-rounding dust |
| Initial WETH amount | Zero, unless subsequently acquired through swaps |

## Standard integrations

Because the market is standard Uniswap V3, compatible routers, aggregators and trading tools can interact with it once they discover the pool. Hatchr does not require a custom trading adapter.

