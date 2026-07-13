---
description: Create a fixed-supply Hatchr token and its locked Uniswap V3 market.
---

# Launch a Token

One Hatchr transaction deploys the token, creates its pool, locks the LP position and optionally buys tokens for the creator.

## Required information

- square token image;
- token name;
- token symbol; and
- connected creator wallet.

Description, X, Telegram and website links are optional. Hatchr uploads the image and metadata to public IPFS before submitting the launch transaction.

## Launch steps

1. Select **Create** in the Hatchr header.
2. Upload the token image.
3. Enter the token name and symbol.
4. Add a description and official links if available.
5. Review the creator fee wallet.
6. Optionally enter an initial-buy amount in ETH.
7. Review the predicted contract address ending in `e99`.
8. Select **Launch Token** and review the wallet transaction.
9. Wait for confirmation and open the new token page.

{% hint style="info" %}
The current launch fee is `0.0005 ETH`. An optional initial buy is added to this value. Network gas is charged separately by Robinhood Chain.
{% endhint %}

## What the transaction does

The factory atomically:

1. deploys a deterministic token clone;
2. initializes the fixed 1 billion supply;
3. creates and initializes a token/WETH Uniswap V3 pool;
4. deposits the launch supply into concentrated liquidity;
5. transfers the LP position NFT to the Hatchr locker;
6. registers creator and platform fee recipients;
7. locks tick-rounding dust; and
8. executes the optional initial buy.

If any step fails, the entire launch reverts.

## Creator allocation

Creators receive **no free token allocation**. A creator obtains tokens only through the optional initial buy or later market purchases.

## After confirmation

Save the transaction hash and token address. Share the token page rather than relying only on the name or ticker, because different tokens can use similar metadata.

