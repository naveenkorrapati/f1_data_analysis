# Formula-1 Data Engineering and Analytics Platform
Overview

This project presents an end-to-end cloud-based data engineering solution designed to ingest, process, and analyze Formula-1 racing data at scale. Using Azure Data Lake Storage Gen2, Azure Data Factory, Azure Databricks, and Delta Lake, the platform automates data collection from external APIs and transforms raw datasets into clean, analytics-ready tables following the medallion architecture. The curated data powers advanced analytics, machine learning workflows, and interactive visual dashboards that reveal insights into driver performance, team dominance, race patterns, and long-term historical trends in Formula-1.

Key Features

• Automated ingestion of Formula-1 datasets from external APIs into ADLS Gen2 <br>
• Medallion architecture implementation (Bronze, Silver, Gold layers) <br>
• Delta Lake storage for ACID transactions, schema enforcement, and time travel <br>
• Scalable transformations using PySpark and Databricks notebooks<br>
• Support for incremental and historical reprocessing<br>
• Power BI dashboards for visualizing dominant drivers, constructors, and race statistics<br>
• SharePoint-triggered ingestion pipeline for ad-hoc data updates<br>
• Unified lakehouse design enabling analytics and ML workloads on the same data<br>

Architecture

The platform is built on a modern data lakehouse architecture.
Bronze Layer stores raw API data exactly as received.
Silver Layer applies cleaning, normalization, deduplication, and schema refinement.
Gold Layer computes business-friendly aggregates such as yearly standings, team performance metrics, race summaries, and driver dominance trends.
The curated tables are consumed by analytics teams via SQL, Databricks notebooks, or Power BI dashboards. Delta Lake ensures reliability, consistency, and the ability to time-travel or restore historical versions of the data.

Data Model

The project includes structured Delta tables for the following domains:<br>
• Race information (seasons, races, circuits)<br>
• Participants (drivers, constructors)<br>
• Performance metrics (results, qualifying, pit stops, lap times)<br>
• Seasonal standings (driver standings, constructor standings)<br>
• Supporting metadata (status codes)<br>

Foreign-key relationships follow the natural structure of Formula-1 competition, enabling efficient joins and analysis across tables.<br>

Dashboards

Interactive visual reports are built in Power BI to highlight:<br>
• Dominant drivers across decades<br>
• Constructor performance and team dominance trends<br>
• Yearly points progression<br>
• Historical competitiveness patterns<br>
These dashboards provide an intuitive view of how Formula-1 racing has evolved over time.<br>

Technologies Used

• Azure Data Factory<br>
• Azure Data Lake Storage Gen2<br>
• Azure Databricks<br>
• PySpark / Spark SQL<br>
• Delta Lake<br>
• Power BI<br>
• SharePoint (ad-hoc ingestion triggers)<br>
