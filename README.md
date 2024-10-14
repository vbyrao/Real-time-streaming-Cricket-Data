# Real-time-streaming-Cricket-Data
It outlines the flow from CricAPI to Azure Event Hubs, processing through Azure Databricks into Bronze, Silver, and Gold layers, and finally being visualized in Power BI.
# Real-time Cricket Data Pipeline using Azure Event Hubs, Databricks, and Power BI

## Overview
This project demonstrates a real-time data pipeline using **CricAPI**, **Azure Event Hubs**, **Databricks**, and **Power BI** for visualization. The data flows through Bronze, Silver, and Gold layers to enable clean, aggregated, and real-time data processing.

### Steps:

1. **CricAPI to Event Hubs**:
   - Live cricket match data is fetched from CricAPI and sent to Azure Event Hubs using a Python script.

2. **Databricks Streaming**:
   - Databricks reads the real-time data stream from Event Hubs, processes it, and writes it into different Delta Lake layers: Bronze, Silver, and Gold.

3. **Bronze Layer**:
   - Raw event data is stored as-is in the Bronze layer.

4. **Silver Layer**:
   - Cleaned and filtered data (matches that have started or finished) is stored in the Silver layer.

5. **Gold Layer**:
   - Aggregated data for insights (average scores by series and match type) is stored in the Gold layer.

6. **Power BI Visualization**:
   - The Gold layer is connected to Power BI for real-time visualization of cricket match statistics.

## Getting Started

### Prerequisites:
- Azure Databricks workspace.
- Azure Event Hubs instance.
- Power BI Desktop.
- A CricAPI key.

### How to Run:
1. Clone the repository.
2. Replace the `<YOUR_EVENT_HUB_CONNECTION_STRING>` with your actual Event Hubs connection string.
3. Run the provided Python script to stream data from CricAPI to Event Hubs.
4. Import the Databricks notebook to process the data in Bronze, Silver, and Gold layers.
5. Connect Power BI to the Gold layer for visualization.
