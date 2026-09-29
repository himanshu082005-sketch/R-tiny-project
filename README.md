# R-tiny-project
Project Overview

This project performs a basic exploratory analysis of a bank customer dataset using R and R Markdown. The dataset is named Bank_Churn.csv and contains customer information such as credit score, geography, gender, age, tenure, balance, number of products, credit-card status, active-member status, estimated salary, and whether the customer exited the bank.

The analysis is presented through an R Markdown document and rendered as an HTML/PDF report.

Dataset

The project uses the following dataset:

• File: Bank_Churn.csv
• Observations: 200
• Variables: 13

Variables

|Variable         |Description                             |
|-----------------|----------------------------------------|
|`CustomerId`     |Unique customer identifier              |
|`Surname`        |Customer surname                        |
|`CreditScore`    |Customer credit score                   |
|`Geography`      |Customer country/geography              |
|`Gender`         |Customer gender                         |
|`Age`            |Customer age                            |
|`Tenure`         |Number of years associated with the bank|
|`Balance`        |Customer account balance                |
|`NumOfProducts`  |Number of bank products used            |
|`HasCrCard`      |Whether the customer has a credit card  |
|`IsActiveMember` |Whether the customer is an active member|
|`EstimatedSalary`|Estimated customer salary               |
|`Exited`         |Whether the customer exited the bank    |

The project report shows that the Exited variable has a mean of 0.185, meaning 18.5% of the 200 records are marked as exited in this dataset. fileciteturn2file0L488-L494

Objectives

The main objectives of the project are:

1. Load the bank customer churn dataset into R.
2. Inspect the structure and summary of the dataset.
3. Check for missing values.
4. Calculate basic descriptive statistics.
5. Examine gender and active-member distributions.
6. Visualize customer credit scores.
7. Examine the relationship between active membership and balance.
8. Perform basic exploratory analysis of customer churn-related information.

R Packages / Tools

The analysis is based on base R functions and R Markdown, including:

• read.csv()
• head()
• summary()
• str()
• colSums()
• median()
• var()
• sd()
• table()
• pie()
• barplot()
• cor()

The original report identifies the document as an R Markdown project and loads the dataset with read.csv(). fileciteturn2file0L10-L21

Data Inspection

The dataset structure contains 200 observations and 13 variables. Numeric fields include CustomerId, CreditScore, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, and Exited; Surname, Geography, and Gender are character fields. fileciteturn2file0L495-L510

Missing-Value Check

The project uses:

colSums(is.na(Bank_Churn))

The report shows zero missing values for all 13 variables. fileciteturn2file0L511-L520

Descriptive Statistics

Some reported statistics include:

• Mean Credit Score: 644.3
• Median Credit Score: 643
• Minimum Credit Score: 429
• Maximum Credit Score: 850
• Mean Age: 38.22
• Median Age: 37
• Mean Tenure: 5.07
• Median Tenure: 5
• Mean Balance: 77,942
• Median Balance: 98,284.43
• Mean Estimated Salary: 103,988.6
• Mean IsActiveMember: 0.47
• Mean Exited: 0.185 fileciteturn2file0L467-L494

The project also reports:

Median Balance = 98284.43
Variance of Balance = 4003826295
Standard Deviation of Balance = 63275.8

fileciteturn2file0L521-L526

Gender Distribution

The dataset contains:

• Female: 91
• Male: 109

The project visualizes this distribution using a pie chart. fileciteturn2file0L527-L539

Visualizations

The R Markdown report includes visualizations for:

• Gender distribution
• Bank member/activity distribution
• Customer credit scores
• Bank active-member information

The project uses pie() and barplot() for these visualizations. fileciteturn2file0L532-L563

Correlation Analysis

The project calculates the correlation between IsActiveMember and Balance:

cor(
  Bank_Churn$IsActiveMember,
  Bank_Churn$Balance
)

The reported correlation is:

0.05032984

This is a small positive correlation in the analyzed dataset. fileciteturn2file0L577-L582

Project Structure

Tiny-Project/
│
├── Bank_Churn.csv
├── projecth.Rmd
├── projecth.html
├── Tiny_project.pdf
└── README.md

How to Run the Project

1. Install R.
2. Install RStudio if required.
3. Place Bank_Churn.csv in the same project folder as the R Markdown file.
4. Open projecth.Rmd in RStudio.
5. Make sure the CSV file path in the R code points to the correct location.
6. Click Knit to generate the report.

For example:

Bank_Churn <- read.csv("Bank_Churn.csv")
Bank_Churn

Using a relative file path such as Bank_Churn.csv is recommended when all project files are kept in the same folder.

Conclusion

This project demonstrates a basic exploratory analysis of bank customer data using R and R Markdown. It covers data loading, structure inspection, summary statistics, missing-value checking, categorical distributions, visualizations, and a simple correlation analysis.

The dataset contains 200 customer records with 13 variables, and the analysis provides an initial view of customer characteristics and churn-related information. fileciteturn2file0L495-L510
