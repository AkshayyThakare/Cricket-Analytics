# End-to-End Cricket Analytics Data Engineering Project
<p float="left" >
  <img src="Images/Snowflake_Logo.png"  />
  <img src="Images/Cricket_Walpaper.jpeg" width="300"/>
    <img src="Images/analytics.png" width="300" />
</p>

## Overview

This repository contains the code and documentation for an end-to-end data engineering project focused on cricket analytics. The project includes the ingestion of data from JSON files, processing it through various layers, and building a consumption layer for analytics. The analytics results can be visualized in a dashboard using Snowsight.

## Project Structure

The project is organized into several layers:

1. **Land Layer**: The initial landing layer where raw data in JSON format is stored.
- Used **Json Cracker** tool to visualize our deeply nested Jsons to understand their structure.
- Created internal Stage and Json File Format to store our Json files in Snowflake.
![](Images/JsonCrackDemo.png)
2. **RAW Layer**: The raw layer stores the ingested data without any transformation. It includes tasks to load data from JSON files into Snowflake tables.

- ingested our data in a Raw Format to MATCH_RAW_TABLE Table
![](Images/MATCH_RAW_TABLE.png)

3. **Clean Layer**: The clean layer is responsible for cleaning and transforming the raw data. It includes tasks to create clean tables that are more suitable for analysis.
- Created Three Tables in Clean Schema (Layer): Concerning Player , Match_detail , Delivery Table.
![](Images/Clean_Layer.png)
4. **Consumption Layer**: The consumption layer is designed for analytics and reporting. It includes the final tables and views that are used for creating dashboards.
- Use Data Modeling to build our Datawarehouse Facts and dimensions.
![](Images/Data%20Modeling.png)


5. **Dashboard**: The dashboard layer utilizes Snowsight to visualize the analytics results. It can be accessed for insightful data analysis and reporting.
![](dashboard/My-dashboard-Snowflake.png)

5. **Automate Continuous Data Flow**: automating continuous data flow, specifically by creating automated tasks to listen to change data capture (CDC) and update data in all tables.

![](Images/AutomationDagGraph1.png)
![](Images/AutomationDagGraph2.png)

## Getting Started

### Prerequisites

- Snowflake account (Free Trial Account sufficient)
- Snowflake client (SnowSQL or Snowflake web interface)
- Access to Snowsight for dashboard creation



.

