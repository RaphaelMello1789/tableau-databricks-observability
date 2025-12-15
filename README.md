# 📊 Tableau Governance & Observability Pipeline

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Tableau](https://img.shields.io/badge/Tableau-API-orange)](https://www.tableau.com/)
[![Databricks](https://img.shields.io/badge/Databricks-Lakehouse-red)](https://databricks.com/)

## 🚀 Overview
This repository hosts a dual-stage solution for **Tableau Governance** and **Data Observability**. It addresses two critical challenges in modern analytics environments:
1.  **Metadata Management:** Automating the documentation of calculated fields to prevent "Spaghetti Logic".
2.  **Proactive Observability:** Monitoring the freshness of data extracts (SLA) using Databricks and the Tableau Metadata API.

## 📂 Project Structure

### Part 1: Local Metadata Extractor (The MVP)
[Local Metadata Extractor](https://github.com/RaphaelMello1789/tableau-metadata-dictionary)

### Part 2: Scalable Observability on Databricks (Enterprise)
Located in `tableau_observability_pipeline.ipynb`.
* **Goal:** Monitor the health of the Tableau Cloud environment at scale.
* **Architecture:** Python script running on **Databricks** that queries the Tableau Server Client (TSC) API.
* **Storage:** Saves audit logs to a **Delta Lake** table (`bronze_tableau_observability_logs`) for historical analysis.
* **Security:** Uses Databricks Secrets/Key Vault to manage Personal Access Tokens (PAT).

## 🛠️ Tech Stack
* **Languages:** Python 3.x, SQL (SparkSQL)
* **Libraries:** `tableauserverclient`, `pandas`, `lxml`, `pyspark`
* **Platform:** Databricks, Tableau Cloud
* **Concepts:** XML Parsing, API Integration, Data Lakehouse, CI/CD for Analytics.

## ✍️ Articles
This project is detailed in my Medium series:
* [Part 1: Stop Manually Checking Workbooks - Building a Metadata Extractor](LINK_DO_SEU_ARTIGO_AQUI)
* *Part 2: Scaling Observability with Databricks (Coming Soon)*

---
*Created by [Raphael Mello](https://www.linkedin.com/in/raphaelmello/)*
