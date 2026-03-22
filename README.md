# RRBR — rrbr-data

> **Data Layer**: Real-time streaming and historical data lakehouse for Brazilian market data.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)

## Overview

Ingestion, processing, and persistence of Brazilian market data: B3 trades, ANBIMA curves, BCB rates (Selic, CDI), and market data feeds — in real-time and historical.

## Stack

- **Go 1.24+** — ingestion services, Kafka producers/consumers
- **Rust** — heavy data processing (Apache Arrow/Polars)
- **Apache Kafka** — real-time trade and market data streaming
- **Apache Flink** — stream processing and enrichment
- **Apache Iceberg** on MinIO (S3-compatible) — data lakehouse
- **PostgreSQL 17 + TimescaleDB + PGVector** — audit, time series, agent state, RAG
- **Neo4j** — trade/portfolio relationship graph

## Data Sources

| Source | Data | Frequency |
|--------|------|-----------|
| B3 | Trades, prices, futures curves | Real-time |
| ANBIMA | Yield curves, bond prices | Daily |
| BCB | Selic, CDI, PTAX | Daily |
| B3 | Holiday calendar | Annual |

## License

Apache 2.0
