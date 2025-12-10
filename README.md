
<img width="860" height="313" alt="image" src="https://github.com/user-attachments/assets/373328dc-9833-4da1-a07b-8f0f17ec4687" />

# **PhonePe Case Study – Comprehensive Data Analysis**

## **Overview**

This case study involves analyzing transaction data from the PhonePe digital payments platform along with demographic data across various states and districts in India. The aim is to uncover insights related to transaction behavior, device usage, population demographics, and correlations between financial activity and regional characteristics.

The datasets span multiple years and quarters, allowing a thorough exploration of user behavior, transaction trends, and demographic influences.
This project uses **Python** for data loading, exploration, cleaning, merging, and visualization.

---

# ** Dataset Details**

The data is provided through multiple sheets in an Excel file, covering different dimensions of transactions and demographics.

### **1. State_Txn and Users**

Contains state-level transaction and user data:

* Number of transactions
* Total transaction amount
* Average transaction value (ATV)
* Registered users
* App opens

### **2. State_TxnSplit**

Breakdown of transaction types at the state level:

* Transaction type
* Number of transactions
* Total amount
* Average transaction value

### **3. State_DeviceData**

Device usage at the state level:

* Device brand
* Number of registered users per brand
* Percentage usage

### **4. District_Txn and Users**

District-level transaction and user data:

* Transactions
* Transaction amount
* ATV
* Registered users
* App opens

### **5. District Demographics**

District-level demographic details:

* Population
* Area
* Density
* Headquarters
* District codes

---

# **Data Dictionary**

### **State_Txn and Users**

| Column           | Description                |
| ---------------- | -------------------------- |
| State            | Name of the state          |
| Year             | Year of data               |
| Quarter          | Quarter of the year        |
| Transactions     | Total transactions         |
| Amount (INR)     | Total transaction amount   |
| ATV (INR)        | Average transaction value  |
| Registered Users | Number of registered users |
| App Opens        | Total app opens            |

### **State_TxnSplit**

| Column           | Description               |
| ---------------- | ------------------------- |
| State            | Name of the state         |
| Year             | Year of data              |
| Quarter          | Quarter of the year       |
| Transaction Type | Type of transaction       |
| Transactions     | Number of transactions    |
| Amount (INR)     | Total transaction amount  |
| ATV (INR)        | Average transaction value |

### **State_DeviceData**

| Column           | Description            |
| ---------------- | ---------------------- |
| State            | Name of the state      |
| Year             | Year of data           |
| Quarter          | Quarter                |
| Brand            | Device brand           |
| Registered Users | Users using this brand |
| Percentage       | Percentage usage       |

### **District_Txn and Users**

| Column           | Description               |
| ---------------- | ------------------------- |
| State            | State name                |
| Year             | Year                      |
| Quarter          | Quarter                   |
| District         | District name             |
| Code             | District code             |
| Transactions     | Number of transactions    |
| Amount (INR)     | Total amount              |
| ATV (INR)        | Average transaction value |
| Registered Users | Registered users          |
| App Opens        | App opens                 |

### **District Demographics**

| Column         | Description             |
| -------------- | ----------------------- |
| State          | State name              |
| District       | District name           |
| Headquarters   | District HQ             |
| Population     | Total population        |
| Area (sq km)   | Area                    |
| Density        | Population density      |
| Code           | District code           |
| Alternate Name | Alternate district name |

---

# **Task Breakdown (All Questions Included)**

---

## **Task 1: Data Loading and Understanding**

### **1.1 Load datasets and inspect rows**

* Load State_Txn and Users → display first 5 rows
* Load State_TxnSplit → display last 10 rows
* Load State_DeviceData → display 10 middle rows
* Load District_Txn and Users → display first 10 and last 10 rows
* Load District Demographics → display every 10th row

### **1.2 Summary statistics + data types**

* Display mean, median, std for each dataset
* Display data types of all columns

### **1.3 Missing value analysis**

* Identify missing values
* Compute % missing per column
* Highlight column with highest missing %

### **1.4 Create summary**

* Count total states
* Count total districts
* Identify state with highest number of districts

---

## **Task 2: Exploratory Data Analysis (EDA)**

### **2.1 Transaction trends analysis**

* Total transactions & amount for each state over years
* Top 5 states with highest transaction volume
* Bottom 5 states with lowest volume

### **2.2 Most common transaction types**

* Identify most frequent transaction type per state & quarter

### **2.3 Device brand dominance**

* Device brand with the highest registered users per state

### **2.4 Top district per state (population)**

* Identify highest population district per state
* Create a column chart

### **2.5 Average Transaction Value (ATV)**

* Compute ATV for each state
* Top 5 highest ATV states
* Bottom 5 lowest ATV states

### **2.6 App usage trends**

* Total app opens per state over years and quarters
* Line plot for selected state

### **2.7 Distribution of transaction types**

* Bar chart for most recent quarter

### **2.8 Unique district code mapping**

* Create unique mapping using drop_duplicates()
* Export to CSV

---

## **Task 3: Data Quality Checks**

### **3.1 State–District consistency check**

For each state:

* Sum district-level transactions, amount, users
* Compare with state-level data
* Display mismatches

---

## **Task 4: Data Merging & Advanced Analysis**

### **4.1 Ratio of users to population**

* Merge State_Txn with Demographics
* Compute user-to-population ratio
* Column chart

### **4.2 Correlation: population density vs transaction volume**

* Merge District_Txn with Demographics
* Compute correlation
* Scatter plot

### **4.3 Average transaction amount per user**

* Merge datasets
* Compute average amount per user
* Top 5 & bottom 5 states

### **4.4 Device brand usage ratio**

* Merge State_DeviceData with State_Txn
* Compute brand usage ratio per state
* Create bar chart

---

## **Task 5: Data Visualization**

### **5.1 Transactions & amount over time**

* Line plot for selected state (based on years + quarters)

### **5.2 Transaction type distribution (pie chart)**

* For selected state + quarter

### **5.3 Population density visualization**

* Bar plot of population density for districts in selected state

---

## **Task 6: Insights & Conclusions (Advanced)**

### **6.1 Trend identification**

* Analyze long-term transaction trends
* Summarize findings

### **6.2 Demographic correlation**

* Correlate population density with transaction volume
* Discuss insights

### **6.3 Final conclusions**

* Key findings
* Actionable recommendations
* Summary of learning

---

