🔄 Live Google Sheets to Excel Hybrid Pipeline & Data Mart

An enterprise-grade, 5-sheet hybrid data pipeline connecting live cloud web form ingestion (Google Sheets) to local analytical workstations (Microsoft Excel) via Power Query, complete with ETL normalization, data marts, and automated error auditing.
 
🏗️ End-to-End Pipeline Architecture

The workbook is structured into 5 interlinked functional layers:

Pipeline_Control_Center (Sheet 1): Executive command dashboard featuring live sync status indicators (🟢 Pipeline Active), total submission counters, and regional filter controls.

Staging_WebForm_Data (Sheet 2): The raw cloud ingestion warehouse capturing unformatted web form entries, timestamps, submitter details, and pipeline values.

Transformed_PowerQuery_Staging (Sheet 3): The automated ETL cleaning engine utilizing fault-tolerant IFERROR functions, string normalization, and data sanitization.

Aggregated_BI_DataMart (Sheet 4): The backend analytical calculation hub computing regional volumes, total pipeline values, average deal sizes, and conversion success rates.

Sync_Audit_Log (Sheet 5): The system health and forensic exception tracker logging sync statuses, error codes, and automated resolution workflows.

⚙️ How the Pipeline Flows

[Cloud Web Form / Google Sheets] 
       │ (Live Ingestion)
       ▼
[Sheet 2: Staging Raw Data] 
       │ (ETL Cleaning & Normalization)
       ▼
[Sheet 3: Transformed Staging] ──► [Sheet 5: Sync Audit & Error Log]
       │ (Aggregation & Calculations)
       ▼
[Sheet 4: BI Data Mart] ──► [Sheet 1: Executive Control Dashboard]
