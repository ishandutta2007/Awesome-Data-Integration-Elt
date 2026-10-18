# Awesome-Data-Integration-Elt

## Top Data Integration & ELT Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Connector Breadth, Transform Pushdown & Declarative Pipeline Orchestration*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Integration & ELT**. These tools enable organizations to extract data from SaaS applications, databases, and files; load it into warehouses and lakes; and transform it in place—from fully managed platforms with hundreds of pre-built connectors to code-first frameworks that treat pipelines as version-controlled artifacts.



**Examples** include Fivetran, Airbyte, Talend, Stitch, Matillion, Hevo Data, Meltano, AWS Glue, Google Cloud Dataflow, and Informatica (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, declarative pipeline configuration, and open connector ecosystems—ideal for data engineers, analytics teams, and organizations seeking transparent, vendor-independent data integration.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data integration market is estimated between **$14.3 billion and $21.5 billion in 2026**, growing at a CAGR of ~12–14% toward over $50 billion by the mid-2030s, fueled by enterprise migration to cloud data platforms and generative AI data preparation workloads. The sector is **moderately concentrated at the top but fragmented overall** rather than a winner-take-all market: hyperscalers (AWS, Google Cloud) and legacy giants (Informatica, Qlik) control large enterprise workloads, while modern ELT disruptors (Fivetran, Airbyte) and code-first open ecosystems capture fast-evolving multi-cloud pipelines where vendor lock-in is resisted.

## SaaS/Hosted Platforms

| Product | Company Size (Valuation / Revenue) | Pricing | Free Tier / Trial Limits | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Google Cloud Dataflow](https://cloud.google.com/dataflow)** | ~$4.2T Market Cap / ~$446B TTM Rev (Alphabet) | Pay-per-vCPU & memory ($0.056/vCPU-hr, $0.003557/GB-hr on US-Central1 batch); FlexRS offers up to 40% discount | **90-day free trial with $300 cloud credits** (capped at 8 concurrent worker vCPUs; no permanent Always-Free tier for Dataflow compute) | Fully managed stream and batch processing service based on Apache Beam. Auto-scaling worker infrastructure with Dataflow Shuffle and Streaming Engine. |
| **[AWS Glue](https://aws.amazon.com/glue/)** | ~$2.8T Market Cap / ~$776B TTM Rev (Amazon) | $0.44 per DPU-hour (1 DPU = 4 vCPU, 16 GB RAM; 1-min min for Glue 2.0+); Catalog $1/100K objects and $1/1M requests | **Always-Free tier**: 1M free metadata objects stored & 1M free catalog requests/month in AWS Glue Data Catalog (DPU compute for ETL jobs has no free tier and is billed from min 1) | Serverless Spark-based data preparation and ETL service with automatic schema discovery via crawlers and central Data Catalog. |
| **[Stitch (Talend)](https://www.stitchdata.com/)** | ~$10B Valuation / ~$1.5B ARR (Qlik) | Standard plan starts at **$100/month** (for 5M rows/month; scales to $1,500/mo for 100M rows and $3,000/mo for 1B rows) | **14-day free trial** with unlimited row replication and full connector access (plus 7-day initial grace period with unlimited rows for each new integration added) | Cloud-based ELT platform built on the Singer framework. Simple setup and broad connector catalog; now part of Qlik Talend Cloud. |
| **[Informatica](https://www.informatica.com/)** | ~$7.6B Market Cap / ~$1.68B TTM Rev (NYSE: INFA) | IPU consumption starting custom quotes (typical enterprise contracts start at tens of thousands/year; premium connectors $25k–$100k/yr) | **Always-Free tier**: 25 Informatica Processing Units (IPUs)/month on Cloud Data Integration (deleted if unused for 30 consecutive days); plus a **30-day full platform free trial** | Enterprise-grade cloud data integration, data management, and governance platform (IDMC) designed for complex regulatory compliance. |
| **[Fivetran](https://www.fivetran.com/)** | ~$5.6B Valuation / ~$300M+ ARR | Pay-as-you-go based on Monthly Active Rows (MAR) starting at **~$500/1M MAR**; minimum **$5/month per connection** (1–1M MAR); annual commits start at ~$12,000/yr | **Always-Free tier**: Up to **500,000 MAR/month**, 3,500 activation MAR, and 5,000 monthly transformation model runs (soft limit; upgraded/paused if exceeded 2 consecutive months) | Industry-standard managed ELT service offering 700+ automated pre-built connectors with automatic schema drift handling. |
| **[Airbyte](https://airbyte.com/)** | ~$1.5B Valuation / ~$20M+ ARR | Standard plan starts at **$20/month** (includes 5 credits; $5/credit thereafter; API sources: 6 credits/1M rows, DB/files: 4 credits/GB); Plus starts at **$189/month** (40 credits) | **30-day free trial with 400 credits**; open-source self-hosted version (Airbyte OSS) is permanently free | Highly customizable integration platform with 700+ connectors, CDK for custom connectors, and hybrid/cloud deployment models. |
| **[Matillion](https://www.matillion.com/)** | ~$1.5B Valuation / ~$75M–$100M ARR | Basic plans start at **$1,000–$3,000/month** based on Data Processing Units (DPU compute consumption model) | **14-day free trial with 500 platform credits** and unrestricted access across the Data Productivity Cloud | Cloud-native data transformation and integration platform focused on warehouse/lake pushdown transformations. |
| **[Hevo Data](https://hevodata.com/)** | ~$100M–$250M Valuation / ~$30M–$47M ARR | Starter plan starts at **$299/month** ($265/mo billed annually) for up to 5M events/month; Professional starts at **$849/month** | **Always-Free tier**: Up to **1,000,000 events/month** (with limited connectors and 5 user seats); plus a **14-day full-feature free trial** | No-code automated data pipeline platform with 150+ source connectors, automated schema management, and built-in reverse ETL. |
| **[Meltano](https://meltano.com/)** | Seed-stage ($12.4M raised) / GitLab spin-out | Meltano Cloud Starter plan pricing starts with custom quote based on compute hours (e.g. 200 compute-hr tier; pipelines charged by runtime not row volume) | **Open-source framework is 100% free indefinitely**; Meltano Cloud offers demo-based trial access upon request (typically 14 to 30 days upon sales consultation) | Developer-centric, GitOps-driven data integration framework built around Singer taps/targets and dbt pipelines-as-code orchestration. |





## Open-Source GitHub Projects



- **[Meltano](https://github.com/meltano/meltano)**  

  **Declarative data integration and ELT framework** (MIT) — **the code-first, Git-native choice** . **Built on the Singer standard** with **600+ connectors** . **Pipelines live in version control**—changes are reviewed, tested, and promoted through CI/CD rather than clicked through a UI with no audit trail . **`meltano.yml` defines the full stack**: extractors, loaders, transformations (dbt), and schedules . **`meltano run` executes pipelines**; **`meltano schedule` configures orchestration** . **Supports dbt transformations natively** . **The reference implementation for declarative ELT** — **choose when you want pipelines as code, not as vendor configuration** .



- **[Singer](https://github.com/singer-io)**  

  **Open-source standard for writing data extraction and loading scripts** (Apache-2.0) — **the protocol behind Meltano and Stitch** . **Taps (extractors)** output JSON to stdout; **targets (loaders)** read JSON from stdin and write to destinations . **The simplest connector model**—**no framework to learn, just a script that speaks the protocol** . **Community-maintained taps and targets** cover a huge range of sources and destinations . **The foundation for the open ELT ecosystem** .



- **[dlt (data load tool)](https://github.com/dlt-hub/dlt)**  

  **Python library for building data pipelines** (Apache-2.0) — **the developer-friendly ingestion framework** . **Schema inference engine** automatically detects types and flattens nested JSON . **AI-powered pipeline generation** using LLMs to scaffold extraction code . **Moves data to lakehouses, warehouses, or vector databases** . **`pip install dlt`** and start extracting—**the fastest path from Python script to production pipeline** .



- **[Airbyte OSS](https://github.com/airbytehq/airbyte)**  

  **The leading open-source ELT platform** (Elastic-2.0 for core) — **600+ pre-built connectors** and **22,000+ GitHub stars** . **Self-hosted via Docker or Kubernetes** . **Connector Development Kit (CDK)** for building custom connectors . **The most widely adopted open-source alternative to Fivetran** — **budget engineer time honestly**: Docker/Kubernetes management, upgrades, scaling, and monitoring are real ongoing work . **Cloud Standard at $20/month** is often the better kind of cheap for small teams without platform engineers .



- **[Airbyte Cloud](https://airbyte.com/)**  

  See above. **Cloud plans** start at **$20/month (Standard)** and **$189/month (Plus)** with credit-based billing .



### Additional Strong Open-Source Options



- **[Apache NiFi](https://github.com/apache/nifi)** — Flow-based programming platform (Apache-2.0) for visual data pipelines. **The most mature open-source data flow tool**—data provenance, prioritization, and routing.

- **[Apache Airflow](https://github.com/apache/airflow)** — Workflow orchestration platform (Apache-2.0). **The standard for DAG-based pipeline scheduling**—not a data movement tool itself, but the orchestrator that runs ELT jobs.

- **[Kestra](https://github.com/kestra-io/kestra)** — Declarative orchestration platform (Apache-2.0) unifying data, AI, and infrastructure workflows. **YAML-based, language-agnostic**.

- **[Bruin](https://github.com/bruin-data/bruin)** — Multi-language data pipelines (SQL + Python) with built-in lineage (open-source). **The end-to-end data pipeline tool**.

- **[Sling CLI](https://github.com/slingdata-io/sling-cli)** — CLI for extracting data from source databases/storage and loading to destinations (open-source) . **Lightweight and scriptable**.

- **[Artie Transfer](https://github.com/artie-labs/transfer)** — Database replication with CDC (open-source) . **Real-time streaming** to warehouses.

- Community **n8n** workflows for ELT pipeline orchestration and data quality alerting.



**Frameworks for building custom systems**: Combine **Meltano** for declarative pipeline configuration with **dlt** for Python-native ingestion, **Airbyte OSS** for broad connector coverage, **dbt** for in-warehouse transformation, and **Apache Airflow** or **Kestra** for orchestration—creating a fully self-hosted, enterprise-grade ELT stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data integration platforms handling enterprise data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls and audit logging.

- **Pricing models drive behavior.** **Fivetran's MAR model** charges for **every changed row**—as of January 2026, **deletes and history-mode repeated updates count toward paid MAR** . **Meltano's compute-hour model** charges for **pipeline runtime**, not data volume—**backfills don't trigger surprise invoices** . **Airbyte's credit model** meters **API rows at 6 credits/million and database GB at 4 credits/GB** . **Model your expected volume before committing**—the cheapest headline plan can become the most expensive at scale .

- **The "free" open-source option has real costs.** **Airbyte OSS** requires **Docker/Kubernetes management, upgrades, scaling, and monitoring**—for a team without platform engineers, **Cloud Standard at $20/month is the better kind of cheap** . **Meltano Open** is free but **Cloud is built for production teams** with managed infrastructure and engineering support .

- **Declarative vs. managed is a philosophical choice.** **Meltano** treats pipelines as **version-controlled code**—changes go through CI/CD, not a UI . **Fivetran** treats pipelines as **managed configuration**—zero maintenance, but no Git-native audit trail . **Choose based on whether you want to engineer your pipelines or rent them.**

- **Stitch has a real-time limitation.** **No real-time replication on any tier**—sync frequencies range from minutes to hours . **If you need CDC or streaming**, look at **Artie** or **Airbyte's streaming options** .

- **Matillion is the transformation-heavy option.** **Fivetran focuses on replication with minimal transformation**; **Matillion offers more transformation depth** . **dbt Cloud** handles **SQL transformations in the warehouse** but doesn't extract or load . **Many teams combine dbt with an extraction tool rather than choosing one platform for both.**

- Self-hosted open-source solutions require proper infrastructure management, connector maintenance, and ongoing monitoring. **Connectors break when source APIs change**—budget for maintenance regardless of platform choice.



---



**Made for data engineers, analytics teams, and organizations building transparent data integration solutions.**  

Let's make Data Integration & ELT more open, data-driven, and declarative.
