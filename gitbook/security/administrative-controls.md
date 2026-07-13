---
description: Owner-controlled Hatchr parameters and their limits.
---

# Administrative Controls

Hatchr is not presented as fully ownerless. The deployed system contains explicit administrative roles.

## Factory owner

The factory owner can update:

- launch fee;
- minimum required ETH;
- creator share of collected LP fees;
- launch tick; and
- platform fee wallet.

The factory rejects any nonzero creator token allocation.

## Initializer owner

The `TokenInitializer` owner controls which factories may initialize token clones.

## Locker owner

The `LPLocker` owner controls which factories may register positions and locked dust.

## What these roles cannot do

The current contracts do not provide an administrator with a function to:

- mint additional supply for an existing token;
- seize holder balances;
- blacklist transfers;
- add a token transfer tax;
- pause an existing token;
- upgrade an existing minimal clone; or
- withdraw a registered LP position NFT from the locker.

{% hint style="info" %}
Parameter changes are observable on-chain through transactions and emitted events. Integrators should monitor owner and configuration changes.
{% endhint %}

