# Erigon Local Test Node

A Docker Compose setup for running a lightweight Ethereum Sepolia testnet node with monitoring and logging stack.

## Features

- **Erigon Node**: Sepolia testnet with minimal pruning (~100-150 GB storage)
- **Monitoring**: Prometheus + Grafana for metrics visualization
- **Logging**: Loki + Promtail for centralized log aggregation
- **Pre-configured Dashboards**: Ready-to-use Grafana dashboards for node monitoring

## Quick Start

```bash
# Start all services
docker compose up -d

# Check sync progress
docker logs erigon-test --follow

# Stop all services
docker compose down
```

## Access Points

- **Erigon RPC**: http://localhost:8545
- **Grafana Dashboard**: http://localhost:3000 (admin/admin)
- **Prometheus**: http://localhost:9091
- **Metrics**: http://localhost:6060/metrics

## Configuration

Copy `.env.example` to `.env` to customize settings:

```bash
cp .env.example .env
```

## Monitoring

Access Grafana at http://localhost:3000 to view:
- Node sync status and block height
- Connected peers and network stats
- Memory and CPU usage
- Real-time logs from Erigon

## Network

Chain: Sepolia Testnet  
Pruning: Minimal mode  
Sync Time: ~30 minutes to 2 hours (depending on connection)

