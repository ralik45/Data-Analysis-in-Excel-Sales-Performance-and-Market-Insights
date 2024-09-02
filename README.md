# How-to-Analyze-Data-in-Excel

**Data Analysis Report**

**1. Introduction**

This report outlines the analysis performed on a dataset containing sales information, including categories, suppliers, brands, years, months, and monthly profits. The goal of the analysis was to better understand the performance and growth of various suppliers and brands over time, as well as to assess market share and profit trends.

![image](https://github.com/user-attachments/assets/cbac5eec-ba42-42e5-b189-0480659caa73)


**2. Data Navigation**

The dataset initially contains the following columns:

- **Category**: Product category (e.g., Treadmill).
- **Supplier**: Name of the supplier (e.g., Peak Performance Gear).
- **Brand**: Brand of the product (e.g., Apex Athletics).
- **Year**: Year of the sales data (e.g., 2018).
- **Month**: Month of the sales data (e.g., January).
- **Profit (Month)**: Monthly profit amount.

To facilitate easier navigation and analysis, a table was created to organize this data.

![image](https://github.com/user-attachments/assets/6366b309-ff07-4098-95b6-20abe9f89aea)

**3. Analysis Steps and Results**

**Step 1: Suppliers, Brands, Categories Analysis**

- **Objective**: To determine the number of suppliers, brands, and categories.
- **Method**: A pivot table was created in a sheet named "Suppliers, Brands, Categories."
- **Findings**:
  - There are several suppliers, including "Iron Strength Equipment Co." and "Peak Performance Gear."
  - Multiple brands such as "Forge Fitness," "Ironclad Athletics," and "Steel Power."
  - Categories include various fitness equipment like "Rowing Machine" and "Airbike."
 
![image](https://github.com/user-attachments/assets/09b4f655-496d-47dc-8eda-a324155ce6f8)

**Step 2: Year-over-Year (YoY) Growth Analysis**

- **Objective**: To analyze the Year-over-Year growth from 2019 to 2023 for suppliers and brands.
- **Method**: Duplicated the previous pivot table into a new sheet named "YoY Growth" and calculated growth percentages.
- **Enhancements**: Conditional formatting with a color scale was applied to differentiate growth values.
- **Key Insights**:
  - Notable YoY changes, e.g., "Ironclad Athletics" saw a decrease of about -7.7% in 2022.
  - Some brands showed significant declines or moderate growth patterns, indicating varying performance levels.

![image](https://github.com/user-attachments/assets/308029b4-72ef-4f52-92b9-d02b62210136)

**Step 3: Market Share Analysis**

- **Objective**: To assess the market share of each brand from 2018 to 2023.
- **Method**: Created a sheet named "Market Share" to analyze using the sum of monthly profits as values.
- **Visualization**: A line chart was created to visualize brand competition over the years with category filters.
- **Findings**:
  - Brands like "Spartan Sports" Increase significant and "Hercules Gear" Drop Significant.

<img width="384" alt="image" src="https://github.com/user-attachments/assets/f971d721-8ae1-4a7c-bd3a-96acbf69dcbe">

**Step 4: Profit Analysis**

- **Objective**: To calculate Year-to-Date (YTD) Profit and Annual Profit for assessing growth in each category.
- **Method**:
  - In the "raw_data" sheet, new calculated fields were created:
    - **YTD Profit**: `=SUMIFS([Profit (Month)],[Category],[@Category],[Supplier],[@Supplier],[Brand],[@Brand],[Year],[@Year],[Month],"<="&[@Month])`
    - **Annual Profit**: `=[@[YTD Profit]] + SUMIFS([Profit (Month)],[Category],[@Category],[Supplier],[@Supplier],[Brand],[@Brand],[Year],[@Year]-1,[Month],">"&[@Month])`
- **Analysis**: These fields allowed a detailed understanding of profit accumulation and year-over-year changes within categories.

![image](https://github.com/user-attachments/assets/dd7af268-10a2-4a39-84c5-572bfb030e0e)

**Step 5: Sum of Annual Profit**

- **Objective**: To view the sum of annual profit by category, brand, and supplier.
- **Method**: A sheet named "Sum of Annual Profit" was created with filters for year and month, using "Sum of Annual Profit" as the primary value.
- **Findings**:
  - The table shows consolidated annual profits, with specific suppliers "Iron Stength Equipment Co." and brands "Steel Power" achieving notable totals (e.g., 158,973.00 in 2024 for rowing machines).
  
<img width="324" alt="image" src="https://github.com/user-attachments/assets/0f75d2a0-4532-4818-8261-73312ca94768">

**4. Conclusion**

The analysis provides valuable insights into supplier and brand performance, highlighting growth trends, market share dynamics, and profitability across categories. Conditional formatting and calculated fields enhanced the interpretability of trends, supporting strategic decisions in market competition and financial growth assessment.
