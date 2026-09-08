# Arquitectura inicial

```text
Browser / PWA
     |
     | HTTPS + SSE/WebSocket
     v
Control Plane Go
     |
     +-- sesiones, auth, API, Observer, cuotas
     |
     +-- Orquestador Rust
             |
             +-- políticas, sandbox, delegación, receipts
             +-- agentes y procesos delegados

PostgreSQL  <── estado operativo
Engram/Kuzu <── memoria y relaciones
```

## Límites iniciales

- **Go:** API web, autenticación, sesiones, Observer, persistencia y gateway de eventos.
- **Rust:** ejecución segura, políticas, sandbox, delegación, identidad de tarea, failover y receipts.
- **Frontend:** interfaz web desacoplada de procesos y filesystem.

La primera versión debe usar SSE para streaming. WebSocket queda como evolución para control bidireccional cuando el contrato de eventos esté estable.
