---
description: How Hatchr launch price and displayed market capitalization are derived.
---

# Pricing and Market Cap

The factory's launch tick defines the initial Uniswap V3 price boundary.

## Current launch price

At launch tick `202200`, the approximate WETH-denominated token price is:

```text
token price in WETH = 1.0001 ^ (-202200)
                    ≈ 0.0000000016558 WETH
```

With a fixed 1 billion supply:

```text
implied fully diluted value in ETH
  = token price × 1,000,000,000
  ≈ 1.6558 ETH
```

## USD display

Hatchr converts the live WETH-denominated price using a backend-cached ETH/USD reference. The service refreshes the reference every 60 seconds using CoinGecko with a Coinbase fallback.

```text
priceUsd = priceWeth × ethUsd
marketCapUsd = priceUsd × 1,000,000,000
```

At `$1,800/ETH`, the initial implied value is about `$2,980`. It is not permanently fixed at `$3,000` because ETH/USD changes.

## Precision

Hatchr preserves full numeric precision internally and formats very small prices using leading-zero notation rather than scientific notation.

## Important distinction

Market capitalization is a price-derived valuation. It is not the pool's WETH balance, guaranteed liquidity, redemption value or amount paid by creators.

