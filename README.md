# Azure Databricks Training — Lab Notebooks

## Setup

1. Import this repo into your Databricks workspace (Repos → Add Repo → paste URL)
2. Run the setup notebooks first:
   - `setup/00_Lab_Environment_Setup` — Creates catalog, schemas, volumes
   - `setup/01_Generate_Sample_Data` — Generates Day 1 lab data
   - `setup/02_Generate_ADLS_Sample_Data` — Generates Day 2 lab data (requires ADLS config)

## Configuration

Edit the config cell at the top of each notebook:

```python
CATALOG_NAME = "axa_training"  # Change to your catalog name
```

For Day 2 labs (ADLS Gen2), also set:
```python
STORAGE_ACCOUNT = "your_storage_account"
CONTAINER = "data"
```

## Labs

### Day 1
- `jour1/01_Getting_Started_with_Databricks` — Workspace basics, magic commands
- `jour1/02_PySpark_Transformation_Lab` — PySpark DataFrame API
- `jour1/03_Delta_Lake_Lab` — ACID transactions, time travel, constraints

### Day 2
- `jour2/04_Bronze_Layer` — Data ingestion + Auto Loader
- `jour2/05_Silver_Layer` — Data quality + enrichment
- `jour2/06_Gold_Layer` — Aggregations + optimization
- `jour2/07_DLT_Pipeline` — Delta Live Tables

### Solutions
Complete solutions are in `solutions/`.
