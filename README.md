# try2
```
┌──────────┐
│  Client  │
└─────┬────┘
      │ HTTP requests
      ▼
┌─────────────────────┐
│     FastAPI API      │
│  + Metrics middleware │
└──┬────┬────┬────┬───┘
   │    │    │    │
   │    │    │    └─────> GET /health (degraded status)
   │    │    └──────────> Structured logs (request_id, latency_ms, errors)
   │    └───────────────> Metrics store (in-memory or SQLite)
   └────────────────────> SQLite DB
```
