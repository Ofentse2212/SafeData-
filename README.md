# SafeData 🟣

### Women's Safety Data Intelligence Platform

**SafeData** is an end-to-end data engineering and analytics project built with **Microsoft Fabric**, focused on exploring publicly available South African gender-based violence and women's safety data.

The project aims to demonstrate how modern data platforms can transform raw public data into reliable, meaningful insights that can support further research, awareness and data-informed decision-making around women's safety.

---

## 🎯 Project Goal

SafeData explores how data engineering and analytics can be applied to a real-world social-impact problem.

The platform will ingest, clean, transform, model and visualise publicly available data to investigate:

* Trends in reported safety-related incidents
* Geographic patterns across South Africa
* Incident rates relative to population
* The distribution of relevant support services
* Areas that may warrant further investigation based on available data

> **Important:** SafeData analyses reported and publicly available data. Reported incidents should not be interpreted as representing the full prevalence of violence or the experiences of all affected individuals.

---

## 🏗️ Architecture

```text
                    PUBLIC DATA SOURCES
                           │
                           ▼
                    ┌──────────────┐
                    │   INGESTION  │
                    │   PIPELINES   │
                    └──────┬───────┘
                           │
                           ▼
              ┌────────────────────────────┐
              │    MICROSOFT FABRIC        │
              │         LAKEHOUSE          │
              │                            │
              │  🥉 BRONZE — Raw Data      │
              │            ↓               │
              │  🥈 SILVER — Clean Data    │
              │            ↓               │
              │  🥇 GOLD — Analytical Data │
              └────────────┬───────────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │  SEMANTIC MODEL  │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │     POWER BI     │
                  │    DASHBOARD     │
                  └──────────────────┘
```

---

## 🛠️ Technologies

* **Microsoft Fabric**
* **OneLake**
* **Fabric Lakehouse**
* **Data Pipelines**
* **Notebooks**
* **SQL**
* **Semantic Models**
* **Power BI**
* **DAX**

---

## 📊 Planned Data Sources

SafeData will work with publicly available datasets covering areas such as:

| Data                 | Purpose                                              |
| -------------------- | ---------------------------------------------------- |
| Crime / safety data  | Analyse reported incidents and trends                |
| GBV-related data     | Explore available GBV statistics                     |
| Population data      | Calculate population-adjusted rates                  |
| Geographic data      | Standardise locations and enable geographic analysis |
| Support-service data | Explore the distribution of relevant services        |

Specific datasets and sources will be documented during the data-discovery phase.

---

## 🧱 Data Architecture

SafeData will follow a **Bronze → Silver → Gold** data architecture.

### 🥉 Bronze — Raw

Contains data as received from the original source with minimal modification.

**Purpose:** preserve the original source data and provide traceability.

### 🥈 Silver — Clean

Contains cleaned and standardised data.

Typical transformations may include:

* Data-type corrections
* Missing-value handling
* Duplicate removal
* Standardisation of geographic names
* Date standardisation
* Category standardisation
* Data validation

### 🥇 Gold — Analytical

Contains data structured for analysis and reporting.

The planned model includes fact and dimension tables such as:

```text
fact_incidents
dim_date
dim_location
dim_crime_type
dim_population
dim_service
```

---

## 🔍 Key Analytical Questions

SafeData will investigate questions including:

1. How have reported safety-related incidents changed over time?
2. How do reported incident rates differ across geographic areas?
3. How do incident counts change when population size is considered?
4. Where are relevant support services located?
5. What patterns or changes in the available data may warrant further investigation?

---

## 🔐 Data & Ethical Considerations

Because SafeData focuses on a sensitive social issue, the project will prioritise responsible data use.

The project will:

* Prefer aggregated and publicly available data
* Avoid exposing personally identifiable information
* Distinguish reported incidents from underlying prevalence
* Document important data limitations
* Avoid making claims about individual people
* Clearly identify assumptions and methodological limitations
* Treat correlations and observed patterns as areas for investigation rather than proof of causation

---

## 🚧 Project Status

### Phase 1 — Project Setup & Architecture

**Status: ✅ Complete**

* [x] Define project objective
* [x] Define V1 scope
* [x] Create Microsoft Fabric workspace
* [x] Create Fabric Lakehouse
* [x] Design data architecture
* [x] Define Bronze/Silver/Gold layers
* [x] Design initial analytical model

### Phase 2 — Data Discovery & Acquisition

**Status: 🔜 Next**

* [ ] Identify authoritative public datasets
* [ ] Evaluate dataset quality and relevance
* [ ] Document data sources
* [ ] Acquire initial datasets
* [ ] Define source-to-target mappings

### Phase 3 — Data Ingestion

**Status: ⏳ Planned**

* [ ] Build ingestion pipelines
* [ ] Load raw data
* [ ] Validate ingestion
* [ ] Implement incremental processing where appropriate

### Phase 4 — Data Transformation

**Status: ⏳ Planned**

* [ ] Clean datasets
* [ ] Standardise fields
* [ ] Handle missing values
* [ ] Create Silver tables
* [ ] Create Gold analytical tables

### Phase 5 — Data Modelling

**Status: ⏳ Planned**

* [ ] Create dimensional model
* [ ] Build relationships
* [ ] Create semantic model
* [ ] Develop analytical measures

### Phase 6 — Analytics & Visualisation

**Status: ⏳ Planned**

* [ ] Build Power BI report
* [ ] Create geographic analysis
* [ ] Create trend analysis
* [ ] Analyse support-service distribution
* [ ] Add interactive filtering

### Phase 7 — Documentation & Portfolio

**Status: ⏳ Planned**

* [ ] Finalise architecture documentation
* [ ] Document data sources
* [ ] Document transformations
* [ ] Add screenshots
* [ ] Document lessons learned
* [ ] Publish project walkthrough

---

## 💡 Why SafeData?

Technology projects can demonstrate technical skills without necessarily addressing problems that matter to the people building them.

SafeData was created to explore the intersection of:

**Data Engineering × Analytics × AI × Social Impact**

The project is also part of a broader interest in using technology and data to contribute to work around **GBV and women's safety**.

---

## 📌 Disclaimer

SafeData is an educational and portfolio project.

The analysis does not represent official government statistics, professional research, emergency services or advice. Results are dependent on the quality, definitions, coverage and limitations of the underlying public datasets.

---

## 👩🏾‍💻 Author

**Ofentse Seko**

BSc Computer Science & Electronics
Aspiring AI / Data Engineer

---

### Project Status

**🟣 Currently building — Microsoft Fabric / DP-700**
ethodological limitations
Treat correlations and observed patterns as areas for investigation rather than proof of causation
