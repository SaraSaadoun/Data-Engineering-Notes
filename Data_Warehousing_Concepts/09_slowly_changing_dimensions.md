## Slowly Changing Dimensions

The problem is that we need to change values in dimension tables (note that the fact table is always constant). So, how do we handle these changes?

### Standard Approach: Type I, Type II, Type III
### Modern Approach

---

### 1. Standard Approaches

#### 1.1 Type I
- Update the value in the table directly.
- This results in losing historical reports, as they will be refreshed or updated (the last value gets replaced with the new one).
- Sometimes, losing historical reports is not acceptable for the organization.

#### 1.2 Type II
- Add a new row with the updated value and a new ID.

**Example:** Updating category `X` to `Y`

| ID | Description | Category | Start Date | End Date |
|----|------------|----------|------------|------------|
| 1  | "blah"     | X        |            | Today     |
| 2  | "blah"     | Y        | Today      | Future Date (~inf.) |

- Historical reports remain unchanged ✅

#### 1.3 Type III
- Add a column to the dimension table to track changes.

**Example:**

| ID | Description | Category | Past Category |
|----|------------|----------|--------------|
| 1  | "blah"     | Y        | X            |

**Advantages:**
- Past and current values can be seen simultaneously.

**Disadvantages:**
- Requires updating the code for historical reports.
- Limited history tracking (we can add `N` columns to track the `N`th historical value).

---

### 2. Modern Approach
- Snapshot the entire dimension table.
- Data warehouses (DWs) adopt this method due to the benefit of low storage costs.
- Then, update like Type I (update directly).

**Note:**
- Dimension tables have a small number of rows compared to fact tables, so storage is minimal.
- With modern hardware, duplication is not a major concern.
