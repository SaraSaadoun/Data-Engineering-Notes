## Column Store Format

Column store format is the best choice for **Data Warehouse (DWH) tables** that require **analytical workloads** (optimized query speed). But why?

### How It Works
1. Computers store data in **blocks**.
2. When reading data, the system retrieves only the required blocks.
3. If data is spread across many blocks, retrieval takes more time.
4. By storing **likely-needed data** in a small number of blocks, we optimize query performance.

### Column Store vs. Row Store

| Storage Type  | Structure |
|--------------|-----------|
| **Column Store** | Stores data **column-wise** (each column stored separately) | 
| **Row Store** | Stores data **row-wise** (entire row stored together) | 

#### Example
Consider a sales table:

| ID  | Product | Sales  | Date       |
|-----|---------|--------|------------|
| 1   | A       | 100    | 2024-01-01 |
| 2   | B       | 200    | 2024-01-02 |
| 3   | C       | 150    | 2024-01-03 |

- **Row Store:** The entire row is stored together in memory.
- **Column Store:** The `Sales` column is stored separately, meaning a query retrieving `Sales` values will be **faster**.

### Benefits of Column Store
1. **Faster Query Performance**: Frequently accessed columns (e.g., `Sales`) are stored together, making retrieval **fast**.
2. **Efficient Data Compression**: Since each block contains the same data type, compression is **more effective**.

### Drawbacks of Column Store
- **Slow Inserts/Updates**: Writing new data requires modifying multiple blocks, making transactions **slower**.

### Conclusion
For **analytical workloads**, column store is ideal due to **fast retrieval and efficient compression**. For **transactional workloads**, row store remains the better choice.