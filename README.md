# OrbitRelay Specification

This repository is the language-neutral source of truth for OrbitRelay wire
contracts and compatibility fixtures.

## Implemented Contracts

- Realtime Protocol 0.1: Hello, authentication, subscription, Action, Ack,
  Event, Ping/Pong, Close, and Canvas stroke messages
- Query Protocol 0.2: correlated Query/QueryResponse messages
- Queries: `document.list`, `document.get`, `asset.access.resolve`, and
  `canvas.history.page`
- Asset HTTP: bearer-authenticated GET, HEAD, OPTIONS, and one byte range

Action is a request. Event is an accepted fact and is the shared unit for
persistence, propagation, and replay. Event replay order is append order, not
timestamp order. Cursor and checkpoint values are opaque to clients.

## Fixtures

- `fixtures/v0.1`: realtime transport and Canvas messages
- `fixtures/v0.2`: Query and QueryResponse messages

Rust and Flutter implementations validate their codecs against these fixtures.
This repository contains no Rust, Dart, server, client, deployment, or product
implementation.

## License

Licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE).
