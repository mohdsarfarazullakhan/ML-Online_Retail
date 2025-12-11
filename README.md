# ML-Online_Retail

**Online Retail Customer Segmentation and RFM Analysis**

Machine Learning and Business Analytics Project

This project analyzes the Online Retail Dataset and performs data cleaning, exploratory analysis, and customer segmentation using the RFM (Recency, Frequency, Monetary) model. The notebook includes preprocessing, visualization, feature engineering, and clustering.


**Project Overview**

This notebook performs the following tasks:

Load and inspect the online retail dataset

Clean missing values and duplicates

Exploratory data analysis

Compute RFM metrics for each customer

Apply clustering for customer segmentation

Visualize distributions and correlation patterns

**Workflow Details**

1. Data Loading

The dataset is loaded using:

df = pd.read_excel("Online_Retail.xlsx")

2. Data Inspection

The notebook checks:

Data types

Missing values

Duplicate rows

These steps help identify issues in the dataset prior to analysis.

3. Exploratory Data Analysis

Includes:

Summary statistics

Correlation matrix for numerical features

Distribution plots

Customer behavior insights

numeric_df = df.select_dtypes(include=[np.number])
corr = numeric_df.corr()
sns.heatmap(corr, annot=True, fmt=".2f")

4. Data Cleaning

Conversion of InvoiceDate to datetime

Removal of invalid records (returns, negative quantities if necessary)

Handling missing CustomerID

5. RFM Feature Engineering

The notebook calculates:

Recency: Days since last purchase

Frequency: Total number of invoices

Monetary: Total purchase amount

RFM table is merged back with the main dataset for analysis.

6. Customer Segmentation

Clustering (typically KMeans) is performed using RFM features to identify key customer groups.

**Requirements**

Add the following to requirements.txt:

pandas
numpy
matplotlib
seaborn
scikit-learn
openpyxl
