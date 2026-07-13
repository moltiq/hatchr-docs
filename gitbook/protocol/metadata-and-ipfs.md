---
description: Public IPFS metadata, token images and third-party ingestion.
---

# Metadata and IPFS

Hatchr stores token metadata through a public IPFS URI written during initialization.

## Metadata fields

Metadata can include:

- token name;
- symbol;
- description;
- image URI;
- X link;
- Telegram link; and
- website link.

The Hatchr application pins the image and metadata JSON through Pinata before the launch transaction.

## On-chain reference

The token exposes `metadataURI`. It has no setter, so Hatchr cannot replace the URI after initialization.

## IPFS and gateways

IPFS is content-addressed. The CID identifies the content, while gateways provide HTTP access to it. Gateway availability is not the same as content identity.

Hatchr normalizes `ipfs://` links for display and can use gateway fallbacks. Integrators should retain the original CID and avoid treating one gateway hostname as canonical.

## Trading-terminal logos

External terminals maintain their own crawlers, moderation and caches. A token can trade before a third party ingests its image. Publishing correct IPFS metadata does not force immediate display on Dexscreener, GMGN or another service.

