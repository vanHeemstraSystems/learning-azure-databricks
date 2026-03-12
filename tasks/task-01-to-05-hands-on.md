# Task 01 — Spin Up a Databricks Cluster

## 🎯 Goal
Create a Job cluster suitable for a Bronze ingestion pipeline.

## Steps
1. Navigate to your Databricks workspace → Compute
2. Create a Job Cluster with:
   - Runtime: 13.3 LTS (Spark 3.4, Scala 2.12)
   - Node type: Standard_DS3_v2
   - Auto-scaling: 2–4 workers
   - Auto-termination: 20 minutes
3. Add tags: `env=dev`, `owner=your-name`, `cost-centre=learning`

## ✅ Done When
Cluster shows "Running" status in the Compute tab.

---

# Task 02 — Ingest to Bronze

## 🎯 Goal
Write a notebook that reads a CSV from ADLS and writes it as a Delta table in the Bronze zone.

## Steps
1. Upload a sample CSV to `abfss://raw@<your-storage>.dfs.core.windows.net/sample/`
2. Create notebook: `Notebooks/bronze_ingest_sample`
3. Read CSV, add `_ingested_at` and `_source_file` columns
4. Write as Delta to `abfss://refined@.../bronze/sample/`
5. Run `DESCRIBE HISTORY delta.<path>` to verify the transaction log

## ✅ Done When
`_delta_log/` folder exists in your Bronze path and history shows 1 commit.

---

# Task 03 — Transform to Silver

## 🎯 Goal
Write a MERGE notebook that reads Bronze and upserts to Silver with basic cleaning.

## Steps
1. Create notebook: `Notebooks/silver_transform_sample`
2. Read Bronze Delta table
3. Apply: cast types, filter nulls, trim strings, add `_updated_at`
4. MERGE into a Silver Delta table on the business key
5. Run twice — confirm idempotency (row count stays the same on second run)

## ✅ Done When
Running the notebook twice produces the same Silver row count both times.

---

# Task 04 — Aggregate to Gold

## 🎯 Goal
Write a Gold aggregation notebook that reads Silver and writes a business metric table.

## Steps
1. Create notebook: `Notebooks/gold_aggregate_sample`
2. Read Silver Delta table
3. Apply `groupBy` + `agg` to create at least 3 metrics
4. Write as Delta with `mode("overwrite")` to Gold path
5. Add Z-ORDER on the most common filter column

## ✅ Done When
Gold table exists and a SQL query from Databricks SQL returns correct aggregated rows.

---

# Task 05 — Register a Model with MLflow

## 🎯 Goal
Train a simple sklearn model using Gold features and register it in the MLflow Model Registry.

## Steps
1. Create notebook: `Notebooks/ml_train_sample`
2. Load Gold feature table as Pandas DataFrame
3. Wrap training in `with mlflow.start_run():`
4. Log params, metrics, and the model with `mlflow.sklearn.log_model`
5. Register the model: `mlflow.register_model(run_uri, "sample-predictor")`
6. Transition to Staging in the Model Registry UI

## ✅ Done When
Model version 1 appears in the Model Registry with stage "Staging".
