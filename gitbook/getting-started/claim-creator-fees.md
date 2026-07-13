---
description: Review and collect a Hatchr creator's share of Uniswap V3 LP fees.
---

# Claim Creator Fees

Creators currently receive **40% of fees collected from their token's locked Uniswap V3 position**.

## Claim in Hatchr

1. Connect the wallet registered as the token's creator fee wallet.
2. Open the token page.
3. Select **Claim Fees**.
4. Review the claimable WETH and token amounts.
5. Submit the claim transaction.
6. Review the confirmation and explorer transaction.

The claim button is shown only when the connected wallet matches the registered creator wallet.

## Permissionless collection

The locker function itself is permissionless to call. This does not let a caller steal or redirect fees. Collected proceeds are transferred only to the creator and platform wallets registered for that position.

{% hint style="info" %}
Fees can accrue in WETH and in the launched token, depending on pool activity and token ordering. Claimable values are not guaranteed to be WETH-only.
{% endhint %}

See [Creator Fees](../protocol/creator-fees.md) for the contract-level mechanics.

