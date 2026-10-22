# Migration to managed infrastructure plan

A secure, reproducible operating model for the Diamond UI, RPC nodes, Blockscout explorer and data service.

## Scope

- Staking UI hosted on Vercel;
- Public JSON-RPC endpoint and two production RPC nodes;
- Blockscout frontend, backend, and PostgreSQL data;
- Data-ingestion service and PostgreSQL data;
- Nginx and other managed edge services;
- CI/CD, monitoring, backup, and recovery processes.

## Toolset

|  Purpose                | Tools                     |
| ----------------------- | ------------------------- |
| Provisioning            | OpenTofu/Terraform        |
| Host configuration      | Ansible                   |
| Load balancer           | Nginx                     |
| BC nodes runtime        | systemd service           |
| Services runtime        | Docker Compose            |
| Artifacts               | GitHub Releases + GHCR    |
| CI/CD                   | GitHub Actions            |
| Private resource access | SSH over WireGuard        |
| Observability           | Prometheus, Grafana, Loki |
| Backups                 | pgBackRest/WAL            |

## Diagrams

Target infrastructure and deployment flow diagrams.

- [Infrastructure diagram](./infrastructure-diagram.drawio)
- [Deployment flow](./deployment-flow.drawio)
