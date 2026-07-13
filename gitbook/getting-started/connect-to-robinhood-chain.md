---
description: Configure an EVM wallet for Robinhood Chain mainnet.
---

# Connect to Robinhood Chain

Hatchr runs on Robinhood Chain mainnet.

| Setting | Value |
| --- | --- |
| Network name | Robinhood Chain |
| Chain ID | `4663` |
| Currency symbol | ETH |
| Explorer | [robinhoodchain.blockscout.com](https://robinhoodchain.blockscout.com) |

Use Robinhood's official [connection instructions](https://docs.robinhood.com/chain/connecting/) for the current RPC configuration.

## Before using Hatchr

1. Add or select Robinhood Chain in your EVM wallet.
2. Confirm the wallet shows chain ID `4663`.
3. Fund the wallet with ETH on Robinhood Chain.
4. Keep enough ETH for gas in addition to the amount you plan to spend.
5. Open Hatchr and connect the same wallet.

{% hint style="danger" %}
Never enter a seed phrase or private key into Hatchr, Telegram, X, a support form, or a block explorer. Hatchr only requests normal wallet connections and transaction signatures.
{% endhint %}

## What ETH is used for

- network gas;
- the configured token launch fee;
- an optional initial token buy; and
- subsequent token purchases.

