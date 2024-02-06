# Exploring Population Dynamics: A Python-based Analysis of Fertility and Life Expectancy Trends (1960-2013)

This project is designed to conduct a comprehensive analysis of fertility and life expectancy trends spanning the years 1960 to 2013. The primary goal is to leverage Python for advanced data manipulation, aiming to uncover valuable insights into population dynamics. The analysis will delve into potential economic and health impacts, investigate factors contributing to the aging population, and assess immigration needs.

Taking a more focused approach, the investigation will be specifically tailored to the country associated with my student ID as indicated in the metadata. This targeted analysis will offer a nuanced understanding of the region's fertility and life expectancy trends, providing valuable insights into the demographic landscape of the chosen country over the decades.

# Data

The data is stored within a directory, encompassing three Excel sheets: Country_Metadata, Fertility_Rate, and LifeExpectancy_At_Birth.

Country_Metadata: This workbook consist of the countries being used for analysis, the country code, student_id (the use will be discussed upon in later stages of this project), the region in which these countries are located, the income group of the countries and special notes regarding the countries.

Fertility_Rate: This workbook incorporates shared variables from country metadata and data spanning from 1960 to 2013, specifically focusing on fertility rates across the various countries.

LifeExpectancy_At_Birth: This workbook integrates shared variables from country metadata alongside life expectancy data for various countries, spanning the years 1960 to 2013.

# Questions the data will answer

I will build appropriate visuals for the problem set which specifically aims to address the following question.

-- How do the countries compare to the region it is apart of in terms of average fertility

-- How does Life expectancy change, decade to decade ?

-- Any relationship between Life Expectancy and Fertility ?

# Tools

The project utilized Python in Visual Studio Code and Microsoft Excel.

The libraries that will be loaded into pythone for this analysis are;
-- Pandas

-- Openpyxl (Microsoft Excel)

# Steps Followed

# Data Extraction and Transformation (Codes available in the Python code folder)

- Uploaded raw data to GitHub.
  
- Linked to Visual Studio Code and imported data using pandas and openpyxl.

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

