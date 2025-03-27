# 🏗️ Data Warehouse (DWH) Architectures  

There are two main approaches to building a Data Warehouse: **Inmon's Top-Down** and **Kimball's Bottom-Up**.  

## 1️⃣ Inmon (Top-Down Approach)  
- **Data is stored in a normalized form** to reduce redundancy and improve quality.  
- Business rules, **data cleaning, and definitions must be established** before implementation or ingestion.  
- **Process Flow:**  
  `Sources → ETL → DWH → Data Marts → Users`  

### ✅ Pros:  
- **Single Source of Truth** (centralized and structured).  
- **Less storage** required due to normalization.  
- **Easier to modify Data Marts** to support changing reporting needs.  

### ❌ Cons:  
- **More joins** due to normalization → **slower query performance**.  
- **Higher startup cost** due to extensive upfront work.  
- **Slower initial implementation** since DWH must be fully built before analysis begins.  

---

## 2️⃣ Kimball (Bottom-Up Approach)  
- **Focuses on quick reporting and analysis.**  
- Once data is gathered, it is **denormalized into a Star Schema** for fast queries.  
- Each department has its **own Data Mart**, and these are later joined into the DWH.  
- **Process Flow:**  
  `Sources → ETL → Data Marts → DWH → Users`  

### ✅ Pros:  
- **Faster implementation** with lower startup cost.  
- **Denormalized structure = faster queries** and user-friendly analysis.  

### ❌ Cons:  
- **Increased ETL processing time**.  
- **Data duplication** may occur across different Data Marts.  
- **DWH is not a single source of truth**.  
- **Ongoing development required** if a new department is added.  
