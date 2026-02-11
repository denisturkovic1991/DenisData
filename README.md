# Bok, ja sam Denis Turković 👋

### 🚀 Aspiring Analytics Engineer | Data Enthusiast

Trenutno sam u procesu intenzivne promjene karijere prema **Analytics Engineeringu**. Ovaj repozitorij služi kao centralno mjesto mog napretka, projekata i tehnologija koje savladavam tijekom 2026. godine.

---

## 🛠️ Moj Tech Stack

Ovdje su alati i tehnologije na koje se fokusiram:

| Kategorija | Tehnologije |
| :--- | :--- |
| **Data Modeling & SQL** | PostgreSQL, Star Schema, Relational Databases 🏗️ |
| **BI & Visualization** | Microsoft Power BI (Desktop & Service), Data Storytelling 📊 |
| **Analytics Engineering** | dbt (Data Build Tool), Git/Version Control ⚙️ |
| **Big Data & Cloud** | Microsoft Fabric, Azure Databricks, PySpark ☁️ |
| **Programming** | Python (Pandas, Polars), Prompt Engineering 🐍 |

---

## 📈 Roadmap 2026. - Napredak

Moj plan učenja i certificiranja po kvartalima:

| Kvartal | Fokus | Status |
| :--- | :--- | :--- |
| **Q1** | Excel Mastery & SQL Foundations | 🔄 **U tijeku** (Excel 75% Done) |
| **Q2** | Power BI & PL-300 Certification | 📅 Planirano |
| **Q3** | Python & dbt (The Engine Room) | 📅 Planirano |
| **Q4** | Cloud ( Microsoft Fabric) & Spark Integration | 📅 Planirano |

---

## 📂 Izdvojeni Projekti

# 🚗 EcoDrive AI: Intelligent EV Fleet Optimization System

![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen)
![Python](https://img.shields.io/badge/Python-3.11-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791)
![PowerBI](https://img.shields.io/badge/Reporting-PowerBI-F2C811)
![License](https://img.shields.io/badge/License-MIT-green)

> **Business Value:** Transformacija sirovih IoT podataka u konkretne odluke za smanjenje troškova flote i optimizaciju trajanja baterije.

---

## 📖 O Projektu

**EcoDrive AI** je skalabilni *End-to-End Analytics Engineering* projekt dizajniran za obradu telemetrijskih podataka električnih vozila (EV). Za razliku od standardnih dashboarda, ovaj sustav simulira real-time "pingove" vozila, koristi napredne SQL algoritme za **sessionizaciju** (detekciju vožnji i punjenja) i priprema **Gold Layer** podatke za poslovno izvještavanje.

Projekt prati modernu **ELT (Extract, Load, Transform)** arhitekturu, s fokusom na modularnost, kvalitetu podataka i performanse.

---

## 🏗 Arhitektura Sustava

Sustav je dizajniran da oponaša produkcijsko okruženje velikih razmjera.



| Faza | Komponenta | Opis |
| :--- | :--- | :--- |
| **1. Ingestion** | `Python (Faker + SQLAlchemy)` | Generiranje sintetičkih IoT podataka (GPS, Battery SoC, Temp) u realnom vremenu uz SSL enkripciju. |
| **2. Storage** | `PostgreSQL (Partitioned)` | Skladištenje milijuna redova uz korištenje **Table Partitioning** i **BRIN indeksa** za optimizaciju. |
| **3. Silver Layer** | `PL/pgSQL Procedures` | Čišćenje podataka, deduplikacija i **Sessionization** (pretvaranje raw signala u 'Trips' i 'Charging Sessions'). |
| **4. Gold Layer** | `Materialized Views` | **OBT (One Big Table)** pristup za brzo serviranje podataka prema Power BI-u. |
| **5. Vizualizacija** | `Power BI` | Interaktivni dashboardi za praćenje efikasnosti flote (kWh/100km) i degradacije baterije. |

---

## 🚀 Ključne Značajke (Key Features)

### 1. Inteligentna "Sessionizacija"
Sirovi GPS podaci su "šum". Sustav koristi SQL `WINDOW` funkcije (`LAG`, `LEAD`) kako bi inteligentno grupirao podatke:
* **Trip Detection:** Ignorira kratka stajanja (npr. semafori) i registrira vožnju tek nakon definiranog praga kretanja.
* **Charging Analytics:** Automatski detektira kada je vozilo na punjaču i računa krivulju punjenja (kW snagu).

### 2. Optimizacija Performansi (Senior Level)
* **Incremental Processing:** SQL pipeline ne obrađuje cijelu povijest svaki put, već samo nove podatke (`WHERE timestamp > last_run`).
* **Timezone Awareness:** Svi podaci se normaliziraju na UTC (`TIMESTAMPTZ`) kako bi se podržala međunarodna flota.

### 3. Data Quality & Resilience
* **Retry Logic:** Python skripte imaju ugrađen "Self-Healing" mehanizam u slučaju prekida konekcije s bazom.
* **Noise Filtering:** SQL procedure automatski odbacuju GPS "drift" (lažne pomake vozila dok su parkirana).

---

## 🛠 Tech Stack

* **Jezici:** Python 3.10+, SQL (PL/pgSQL)
* **Baza:** PostgreSQL 15+ (Local & Cloud ready)
* **Biblioteke:** `pandas`, `sqlalchemy`, `faker`, `psycopg2`
* **DevOps & Tools:** Git, GitHub Actions (Planirano), Docker
* **BI:** Microsoft Power BI (DirectQuery + Import Mode Composite Models)

---

## 💻 Kako Pokrenuti (Local Setup)

1.  **Kloniraj repozitorij:**
    ```bash
    git clone [https://github.com/tvoj-username/EcoDrive-AI.git](https://github.com/tvoj-username/EcoDrive-AI.git)
    cd EcoDrive-AI
    ```

2.  **Postavi okolinu:**
    Kreiraj `.env` datoteku u root folderu:
    ```text
    DB_HOST=localhost
    DB_NAME=ecodrive_db
    DB_USER=postgres
    DB_PASS=tvoja_lozinka
    ```

3.  **Inicijaliziraj bazu:**
    Pokreni SQL skripte redom (`01_init`, `04_analytics`, `05_gold`) ili koristi Python trigger:
    ```bash
    pip install -r requirements.txt
    python src/data_generator.py  # Za početak simulacije
    python src/analytics_trigger.py # Za pokretanje ETL-a
    ```

---

## 📈 Roadmap (Plan Razvoja)

Ovaj projekt prati moj razvojni put od Data Analysta do Analytics Engineera.

- [x] **Q1 2026:** Python Ingestion & PostgreSQL Core (Završeno) ✅
- [ ] **Q2 2026:** Advanced Analytics (Sessionization) & Power BI
- [ ] **Q3 2026:** Migracija na **dbt** (Data Build Tool) i uvođenje CI/CD testova.
- [ ] **Q4 2026:** Skaliranje na **Azure Cloud** (Databricks/Fabric) i Big Data processing.

---
*Projekt je razvijen kao dio intenzivnog Analytics Engineering bootcampa (2026).*

## 📫 Kontaktirajte me

Otvoren sam za diskusiju o podacima, suradnji ili savjetima za karijeru!

* [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/denis-turkovi%C4%87-1975a0125/)
* 📧 **Email:** denis.turkovic91@gmail.com

---

> *"In God we trust, all others must bring data."* — W. Edwards Deming
