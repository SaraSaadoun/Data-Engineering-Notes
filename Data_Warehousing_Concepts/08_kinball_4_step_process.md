# Kimball's 4-Step Process  

1. **Select the Organizational Process**  
   - Ask for an organizational process such as invoicing and billing.  
   - This approach is applied to a single department or process to create a data mart.  

2. **Declare the Grain (the Level at Which to Store the Fact Table)**  
   - Determine the amount of detail needed in the fact table.  
   - The grain should be the smallest level that cannot be further divided.  

3. **Identify the Dimensions**  
   - Identify dimensions that represent various characteristics of the fact data.  
   - Choose dimensions that apply to each row.  

   **Common examples:**  
   - **Time:** Year, quarter, month  
   - **Location:** Address, state, country  
   - **Users:** Names, email  

   - Answer the question: *"How do organizational users describe the data resulting from the business process?"*  
   - Consult analysts and users who will work with these data.  

4. **Identify the Facts**  
   - Define the key metrics and measures needed for analysis.
   - Ask: *"What business questions do we need to answer?"*  
   - Ensure that measures are valid at the defined grain level.  
