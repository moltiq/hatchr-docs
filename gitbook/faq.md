---
description: Common questions about Hatchr launches, liquidity, fees and graduation.
---

# Frequently Asked Questions

## Does Hatchr use a bonding curve?

No. Every Hatchr market is a standard token/WETH Uniswap V3 pool from launch.

## Does a creator provide starting liquidity?

The factory supplies the fixed token inventory as single-sided concentrated liquidity. The creator does not have to deposit WETH. An optional initial buy is a swap, not creator-owned LP.

## Why can a token display roughly $3,000 market cap with little or no WETH?

The figure is an implied valuation calculated from the initialized pool price and fixed supply. It is not the pool's WETH backing. The USD figure changes with ETH/USD.

## How many tokens are created?

Exactly 1 billion tokens with 18 decimals.

## Does the creator receive tokens for free?

No. The creator allocation is zero. Creators can buy during launch or trade later.

## Can more tokens be minted?

The token implementation has no mint function after its one-time initialization.

## Is liquidity burned?

The Uniswap V3 position is represented by an NFT. Hatchr transfers it to a locker contract without a withdrawal function. Small tick-rounding dust is also held by the locker rather than burned.

## What is the 1% fee?

It is the Uniswap V3 pool fee tier. It is not a token transfer tax.

## How much do creators earn?

The current factory configuration assigns creators 40% of fees collected from the locked LP position. The registered split should be checked on-chain.

## What happens at graduation?

At 4.2 WETH in indexed pool liquidity, Hatchr permanently marks the token graduated and directs trading to Uniswap. The pool and locked LP position do not migrate.

## Does `e99` prove a token is from Hatchr?

No. Verify the official factory's `TokenCreated` event.

## Why has a token image not appeared on another terminal?

External services use independent indexing and caching. Correct IPFS metadata does not guarantee immediate third-party ingestion.

## Is Hatchr audited?

Hatchr has not yet published an independent smart-contract audit. The contract source is publicly available on the Robinhood Chain explorer.

## When will HATCH launch?

Hatchr plans to launch HATCH once the application is live. No contract address or final tokenomics are published in these docs yet.

