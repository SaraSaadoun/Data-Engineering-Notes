## 📂 Database  
- Stores **structured** data (rows & columns).  
- Optimized for **OLTP (Online Transaction Processing)**, handling real-time transactional queries.  
- Supports **ACID properties** (Atomicity, Consistency, Isolation, Durability) for data integrity.  

## 🏢 Data Warehouse (DWH)  
- Central repository for **integrated structured data** from multiple sources (DBs, log files).  
- Uses **ETL** (Extract, Transform, Load) processes.  
- **Complex to modify**; requires careful **upstream/downstream planning**.  
- Typically **>100GB**.  
- Optimized for **OLAP (Online Analytical Processing)**, designed for analytical queries and reporting.  


## 📊 Data Mart  
- **Subset** of a DWH, focused on a **single subject area**.  
- A relational database for analysis.
- Few input data sources.  
- Typically **<100GB**.  


## 🌊 Data Lake  
- Stores **both structured & unstructured** data (e.g., video, audio, logs).  
- Entire organization store of data. 
- Purpose to store data may **not** be known as data may be stored **without an immediate purpose** but can be used later.  
- **More flexible** for changes than a DWH.  

