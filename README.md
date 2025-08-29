# Flight Data Analytics Pipeline

## Overview  
This repository contains two projects developed to process and analyze real-time flight data from the **OpenSky API** using **Azure services** and **Apache Spark**.  

Both projects focus on building **scalable flight data pipelines**, but each has distinct objectives and methodologies:  

- **Project 1: Real-Time Data Pipeline with OpenSky API**  
  Focuses on **real-time ingestion, processing, storage, and visualization** of flight data using Azure services.  

- **Project 2: Flight Data Analytics and Anomaly Detection with Spark**  
  Extends the first pipeline by incorporating **advanced analytics, anomaly detection, and graph-based analysis** using Spark and Cassandra.  

---

## Objectives  

### Project 1: Real-Time Data Pipeline  
- Build a real-time processing pipeline using Azure services  
- Optimize performance & cost for continuous streaming  
- Secure data with encryption and access controls  
- Visualize real-time flight data insights  

### Project 2: Flight Data Analytics and Anomaly Detection  
- Process flight data in both streaming and batch modes  
- Detect anomalies in flight patterns with Spark MLlib  
- Analyze flight networks using GraphFrames  
- Store data scalably with Cassandra  
- Provide real-time anomaly visualizations in Power BI  

---

## Tools & Technologies  

- **OpenSky API** → Real-time flight data (positions, velocity, altitude, etc.)  
- **Azure Event Hubs** → Real-time ingestion & streaming  
- **Azure Databricks** → Apache Spark processing (Streaming, SQL, MLlib, GraphFrames)  
- **Azure Stream Analytics** → SQL-based real-time stream processing  
- **Azure Blob Storage** → Persistent data storage (both projects)  
- **Apache Cassandra** → Scalable data storage (Project 2, via Azure Cosmos DB or VMs)  
- **Power BI** → Dashboards for KPIs, maps, anomalies, and trends  
- **Security** → TLS encryption, RBAC, and diagnostic logging  

---

## Project Workflows  

### Project 1: Real-Time Data Pipeline  
1. **Data Ingestion** → Python script extracts flight data every 60s from OpenSky API → sent to Event Hubs  
2. **Data Processing** →  
   - Spark Streaming (Databricks) filters & aggregates (e.g., avg velocity, flight counts)  
   - Azure Stream Analytics applies SQL-like queries  
3. **Data Storage** → Results stored in Azure Blob Storage  
4. **Visualization** → Power BI dashboard shows KPIs & geographic maps  
5. **Optimization** → Configured Event Hub partitions & auto-scaling  
6. **Security** → TLS encryption, RBAC, and logging  

---

### Project 2: Flight Data Analytics & Anomaly Detection  
1. **Data Ingestion** → PySpark producer sends OpenSky API data to Event Hubs  
2. **Data Processing** →  
   - Spark Streaming & Batch for filtering & aggregation  
   - Spark SQL for querying trends  
   - Spark MLlib for anomaly detection (unusual velocities/altitudes)  
   - GraphFrames (GraphX) for flight network analysis  
3. **Data Storage** → Processed data stored in Cassandra & Azure Blob Storage  
4. **Visualization** → Power BI dashboard displays anomalies, flight metrics, and network insights  
5. **Security** → TLS encryption, RBAC, and logging  

