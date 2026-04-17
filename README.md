
# 📊 Trade Intelligence: Import Trends by Commodity Level – Data Analysis using Power BI

## 📌 Project Overview

This project focuses on analyzing **Trade Intelligence: Import Trends by CommodityLevel** using Microsoft Power BI to generate meaningful insights into trade patterns.
The dataset includes key attributes such as state, port, country, commodity, quantity, and import values (in INR and USD). Initial data cleaning and preprocessing were performed within Power BI using DAX and Power Query, including handling missing and zero values, correcting data inconsistencies, and formatting fields to ensure accurate and reliable analysis.
The transformed data was then used to build an interactive dashboard in Power BI, enabling dynamic visualization of import trends across different commodities, states, and countries.
 

---

## 🎯 Objectives

*	Analyze import distribution by commodity and region
*	Identify top-performing commodities and major countries
* Analyze trends in import values and quantities
*	Develop interactive dashboards
*	Measure KPIs like total imports, quantity, and YoY growth
*	Rank commodities, countries, and ports based on import value and volume 
*	Analyze relationships between quantity and value to identify high-value vs high-volume commodities 
*	Enable dynamic filtering (Year, State, Commodity, Country) for interactive exploration 


---

## 📂 Data Sources
**Source Description and Timeline**:
The dataset is obtained from government trade data sources such as the Ministry of Commerce and Industry, Directorate General of Commercial Intelligence and Statistics, or open platforms like https://indiadataportal.com
The data typically covers import transactions over a specific period (e.g., 2018–2024), including monthly records. 
**	Domain**:
The project falls under the Commerce / International Trade Analytics domain, focusing on import activities across commodities, states, ports, and countries.

---

## 🛠️ Tools & Technologies

* **Power BI** – Data visualization & dashboard creation
* **Excel / CSV** – Data preprocessing


---

## 🔄 Data Preprocessing

* Handled **missing and zero values**
* Created **imputed measures** for missing quantities and values
* Converted large numeric values into **billions/trillions**
* Cleaned and standardized dataset for analysis

---

## 📊 Data Modeling
The import dataset was initially in a denormalized format, where all attributes were stored in a single table. To improve data structure and analytical efficiency, the data model was normalized by creating a separate Calendar table and establishing relationships between the date field in the import table and the Calendar table. This transformation enabled better time-based analysis, such as monthly, quarterly, and yearly trends, and enhanced overall performance and scalability.

---

## 📈 Dashboard Features

### 🔹 Visualizations Used

* 📌 **Treemap** – Top commodities contribution
* 📌 **Decomposition Tree** – Root cause analysis
* 📌 **Ribbon Chart** – Ranking changes over time
* 📌 **Line Chart** – Trend & seasonality
* 📌 **Waterfall Chart** – Contribution analysis
* 📌 **Scatter Plot** – Efficiency (value vs quantity)

---

## 📊 Key Insights

*	The total import value for 2024 is ₹33.54Tn with Petroleum: Crude contributing ₹ 7.3Tn, making it the highest contributor. 
*	Australia is the leading import partner in 2024 with imports worth ₹470.41Bn , followed by Angola with ₹201.4Bn. 
*	Gujarat recorded the highest imports at ₹5.1Tn mainly through Nhava sheva port contributing ₹1.7Tn. 
*	Monthly analysis shows the highest imports in May 2024 with ₹3.54Tn and the lowest in January 2024 with ₹4.6Bn.


---


## 📷 Dashboard Preview

*<img width="602" height="320" alt="image" src="https://github.com/user-attachments/assets/6834070e-ec2e-4278-9e78-08a435ee6900" />
*<img width="598" height="309" alt="image" src="https://github.com/user-attachments/assets/b1cd27a3-bad3-432c-b26c-ef24dc89f95d" />


---

## 📎 Conclusion

The analysis shows that Petroleum: Crude are the primary driver of import value, contributing the largest share throughout 2024. Key countries like China and Russia dominate as major trading partners, indicating a high dependency on limited sources. Nhava sheva port plays a crucial role, handling the majority of import activities in Gujarat. Import trends display a gradual increase, with peak activity observed in the mid-year months. However, some data inconsistencies such as zero quantity with recorded value need to be addressed. Overall, diversification of trade partners and improvement in port infrastructure can enhance efficiency and reduce risk.
The dashboard provided clear insights into import trends, helping identify key contributing commodities and trade patterns. 
Overall, the analysis demonstrates how business intelligence tools can enhance decision-making in import management and trade analysis. 
