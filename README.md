# 🏎️ learning-azure-databricks
## *Scuderia Data — Building Your F1 Data Platform on Azure*

> **"Data Engineering is just F1. Raw fuel in, championship insight out."**

This repository follows the **Scuderia Data** metaphor: every Azure Databricks and Data Platform concept mapped to a Formula 1 Racing Team. If you understand F1, you understand Azure Databricks.

---

## 🗺️ The Metaphor Map

| F1 Concept | Azure / Databricks Concept |
|---|---|
| 🏭 F1 Factory | Azure Data Platform (the whole thing) |
| 🏎️ Race Car | Azure Databricks |
| ⚙️ V10 Engine | Apache Spark |
| ⛽ Raw Fuel | Raw Data (events, logs, transactions) |
| 🚛 Fuel Logistics | Azure Data Factory (ADF) |
| 🛢️ Fuel Tank | Azure Data Lake Storage Gen2 (ADLS) |
| 🔧 Pit Lane + Fuel Grades | Delta Lake (Bronze / Silver / Gold) |
| 👷 Pit Crew | Data Engineers |
| 🧑‍✈️ Driver | Data Scientists & Analysts |
| 🖥️ Cockpit | Databricks Notebooks |
| 📡 Telemetry System | Azure Monitor + Databricks Observability |
| 🧠 Race Strategist | Unity Catalog (Governance) |
| 💨 Wind Tunnel | AutoML + MLflow (ML Experiments) |
| 📺 Race Broadcast | Power BI Dashboards |
| 🏆 Championship Table | Lakehouse Architecture |

---

## 📁 Repository Structure

```
learning-azure-databricks/
│
├── flows/                          ← End-to-end learning journeys
│   ├── flow-01-factory-tour.md     ← Overview: the whole F1 factory
│   ├── flow-02-fuel-to-finish.md   ← Data: raw → insights pipeline
│   └── flow-03-race-day-ops.md     ← Production: monitoring & governance
│
├── stories/                        ← Focused concept narratives
│   ├── story-01-the-fuel-tank.md   ← ADLS Gen2 deep dive
│   ├── story-02-the-engine.md      ← Apache Spark internals
│   ├── story-03-pit-lane.md        ← Delta Lake operations
│   ├── story-04-race-strategy.md   ← Unity Catalog governance
│   └── story-05-wind-tunnel.md     ← MLflow & AutoML
│
├── tasks/                          ← Hands-on exercises
│   ├── task-01-spin-up-cluster.md
│   ├── task-02-ingest-bronze.md
│   ├── task-03-transform-silver.md
│   ├── task-04-aggregate-gold.md
│   └── task-05-register-model.md
│
├── 100-foundations/                ← Azure + Databricks fundamentals
├── 200-data-ingestion/             ← ADF, Event Hubs, streaming
├── 300-delta-lake/                 ← Delta operations & optimization
├── 400-databricks-core/            ← Clusters, notebooks, jobs, SQL
├── 500-unity-catalog/              ← Governance, lineage, access
├── 600-medallion-architecture/     ← Bronze → Silver → Gold patterns
├── 700-ml-and-mlflow/              ← Feature store, AutoML, model registry
├── 800-synapse-and-powerbi/        ← Serving layer & reporting
├── 900-production-patterns/        ← CI/CD, cost, monitoring
│
└── articles/                       ← Dev.to series: "Scuderia Data"
    ├── episode-01-welcome-to-the-factory.md
    ├── episode-02-the-fuel-tank.md
    ├── episode-03-fuel-logistics.md
    ├── episode-04-the-race-car.md
    ├── episode-05-the-engine.md
    ├── episode-06-pit-lane-bronze.md
    ├── episode-07-silver-refinement.md
    ├── episode-08-gold-aggregation.md
    ├── episode-09-the-cockpit.md
    ├── episode-10-race-strategy-governance.md
    ├── episode-11-telemetry.md
    ├── episode-12-wind-tunnel-ml.md
    ├── episode-13-race-broadcast.md
    └── episode-14-championship-architecture.md
```

---

## 🚦 How to Use This Repo

1. **Start with `flows/`** — get the big picture of each learning journey
2. **Read the `stories/`** — go deep on individual concepts with the F1 metaphor
3. **Do the `tasks/`** — hands-on exercises to build muscle memory
4. **Browse numbered directories** — structured reference material by topic
5. **Follow the `articles/`** — the Dev.to series tells the whole story episodically

---

## 📚 Dev.to Series: *"Scuderia Data"*

> Published under: **Infrastructure as Code Adventures** or new series **"Like F1? Love Data!"**

14-episode series covering Azure Databricks from factory floor to championship podium.

---

## 🔗 Related Repositories

- `learning-crossplane-schemas` — Infrastructure provisioning
- `learning-audit-automation` — Security & compliance automation
- `learning-tailscale` — Secure networking

---

*Part of the [stallone](https://github.com/stallone) learning ecosystem.*
