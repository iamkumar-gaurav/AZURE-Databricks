# AZURE-Databricks — 30 Days of Azure Databricks

A collection of Jupyter notebooks documenting a 30-day learning journey through Azure Databricks. Each notebook contains concepts, examples, and hands-on exercises to help you learn Spark, Delta Lake, and Databricks integrations with Azure services.

Author: iamkumar-gaurav  
Repository description: 30 Days learning of Azure DBT

---

## Table of contents

- [About](#about)
- [Repo structure](#repo-structure)
- [What you'll learn](#what-youll-learn)
- [Prerequisites](#prerequisites)
- [Running the notebooks locally](#running-the-notebooks-locally)
- [Using these notebooks with Azure Databricks](#using-these-notebooks-with-azure-databricks)
- [Contributing](#contributing)
- [License & contact](#license--contact)

---

## About

This repository contains Jupyter notebooks that follow a day-by-day progression for learning Azure Databricks fundamentals and common workflows. It's intended as a learning log and practical reference for hands-on tasks such as Spark basics, data ingestion, transformations, Delta Lake, and integration with other Azure services.

## Repo structure

- `*.ipynb` — Jupyter Notebooks (one or more notebooks, typically organized by day/topic).
- `assets/` or `data/` (optional) — Supporting files used by notebooks (CSV, images, sample data).
- `README.md` — This file.

Typical notebook naming convention used in this repo:
- `Day-01-Introduction.ipynb`
- `Day-02-Spark-Basics.ipynb`
- `Day-15-Delta-Lake.ipynb`
- etc.

## What you'll learn

Examples of topics covered across the 30-day series:
- Databricks and Spark basics (RDDs, DataFrames, Spark SQL)
- Cluster setup and configuration patterns
- Data ingestion from Azure Blob Storage / ADLS
- ETL and transformation patterns in Spark
- Delta Lake fundamentals and ACID operations
- Performance tuning and partitioning strategies
- Job scheduling and orchestration (Databricks Jobs)
- Basic ML workflows and model tracking (optional)
- Integration with Azure services (Storage, Key Vault, Synapse, Event Hubs)

## Prerequisites

- Python 3.8+ (for running notebooks locally)
- JupyterLab or Jupyter Notebook
- (Optional) Azure subscription and a Databricks workspace to follow Azure-specific steps
- (Optional) Databricks CLI if you plan to sync notebooks with a Databricks workspace

Recommended CLI / packages:
```bash
pip install jupyterlab notebook
pip install databricks-cli  # optional, for pushing notebooks to Databricks
```

## Running the notebooks locally

1. Clone the repository:
```bash
git clone https://github.com/iamkumar-gaurav/AZURE-Databricks.git
cd AZURE-Databricks
```

2. (Optional) Create a virtual environment and install dependencies:
```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install --upgrade pip
pip install jupyterlab
```

3. Start JupyterLab / Notebook and open the notebooks:
```bash
jupyter lab
# or
jupyter notebook
```

4. Open any `Day-*.ipynb` notebook and run the cells. Adjust file paths and credentials as needed.

## Using these notebooks with Azure Databricks

To run the notebooks inside an Azure Databricks workspace:

1. Export or upload the notebook to Databricks:
   - Use the Databricks UI to import the `.ipynb`
   - Or use `databricks-cli` to import notebooks programmatically

2. Configure clusters and libraries in Databricks that match the notebook environment (Spark, Python packages).

3. Replace any local filesystem paths with ADLS/Blob paths or Databricks File System (dbfs:/) paths.

Quick example using databricks-cli:
```bash
# configure databricks-cli with a token first
databricks workspace import Day-01-Introduction.ipynb /Users/you@domain/Day-01-Introduction.ipynb
```

Notes:
- When moving to Databricks, manage secrets (keys, tokens) via Databricks Secret Scopes or Azure Key Vault — never hardcode credentials in notebooks.

## Contributing

Contributions, improvements, and corrections are welcome.

- Add or update notebooks to reflect clearer examples or corrections.
- Open issues for any errors or suggestions.
- Create a PR with a concise description of what you've changed.

Guidelines:
- Keep notebooks focused and well-documented.
- Avoid committing large datasets; prefer small sample data or links to public data sources.

## License & contact

This repository is intended for learning and reference. If no LICENSE file is present, assume "All rights reserved" until a license is added. To propose a license, open an issue or PR.

Author / Maintainer: iamkumar-gaurav  
GitHub: https://github.com/iamkumar-gaurav

---
