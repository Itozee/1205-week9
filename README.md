# Exploring Population Dynamics: A Python-based Analysis of Fertility and Life Expectancy Trends (1960-2013)

This project is designed to conduct a comprehensive analysis of fertility and life expectancy trends spanning the years 1960 to 2013. The primary goal is to leverage Python for advanced data manipulation, aiming to uncover valuable insights into population dynamics. The analysis will delve into potential economic and health impacts, investigate factors contributing to the aging population, and assess immigration needs.

Taking a more focused approach, the investigation will be specifically tailored to the country (Swaziland) associated with my student ID (100871852) as indicated in the metadata. This targeted analysis will offer a nuanced understanding of the region's fertility and life expectancy trends, providing valuable insights into the demographic landscape of the chosen country over the decades.

# Data

The data is stored within a directory, encompassing three Excel sheets: Country_Metadata, Fertility_Rate, and Life Expectancy_At_Birth.

Country_Metadata: This workbook consist of the countries being used for analysis, the country code, student_id (the use will be discussed upon in later stages of this project), the region in which these countries are located, the income group of the countries and special notes regarding the countries. Metadata refers to data that provides information about other data. In other words, it is data about the information provided in the fertility and life expectancy worksheets.

The columns in this dataset include;

-- Country Name: The entries in this column correspond to various countries.

-- Country Code: The entries in the column correspond to three-letter codes representing their respective countries.

-- Student ID: This represents the student id of each students in my class taking the course.

-- Region: This represents the regions where each countries are located in the world. ie Sub-Saharan Africa

-- Income Group: This denotes the economic classification of countries based on their present Gross Domestic Product (GDP)

-- Special Notes: This represents some additional written information about the countries.

Fertility_Rate: This workbook incorporates shared variables from country metadata and data spanning from 1960 to 2013, specifically focusing on fertility rates across the various countries.

The columns in this dataset include;

-- Country Name: The entries in this column correspond to various countries.

-- Country Code: The entries in the column correspond to three-letter codes representing their respective countries.

-- Indicator Name: The column communicates that the data relates to total fertility rate, specifically measured in "births per woman."

-- rom the year 1960 to 2013, data is available for each country, representing the recorded fertility rates for each respective year.


LifeExpectancy_At_Birth: This workbook integrates shared variables from country metadata alongside life expectancy data for various countries, spanning the years 1960 to 2013.

The columns in this dataset include;

-- Country Name: The entries in this column correspond to various countries.

-- Country Code: The entries in the column correspond to three-letter codes representing their respective countries.

-- Indicator Name: The column communicates that the data relates to life expectancy age, specifically measured in "years."

-- From 1960 to 2013, data is available for each country, representing recorded life expectancy values for each respective year


# Questions the data will answer

I will create targeted visualizations to address the following questions within the problem set

-- Bar chart showing how Swaziland (country associated with my student ID) is compared to its region(Sub-Sharan Africa) in terms of average fertility


-- Bar chart showing how Swaziland (country associated with my student ID) is compared to its region(Sub-Sharan Africa) in terms of average Life expectancy


-- Line Chart showing how Life expectancy in Swaziland change from decade to decade ?


-- Scatterplot showing relationship between Life Expectancy and Fertility in Swaziland?


# Tools

The project utilized Python in Visual Studio Code and Microsoft Excel.

The libraries that will be loaded into python for this analysis are;

-- Pandas: The pandas library in Python is a powerful and widely used open-source data manipulation and analysis library. It provides data structures for efficiently storing and manipulating large datasets, along with tools for cleaning, aggregating, and analyzing data.


-- Openpyxl (Microsoft Excel): This library is used for working with Excel files in Python.


-- Matplotlib: Provides a wide variety of static, animated, and interactive plots and charts for analyzing and presenting data. Matplotlib is highly customizable and can be used to create publication-quality figures in various formats.

 We also used some modules imported from the openpyxl library, the modules used are;

-- from openpyxl import Workbook

-- from openpyxl.utils.dataframe import dataframe_to_rows

-- from openpyxl.chart import BarChart, Series, Reference

I plan to elaborate on the utilization of these modules when I begin implementing them during the course of the project.


# Steps Followed

# Data Extraction and Transformation (Codes available in the Python code folder)

- Uploaded the raw data(Metadata, Fertility and Life expectancy files) to GitHub.
  
- Linked the datasets to Visual Studio Code and imported data using pandas and openpyxl.
  
- I Set the maximum number of columns to 500 when showing a DataFrame.

# Functions

I started by creating Functions to read the datasets and access the worksheets in Excel format after which was stored in a dataframe.

Functions in Python serve several crucial purposes, some of the reasons why i have used a function for the purpose stated above include;

Modularity: It allow me to break down a program into smaller, more manageable, and reusable pieces of code. 

Abstraction: Functions provide a level of abstraction, allowing me to use code without needing to understand its internal details. Abstraction allows you to hide the complex inner workings of a function. When you call a function, you don't need to know how it accomplishes its task; you only need to know what the function does and how to use it.

Readability: Well-named functions enhance code readability by providing a clear and concise way to express the purpose of a block of code. This is especially important in larger programs.

# Transformations
--Melt
Our datasets (Fertility and Life Expectancy) consists of columns representing the values recorded for years 1960 to 2013. This wide-format isn't ideal for analysis so I used the melt function in converting into long-format data. The other columns will remain unpivoted.

melted_fertility and melted_life_expectancy became the new dataframes showing the effect of the melt meaning df_fertility and df_life_expectancy dataframes would be disregarded for ongoing analysis.

-- About Melt
In Python, the pd.melt() function is used to reshape or transform a DataFrame. The basic idea is to unpivot or melt the DataFrame, moving the columns (except for the specified identifier variables) into two columns: one for variable names and another for the corresponding values. This can be helpful in scenarios where you have data in a format where variables are spread across columns, and you want to reorganize it for analysis or visualization.

-- Datatype
I observed the datatype for the year column was operated as a float for both melted_fertility and melted_life_expectancy. I converted the datatype for both dataframes into Integer. 

-- Merge
When working with real-world datasets, information is often split across multiple tables. pd.merge() helps integrate this information into a single, unified view. The use of a merge will help us better analyse and visualize to give us insights about the datasets. We have three datasets (Df_metadata, melted_fertility and melted_life_expectancy) in their respective dataframes and the information in them relate with each other. To perform a join, we need to have a matching column that is with common identifier with the dataframes/datasets. Country code and Country name are unique columns present in all. I merged with the country code as it reprsented thr best keys to match with.

I first merged df_metatdata with melted_fertility dataframes into a dataframe called first_merge then merged first_merge dataframe with melted_life_expectancy into a second_merge dataframe. The second_merge dataframe now consists of all the information found in df_metatdata, melted_fertility and melted_life_expectancy dataframes.

At this stage, we can now perform various indept analysis on the second_merge table/dataset/dataframe to get insights about our data.

-- Filter
Similar to the 'WHERE' clause on SQL, I filtered the data to show on the country associated with my student ID (100871852). This will show me only the records related to Swaziland as  the country associated to my student ID. This is reflected in the df_studentid dataframe

It is important to know that every transformations con be contained in a new dataframe and that dataframe could be used for further insights.


Some analysis that were further done, to answer question questions 1 and 2 are;

# Question 1

-- Average fertility and life expectancy rate for Swaziland

-- Average fertility and life expectancy for all countries in Sub-Saharan region where Swaziland is in

I joined both dataframes using pd.concat. The pd.concat() function in pandas is used to concatenate two or more pandas objects along a particular axis. The objects can be DataFrames or Series. The concatenation process essentially combines the rows or columns of these objects to create a new object. The key parameters for pd.concat() are objs, axis, and ignore_index.

I also had to ensure that both analysis (Average for Swaziland and Sub-Saharan region) had a similar key (column) before using the cconcat function. The original keys were 'Country name' for Swaziland and 'Region' for Sub-Saharan region. Both dataframs column was changed to location.

This allowed to create bar charts showing us the average fertility and life expectancy statistic of Swaziland compared to Sub-saharan region.


# Question 2

From the df_studentid dataframe, I extracted the Country Name, Fertility, Life Expectancy, YearR columns and its records into a second_studentid dataframe.

I've implemented code to generate a new column named 'Decade,' wherein each statistic is assigned a numeric value representing the corresponding decade. all this was effected in a new dataframe called third_sudentid

This enabled me to calculate the average life expectancy for each decade, spanning from the 1960s to the 2000s, using the 'groupby' operation.

This enabled the generation of a line chart illustrating the average life expectancy across the years.


# Question 3
Using the second_studentid dataframe and the help of matplotlib, I wrote code to show the correlation between the fertility rate and life expectancy rate in Swaziland.


# Leassons Learnt from this project

- Performed actions such as resetting index for any dataframe i work with, changing column names, The concept of Functions, Merging dataframes, and creating new columns. 

- The use of iloc (integer-location)
When performing the groupby function to get the averages of ferility and life expectancy in all the regions. I specifically wanted the output to show the average for Subsharan region. Using the reset index for a dataframe allows for integer-location based indexing allowing me to select specific rows and columns using integer indices.
All the regions are presented but using iloc[[6]] gives you the oppourtunity to select only the record that relates to Sub-Sharan Africa.

- The use of loc (label-based location)
I utilized .loc when i generated a new column named 'Decade' and assigned values. .loc is a label-based selector. It is used when you want to select data based on labels(columns) or/and conditions.

- Exploring Openpyxl for Excel has been a novel experience. Leveraging Python for data transformations and analysis not only saved time but also proved to be an efficient and streamlined process.

# Outcome
The analysis reveals a decline in fertility rates and an increase in life expectancy in Canada. Fertility dropped from 3.81 in 1960 to 1.61 in 2013, averaging 1.96 over the period, compared to North America's 2.02. Life expectancy in Canada increased from 71.13 in 1960 to 81.40 in 2013, averaging 76.32, compared to North America's 75.64. This trend contributes to Canada's demographic structure with more aged individuals than young ones and emphasizes the country's high immigration requirements. Future analyses may incorporate additional data, such as medical, education, and economic indicators, using advanced statistical tools to explore correlations, make predictions, and offer recommendations.   

