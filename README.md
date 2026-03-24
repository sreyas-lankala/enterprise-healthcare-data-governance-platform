# Enterprise Healthcare Data Governance Platform

> **Airflow · Azure Data Lake · Microsoft Purview · dbt · Python · SQL · Power BI**

An enterprise-grade healthcare data governance platform processing **2M+ synthetic clinical records**, demonstrating production-level data quality engineering, metadata management, lineage tracking, and observability — built to meet real-world healthcare compliance standards.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)]()
[![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)](https://getdbt.com)
[![Apache Airflow](https://img.shields.io/badge/Apache_Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)](https://airflow.apache.org)
[![Azure](https://img.shields.io/badge/Azure_Data_Lake-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)]()
[![Microsoft Purview](https://img.shields.io/badge/Microsoft_Purview-0078D4?style=flat-square&logo=microsoft&logoColor=white)]()
[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)]()

---

## 🎯 Problem Statement

Healthcare organizations generate massive volumes of clinical data across disparate systems — patient records, claims, procedures, lab results. Without a governance framework, this data becomes unreliable, unauditable, and non-compliant. This platform simulates how a modern healthcare analytics team would architect a **trusted, governed data platform** from ingestion to analytics.

---

## 📐 Architecture

```
Source Systems (Synthea Synthetic EHR — 2M+ records)
        │
        ▼
   ┌─────────┐
   │   RAW   │  ← Azure Data Lake ingestion layer
   └────┬────┘
        │
        ▼
   ┌─────────┐
   │ STAGING │  ← Schema normalization · validation rules · deduplication
   └────┬────┘
        │
        ▼
   ┌──────────┐
   │ CURATED  │  ← dbt transformations · business logic · lineage-tracked models
   └────┬─────┘
        │
        ▼
   ┌────────────┐
   │ GOVERNANCE │  ← Metadata catalog (Purview) · lineage maps · data dictionary
   └────┬───────┘
        │
        ▼
   ┌───────────┐
   │ ANALYTICS │  ← Power BI dashboards · quality scorecards · observability views
   └───────────┘

   Orchestration: Apache Airflow DAGs scheduling all layers end-to-end
```

---

## 📊 Key Metrics & Results

| Metric | Value |
|--------|-------|
| **Records Processed** | 2M+ synthetic clinical records |
| **Data Domains** | Patient encounters, claims, procedures, clinical observations |
| **Quality Checks** | Completeness, schema integrity, duplicates, referential integrity |
| **Governance Artifacts** | Dataset ownership, lineage mappings, business definitions, SLA tracking |
| **Observability** | Schema drift detection · data freshness delays · volume anomaly alerts |
| **Compliance Alignment** | Structured to meet HIPAA-aligned governance requirements |

---

## 🔧 Tech Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **Data Source** | Synthea (Synthetic EHR) | Realistic 2M+ patient record generation |
| **Storage** | Azure Data Lake | Raw and staged data storage |
| **Transformation** | dbt | Modular, lineage-tracked SQL transformations |
| **Orchestration** | Apache Airflow | DAG-based pipeline scheduling |
| **Data Catalog** | Microsoft Purview | Metadata management and lineage tracking |
| **Quality Framework** | Python + SQL | Automated validation rule engine |
| **Visualization** | Power BI | Observability dashboards and quality scorecards |
| **Version Control** | GitHub | Source control and CI/CD |

---

## 🏗️ Core Platform Components

### 1. Data Ingestion Layer
- Ingests Synthea-generated synthetic healthcare records into Azure Data Lake
- Covers patient encounters, claims, procedures, clinical observations
- Preserves raw source-of-truth without transformation

### 2. Data Quality Framework
- **Automated validation rules:** schema consistency checks, completeness validation, duplicate detection, referential integrity
- **Exception tracking:** failed records logged with root cause context
- **Quality scorecards:** pipeline health metrics tracked per run

### 3. Metadata Governance (Microsoft Purview)
- Dataset ownership and stewardship assignments
- Governance classification (PHI, PII, operational data)
- Business definitions and data dictionary entries
- End-to-end data lineage: source → staging → curated → analytics

### 4. Observability Layer
- **Schema drift monitoring:** alerts when column types or structures change unexpectedly
- **Data freshness checks:** detects pipeline delays against defined SLAs
- **Volume anomaly detection:** flags unexpected record count changes
- **Pipeline execution monitoring:** tracks DAG run status and failure patterns

### 5. Apache Airflow Orchestration
- DAGs schedule ingestion → staging → dbt → quality validation → governance updates → monitoring
- Dependency management ensures each layer completes before the next begins
- Failure alerting and retry logic for production resilience

---

## 📁 Repository Structure

```
enterprise-healthcare-data-governance-platform/
│
├── ingestion/                    # Data ingestion scripts
├── staging/                      # Staging transformation SQL
├── dbt_models/                   # dbt project (models, tests, macros)
│   ├── models/
│   ├── tests/
│   └── dbt_project.yml
├── governance/                   # Metadata catalog schemas and Purview config
├── quality_framework/            # Python validation rule engine
├── observability/                # Monitoring views and alerting scripts
├── orchestration/                # Apache Airflow DAGs
│   └── healthcare_platform_dag.py
├── dashboards/                   # Power BI report definitions
└── docs/                         # Architecture docs and governance framework
```

---

## 🎯 Target Roles Demonstrated

This project showcases skills relevant to:
- **Data Quality Engineer** — automated validation, rule engines, exception handling
- **Data Governance Engineer** — metadata catalog, lineage, stewardship, classification
- **Data Engineer** — pipeline architecture, ETL/ELT, orchestration, dbt modeling
- **Healthcare Data Engineer** — HIPAA-aligned governance, clinical data domains
- **Analytics Engineer** — dbt transformations, data modeling, curated analytical layers

---

## 👤 Author

**Sreyas Lankala** — Data Quality & Governance Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sreyas-lankala/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sreyaslankala@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/sreyas-lankala)

> 🛂 Authorized to work in the USA on F-1 OPT starting May 27, 2026 (STEM OPT eligible — 3-year authorization)
