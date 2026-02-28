# Bok, ja sam Denis Turković 👋

### 🚀 Aspiring Analytics Engineer | Data Enthusiast

Trenutno sam u procesu intenzivne promjene karijere prema **Analytics Engineeringu**. Ovaj repozitorij služi kao centralno mjesto mog napretka, projekata i tehnologija koje želim savladati tijekom 2026. godine te 1. dijelom 2027. godine.

---

## 🛠️ Moj Tech Stack

Ovdje su alati i tehnologije na koje se fokusiram:

| Kategorija | Tehnologije |
| :--- | :--- |
| **Data Modeling & SQL** | PostgreSQL, Star Schema, Relational Databases 🏗️ |
| **BI & Visualization** | Microsoft Power BI (Desktop & Service), Data Storytelling 📊 |
| **Analytics Engineering** | dbt (Data Build Tool), Git/Version Control ⚙️ |
| **Programming** | Python (Pandas, Polars), Prompt Engineering 🐍 |
| **Big Data & Cloud** | Microsoft Fabric, Azure Databricks, PySpark ☁️ |


---

## 📈 Roadmap 2026. - Napredak

Moj plan učenja i certificiranja po kvartalima:

| Kvartal | Fokus | Status |
| :--- | :--- | :--- |
| **Q1** | Excel Mastery & SQL Foundations | 🔄 **U tijeku** (Excel Done, SQL started) |
| **Q2** | Power BI & PL-300 Certification | 📅 Planirano |
| **Q3** | Python & dbt (The Engine Room) | 📅 Planirano |
| **Q4** | Cloud ( Microsoft Fabric) & Spark Integration | 📅 Planirano |

---




## 📂 Izdvojeni Projekti

# 🚗⚡ EcoDrive AI: Intelligent EV Fleet Optimization System

> **A progressive data engineering project** — built quarter-by-quarter as a career transition portfolio piece, demonstrating end-to-end skills from SQL foundations to cloud-scale analytics.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status: In Progress](https://img.shields.io/badge/Status-Q1%20In%20Progress-blue.svg)]()
[![Stack: SQL · Python · dbt · Azure · Power BI](https://img.shields.io/badge/Stack-SQL%20%C2%B7%20Python%20%C2%B7%20dbt%20%C2%B7%20Azure%20%C2%B7%20Power%20BI-orange.svg)]()

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Business Context](#business-context)
- [Architecture Overview](#architecture-overview)
- [Quarterly Roadmap](#quarterly-roadmap)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Data Model](#data-model)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

---

## About the Project

**EcoDrive AI** simulates an intelligent fleet management platform for electric vehicles (EVs). The system ingests telemetry data from a fleet of EVs, optimizes charging schedules, predicts energy consumption, and provides actionable dashboards for fleet managers.

The project is intentionally designed to **scale with my learning journey** — starting with clean SQL modeling and Excel analytics, evolving through Power BI dashboards, Python automation, dbt transformations, and culminating in a full Azure cloud pipeline with Microsoft Fabric.

### Why This Project?

The EV fleet management domain sits at the intersection of several high-demand data engineering challenges:
- **High-volume time-series data** (telemetry, GPS, battery metrics)
- **Real-time and batch processing** patterns
- **Complex business logic** (charging optimization, route planning, cost analysis)
- **Clear ROI storytelling** (fuel savings, carbon reduction, fleet utilization)

---

## Business Context

**Scenario:** *GreenFleet d.o.o.*, a fictional Croatian logistics company, operates a fleet of 250 electric delivery vehicles across Zagreb, Split, Rijeka, and Osijek. They need a data platform to:

1. **Monitor** real-time vehicle telemetry (battery %, location, speed, temperature)
2. **Optimize** charging schedules to minimize electricity costs (off-peak pricing)
3. **Predict** energy consumption per route based on weather, cargo weight, and terrain
4. **Report** fleet KPIs to management (utilization rate, cost per km, CO₂ savings)
5. **Scale** analytics as the fleet grows to 1000+ vehicles

### Key Business Questions

| # | Question | Data Domain |
|---|----------|-------------|
| 1 | What is the average energy consumption per vehicle per route? | Telemetry + Routes |
| 2 | Which charging stations are underutilized vs. overloaded? | Charging Events |
| 3 | How much money do we save by charging during off-peak hours? | Pricing + Schedules |
| 4 | Which drivers have the most energy-efficient driving patterns? | Driver Behavior |
| 5 | What is our fleet's total CO₂ offset compared to diesel equivalents? | Sustainability |
| 6 | Can we predict battery degradation to schedule maintenance? | Predictive Analytics |

---

## Architecture Overview

The architecture evolves across quarters:

```
Q1 (Foundations)          Q2 (Visualization)       Q3 (Engineering)
┌─────────────┐          ┌─────────────┐          ┌─────────────┐
│  CSV / Excel │          │  Power BI   │          │   Python    │
│  Raw Data    │───SQL───▶│  Dashboards │    ┌────▶│  Automation │
│  PostgreSQL  │          │  Reports    │    │     │  Pandas/dbt │
└─────────────┘          └─────────────┘    │     └─────────────┘
                                            │
Q4 (Cloud)               Q5 (Portfolio)     │
┌─────────────┐          ┌─────────────┐    │
│ Azure Data  │          │  Microsoft  │    │
│ Lake +      │◀─────────│  Fabric     │────┘
│ Databricks  │          │  End-to-End │
└─────────────┘          └─────────────┘
```

### Target Architecture (Final State — Q5)

```
Data Sources          Ingestion           Transform           Serve
┌──────────┐        ┌──────────┐        ┌──────────┐       ┌──────────┐
│ Vehicle   │──CSV──▶│          │        │          │       │ Power BI │
│ Telemetry │       │  Azure   │──────▶ │   dbt    │──────▶│ Dashboard│
│           │       │  Data    │        │  Models  │       │          │
│ Charging  │──API──▶│  Lake   │        │          │       │ Fabric   │
│ Stations  │       │  Gen2   │        │ Spark on │       │ Lakehouse│
│           │       │          │        │Databricks│       │          │
│ Weather   │──API──▶│          │        │          │       │ REST API │
│ Data      │       └──────────┘        └──────────┘       └──────────┘
│           │
│ Electricity│
│ Pricing   │
└──────────┘
```

---

## Quarterly Roadmap

### Q1: Foundations (Veljača – Travanj 2026) 🟢 CURRENT

**Learning Focus:** Excel (Power Query/DAX), SQL & PostgreSQL, Statistics, Business Analysis

**Project Deliverables:**
- [ ] Design and implement PostgreSQL database schema (3NF + star schema)
- [ ] Generate synthetic fleet data (vehicles, routes, charging events, telemetry)
- [ ] Write 20+ analytical SQL queries (window functions, CTEs, complex JOINs)
- [ ] Excel dashboard with Power Query data connections
- [ ] Statistical analysis of fleet performance (distributions, correlations)
- [ ] Business requirements document (BRD) for the platform

**Key Files:** `src/q1_foundations/`

---

### Q2: Visualization & Storytelling (Svibanj – Srpanj 2026) 🔵 UPCOMING

**Learning Focus:** Power BI Desktop, Data Storytelling, PL-300 Certification, Python basics

**Project Deliverables:**
- [ ] Power BI data model connected to PostgreSQL
- [ ] Executive dashboard (fleet KPIs, cost analysis, utilization)
- [ ] Operational dashboard (real-time vehicle status, charging schedules)
- [ ] Data storytelling report: "How EcoDrive saves €50K/month"
- [ ] Python scripts for basic data cleaning and CSV processing

**Key Files:** `src/q2_visualization/`

---

### Q3: Engineering Mindset (Kolovoz – Listopad 2026) 🟡 PLANNED

**Learning Focus:** Python (Pandas/NumPy), Prompt Engineering, GenAI, dbt

**Project Deliverables:**
- [ ] Python ETL pipeline for data ingestion and transformation
- [ ] Pandas-based data quality checks and anomaly detection
- [ ] AI-assisted code generation workflows (documented)
- [ ] Full dbt project with staging, intermediate, and mart layers
- [ ] dbt tests, documentation, and data lineage graphs
- [ ] Automated reporting scripts

**Key Files:** `src/q3_engineering/`

---

### Q4: Cloud & Big Data (Studeni 2026 – Siječanj 2027) 🟠 PLANNED

**Learning Focus:** Azure (DP-900), Databricks, Spark, Cloud Integration

**Project Deliverables:**
- [ ] Azure Data Lake Gen2 setup for raw/processed/curated zones
- [ ] Databricks notebooks for Spark-based transformations
- [ ] Migrate dbt models to run on Databricks
- [ ] Implement medallion architecture (Bronze → Silver → Gold)
- [ ] Orchestration with Azure Data Factory
- [ ] Integration project: dbt + SQL + Azure pipeline

**Key Files:** `src/q4_cloud/`

---

### Q5: Portfolio Finalization (Veljača – Ožujak 2027) 🔴 PLANNED

**Learning Focus:** Microsoft Fabric (DP-600), Portfolio, Career Launch

**Project Deliverables:**
- [ ] Migrate to Microsoft Fabric Lakehouse
- [ ] End-to-end pipeline in Fabric (Dataflows, Notebooks, Pipelines)
- [ ] Semantic model with Direct Lake mode
- [ ] Comprehensive project documentation and architecture diagrams
- [ ] Video walkthrough / demo recording
- [ ] Polished GitHub repository with CI/CD

**Key Files:** `src/q5_portfolio/`

---

## Tech Stack

| Category | Technology | Quarter Introduced |
|----------|-----------|-------------------|
| **Database** | PostgreSQL 16 | Q1 |
| **Spreadsheet** | Excel (Power Query, DAX) | Q1 |
| **Analytics** | Statistical methods, Business Analysis | Q1 |
| **Visualization** | Power BI Desktop | Q2 |
| **Certification** | PL-300 (Power BI Data Analyst) | Q2 |
| **Programming** | Python 3.12 (Pandas, NumPy) | Q3 |
| **AI Tools** | Prompt Engineering, GenAI for Data | Q3 |
| **Transformation** | dbt Core | Q3 |
| **Cloud** | Azure Data Lake Gen2 | Q4 |
| **Big Data** | Azure Databricks, Apache Spark | Q4 |
| **Orchestration** | Azure Data Factory | Q4 |
| **Certification** | DP-900 (Azure Fundamentals) | Q4 |
| **Platform** | Microsoft Fabric | Q5 |
| **Certification** | DP-600 (Fabric Analytics Engineer) | Q5 |
| **Version Control** | Git + GitHub | All |
| **IDE** | Claude Code (AI-assisted development) | All |

---

## Project Structure

```
ecodrive-ai/
├── README.md                          # This file
├── LICENSE                            # MIT License
├── CHANGELOG.md                       # Version history per quarter
├── .gitignore                         # Git ignore rules
├── .env.example                       # Environment variable template
│
├── docs/                              # Project documentation
│   ├── PROJECT_ROADMAP.md             # Detailed quarterly roadmap
│   ├── DATA_DICTIONARY.md             # Column-level data documentation
│   ├── DATA_SOURCES.md                # External API registry & documentation
│   ├── BUSINESS_REQUIREMENTS.md       # BRD document
│   ├── ARCHITECTURE.md                # Architecture decision records
│   └── LEARNING_LOG.md                # Personal learning journal
│
├── config/                            # Configuration files
│
├── scripts/                           # Operational scripts
│   ├── backup/
│   │   └── backup.sh                 # Automated backup (full/diff/validate/cleanup)
│   └── monitoring/
│       └── healthcheck.sh            # System health check (DB/backups/alerts/sources)
│
├── data/                              # Data files (gitignored for large files)
│   ├── raw/                           # Original, immutable data
│   ├── processed/                     # Cleaned and transformed data
│   └── models/                        # ML model artifacts (Q3+)
│
├── src/                               # Source code, organized by quarter
│   ├── q1_foundations/                 # Q1: SQL, Excel, Statistics
│   │   ├── sql/
│   │   │   ├── schema/
│   │   │   │   ├── 001_create_database.sql        # DB & user creation
│   │   │   │   ├── 002_create_tables.sql          # Core tables + star schema
│   │   │   │   ├── 003_create_source_tables.sql   # External API landing tables
│   │   │   │   ├── 004_create_notification_system.sql  # Alert rules & triggers
│   │   │   │   └── 005_create_backup_system.sql   # Backup tracking & validation
│   │   │   ├── seed/                  # Data seeding scripts
│   │   │   ├── queries/               # Analytical queries
│   │   │   └── views/                 # Database views
│   │   ├── excel/                     # Power Query / DAX workbooks
│   │   └── statistics/                # Statistical analysis scripts
│   │
│   ├── q2_visualization/              # Q2: Power BI, Storytelling
│   ├── q3_engineering/                # Q3: Python, dbt, AI
│   ├── q4_cloud/                      # Q4: Azure, Databricks, Spark
│   └── q5_portfolio/                  # Q5: Fabric, Final Integration
│
├── tests/                             # Test suites
└── .github/workflows/ci.yml          # CI/CD pipeline
```

---

## Getting Started

### Prerequisites

**Q1 (Current):**
- PostgreSQL 16+ installed locally
- Excel (Microsoft 365 or standalone)
- Git + GitHub account
- Claude Code CLI

### Quick Start

```bash
# Clone the repository
git clone https://github.com/<your-username>/ecodrive-ai.git
cd ecodrive-ai

# Copy and configure environment
cp .env.example .env
# Edit .env with your PostgreSQL credentials and API keys

# 1. Create database and users
psql -U postgres -f src/q1_foundations/sql/schema/001_create_database.sql

# 2. Create core tables (operational + analytical)
psql -U ecodrive_admin -d ecodrive -f src/q1_foundations/sql/schema/002_create_tables.sql

# 3. Create external data source landing tables
psql -U ecodrive_admin -d ecodrive -f src/q1_foundations/sql/schema/003_create_source_tables.sql

# 4. Set up notification & alert system
psql -U ecodrive_admin -d ecodrive -f src/q1_foundations/sql/schema/004_create_notification_system.sql

# 5. Set up backup tracking system
psql -U ecodrive_admin -d ecodrive -f src/q1_foundations/sql/schema/005_create_backup_system.sql

# 6. Make scripts executable
chmod +x scripts/backup/backup.sh
chmod +x scripts/monitoring/healthcheck.sh

# 7. Run health check
./scripts/monitoring/healthcheck.sh

# 8. Seed sample data (coming next)
# psql -U ecodrive_admin -d ecodrive -f src/q1_foundations/sql/seed/001_seed_vehicles.sql
```

---

## External Data Sources (Real / Official)

All data is sourced from **real, official APIs** — not synthetic where avoidable. See [`docs/DATA_SOURCES.md`](docs/DATA_SOURCES.md) for full documentation.

| Source | Provider | Type | Data Used |
|--------|----------|------|-----------|
| 🌦️ Weather | [Open-Meteo](https://open-meteo.com/) | REST API (free) | Hourly temp, rain, wind for fleet cities |
| ⚡ Electricity Prices | [ENTSO-E](https://transparency.entsoe.eu/) | REST API (free key) | Day-ahead EUR/MWh prices for Croatia |
| 🔌 Charging Stations | [Open Charge Map](https://openchargemap.org/) | REST API (free key) | Real station locations, charger types, power |
| 🚗 EV Specs | [EV Database](https://ev-database.org/) | Web/CSV | Battery capacity, range, efficiency per model |
| 🗺️ Routes | [OSRM](http://project-osrm.org/) | REST API (free) | Real road distances & durations via OpenStreetMap |
| 🏦 Holidays/Tariffs | [data.gov.hr](https://data.gov.hr/) + [HEP](https://www.hep.hr/) | CSV/Published | Croatian holidays, HEP VT/NT tariff rates |
| 💱 Currency | [HNB API](https://api.hnb.hr/) | REST API (free) | Croatian National Bank exchange rates |

All raw data lands in a dedicated `raw_sources` schema with full ingestion audit logging.

---

## 💾 Backup System

Follows the **3-2-1 backup rule**: 3 copies, 2 storage types, 1 offsite.

| Schedule | Type | Frequency | Retention | Command |
|----------|------|-----------|-----------|---------|
| Full database | `pg_dump` custom | Weekly (Sun 02:00) | 90 days | `./scripts/backup/backup.sh full` |
| Differential | Data-only dump | Daily (Mon-Sat 03:00) | 30 days | `./scripts/backup/backup.sh differential` |
| Critical tables | CSV export | Hourly | 7 days | `./scripts/backup/backup.sh tables` |
| Validate backup | Checksum + restore test | Daily (06:00) | — | `./scripts/backup/backup.sh validate` |
| Cleanup expired | Auto-delete | Weekly (Sun 05:00) | — | `./scripts/backup/backup.sh cleanup` |

**Features:**
- SHA-256 checksum verification on every backup
- Automated anomaly detection (unexpected row count changes)
- Database-tracked backup history with status dashboard (`backup_mgmt.v_latest_backups`)
- Backup failure triggers immediate notification via alert system
- Q4 expansion: Azure Blob Storage offsite replication

---

## 🔔 Notification & Alert System

Database-native alerting with PostgreSQL triggers that fire automatically on data changes.

### Alert Rules (13 pre-configured)

| Rule | Severity | Trigger | Channels |
|------|----------|---------|----------|
| Battery < 10% | 🔴 CRITICAL | After trip completion | Dashboard, Email, Slack |
| Battery < 20% | 🟡 WARNING | After trip completion | Dashboard, Email |
| Charging failed/interrupted | 🟡 WARNING | Charging event update | Dashboard, Email |
| Peak tariff charging (>10 kWh) | 🔵 INFO | Charging completed | Dashboard |
| Speed > 130 km/h | 🟡 WARNING | After trip completion | Dashboard, Email |
| Vehicle → maintenance | 🟡 WARNING | Vehicle status change | Dashboard, Email |
| Odometer > 150,000 km | 🔵 INFO | Vehicle odometer update | Dashboard, Email |
| Daily fleet cost > €500 | 🟡 WARNING | Scheduled check | Dashboard, Email |
| Data ingestion failed | 🔴 CRITICAL | Ingestion log update | Dashboard, Email, Slack |

**Features:**
- Cooldown periods prevent alert storms (configurable per rule)
- Suppression windows for planned maintenance
- Full dispatch tracking (sent/delivered/failed per channel)
- Dashboard views: active alerts, daily summary, per-vehicle frequency
- Q3 expansion: Python dispatcher for Email/Slack/SMS delivery

### Alert Flow

```
Data Change (INSERT/UPDATE)
       │
       ▼
┌─────────────────────┐
│  PostgreSQL Trigger  │ ◄── Fires automatically
│  (check_battery,     │
│   check_charging,    │
│   check_vehicle)     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐     ┌───────────────────┐
│  notifications.      │────▶│  v_active_alerts  │ ◄── Dashboard widget
│  notifications       │     │  v_daily_summary  │
│  (central store)     │     └───────────────────┘
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Dispatch Engine     │ ◄── Q3: Python service polls & sends
│  (Email/Slack/SMS)   │
└─────────────────────┘
```

---

## 🏥 System Health Monitoring

Run `./scripts/monitoring/healthcheck.sh` for a full system health report:

```
📊 Database Connectivity .............. ✅ PASS
📋 Core Table Health .................. ✅ PASS
🔔 Notification System ................ ✅ PASS
💾 Backup System ...................... ✅ PASS
🌐 External Data Sources .............. ✅ PASS
⚡ Database Performance ................ ✅ PASS

Overall Status: ✅ HEALTHY
```

---

## Data Model

### Core Entities (Q1 — Star Schema)

```
                    ┌──────────────┐
                    │  dim_vehicle  │
                    │──────────────│
                    │ vehicle_id   │
                    │ make         │
                    │ model        │
                    │ year         │
                    │ battery_kwh  │
                    │ range_km     │
                    │ status       │
                    └──────┬───────┘
                           │
┌──────────────┐    ┌──────┴───────┐    ┌──────────────┐
│  dim_driver   │    │  fact_trip   │    │  dim_route   │
│──────────────│    │──────────────│    │──────────────│
│ driver_id    │◄───│ trip_id      │───▶│ route_id     │
│ name         │    │ vehicle_id   │    │ origin       │
│ license_type │    │ driver_id    │    │ destination  │
│ hire_date    │    │ route_id     │    │ distance_km  │
│ rating       │    │ start_time   │    │ elevation_m  │
└──────────────┘    │ end_time     │    │ road_type    │
                    │ energy_kwh   │    └──────────────┘
                    │ distance_km  │
                    │ avg_speed    │    ┌──────────────┐
                    │ weather_id   │───▶│ dim_weather  │
                    │ cargo_kg     │    │──────────────│
                    └──────┬───────┘    │ weather_id   │
                           │            │ temperature  │
                    ┌──────┴───────┐    │ precipitation│
                    │fact_charging │    │ wind_speed   │
                    │──────────────│    │ condition    │
                    │ charge_id    │    └──────────────┘
                    │ vehicle_id   │
                    │ station_id   │    ┌──────────────┐
                    │ start_time   │───▶│dim_station   │
                    │ end_time     │    │──────────────│
                    │ energy_kwh   │    │ station_id   │
                    │ cost_eur     │    │ name         │
                    │ tariff_type  │    │ city         │
                    │ soc_start    │    │ charger_type │
                    │ soc_end      │    │ power_kw     │
                    └──────────────┘    └──────────────┘
```

---

## Contributing

This is a personal portfolio project, but feedback and suggestions are welcome! Feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

*Projekt je razvijen kao dio intenzivnog Analytics Engineering bootcampa (2026).*



## 📫 Kontaktirajte me

* [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/denis-turkovi%C4%87-1975a0125/)
* 📧 **Email:** denis.turkovic91@gmail.com

---

> *"In God we trust, all others must bring data."* — W. Edwards Deming
