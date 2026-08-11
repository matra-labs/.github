# MATRA Labs

**The connected business platform**

MATRA Labs develops a connected suite of business applications for service companies, commerce and digital operations.

## Platform

- **MATRA OS** — Business operations, customers, services, delivery notes, invoicing and e-invoicing
- **MATRA Server** — Provisioning, deployment, monitoring, backups and lifecycle management
- **MATRA Shop** — Standalone commerce platform connected through MATRA Connect
- **MATRA Portal** — Secure customer and service portal
- **MATRA Connect** — APIs, events and integrations between MATRA applications and external services

## Architecture

MATRA applications are built as independent, containerized services with separate APIs, databases and permission systems.

```text
Browser
   │
 HTTPS
   │
MATRA Applications
   │
   ├── MATRA OS ─────── API ─── PostgreSQL
   ├── MATRA Server ─── API ─── PostgreSQL
   ├── MATRA Shop ───── API ─── PostgreSQL
   └── MATRA Portal ─── API ─── PostgreSQL
              │
        MATRA Connect
```

No application accesses another application's database directly. Communication is handled through versioned APIs, events and MATRA Connect.
