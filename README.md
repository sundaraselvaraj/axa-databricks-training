# AXA Databricks Training — Participant Labs

## Quick Start

1. Import this repo into your Databricks workspace: **Workspace → Import → URL**
2. Run labs in order: Day 1 → Day 2
3. Each lab generates its own data — no external storage needed

## Structure

```
jour1/                          # Day 1: Fundamentals
├── 01_Getting_Started          # Workspace tour, notebook basics
├── hive_02_PySpark             # Filters, joins, aggregations, window functions
└── hive_03_Delta_Lake          # ACID, MERGE, time travel, schema evolution, constraints

jour2/                          # Day 2: Medallion Pipeline
├── hive_04_Bronze_Layer        # Batch ingestion, audit columns, incremental append
├── hive_04a_Bronze_AutoLoader  # (Optional) Auto Loader with cloudFiles — requires all-purpose cluster
├── hive_05_Silver_Layer        # Data profiling, cleaning, enrichment, business metrics
├── hive_06_Gold_Layer          # Aggregations, OPTIMIZE, ZORDER, VACUUM, orchestration
├── hive_07_DLT_Pipeline        # Delta Live Tables — declarative ETL with expectations
└── hive_08_Streaming_Lab       # Structured Streaming, watermarking, triggers

solutions/                      # Solution notebooks (all blanks filled in)
```

## How It Works

- **No Unity Catalog needed** — all labs use Hive Metastore
- **Per-user isolation** — each participant gets a unique database (`training_lab_<your_name>`) derived from `current_user()`
- **Idempotent** — safe to re-run any lab multiple times
- **Sequential Day 2** — Labs 04 → 05 → 06 must run in order (each reads the previous layer's output)
- **Lab 07 (DLT)** — run via Jobs & Pipelines → Create → ETL pipeline (not "Run All")
- **Lab 08 (Streaming)** — run cells top to bottom like a normal notebook

## Lab Dependencies

```
Day 1 (independent):
  01 → standalone
  02 → standalone (generates own data)
  03 → standalone (generates own data)

Day 2 (sequential):
  04 (Bronze) → 05 (Silver) → 06 (Gold)
  07 (DLT) → standalone (reads from Lab 03 data)
  08 (Streaming) → standalone (generates own data)
```

## Exercises

Labs contain `________` blanks that you fill in during the session.  
Solutions are in the `solutions/` folder — use them as reference after attempting the exercises.

## Requirements

- Azure Databricks workspace
- All-purpose cluster (recommended) or serverless
- No ADLS, no secret scopes, no Unity Catalog required
