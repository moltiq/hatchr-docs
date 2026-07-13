---
description: Deterministic Hatchr token deployment with CREATE2 and an e99 suffix.
---

# e99 Addresses

Official Hatchr token addresses are prepared to end in `e99`.

## How it works

Hatchr uses OpenZeppelin `Clones.cloneDeterministic`, which deploys an ERC-1167-style minimal proxy through CREATE2.

The backend searches salts until the predicted token address has the required suffix. A three-hex-character target takes about `16³ = 4,096` attempts on average.

The effective salt is:

```text
keccak256(creator wallet, fee wallet, mined salt)
```

The predicted address can be shown before the launch transaction is signed.

## What affects the address

- official factory address;
- token implementation address;
- creator wallet;
- fee wallet; and
- mined salt.

Token name, symbol and metadata are supplied during initialization and do not alter the minimal clone bytecode.

## Branding is not verification

{% hint style="danger" %}
Anyone can mine an unrelated address ending in `e99`. Never treat the suffix as proof that a token is official.
{% endhint %}

Verify the factory's `TokenCreated` event and the clone implementation. See [Verify a Hatchr Token](../developers/verify-a-token.md).

