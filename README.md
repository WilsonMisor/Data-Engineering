# Data Engineering Portfolio (Monorepo)

This repository contains my end-to-end Data Engineering portfolio.
It is structured as a single monorepo with three production-style projects
that share utilities, data generators, and documentation.

## What’s inside

### 1) Platform-in-a-Repo
**Folder:** `platform/`

A reproducible local data platform that prioritizes developer experience,
repeatability, and safe re-runs.

**Core tools**
- Docker
- Postgres
- Airflow
- Kafka
- Spark
- dbt

**Optional add-ons**
- Kubernetes
- Terraform

**What this demonstrates**
- You can set up and run a reliable data environment.
- You can package a stack that other engineers can reuse.

---

### 2) Batch Medallion Pipeline
**Folder:** `batch-medallion/`

A Bronze → Silver → Gold pipeline using Spark, Airflow, and dbt.

**Core tools**
- PySpark
- Airflow
- dbt
- Postgres (local warehouse)

**What this demonstrates**
- Incremental batch processing
- Data modeling with tests and documentation
- Reliable, re-runnable orchestration

---

### 3) Real-time Risk Pipeline
**Folder:** `realtime-risk/`

A low-latency pipeline that ingests events with Kafka, processes with Flink,
and produces analytics-ready models with dbt.

**Core tools**
- Kafka
- Flink
- Airflow
- dbt
- Spark (daily reconciliation)
- Postgres (local landing)

**What this demonstrates**
- Event-driven architecture
- Stateful stream processing
- Daily truth reconciliation logic

---

## Shared components
**Folder:** `shared/`

Includes:
- Data generators
- Sample datasets
- Common scripts
- Reusable SQL
- Cross-project diagrams

---

## Quickstart (local)

### Prerequisites
- Git
- Python 3.x
- VS Code
- Docker Desktop

### 1) Clone
```bash
git clone <YOUR_REPO_URL>
cd "Data Engineering"
```

### 2) Start the platform
```bash
cd platform/docker/compose
docker compose up -d
```

### 3) Validate core services
```bash
docker ps
```

---

## Documentation
Each project folder has:
- Its own README
- Architecture diagram
- Setup steps
- Demo commands
- Tests and validation notes

---

## Roadmap
- Add Kubernetes manifests for the full stack
- Add Terraform modules for a minimal cloud demo
- Add GitHub Actions CI
- Add a short demo video for each project
