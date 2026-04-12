# Trade-Intelligence-Import-Trends-by-CommodityLevel-
Project Overview
This project focuses on analyzing Trade Intelligence: Import Trends by CommodityLevel using Microsoft Power BI to generate meaningful insights into trade patterns.
The dataset includes key attributes such as state, port, country, commodity, quantity, and import values (in INR and USD). Initial data cleaning and preprocessing were performed within Power BI using DAX and Power Query, including handling missing and zero values, correcting data inconsistencies, and formatting fields to ensure accurate and reliable analysis.
The transformed data was then used to build an interactive dashboard in Power BI, enabling dynamic visualization of import trends across different commodities, states, and countries.
2. Objectives
•	Analyze import distribution by commodity and region
•	Identify top-performing commodities and major countries
•	Analyze trends in import values and quantities
•	Develop interactive dashboards
•	Measure KPIs like total imports, quantity, and YoY growth
•	Rank commodities, countries, and ports based on import value and volume 
•	Analyze relationships between quantity and value to identify high-value vs high-volume commodities 
•	Enable dynamic filtering (Year, State, Commodity, Country) for interactive exploration 
3. Data Sources
•	Source Description and Timeline:
The dataset is obtained from government trade data sources such as the Ministry of Commerce and Industry, Directorate General of Commercial Intelligence and Statistics, or open platforms like https://indiadataportal.com
The data typically covers import transactions over a specific period (e.g., 2018–2024), including monthly records. 
•	Domain:
The project falls under the Commerce / International Trade Analytics domain, focusing on import activities across commodities, states, ports, and countries.
4. Problem Statement
•	To analyze import performance across different states, ports, and countries to identify key contributors to total imports. 
•	To evaluate import trends across various commodities in terms of quantity and value (INR/USD). 
•	To identify top-imported commodities and major trading partner countries. 
•	To study monthly and yearly import patterns for better trade planning and forecasting. 
•	To detect inconsistencies or missing values in import data and improve data quality through preprocessing. 
•	To develop an interactive dashboard that enables stakeholders to explore import insights and support data-driven decision-making.
•	Improve data quality through preprocessing
5. Attributes

Attribute Name	Data Type	Description
id	Integer	Unique identifier for each record
month	Date / String	Month and year of the import transaction
state_name	String (Text)	Name of the state where the import occurred
state_code	Integer	Unique code assigned to each state
port	String (Text)	Name of the port through which goods are imported
country	String (Text)	Exporting country from which goods are imported
pc_code	String (Text)	Principal commodity code representing category of goods
commodity	Categorical	Type of commodity imported (e.g., Tea, Coffee, Cashew)
units	String (Text)	Unit of measurement (e.g., Kgs, Tons)
quantity	Numeric (Decimal/Integer)	Quantity of goods imported
dollars_value	Numeric (Decimal)	Import value in US Dollars (USD)
inr_value	Numeric (Decimal)	Import value in Indian Rupees (INR)

6. Tools & Technologies

•	Excel: Data cleaning.
•	Power BI: Data cleaning, transformation, Data modelling, DAX calculations, visualization, and interactive dashboard creation.

7. Data Preprocessing (Using Power BI)
Handling Missing and Zero Values:
Missing and zero values in the quantity and dollars_value columns were identified, as they could significantly impact the accuracy of analysis and insights.
Imputation of Quantity:
To address missing or zero quantity values, an average price-based approach was used:
•	Calculated Average Price = INR Value / Quantity for valid records 
•	Estimated missing or zero quantities using:
Quantity = INR Value / Average Price 
This method ensured realistic estimation based on existing data patterns.
Imputation of Dollar Value:
Missing or zero values in the dollars_value column were imputed using the relationship between INR and USD values:
•	Derived a conversion factor from available data 
•	Calculated:
Dollar Value = INR Value / Conversion Factor 
This maintained consistency between currency values across the dataset.
Data Transformation in Power BI:
•	Performed data cleaning and transformations using Power Query Editor 
•	Created calculated columns and measures using DAX (Data Analysis Expressions) 
•	Standardized data types and ensured uniform units across all records 
Data Validation:
Data validation was performed to ensure the accuracy and consistency of the dataset after handling missing and zero values. Validation checks were applied to confirm that imputed quantity and dollar values were logically correct, non-negative, and aligned with existing data patterns.
Additionally, relationships between INR and USD values, data types, and unit consistency were verified to maintain reliability and ensure that the transformed data supports accurate analysis and reporting.


8. Data Modelling and DAX (Power BI)
Data Model:

The import dataset was initially in a denormalized format, where all attributes were stored in a single table. To improve data structure and analytical efficiency, the data model was normalized by creating a separate Calendar table and establishing relationships between the date field in the import table and the Calendar table. This transformation enabled better time-based analysis, such as monthly, quarterly, and yearly trends, and enhanced overall performance and scalability.
 

Calculated Columns & DAX Measures: Implemented DAX formulas for key metrics, such as total sales, growth percentages, and cumulative totals.
Calculated Columns:
•	Imputed Quantity
•	Imputed Dollars
Calculated Measures:
•	INR 2024
•	INR Previous Year (Dynamic)
•	Rank by Commodity 2024

•	YTD Quantity
•	YoY Growth%
•	Total Quantity
•	Total Sales( INR Value)
•	Rank by Commodity
•	Rank by Year
DAX Function Definitions
1. Imputed Quantity
Estimates missing or zero quantity values by dividing the INR value by the average price. If quantity is available, the original value is retained.
2. Imputed Dollars
Replaces missing or zero dollar values by converting INR to USD using a fixed exchange rate (83). Otherwise, it keeps the existing dollar value.

3. INR 2024
Calculates the total import value (INR) for the specific year 2024 by applying a filter on the Calendar table.
4. INR Previous Year (Dynamic)
Computes the previous year’s total import value dynamically based on the selected date context using time intelligence. 
5. Rank by Commodity 2024

Ranks commodities based on their total import value for 2024 in descending order using dense ranking (no gaps in rank). 
6. YTD Quantity
Calculates the cumulative quantity of imports from the beginning of the year up to the selected date.
7. YoY Growth %
Measures the percentage change in import value compared to the previous year.
8. Total Quantity
Returns the total sum of imported quantity across all records.
9. Total Sales (INR Value)
Calculates the total import value in INR across the dataset.
10. Rank by Commodity
Ranks commodities based on total import value while maintaining the commodity context and ignoring other filters. 
11. Rank by Year
Ranks years based on total import value to identify the highest-performing year.
 9.  Analysis and Visualizations (Power BI)
Dashboard Features
•	Interactive Dashboard: Designed with user-friendly navigation, enabling dynamic exploration of import data across multiple dimensions 
•	Slicers and Filters: Implemented slicers for Year to allow customized analysis 
•	KPI Cards: Display key metrics such as Total Import Value (INR), Total Quantity, Previous Year Value, and YoY Growth % 
•	Treemap Visualization: Shows commodity-wise distribution of import value, highlighting top contributing commodities 
•	Decomposition Tree: Provides hierarchical breakdown of INR value by commodity, country, and state for root cause analysis 
•	Ribbon Chart: Illustrates ranking of commodities across different states based on quantity 
•	Line Chart: Displays monthly trends in import value, helping identify patterns and seasonality 
•	Waterfall Chart: Represents contribution of individual factors to total import value (INR) 
•	Scatter Chart: Analyzes import efficiency (quantity vs value) to distinguish high-value and high-volume commodities 
•	Map Visualization: Highlights geographical distribution of ports involved in imports 
•	Bar Chart: Shows Top 5 import countries based on import value 
•	Drill-Down & Drill-Through: Enables deeper analysis from country → port → commodity level 
•	Dynamic Ranking: Uses DAX to rank commodities and countries based on selected filters 
•	Tooltips & Data Labels: Provide additional context and detailed insights on hover
 

 

9. Insights & Conclusions
Key Findings
•	The total import value for 2024 is ₹33.54Tn with Petroleum: Crude contributing           ₹ 7.3Tn, making it the highest contributor. 
•	Australia is the leading import partner in 2024 with imports worth ₹470.41Bn , followed by Angola with ₹201.4Bn. 
•	Gujarat recorded the highest imports at ₹5.1Tn mainly through Nhava sheva port contributing ₹1.7Tn. 
•	Monthly analysis shows the highest imports in May 2024 with ₹3.54Tn and the lowest in January 2024 with ₹4.6Bn.

________________________________________
Analysis Insights
1.	Descriptive Analysis (What happened?)
•	The Treemap shows Petroleum: Crude as the top commodity in 2024 with ₹7.38Tn, followed by Petroleum Products with ₹2.13Tn. 
•	The Bar Chart indicates China as the highest contributor with ₹5.1Tn.
•	The Map Chart highlights handling Nhava sheva port imports worth ₹35.06 Bn in 2024. 
•	The Ribbon Chart shows Bulk Minerals And Ores ranked 1st in Andhra Pradesh with ₹58Bn. 
•	The Line Chart shows import trends ranging from ₹0.46 Bn to ₹0.35Tn across months in 2024. 
________________________________________
2.	Diagnostic Analysis (Why did it happen?)
•	The Decomposition Tree shows that Petroleum: Crude from Iraq contributes ₹1.48Tn, the highest combination in 2024. 
•	High import values are driven by Petroleum: Crude with ₹5.1Tn, even with comparatively lower quantity. 
•	Gujarat dominates imports with ₹5.1Tn, due to major ports like Nhava sheva port  
________________________________________
3.	Predictive Analysis (What is likely to happen?)
•	Import values are expected to follow similar patterns, with peaks potentially reaching ₹45Tn based on 2024 trends. 
•	Commodities like Petroleum: Crude are expected to maintain high import values around ₹3Tn monthly. 
•	Countries like China and Russia will likely continue contributing ₹3Tn imports regularly.
•	Ports like Nhava sheva port and Visakhapatnam Sea will continue to dominate import handling due to high volume capacity.
________________________________________
4. Prescriptive Analysis (What should be done?)
•	Diversify import sources to reduce dependency on a limited number of countries 
•	Focus on high-value commodities to optimize trade profitability 
•	Improve data quality by handling missing and inconsistent values using DAX and Power Query 
•	Strengthen infrastructure at high-performing ports to handle increasing trade volume 
•	Use dashboard insights for strategic decision-making in procurement and supply chain planning 
________________________________________
Visualization-Based Insights
•	Treemap: Shows Petroleum: Crude as the top commodity contributing approximately ₹7.3Tn to total imports. 
•	Decomposition Tree: Highlights that Petroleum: Crude from Russia via Visakhapatnam Port contribute the highest value of around ₹2.3Tn (per major combination). 
•	Ribbon Chart: Displays Petroleum: Crude consistently ranked 1st in Andhra Pradesh, contributing ₹2.3Tn monthly. 
•	Line Chart: Shows import values increasing from ₹1Tn (January) to ₹2Tn (July peak). 
•	Waterfall Chart: Explains total import value of ₹33.54Tn, with major contributions from Gujarat (~₹9Tn) and Maharashtra (~₹6Tn). 
•	Scatter Chart: Reveals high-value imports like ₹2Tn with very large quantities indicating bulk shipment efficiency. 
•	Map Chart: Highlights Nhava sheva port and Visakhapatnam Port as major hubs. 
•	Bar Chart: Shows China (₹5.1Tn) as the top import country, followed by Russia (₹3Tn) and UAE (₹2.9Tn).
10. Conclusion
The analysis shows that Petroleum: Crude are the primary driver of import value, contributing the largest share throughout 2024. Key countries like China and Russia dominate as major trading partners, indicating a high dependency on limited sources. Nhava sheva port plays a crucial role, handling the majority of import activities in Gujarat. Import trends display a gradual increase, with peak activity observed in the mid-year months. However, some data inconsistencies such as zero quantity with recorded value need to be addressed. Overall, diversification of trade partners and improvement in port infrastructure can enhance efficiency and reduce risk.
The dashboard provided clear insights into import trends, helping identify key contributing commodities and trade patterns. 
Overall, the analysis demonstrates how business intelligence tools can enhance decision-making in import management and trade analysis. 
