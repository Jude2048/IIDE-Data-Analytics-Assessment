# IIDE Data Analytics Assessment: Placement Operations Pipeline

## Project Overview
This repository contains my submission for the IIDE Data Analyst skill test. The objective was to ingest a denormalized dataset of campus placements, engineer a scalable relational database architecture and develop an executive-level dashboard to identify pipeline bottlenecks and drive strategic decisions.

## Tech Stack
* **Data Ingestion & ETL:** Power Query (M Code)
* **Data Modeling:** Dimensional Modeling (Star Schema / 3NF)
* **Data Visualization & Analytics:** Microsoft Power BI (DAX)

## Data Architecture & Relational Schema
The provided dataset consisted of denormalized, flat data. Loading this directly into a BI tool violates normalization principles and harms query performance. 

To ensure a scalable and optimized system as per the job description, I engineered a **Star Schema** using Power Query. I isolated unique dimensions (`Dim_Candidate`, `Dim_Job`) to act as the single source of truth, and separated transactional events (`Fact_Application`, `Fact_Interview`). 

![Star Schema]()

## Executive Dashboard
The dashboard was structured specifically for executive scannability, anchoring high-level KPIs at the top, followed by pipeline bottleneck analysis and dimensional drill-downs.

![Dashboard Preview]()

## Key Executive Insights
Based on the dashboard analytics, here are the strategic recommendations for the Core Management Team:
1. **Pipeline Bottleneck:** The application stage visual highlights a severe drop-off immediately following the 'Submissions' stage. 
**Recommendation:** Audit the initial eligibility criteria. Either corporate partners are setting unrealistic baseline expectations, or candidates are applying to roles they are fundamentally unqualified for.
2. **Corporate Demand Alignment:** The 'Total Applications by Posting Title' chart reveals a massive skew toward Social Media and Digital Marketing roles. **Recommendation:** Adjust procurement strategy to source more digital marketing partners to satisfy this overwhelming student demand.
3. **Cohort Imbalance:** 91.43% of active placement candidates originate from the 'Professional Certification' cohort. 
**Recommendation:** Investigate the Advanced Certification batch to determine if the lack of applications is due to placement readiness, job misalignment, or disengagement.

## How to View the Interactive Dashboard
Since Power BI Service requires an organizational email for web-publishing, the fully interactive `.pbix` file is included in this repository. 
1. Download `IIDEPlacementAnalytics.pbix` from the files above.
2. Open using **Power BI Desktop**.
3. Alternatively, a static overview can be viewed instantly by opening the `IIDEPlacementAnalytics.pdf` included in this repository.
