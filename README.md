# 🚀 Tower Pulse  
### Streaming Data System for Cell Towers Operations & Maintenance

**Tower Pulse** is an end-to-end **Data Engineering graduation project** developed as part of the  
🎓 **ITI – Data Engineering Track**.

The project delivers a **modern, scalable data platform** that combines **batch analytics** and **real-time streaming** to monitor, analyze, and visualize telecom **cell tower performance and maintenance operations**.

---

## 🌟 Why Tower Pulse?

Telecom networks generate massive volumes of data every second.  
Tower Pulse was built to answer critical business and operational questions such as:

- Which towers are at **high operational risk**?
- How does **maintenance impact network quality**?
- Where are the **coverage gaps**?
- What is happening **right now** across the network?

---

## 🎯 Project Objectives

Tower Pulse aims to:

- 📡 Monitor cell tower performance and network health  
- 🛠 Analyze the impact of maintenance activities on service quality  
- ⚠️ Detect high-risk towers and anomalies  
- 🗺 Identify geographic coverage gaps  
- 📊 Provide both historical insights and real-time visibility  
- 🏗 Build a scalable, analytics-ready data platform  

---

## 🏗️ Architecture Overview

Tower Pulse follows a **Modern Data Stack** and is built around **two core layers**:

---

### 1️⃣ Batch Layer – Historical Analytics

Designed for deep analysis, reporting, and business insights.

**Data Flow**
Python → CSV → Snowflake → dbt → Data Warehouse → Power BI


**Responsibilities**

- Data ingestion & validation  
- Data cleaning and standardization  
- Dimensional modeling (Star Schema)  
- Analytics-ready datasets for BI  

---

### 2️⃣ Streaming Layer – Real-Time Monitoring

Designed for low-latency processing and live observability.

**Data Flow**
API Producer → Kafka → Spark Streaming → Cassandra → Grafana


**Responsibilities**

- Real-time data ingestion  
- Streaming transformations & aggregations  
- Fast time-series storage  
- Live dashboards and alerting  

---

## 📦 Batch Layer Details

### 🔹 Data Ingestion
- Telecom data is preprocessed using **Python**
- Exported as **CSV files**
- Loaded into **Snowflake** staging tables

### 🔹 Data Transformation
Implemented using **dbt**:
- Business logic transformations  
- Data quality tests  
- Documentation & lineage  
- Reusable, modular SQL models  

### 🔹 Medallion Architecture
- **Bronze**: Raw staging data  
- **Silver**: Cleaned & standardized data  
- **Gold**: Analytics-ready Star Schema  

---

## 📐 Data Warehouse Design

The warehouse is modeled using a **Star Schema** optimized for analytical workloads.

### ⭐ Fact Table

**FACT_TOWER_OPS_MAINTENANCE**

**Granularity**
Tower × Maintenance Event × Date


**Key Measures**
- Drop Rate  
- Downtime Hours  
- Quality of Experience (QoE)  
- Latency  
- Coverage Gap  
- Signal Quality  
- Anomaly Indicators  

---

### 📊 Dimension Tables

| Dimension | Description |
|--------|------------|
| **DIM_TOWER** | Tower metadata and radio technology |
| **DIM_LOCATION** | Geographic attributes and location analytics |
| **DIM_NETWORK** | Network operator and mobile technology |
| **DIM_DATE** | Time-based analysis (events & maintenance dates) |
| **DIM_MAINTENANCE_TYPE** | Preventive, predictive, and emergency maintenance |

✅ This design ensures:
- High query performance  
- Clean and understandable analytics  
- Easy future extensibility  

---

## ⚡ Streaming Layer Details

- **API Producer** simulates live telecom events  
- **Apache Kafka** handles event streaming  
- **Apache Spark Streaming** processes data in real time  
- **Apache Cassandra** stores low-latency time-series data  
- **Grafana** visualizes metrics and triggers alerts  

---

## 📊 Analytics & Dashboards

### 🔹 Power BI (Batch Analytics)
- Network health overview  
- Drop rate & QoE trends  
- Maintenance cost analysis  
- High-risk tower identification  
- Geographic coverage analysis  

### 🔹 Grafana (Real-Time Monitoring)
- Live performance metrics  
- Tower operational status  
- Real-time anomaly detection  

---

## 🛠 Tools & Technologies

### 🧱 Batch & Analytics
- Python  
- Snowflake  
- dbt  
- SQL  
- Power BI  

### ⚡ Streaming
- Apache Kafka  
- Apache Spark Streaming  
- Apache Cassandra  
- Grafana  

### ⚙️ Orchestration & DevOps
- Apache Airflow  
- Docker  

---

## 📈 Key Insights

- Identified **high-risk towers** with extreme downtime in single events  
- Analyzed **drop rate vs QoE** relationships  
- Evaluated **preventive vs emergency maintenance effectiveness**  
- Detected **geographic coverage gaps**  
- Linked **maintenance cost directly to network performance**  

---

## 🎓 Learning Outcomes

This project provided hands-on experience in:

- Data Engineering & Analytics Engineering  
- Batch and Streaming Data Pipelines  
- Dimensional Modeling (Star Schema)  
- Telecom Network Analytics  
- Building production-ready data systems  

---

## 🏁 Final Note

**Tower Pulse** represents a complete, real-world data engineering solution that bridges  
📊 analytics, ⚡ real-time streaming, and 🏗 scalable system design.

Built with industry-standard tools and best practices, it reflects the skills and mindset required for modern data engineering roles.

