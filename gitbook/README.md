---
description: The official technical and user documentation for Hatchr on Robinhood Chain.
cover: .gitbook/assets/User attachment (1).png
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Welcome to Hatchr

Hatchr is a token launch and discovery platform for **Robinhood Chain**. A Hatchr launch deploys a fixed-supply ERC-20, creates its token/WETH Uniswap V3 market, deposits the launch supply into concentrated liquidity, and permanently locks the resulting position NFT.

All of this happens in one atomic transaction.

{% hint style="info" %}
Hatchr does **not** use a separate bonding curve. Tokens trade through a standard Uniswap V3 pool from the launch block.
{% endhint %}

## Start here

| I want to...            | Read this                                                |
| ----------------------- | -------------------------------------------------------- |
| Create a token          | [Launch a Token](getting-started/launch-a-token.md)      |
| Buy or sell             | [Trade a Token](getting-started/trade-a-token.md)        |
| Understand the protocol | [Launch Architecture](protocol/launch-architecture.md)   |
| Verify a token          | [Verify a Hatchr Token](developers/verify-a-token.md)    |
| Integrate Hatchr data   | [Events and Indexing](developers/events-and-indexing.md) |
| Review protocol risks   | [Security Model](/broken/pages/axBdth8NLF8KbuRsZ4WL)     |

## Core design

* **Direct market:** token/WETH Uniswap V3 pool from launch.
* **Fixed supply:** 1 billion tokens, minted once during initialization.
* **Zero creator allocation:** creators receive no free token inventory.
* **Locked position:** the LP NFT is transferred to a locker without a withdrawal function.
* **Creator fees:** creators currently receive 40% of fees collected from the locked position.
* **Recognizable addresses:** official token addresses are deterministically mined to end in `e99`.
* **Graduation:** a permanent Hatchr milestone at 4.2 WETH in indexed pool liquidity; no migration occurs.



{% hint style="warning" %}
An `e99` suffix alone does not prove that a token came from Hatchr. Verify the official factory event before interacting.
{% endhint %}
