---
description: Prove that a token was launched by the official Hatchr factory.
---

# Verify a Hatchr Token

An address ending in `e99` is not enough. Verify origin from the official factory.

## Verification checklist

1. Confirm the network is Robinhood Chain, chain ID `4663`.
2. Open the [official factory](https://robinhoodchain.blockscout.com/address/0x99bf0f2f7de390225738bb21847086a9cd6826a2).
3. Find the `TokenCreated` event containing the token address.
4. Record the emitted creator, pool and position token ID.
5. Confirm the pool contains the token and official WETH.
6. Confirm the position is registered in the official LP locker.
7. Confirm the token clone delegates to the published implementation.
8. Compare metadata with the URI stored by the token.

## Canonical factory

```text
0x99bf0f2f7de390225738bb21847086a9cd6826a2
```

## Why suffix matching fails

CREATE2 address mining is permissionless. Another deployer can create an unrelated address with the same final characters. The `TokenCreated` event binds a token to the official Hatchr factory.

{% hint style="danger" %}
Names, tickers, logos and social accounts can be copied. Contract provenance is the primary identity check.
{% endhint %}

