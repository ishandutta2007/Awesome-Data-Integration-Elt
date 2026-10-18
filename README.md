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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Fivetran](https://www.fivetran.com/)**  

  **Fully managed ELT platform with 700+ pre-built connectors** . **Pricing**: **Monthly Active Rows (MAR)** model—costs scale with data volume, not compute time . **Free plan**: limited MAR and 5,000 monthly model runs for transformations . **Standard plan**: connections generating 1–1M MAR incur a **minimum $5 per connection** charge (effective January 2026) . **Business Critical** adds cloud region selection for data residency . **Note**: As of January 2026, **deletes and history-mode repeated updates count toward paid MAR**—a row synced multiple times in a month is only charged once, but a deleted row now consumes MAR where it previously did not . **The managed standard** for teams wanting zero-maintenance replication .



- **[Airbyte](https://airbyte.com/)**  

  **Open-source data integration platform with a managed cloud option** . **Cloud pricing**: **Standard** starts at **$20/month with 5 credits** ($5 per extra credit) . **Plus** starts at **$189/month for 40 credits**—recommended once you consume **40+ credits monthly**, adding SSO, 15-minute syncs, and a 24-hour support SLA . **Credit metering varies by source type**: API sources consume **6 credits per million rows**; databases and files consume **4 credits per gigabyte** . **Pro and Enterprise Flex** shift to **capacity-based pricing** via **Data Workers**—roughly **0.5 workers per running database sync** or **0.2 per API sync**, stabilizing costs during volume spikes . **Enterprise Flex** supports **in-boundary and hybrid deployment** for data sovereignty . **The most flexible connector ecosystem** with **700+ connectors** and a 30-day trial with 400 credits .



- **[Stitch (Talend)](https://www.stitchdata.com/)**  

  **Cloud-based ELT built on the Singer framework** . **Pricing**: **Standard** from **$100/month for 5–300 million rows** . **Advanced** at **$1,500/month** (billed annually) for **100 million rows** . **Premium** at **$3,000/month** (billed annually) for **1 billion rows** . **14-day free trial** available . **SOC 2 compliance on all plans**; HIPAA via BAA signing . **Limitations**: **no real-time replication**—sync frequencies range from minutes to hours . **Now part of Qlik Talend Cloud** .



- **[Matillion](https://www.matillion.com/)**  

  **Cloud-native ELT with strong transformation capabilities** . **Pricing**: **Data Processing Units (DPUs)** model—costs scale with compute consumed, not rows . **Typical basic plans**: **$1,000–$3,000+ per month** . **Multi-year agreements** typically unlock **15–25% discounts** . **Negotiation window**: **late January** (fiscal year end) and **quarter ends** offer the strongest leverage . **Best for**: organizations needing **robust transformation** alongside extraction—**Matillion vs Fivetran**: Fivetran focuses on replication with minimal transformation; Matillion offers more transformation depth .



- **[Hevo Data](https://hevodata.com/)**  

  **No-code ELT platform with 150+ connectors** . **Pricing**: **Free plan** with **1 million events/month** (limited connectors, 5 users) . **Starter** from **$299/month** (or **$265/month annual**) for **5 million events**, 10 users, 150+ connectors, and dbt integration . **Professional** from **$849/month** (or **$750/month annual**) for **20 million events**, unlimited users, and pipeline automation APIs . **Business Critical** adds streaming pipelines, RBAC, SSO, and VPC peering . **Each inserted, updated, or deleted record counts as one event** . **14-day free trial** available .



- **[Meltano](https://meltano.com/)**  

  **Declarative data integration and ELT framework** . **Cloud pricing**: **Compute-hour model**—costs scale with **pipeline runtime**, not data volume . **Starter** includes **200 compute hours/month**, 25 workspaces, unlimited users, and 600+ connectors . **Growth** at **2,000 compute hours** adds 100 workspaces and **8 hours/month of engineering support** . **Scale** at **5,000 compute hours** adds unlimited workspaces and **15 hours/month of engineering** . **Enterprise** is custom with custom connectors and SLAs . **Key claim**: **40–80% cheaper than row-based pricing** for high-frequency database or bulk connectors—**data volume has no direct cost impact**, so backfills don't trigger surprise invoices . **The code-first choice**—pipelines live in Git with CI/CD .



- **[AWS Glue](https://aws.amazon.com/glue/)**  

  **Fully managed serverless ETL service** . **Pricing**: **$0.44 per DPU-hour** (billed per second, 1-minute minimum for Glue 2.0+) . A DPU provides **4 vCPUs and 16 GB memory** . **Default allocation**: **10 DPUs** for Spark jobs, **2 DPUs** for streaming jobs . **Data Catalog**: **$1 per 100,000 objects** and **$1 per million requests** . **Crawler runtime**: billed per DPU-hour with a **10-minute minimum** per crawl . **DataBrew**: **$0.48 per 30-minute interactive session** and **$0.46 per node-hour** for cleaning jobs . **The AWS-native standard** for serverless Spark ETL .



- **[Google Cloud Dataflow](https://cloud.google.com/dataflow)**  

  **Fully managed stream and batch data processing** . **Pricing**: **per-vCPU and per-GB memory** for worker resources, plus charges for **Dataflow Shuffle** (batch) or **Streaming Engine** (streaming) . **FlexRS (Flexible Resource Scheduling)** offers **up to 40% discount** on batch jobs—**trade-off**: Google can delay execution **up to six hours** and use preemptible VMs . **Cost optimization**: **Dataflow Shuffle** offloads shuffle operations from workers, enabling **smaller machine types** and **faster job completion** . **Streaming Engine** offloads state management, reducing worker requirements . **The GCP-native choice** for unified batch and stream processing .



- **[Informatica](https://www.informatica.com/)**  

  **Enterprise data integration and management platform** . **Pricing**: **quote-only** with **IPU (Informatica Processing Unit)** consumption model . **IPUs are driven by "scalers"**: Secure Agent runtime, CDI-e elastic compute, data mass ingestion volume, and workload-specific metrics . **Premium connectors** (SAP, Salesforce, mainframe) can add **$25,000–$100,000 annually** . **Premium support** up to **$60,000 annually** . **PowerCenter five-year TCO** reportedly ranges **$3.6M to $15M+** for mid-to-large deployments . **Best for**: large enterprises with **complex legacy integration** and **deep regulatory compliance** needs .



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
