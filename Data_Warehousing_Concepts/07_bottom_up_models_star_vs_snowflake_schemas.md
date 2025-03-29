# ⭐ Bottom-Up Models: Star & Snowflake Schemas  

## 📌 Fact Table  
- Stores **measurements, metrics, or facts** about an organization.  
- Contains **foreign keys (FKs) to Dimension Tables** for more details.  
- Example Schema:  

| Column Name  | Type  | Description |
|-------------|------|-------------|
| `CustomerID` | FK   | Links to customer details in a **Dimension Table** |
| `DateID`     | FK   | Links to date details in a **Dimension Table** |
| `Tax`        | Value | Tax amount per transaction |
| `Sales`      | Value | Sales amount per transaction |
| `UnitsSold`  | Value | Number of units sold |

---

## 📌 Dimension Table  
- Stores **attributes or descriptive data** about a process.  
- Example: `Customer_Dim` (Customer Dimension Table).  
- Holds **reference data** used to analyze facts.  

---

## ⭐ Star Schema  
- **Fact Table** is directly connected to **one or more Dimension Tables**.  
- **Simple structure**, easy for business users.  
- **Example Shape:**  

               Dim1      Dim2      Dim3  
                │         │         │  
                └────────Fact Table  


---

## ❄️ Snowflake Schema  
- **Dimension Tables are connected through other Dimension Tables** (normalized structure).  
- Unlike Star Schema, not all Dimension Tables link directly to the Fact Table.  
- **Example Shape:**  

            Dim1 ─── Dim3
            │          
            └────────Fact Table  
            │  
            Dim2  
