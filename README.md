Go back to [Aldo Reyes Portfolio](https://aldoreyes84.github.io/AldoReyes.github.io/)

Go back to [Data Analysis Project](https://github.com/AldoReyes84/Data-Analisys_For-AdventureWorksDW2022_SQL_PowerBI_Python_Excel/tree/main)

# Power_BI_AdventureWorks2022_Data_Analysis

### Resellers Sales

This section connects Power BI to SQL Server using **Power Query** with an **imported query** approach:

SQL Server Connection

<img width="401" height="311" alt="image" src="https://github.com/user-attachments/assets/7696424c-df0c-4e99-be34-430551cbe546" />

Star Schema

<img width="577" height="313" alt="image" src="https://github.com/user-attachments/assets/fdb2d333-68f9-43b3-8db3-0df9401738e2" />

To begin data exploration using Power BI visualizations for the **FactResellerSales** table:

- Quantity  
- Product Cost  
- Total Discount  
- Sales Amount  
- Gross Margin *(DAX measure)*  
- Margin Percentage *(DAX measure)*

<img width="1261" height="720" alt="image" src="https://github.com/user-attachments/assets/4d7eb5e2-4c36-4ad9-b45c-282dc14c6a11" />

The interpretation of these results are addresserd in the [Data Analysis Project/FactResellersSales_Table](https://github.com/AldoReyes84/Data-Analisys_For-AdventureWorksDW2022_SQL_PowerBI_Python_Excel/tree/main#factresellerssales-table) 

### Internet Sales

Using the **Recent Sources** lets bring the **FactInternetSales** 

 <img width="433" height="404" alt="image" src="https://github.com/user-attachments/assets/30509f2a-51f4-4aa8-8c4e-d825f1d0c5ff" />

Create two more measures

               InternetGrossMargin = CALCULATE(sum(FactInternetSales[SalesAmount])-SUM(FactInternetSales[TotalProductCost]))
And  
  
              Internet Margin Percentage = CALCULATE(([InternetGrossMargin]/sum(FactInternetSales[SalesAmount])))

To begin data exploration using Power BI visualizations for the **FactInternetSales** table:

- Quantity  
- Product Cost  
- Total Discount  
- Sales Amount  
- Internet Gross Margin *(DAX measure)*  
- Internet Margin Percentage *(DAX measure)*

<img width="1201" height="730" alt="image" src="https://github.com/user-attachments/assets/55fd3d19-8bc0-430c-8d69-89a50b97b3c9" />
