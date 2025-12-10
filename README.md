<img width="500" height="333" alt="image" src="https://github.com/user-attachments/assets/dfdd5b5d-b7d3-4949-8424-d2138eccf549" />

# phonepe-data-analysis
Overview: This case study involves analyzing transaction data from the financial application PhonePe along with demographic data across various states and districts in India. The objective is to provide insights into transaction trends, device usage, and demographic correlations, while ensuring data consistency and performing advanced analyses to uncover deeper insights.

The datasets span multiple years and quarters, providing a comprehensive view of transactions, user behavior, and demographic details. Participants are expected to use their Python skills to load, explore, and analyze the data, ultimately deriving meaningful insights and visualizations.
 

Dataset Details:

The data is spread across multiple sheets in an Excel file, each containing different aspects of the transaction and demographic data. Below is an overview of each dataset:
 

Dataset (Open link in a new tab and download the dataset.)

 

This case study utilizes three key datasets, each providing daily updates on different aspects of the pandemic for various countries and regions:

State_Txn and Users: This dataset contains transaction and user data at the state level. It includes information on the number of transactions, total transaction amount, average transaction value, number of registered users, and app opens.
State_TxnSplit: This dataset provides a breakdown of transaction types at the state level. It includes information on different transaction types, the number of transactions, total transaction amount, and average transaction value for each type.
State_DeviceData: This dataset details the device brands used by registered users at the state level. It includes information on the number of registered users per device brand and the percentage of users using each brand.
District_Txn and Users: This dataset contains transaction and user data at the district level. It includes information on the number of transactions, total transaction amount, average transaction value, number of registered users, and app opens for each district.
District Demographics: This dataset provides demographic details for each district. It includes information on the population, area, population density, and district headquarters.
Data Dictionary:

Below is the data dictionary for the datasets used in this case study:

State_Txn and Users
State: Name of the state
Year: Year of the data
Quarter: Quarter of the year
Transactions: Number of transactions
Amount (INR): Total amount of transactions in INR
ATV (INR): Average transaction value in INR
Registered Users: Number of registered users
App Opens: Number of app opens
 
State_TxnSplit
State: Name of the state
Year: Year of the data
Quarter: Quarter of the year
Transaction Type: Type of transaction (e.g., Recharge & bill payments, Peer-to-peer payments)
Transactions: Number of transactions
Amount (INR): Total amount of transactions in INR
ATV (INR): Average transaction value in INR
 
State_DeviceData
State: Name of the state
Year: Year of the data
Quarter: Quarter of the year
Brand: Brand of the device
Registered Users: Number of registered users using the brand
Percentage: Percentage of registered users using the brand
 
District_Txn and Users
State: Name of the state
Year: Year of the data
Quarter: Quarter of the year
District: Name of the district
Code: District code
Transactions: Number of transactions
Amount (INR): Total amount of transactions in INR
ATV (INR): Average transaction value in INR
Registered Users: Number of registered users
App Opens: Number of app opens
 
District Demographics
State: Name of the state
District: Name of the district
Headquarters: District headquarters
Population: Population of the district
Area (sq km): Area of the district in square kilometers
Density: Population density
Code: District code
Alternate Name: Alternate name of the district
Based on the above, please solve the questions below. Please ensure to have fun and learn from this exercise. If you have difficulty solving some part, you can take help from your peers to solve it but ensure that you understand why you have applied a specific query as the interviewer might ask you to explain all or some parts of the code.


Task 1: Data Loading and Understanding

1.1: Load each dataset and display its structure

Load the State_Txn and Users dataset and display its first 5 rows.
Load the State_TxnSplit dataset and display its bottom 10 rows.
Load the State_DeviceData dataset and display 10 rows from the middle of the dataset.
Load the District_Txn and Users dataset and display its first 10 rows and last 10 rows.
Load the District Demographics dataset and display every 10th row.
 
1.2: Display basic statistics and data types for each dataset

For each dataset, display the summary statistics (mean, median, std, etc.) for numerical columns.
Display the data types of each column in each dataset.
 
1.3: Check for missing values

Identify any missing values in each dataset.
Calculate the percentage of missing values for each column that has missing values.
Highlight which column has the highest percentage of missing values in each dataset.
 
1.4: Create a summary

Calculate the total number of states and the total number of districts.
Identify the state with the highest number of districts. [hint: you can use value_counts() and idxmax()]
 
Task 2: Exploratory Data Analysis (EDA)

2.1: Analyze transaction trends over the years for each state

Calculate the total number of transactions and total transaction amount for each state over the years. Display the results in a tabular format.
Identify the top 5 states with the highest transaction volumes and the top 5 states with the lowest transaction volumes. Display the results.
 
2.2: Identify the most common transaction types in each state and quarter

For each state and quarter, determine the most frequent transaction type. Display the results in a tabular format.
 
2.3: Determine the device brand with the highest number of registered users in each state

Identify the device brand with the highest number of registered users in each state. Display the results in a tabular format.
 
2.4: Create a list of the top district per state based on population

For each state, identify the district with the highest population. Display the results in a tabular format.
Create a column chart depicting the district with the highest population for each state.
 
2.5: Calculate the average transaction value (ATV) for each state

Compute the average transaction value for each state. Display the results in a tabular format.
Identify the top 5 states with the highest ATV and the top 5 states with the lowest ATV. Display the results.
 
2.6: Analyze app usage trends

Calculate the total number of app opens over the years and quarters for each state. Display the results in a tabular format.
Identify trends in app usage by creating a line plot showing the number of app opens over time for a selected state.
 
2.7: Distribution of transaction types

Create a bar chart showing the distribution of different transaction types for each state for the most recent quarter in the dataset.
 
2.8: Find unique mapping between district name and district code

Identify the unique mapping between district names and district codes from the dataset. [hint: you can use drop_duplicates()] 
Create a CSV file containing the unique district name and district code mappings.
Export the CSV file.
 
Task 3: Data Quality Checks

3.1: Ensure data consistency across state and district levels

For each state, calculate the total number of transactions, total transaction amount, and total registered users by summing up the values from the district level data.
Compare the results with the corresponding values at the state level to ensure they match.
Display any discrepancies found between the district-level and state-level data.
 
Task 4: Data Merging and Advanced Analysis

4.1: Ratio of users to population by state

Merge the State_Txn and Users dataset with the District Demographics dataset to calculate the ratio of registered users to the population for each state. Display the results in a tabular format.
Create a column chart depicting the ratio of users to population by state.
 
4.2: Correlate population density with transaction volume

Merge the District_Txn and Users dataset with the District Demographics dataset.
Calculate the correlation between population density and transaction volume.
Create a scatter plot to visualize the correlation between population density and transaction volume.
 
4.3: Average transaction amount per user

Merge relevant datasets to calculate the average transaction amount per user for each state. Display the results in a tabular format.
Identify the top 5 states with the highest average transaction amount per user and the top 5 states with the lowest average transaction amount per user. Display the results.
 
4.4: Device brand usage ratio

Merge the State_DeviceData dataset with the State_Txn and Users dataset.
Calculate the ratio of users using each device brand to the total number of registered users in each state. Display the results in a tabular format.
Create a bar chart depicting the device brand usage ratio for each state.
 
Task 5: Data Visualization

5.1: Plot the total transactions and amount over time for a selected state

Create a line plot showing the total number of transactions and the total transaction amount over time (years and quarters) for a selected state. 
[Hint: you can select any state, maybe your home state or state with max transactions]
 

5.2: Create a pie chart showing the distribution of transaction types for a specific quarter

Create a pie chart showing the distribution of different transaction types for a selected state and quarter.
 
5.3: Visualize the population density of districts in a selected state

Create a bar plot showing the population density of districts in a selected state.
 
Task 6: Insights and Conclusions [Advanced Section] 

6.1: Identify any trends or patterns in the transaction data

Analyze the transaction data to identify any noticeable trends or patterns. Summarize your findings. [hint: you can create line graph – at year or quarter and discuss your findings with interviewer] 
 
6.2: Correlate demographic data with transaction data

Find correlations between demographic data (e.g., population density) and transaction data (e.g., transaction volume). Summarize your findings. [Hint: you can use corr()]
 
6.3: Summarize findings and insights

Summarize the key findings and insights from your analysis. Provide actionable recommendations based on the data. [Hint: type and print your recommendations and findings in the notebook. This is open ended]

