# Study on Trends in Fertility and Life Expectancy in Canada Over the Decades

This project aims to analyze the trends in fertility and life expectancy rates in Canada from 1960 to 2013. The objective is to utilize Python for data manipulation and employ Power BI for visualization to provide insights into population dynamics, potential economic and health impacts, explanations for the aging population, and immigration needs.

# Data

The data sources are contained in a folder with three Excel sheets: Country_Metadata, Fertility_Rate, and LifeExpectancy_At_Birth.

# Tools

The project utilized Python in Visual Studio Code, Microsoft Excel, Power Query, and Power BI.

# Steps Followed

# Data Extraction and Transformation (Codes available in the Python code folder)

- Uploaded raw data to GitHub.
  
- Linked to Visual Studio Code and imported data using pandas, numpy, and openpyxl.

- Set maximum columns and created dataframes for each Excel sheet.

- Utilized islice from itertools for various transformations.

- Performed actions such as creating headers, resetting index, changing column names, melting columns, converting types, merging, creating new columns, and 
  calculating averages.

- Saved the transformed dataframes in Excel format for local download.

  The resulting dataframes are df_region, df_country, and df_canada.

# Data Loading into Power BI

- Imported the created dataframes into Power BI.

- Used Power Query for basic editing like decimal reduction and removing index columns.

- In Power BI:

  1. Utilized a line graph to depict the trend of fertility and life expectancy over the years.
  2. Employed scorecards to display the averages of life expectancy and fertility.
  3. Generated visuals comparing North America's average fertility rate and life expectancy to Canada's.
 
# Outcome
The analysis reveals a decline in fertility rates and an increase in life expectancy in Canada. Fertility dropped from 3.81 in 1960 to 1.61 in 2013, averaging 1.96 over the period, compared to North America's 2.02. Life expectancy in Canada increased from 71.13 in 1960 to 81.40 in 2013, averaging 76.32, compared to North America's 75.64. This trend contributes to Canada's demographic structure with more aged individuals than young ones and emphasizes the country's high immigration requirements. Future analyses may incorporate additional data, such as medical, education, and economic indicators, using advanced statistical tools to explore correlations, make predictions, and offer recommendations.   

