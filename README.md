Women's Safety Data Intelligence Platform

SafeData is an end-to-end data engineering and analytics project built with Microsoft Fabric, focused on exploring publicly available South African gender-based violence and women's safety data.

The project aims to demonstrate how modern data platforms can transform raw public data into reliable, meaningful insights that can support further research, awareness and data-informed decision-making around women's safety.

🎯 Project Goal

SafeData explores how data engineering and analytics can be applied to a real-world social-impact problem.

The platform will ingest, clean, transform, model and visualise publicly available data to investigate:

Trends in reported safety-related incidents
Geographic patterns across South Africa
Incident rates relative to population
The distribution of relevant support services
Areas that may warrant further investigation based on available data

Important: SafeData analyses reported and publicly available data. Reported incidents should not be interpreted as representing the full prevalence of violence or the experiences of all affected individuals.

🏗️ Architecture
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
🛠️ Technologies
Microsoft Fabric
OneLake
Fabric Lakehouse
Data Pipelines
Notebooks
SQL
Semantic Models
Power BI
DAX
📊 Planned Data Sources

SafeData will work with publicly available datasets covering areas such as:

Data	Purpose
Crime / safety data	Analyse reported incidents and trends
GBV-related data	Explore available GBV statistics
Population data	Calculate population-adjusted rates
Geographic data	Standardise locations and enable geographic analysis
Support-service data	Explore the distribution of relevant services

Specific datasets and sources will be documented during the data-discovery phase.

🧱 Data Architecture

SafeData will follow a Bronze → Silver → Gold data architecture.

🥉 Bronze — Raw

Contains data as received from the original source with minimal modification.

Purpose: preserve the original source data and provide traceability.

🥈 Silver — Clean

Contains cleaned and standardised data.

Typical transformations may include:

Data-type corrections
Missing-value handling
Duplicate removal
Standardisation of geographic names
Date standardisation
Category standardisation
Data validation
🥇 Gold — Analytical

Contains data structured for analysis and reporting.

The planned model includes fact and dimension tables such as:

fact_incidents
dim_date
dim_location
dim_crime_type
dim_population
dim_service
🔍 Key Analytical Questions

SafeData will investigate questions including:

How have reported safety-related incidents changed over time?
How do reported incident rates differ across geographic areas?
How do incident counts change when population size is considered?
Where are relevant support services located?
What patterns or changes in the available data may warrant further investigation?
🔐 Data & Ethical Considerations

Because SafeData focuses on a sensitive social issue, the project will prioritise responsible data use.

The project will:

Prefer aggregated and publicly available data
Avoid exposing personally identifiable information
Distinguish reported incidents from underlying prevalence
Document important data limitations
Avoid making claims about individual people
Clearly identify assumptions and methodological limitations
Treat correlations and observed patterns as areas for investigation rather than proof of causation
