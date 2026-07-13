---
description: Contract-enforced Hatchr invariants and current hardening status.
---

# Security Model

## Enforced by deployed contracts

- Fixed 1 billion token supply.
- No post-initialization mint path.
- One-time clone initialization through a trusted initializer.
- Zero creator token allocation.
- LP position NFT transferred to a locker without a withdrawal function.
- Tick-rounding token dust remains locked.
- Fee claims cannot redirect registered recipients.
- Factory launch execution is atomic and reentrancy-protected.
- Token contracts contain no tax, blacklist, pause or confiscation controls.

## Application protections

- Wallet network validation.
- Quote simulation before submission.
- Exact sell approvals rather than default unlimited approvals.
- Minimum-received calculation in the swap interface.
- Confirmed-block indexing.
- Stale-data and recovery behavior.
- Database-backed production data without mock fallbacks.

## Current status

The mainnet contracts have published source on Robinhood Chain Blockscout. Hatchr has **not yet published an independent smart-contract audit**.

{% hint style="warning" %}
Published source and scanner results are not substitutes for an independent audit. Users should verify transactions and use amounts appropriate for their own risk tolerance.
{% endhint %}

## Responsible disclosure

Do not publish an exploitable issue before the team has had a reasonable opportunity to investigate. Contact Hatchr through the official channels listed on the [Official Links](../official-links.md) page and request a private security contact.

