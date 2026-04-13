# Fragrance Sales Performance Analysis

## 📖 Table of Contents

* [**Project Overview**](#-project-overview)
* [**Data Source**](#-data-source)
* [**Tools & Technologies**](#-tools--technologies)
* [**Data Cleaning & Preparation**](#-data-cleaning--preparation)
* [**Exploratory Data Analysis (EDA)**](#-exploratory-data-analysis-eda)
* [**Key Insights**](#-key-insights)
* [**Recommendations**](#-recommendations)
* [**Conclusion**](#-conclusion)

## 📊 Project Overview
This project provides a comprehensive analysis of a global fragrance dataset (2,000+ records) spanning markets like India, Canada, and United States. The goal was to transform raw, messy retail data into an interactive decision-making tool that tracks revenue trends, inventory health, and consumer demographic preferences.

## 🗂️ Data Source
●	**Source:** Web scrapping

●	**Domain:** Sales


## 🛠️ Tools & Technologies

●	**Excel:** Data cleaning and transformation.

●	**Power BI:** Data modelling, DAX calculations, visualization, and interactive dashboard creation.


## 🧹 Data Cleaning & Preparation
●	Standardized formats

●	Created calculated field 

1.Total_Revenue = =[@PRICE]*[@sold] 

●	Applied clean and Trim formulas to Type column.

●	Applied clean and Trim formulas to Type column.	Separated Last updated Date and time column into Date, time and time zone using delimiter.

●	Applied clean and Trim formulas to Type column.	Extracted country name from Item location column using formula
Country =TRIM(RIGHT(SUBSTITUTE(A2, ",", REPT(" ", LEN(A2))), LEN(A2)))

●	Sorting: Sorted date column from Newest to oldest.

●	Convert the data into Fact and Dimension Table. Created 2 dimension tables.

1.	Type_Dim
   
2.	Country_Dim
   
● Extracted Type ID and Country ID from dimension tables to fact tables using Xlookup function.

E.g.,

         =XLOOKUP(A2, Type\_Dim!B:B, Type\_Dim!A:A)
         
Likewise Country_ID column.   


## 🔍 Exploratory Data Analysis (EDA)


<img width="944" height="533" alt="image" src="https://github.com/user-attachments/assets/5695913a-714a-4335-bb20-dbe1453c377d" />



●	Map visualization helps understanding the geographical view of Fragrance sales and total revenue distribution across the country.

●	Filtered top 10 types of perfume by their total revenue.

●	Eau De Toilette ranks number 1 and Eau De Parfum ranks 2.

●	Trend chart plotted to identify the trend of perfume sales across years, quarters and months.

●	In the year 2024 only a greater number of perfumes sold and in the month of May.


## 💡 Key Insights 


●	Based on the Revenue by Country map, United States and Hong Kong emerged as the highest revenue-generating markets, suggesting these regions have the highest brand penetration.

●	Markets like Pakistan showed steady growth but lower total volume, identifying them as prime candidates for targeted marketing campaigns.

●	The Treemap and Revenue by Type visuals clearly show that Eau De Toilette and Eau De Parfum account for over 60% of total revenue.

●	Through the Gender Slicer, we discovered that the Women’s segment drives significantly higher volume in "Parfum" categories, while the Men’s segment prefers "Toilette" and "Cologne" types.


## 🚀 Recommendations

●	The Price vs. Quantity sold analysis identified several high-demand items (High Sold Quantity) that are currently running on Low Available Stock, presenting a risk of lost revenue.

●	Certain high-priced items in the Bottom-Left of our scatter plot are not moving as quickly as expected, suggesting a need for seasonal discounts or promotional bundling.

●	There are no Women customers in Brazil, Poland, Israel and Portugal. Whereas there are no Men customers in Bulgaria, Japan and Pakistan.

●	Can start a targeted digital marketing campaign (social media ads) specifically for the "missing" gender in those countries.

●	Using Price vs. Popularity table can find our globally most popular product for that gender and test it in the new market at a discount.

## Conclusion

The integration of Excel and Power BI proved effective for end-to-end data analysis, from raw data to visual reporting.
