**Español** · [English](README.en.md)

# OAW — Orquestador de Agentes Web

> [!IMPORTANT]
> Estado actual: proyecto conceptual y roadmap vivo. No es todavía una plataforma funcional.

OAW será una interfaz web AGPLv3 para orquestar, supervisar y auditar agentes, tareas, herramientas y workflows.

## Arquitectura inicial

| Capa | Tecnología | Responsabilidad |
|---|---|---|
| Control plane | Go | API web, auth, sesiones, Observer y cuotas |
| Ejecución | Rust | políticas, sandbox, delegación, failover y receipts |
| UI | Por definir | navegador, móvil y futura PWA |
| Datos | PostgreSQL/SQLite + Engram/Kuzu | estado operativo, memoria y relaciones |

## Seguridad

- El navegador nunca ejecutará agentes directamente.
- Cada tarea tendrá `task_id`, eventos y receipt.
- No se commitean secretos, tokens ni `.env` reales.
- Las aprobaciones y políticas serán fail-closed.

## Inspiraciones y créditos

OAW toma ideas de `agent-orchestrator`, Orque y [`hermes-webui`](https://github.com/nesquena/hermes-webui). Hermes WebUI se distribuye bajo MIT. Las atribuciones completas están en [CREDITS.md](CREDITS.md).

## Documentación

- [Visión](PRODUCT-VISION.md)
- [Roadmap](ROADMAP.md)
- [Arquitectura](ARCHITECTURE.md)
- [Seguridad](SECURITY.md)
- [Releases](RELEASES.md)
- [Contribución](CONTRIBUTING.md)
- [Créditos](CREDITS.md)

## Licencia

El código original de OAW se publica bajo AGPLv3. Ver [LICENSE](LICENSE) y [NOTICE](NOTICE).
