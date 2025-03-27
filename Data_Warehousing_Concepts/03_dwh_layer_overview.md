# 🏛️ Data Warehouse (DWH) Layer Overview  

## 1️⃣ Data Sources  
- Various sources, including:  
  - **Transactional Databases**  
  - **Log Files**  
  - **Spreadsheets** 
  - (May contain unstructured data)  

## 2️⃣ Data Staging  
- Includes **ETL process** and **staging database** (temporary storage).  
- **ETL Breakdown:**  
  - **E - Extract:** Retrieve raw data.  
  - **T - Transform:** Apply business rules (cleaning, mathematical operations).  
  - **L - Load:** Store transformed data.  
- **Output:** Data is structured and ready for batch or real-time storage.  

## 3️⃣ Data Storage  
- Can follow different architectures:  
  - **DWH → Data Marts** (Centralized approach).  
  - **Data Marts → DWH** (Decentralized approach).  

## 4️⃣ Data Presentation  
- Used for **analytics, reporting, and querying**.  
- **Common Tools:**  
  - **Power BI tools**  
  - **Data mining tools**  
  - **Direct database queries**  
