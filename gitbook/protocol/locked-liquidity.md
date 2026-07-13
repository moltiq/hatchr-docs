---
description: Permanent custody of Hatchr Uniswap V3 position NFTs and token dust.
---

# Locked Liquidity

The factory transfers each Uniswap V3 position NFT to the Hatchr `LPLocker` during the launch transaction.

## Position lock

The deployed locker has no function that withdraws or transfers a registered position NFT. Neither the token creator nor the Hatchr factory receives custody of the LP NFT after registration.

The pool remains active and the position continues earning fees. Locking prevents removal of this Hatchr-created position; it does not prevent independent users from creating other positions in the same pool.

## Rounding dust

Uniswap tick mathematics may prevent a tiny portion of the fixed supply from entering the position. The factory transfers this dust to the locker and records it in `lockedDust`.

The dust:

- is not sent to the creator;
- is not shown as a burn transaction;
- remains held by the locker; and
- does not have a withdrawal path in the deployed locker.

{% hint style="warning" %}
“Locked liquidity” describes the Hatchr position NFT. It is not a guarantee of token value, stable pricing, minimum WETH depth or trading profitability.
{% endhint %}

