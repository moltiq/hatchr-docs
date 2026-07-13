---
description: Token-scoped Hatchr WebSocket updates with SSE and REST recovery.
---

# Realtime Updates

Hatchr uses a dedicated WebSocket service for confirmed token updates. REST supplies initial state and periodic reconciliation; SSE is the automatic fallback.

## Connect

Production clients connect to the configured secure endpoint:

```text
wss://<realtime-domain>/realtime
```

The server validates the request origin and limits messages to 16 KB.

## Subscribe

```json
{
  "type": "subscribe",
  "token": "0x..."
}
```

The service responds with `subscribed` and a `token.update` snapshot when available.

## Update message

```json
{
  "type": "token.update",
  "sequence": 12,
  "token": { "address": "0x...", "symbol": "TOKEN" },
  "latestTrade": null,
  "holders": [],
  "reason": "chain",
  "sourceBlock": "7800000",
  "timestamp": "2026-07-13T20:00:00.000Z"
}
```

The full token object contains current indexed identity, market, pool, fee and graduation fields.

## Unsubscribe

```json
{
  "type": "unsubscribe",
  "token": "0x..."
}
```

## Delivery behavior

- Updates are broadcast only to clients subscribed to the affected token.
- A monotonically increasing token sequence helps clients reject stale messages.
- Ping/pong heartbeats detect dead connections.
- Browser clients reconnect with exponential backoff.
- SSE activates when WebSocket is unavailable.
- Periodic REST reconciliation repairs missed state.

{% hint style="info" %}
Realtime delivery begins only after the indexer commits confirmed state to PostgreSQL. It is not a mempool feed.
{% endhint %}

