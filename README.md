# Azure Databricks Training — Lab Notebooks

## Quick Start

1. **Import** this repo into your Databricks workspace:
   - Go to **Repos → Add Repo**
   - Paste: `https://github.com/sundaraselvaraj/axa-databricks-training`

2. **Run setup notebooks** (in order):
   - `setup/00_Lab_Environment_Setup` — Creates catalog `axa_training`, schemas, volume
   - `setup/01_Generate_Sample_Data` — Generates Day 1 lab data

3. **Start labs:**
   - `jour1/01_Getting_Started_with_Databricks`

## Configuration

The default catalog name is `axa_training`. Change it in the config cell if needed:

```python
CATALOG_NAME = "axa_training"  # Change to your catalog name
```

## Day 2 Labs (Optional — requires ADLS Gen2)

Day 2 labs require an Azure Data Lake Storage Gen2 account. Edit the config cell:

```python
STORAGE_ACCOUNT = "your_storage_account"
CONTAINER = "data"
```

Run `setup/02_Generate_ADLS_Sample_Data` to generate Day 2 data.

## Labs

### Day 1
| Lab | Topic |
|-----|-------|
| 01 | Getting Started with Databricks |
| 02 | PySpark Transformations |
| 03 | Delta Lake Operations |

### Day 2 (requires ADLS)
| Lab | Topic |
|-----|-------|
| 04 | Bronze Layer (Ingestion + Auto Loader) |
| 05 | Silver Layer (Data Quality + Enrichment) |
| 06 | Gold Layer (Aggregations + Optimization) |
| 07 | DLT Pipeline |

Solutions are in `solutions/`.
