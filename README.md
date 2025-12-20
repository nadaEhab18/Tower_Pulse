# Tower_Pulse
Streaming Data System for Cell Towers Operational & Maintenance Coverage

Tower Pulse is an end-to-end data engineering project designed to monitor, analyze, and visualize telecom cell tower performance and maintenance operations using both batch analytics and real-time streaming.

This project was developed as a Graduation Project for the ITI – Data Engineering Track and demonstrates the design and implementation of a modern data engineering architecture using industry-standard tools and best practices.

📌 Project Objectives

The main goals of Tower Pulse are to:

Monitor cell tower performance and network health

Analyze the impact of maintenance activities on service quality

Detect coverage gaps and high-risk towers

Provide historical insights and real-time operational visibility

Build a scalable, analytics-ready data platform

🏗️ Architecture Overview

Tower Pulse follows a Modern Data Stack architecture and is divided into two main layers:

1️⃣ Batch Layer (Historical Analytics)

Handles historical telecom data and supports strategic analysis and reporting.

Flow:

Python → CSV → Snowflake → dbt → Data Warehouse → Power BI


Key Responsibilities:

Data ingestion and validation

Data cleaning and standardization

Dimensional modeling (Star Schema)

Analytics-ready data for BI tools

2️⃣ Streaming Layer (Real-Time Monitoring)

Processes live events to enable monitoring and alerting.

Flow:

API Producer → Kafka → Spark Streaming → Cassandra → Grafana


Key Responsibilities:

Real-time data ingestion

Streaming transformations and aggregations

Low-latency storage

Live dashboards and alerts

📦 Batch Layer Details
🔹 Data Ingestion

Telecom data is preprocessed using Python

Exported as CSV files

Loaded into Snowflake as staging tables

🔹 Data Transformation

dbt is used for:

Data transformations

Business logic implementation

Data quality checks

Documentation and lineage

🔹 Medallion Architecture

Bronze: Raw staging data

Silver: Cleaned and standardized data

Gold: Analytics-ready Star Schema

📐 Data Warehouse Design

The data warehouse is modeled using a Star Schema optimized for analytical workloads.

⭐ Fact Table

FACT_TOWER_OPS_MAINTENANCE

Represents tower operational and maintenance events

Granularity:
Tower × Maintenance Event × Date

Includes key measures such as:

Drop rate

Downtime hours

Quality of Experience (QoE)

Latency

Coverage gap

Signal quality

Anomaly indicators

📊 Dimension Tables
Dimension	Description
DIM_TOWER	Tower metadata and radio information
DIM_LOCATION	Geographic attributes and location analysis
DIM_NETWORK	Mobile network and operator details
DIM_DATE	Time-based analysis (created, updated, maintenance dates)
DIM_MAINTENANCE_TYPE	Maintenance classification (preventive, predictive, emergency)

This design ensures:

High query performance

Clean analytics

Easy extensibility

⚡ Streaming Layer Details

API Producer simulates real-time telecom events

Apache Kafka handles event streaming

Apache Spark Streaming processes data in real time

Cassandra stores time-series data with low latency

Grafana provides live dashboards and alerting

📊 Analytics & Dashboards
Power BI (Batch Analytics)

Network health overview

Drop rate & QoE trends

Maintenance cost analysis

High-risk tower identification

Geographic coverage analysis

Grafana (Real-Time Monitoring)

Live performance metrics

Tower status monitoring

Real-time anomaly detection

🛠 Tools & Technologies

Batch & Analytics

Python

Snowflake

dbt

SQL

Power BI

Streaming

Apache Kafka

Apache Spark

Cassandra

Grafana

Orchestration & DevOps

Apache Airflow

Docker

📈 Key Insights

Identified high-risk towers with extreme single-event downtime

Analyzed drop rate vs Quality of Experience trends

Evaluated preventive vs emergency maintenance effectiveness

Detected geographic coverage gaps

Linked maintenance cost directly to network performance

🎓 Learning Outcomes

This project provided hands-on experience in:

Data Engineering & Analytics Engineering

Batch and Streaming Data Pipelines

Dimensional Modeling (Star Schema)

Telecom Network Analytics

Building production-ready data systems
