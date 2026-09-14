# Universe Node

**Shared Reality Protocol** — a protocol for deterministic generation of persistent, shared simulated realities.

Universe Node is not a game, a game engine, or a file format. It is a specification: a small set of rules that let any independent implementation, in any language, generate the exact same universe from the same seed — and let multiple implementations share the same reality without ever needing a central authority or server.

Given the same seed, the same rules, and the same sequence of events, any two correct implementations of the protocol will always arrive at the same state:

```
SEED + RULES + EVENTS = STATE
```

## Read the protocol

- [`universe-node-whitepaper-en.pdf`](./universe-node-whitepaper-en.pdf) — the whitepaper. Explains the *why*: the design principles, the physical-substrate/narrative-layer separation, the seven primitives, determinism, and multiverse portability.
- [`protocol/SPEC.md`](./protocol/SPEC.md) — the technical specification. Explains the *how*: exact data shapes (JSON) for Entity/Property/Relation/Action/Event, the mandatory Action → Validation → Event → State flow, and the conventions any implementation must follow to interoperate.

## Reference implementation

[`node/universe-node.html`](./node/universe-node.html) is a minimal, single-file Node that implements the protocol as described in `SPEC.md`: the seven primitives, the Action/Event/State flow, identity-as-event, deterministic seed-based generation, and `probability_of()` preview.

**Its purpose is to illustrate and prove the protocol is implementable and internally consistent — it is not a production Node.** It intentionally does not implement anything the protocol itself, or SPEC.md §11, marks as future work (Node-to-Node sync, cryptographic identity, multiverse, detailed physics). Real applications built on top of the protocol — games, tools, simulations — are separate clients, released independently.

## Status

This repository holds the protocol specification and its reference Node. Client applications built on top of the protocol (games, tools) will be linked here as they're released.

## License

- The whitepaper is released under **CC BY-NC-ND 4.0** — see [`LICENSE-WHITEPAPER.md`](./LICENSE-WHITEPAPER.md). You may share it unmodified, with credit, for non-commercial purposes.
- The specification and reference code are released under **CC BY-NC 4.0** — see [`LICENSE-CODE.md`](./LICENSE-CODE.md). You may use and adapt them non-commercially, with credit.

For commercial use or licensing inquiries, contact the author.

## Author

**Ozalune**
Email: ozalune@outlook.com
Social: [@ozalune](https://twitter.com/ozalune)

---

*This document and its provenance are timestamped independently via [OpenTimestamps](https://opentimestamps.org).*
