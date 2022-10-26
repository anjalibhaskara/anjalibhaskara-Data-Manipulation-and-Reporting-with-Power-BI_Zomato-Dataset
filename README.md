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
        
      - **For example:**
       
         “Cedar Rapids/Iowa City” should be corrected to “Cedar Rapids”
         
         “ÛÁstanbul” should be corrected to “Istanbul”
         
  - As Restaurant name and address are present in same column,I have created two  Columns for displaying **Restaurant Name** and **Restaurant Address**.
  - All Continent tables are appended to a single table named **"Restaurant Details"**
  - Fact-table has been renamed as KPIs and done appropriate changes.
  - Country-Code has been renamed as Country Master and done appropriate changes.
  
  **Below  relationships have been created to get better insights from Data using "Manage Relationships" in Data View.**
  
   1. **"Many to One relationship"** between **"Cuisine table"** and **"Restaurant Details"** tables with common column **"Restaurant ID"** .
  
   2. **"Many to One relationship"** between **"Restaurant Details"** and **"Country Master"** tables with common column **Country code** 
  
   3. **"Many to One relationship"** between **"KPIs"** and **"Restaurant Details"** tables with common column **Country code** .
     
  - Created a new column "Restaurant.Continent" in the table  “Country Master”  using the continent column from Restaurant table s using the below 
     mentioned convention.
     Note: The mapping is continent - country, for example ''Africa – South Africa''  
    
  - As **Country-Code table** is dimension table I have removed duplicates and blank values.
 
  - **Following measures have been created in the appropriate tables and all measures are segregated in to a Measures Master** 

     a. Restaurant count
     
     b. Average cost
     
     c. Average rating
     
     d. Cuisine count
     
     e. Max Cost
     
     f. Min Cost
   
   
   ## **PowerBI  Dashboard**
   
   Added different graphs, cards, tables, filters, etc. You can have a look at the interactive Power-BI report [here](Zomato dashboard_anjali.pbix) and try different  filters as per your need. Feel     free to try different Drill options in Map visual to get insights of Continent, Country,City wise  analysis in "Global Analysis" 
and try different filters in "Restaurant analysis" to get insights of Restaurant wise analysis.

You can use the icons in Report to navigate between Global analysis and Restaurant analysis reports in the Dashboard.

In case if above link isn't accessible, I am attaching the following snap-shots for reference.
  
  
   
   ![Global analysis](https://user-images.githubusercontent.com/73122719/198102560-5e95f321-8818-497f-9109-ebebbf01d32b.PNG)
   ![Global analysis_2](https://user-images.githubusercontent.com/73122719/198102806-c77b9c9a-8447-4458-b8b8-43d47a0b36f0.PNG)
   ![Restaurant analysis](https://user-images.githubusercontent.com/73122719/198103428-66d18f1c-5ee0-4833-adaf-902d5a9e1159.PNG)
   ![Restaurant analysis_2](https://user-images.githubusercontent.com/73122719/198103466-d96454af-fb67-4b44-a660-8c3b09d8fa6b.PNG)

   
   

