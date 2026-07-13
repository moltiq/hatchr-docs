---
description: Buy and sell Hatchr tokens through their Uniswap V3 pools.
---

# Trade a Token

All Hatchr markets execute through Uniswap V3 from the first block. Hatchr does not custody swap funds.

## Before graduation

The Hatchr token page provides an integrated swap interface for the token's existing Uniswap V3 pool.

Current interface defaults:

- token/WETH route;
- 1% Uniswap V3 pool fee;
- 3% slippage tolerance;
- exact token approval for sells;
- native ETH wrapping for buys; and
- WETH unwrapping for supported native ETH settlement.

## Buy

1. Connect a wallet on Robinhood Chain.
2. Select **Buy**.
3. Enter the ETH amount.
4. Review the quote, minimum received, price impact and estimated gas.
5. Confirm the swap in the wallet.

## Sell

1. Select **Sell**.
2. Enter a whole-token amount or use a percentage shortcut.
3. Approve the exact token amount if required.
4. Review the refreshed quote.
5. Confirm the swap transaction.

{% hint style="warning" %}
Quotes are temporary. New concentrated-liquidity markets can move sharply, especially when trade history and WETH liquidity are limited.
{% endhint %}

## After graduation

When Hatchr marks a token graduated, the same locked pool remains active. Hatchr retires its integrated swap form for that token and directs traders to the Uniswap interface.

No liquidity migration occurs.

