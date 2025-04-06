# The Modern Data Stack Diagram (ELT)



```mermaid   
Data Sources
     │
     ▼
Data Ingestion
  ├─ Airbyte
  └─ Apache NiFi
     │
     ▼
Cloud DWH
  ├─ Snowflake
  ├─ BigQuery
  └─ Redshift
     │
     ▼
Transformation
  └─ dbt
     │
     ▼
BI & Analytics
  ├─ Power BI
  ├─ Tableau
  └─ Clicksense
  
```