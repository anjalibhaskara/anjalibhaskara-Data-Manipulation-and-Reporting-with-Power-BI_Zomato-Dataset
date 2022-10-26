# **Data Manipulation and Reporting with PowerBI**

The **Data Manipulation and Reporting with PowerBI** project aims to provide an analysis of Zomato Dataset(Datasets). In this repo, you'll find a precise and interactive PowerBI report that will allow Zomato to quickly assess the required data.

## **Datasets**
We've got the datasets in the raw form as you can see [here](Datasets) , we have  different `.csv` files for each [Continent](Datasets/Continents) where details of restaurants corresponding to those continents are maintained.Also we have got [FactData](Datasets/Fact-Table.xlsx) and [CountryCodeData](Datasets/Country-Code.xlsx) to analyze the Zomato Dataset. 


  ### **Data Pre-processing**
  
  Data Pre-processing is done using Power Query(ETL tool) of PowerBI.
  
  For each continent table (`.csv`) below changes are done.
  
    - I have made sure that "CITY" Column names are corrected and are not ambiguous.
      - **For example:**
       
         “Sí£o Paulo” should be corrected to “São Paulo”
      -  **For example:**
       
         “Cedar Rapids/Iowa City” should be corrected to “Cedar Rapids”
         
         “ÛÁstanbul” should be corrected to “Istanbul”
         
  - As Restaurant name and address are present in same column,I have created two  Columns for displaying **Restaurant Name** and **Restaurant Address**.
  
  - 
  
  
  - As Country-Code table is dimension table I have removed duplicates and blank values.
