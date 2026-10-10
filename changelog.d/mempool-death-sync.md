Fixed

- **Block accept no longer fdatasyncs the mempool once per removed tx.**
  A strip `pwrite`s each durable DEAD slot, then syncs `slots` once and
  `meta` once for the confirmed txs and the conflict spends together.
  Open still reloads from slot status, and the strip still does not
  rewrite `tx.body` or the full slot table.
