# Data Cleaning and Data Governance  

## Data Cleaning  

- It’s best to ensure data follows certain rules from the **source systems** right from the beginning.  
- If that’s not possible, we define **requirements** that help determine which rows are valid and which are not.  
- Since we perform operations like **joins**, **unions**, and other transformations, having **consistent data** is essential for smoother processing.  
- Data cleaning depends on the specific **business requirements** and use cases.  

### Common Data Cleaning Tasks  

1. **Data Format Cleaning**  
   - Standardize formats (e.g., dates, capitalization).  
   - Fix naming conventions, abbreviations, and option names.  

2. **Address Parsing**  
   - Break down address fields into components (e.g., street, city, zip).  
   - Helps standardize data and enables ETL tools to perform validations and lookups.  

3. **Data Validation**  
   - Perform range checks (e.g., age should not be 300).  
   - Type checks (e.g., a numeric value should not be stored as text).  

4. **Duplicate Row Elimination**  

---  

## Data Governance  

- Data governance focuses on defining and enforcing **rules, standards, and definitions** for managing data across the organization.  
- It helps maintain data **quality, integrity, and consistency** over time.  
- Organizations with strong data governance typically require **less cleaning**, as data is already structured, validated, and monitored according to agreed-upon policies.  

### Summary  
While **data cleaning** is reactive and task-specific, **data governance** is proactive, aiming to reduce the need for cleaning by embedding quality standards into the data lifecycle.  (note that this line from chatgpt, and I love it :))
