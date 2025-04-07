# dbt (Data Build Tool)

**dbt** is an open-source tool that helps you **transform**, **test**, and **document** your data inside a data warehouse using **SQL**.

---

## ✅ Benefits of dbt

- **SQL-based**
- **Modular & Scalable**: break transformations into reusable models  
- **Version Control**: integrates well with Git  
- **Automated Testing**
- **Documentation & Lineage**: auto-generate docs with data lineage

---

## 📊 Data Flow with dbt

```mermaid

    Raw Data > dbt Models (Transformations) > Cleaned & Transformed Data
    
```
## 🕰️ Before vs After dbt
### Before dbt

- Writing large, complex SQL queries

- Repeating similar logic across multiple reports

- Difficult to debug and maintain

### After dbt

- Split logic into small, reusable models

- Each model can reference others

- Easier to test, document, and scale your transformations