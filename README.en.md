# OAW — Web Agent Orchestrator

> [!IMPORTANT]
> Current status: conceptual project with a living roadmap. It is not a functional platform yet.

OAW will be an AGPLv3 web interface for orchestrating, supervising, and auditing agents, tasks, tools, and workflows.

## Initial architecture

| Layer | Technology | Responsibility |
|---|---|---|
| Control plane | Go | Web API, auth, sessions, Observer, and quotas |
| Execution | Rust | Policies, sandboxing, delegation, failover, and receipts |
| UI | To be defined | Browser, mobile, and future PWA |
| Data | PostgreSQL/SQLite + Engram/Kuzu | Operational state, memory, and relationships |

## Inspiration and attribution

OAW is inspired by `agent-orchestrator`, Orque, and [`hermes-webui`](https://github.com/nesquena/hermes-webui). Hermes WebUI is MIT-licensed. Full attribution is documented in [CREDITS.md](CREDITS.md).

## Documentation

- [Product vision](PRODUCT-VISION.md)
- [Roadmap](ROADMAP.md)
- [Architecture](ARCHITECTURE.md)
- [Security](SECURITY.md)
- [Releases](RELEASES.md)
- [Contributing](CONTRIBUTING.md)
- [Credits](CREDITS.md)

## License

Original OAW code is released under AGPLv3. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
