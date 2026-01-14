# try2
graph TB
    Client[Client / Load Test Script] -->|HTTP| API[FastAPI API]
    API --> DB[(SQLite DB)]
    API --> Metrics[Metrics Store<br/>(in-memory or SQLite)]
    API --> Logs[Structured logs]
    API --> Health[/health]
    API --> Data[JWT-protected endpoints]

    style API fill:#4A90E2,stroke:#2E5C8A,stroke-width:2px,color:#fff
    style DB fill:#50C878,stroke:#2E7D4E,stroke-width:2px,color:#fff
