🛒 Supermarket Sales Exploratory Data Analysis (EDA)
📌 Project Description

This project focuses on performing Exploratory Data Analysis (EDA) on a supermarket sales dataset using Python. The analysis helps understand customer purchasing behavior, sales trends, branch performance, product category performance, and relationships between business variables.

The project uses powerful Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn to clean, process, analyze, and visualize the dataset.

The main objective is to extract meaningful business insights from raw sales data through statistical analysis and graphical visualizations.

🎯 Objectives of the Project
Perform data cleaning and preprocessing
Analyze customer purchasing patterns
Identify top-performing branches and product lines
Study revenue and gross income trends
Understand relationships between sales variables
Visualize insights using graphs and charts
Detect duplicates and missing values
Generate business insights from the dataset
📂 Dataset Information
Dataset Name:

supermarket_sales.csv

Dataset Contains:

The dataset contains transaction-level supermarket sales records including:

Invoice ID
Branch
City
Customer Type
Gender
Product Line
Unit Price
Quantity Purchased
Tax Amount
Total Sales
Date and Time
Payment Method
Cost of Goods Sold (COGS)
Gross Income
Customer Ratings
🛠️ Technologies & Tools Used
Technology	Purpose
Python	Programming Language
Pandas	Data manipulation and analysis
NumPy	Numerical operations
Matplotlib	Data visualization
Seaborn	Statistical visualization
Jupyter Notebook	Development environment
📚 Python Libraries Used
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

Optional libraries:

import calmap
from ydata_profiling import ProfileReport
🔍 Project Workflow

The project follows the complete Data Analysis lifecycle:

Importing libraries
Loading dataset
Basic data exploration
Data preprocessing
Handling missing values
Removing duplicates
Feature engineering
Univariate analysis
Bivariate analysis
Correlation analysis
Data visualization
Final business insights
📊 Step-by-Step Analysis Performed
1️⃣ Basic Data Exploration

The following operations were performed:

Displayed first 5 rows
Checked dataset dimensions
Examined column names
Inspected data types
Generated statistical summaries
Checked missing values
Key Findings:
Dataset contains 1003 rows and 17 columns initially.
Some missing values existed in:
Customer type
Product line
Unit price
Quantity
Dataset also contained duplicate rows.
2️⃣ Data Preprocessing
✔ Date Conversion

The Date column was converted into datetime format.

df['Date'] = pd.to_datetime(df['Date'])
✔ Time Conversion

The Time column was converted into datetime format.

df['Time'] = pd.to_datetime(df['Time'])
✔ Feature Engineering

New columns were created:

Column	Purpose
Month	Monthly analysis
Day	Day-wise analysis
Hour	Hourly sales analysis
3️⃣ Missing Value Treatment
Numerical Columns

Missing values were replaced using the column mean.

df[col] = df[col].fillna(df[col].mean())
Categorical Columns

Missing values were replaced using the mode.

df[col] = df[col].fillna(df[col].mode()[0])
Result

All missing values were successfully handled.

4️⃣ Duplicate Handling

Duplicate rows were identified and removed.

df = df.drop_duplicates()
Result
Initial rows: 1003
Final rows after removing duplicates: 1000
5️⃣ Univariate Analysis

Univariate analysis was performed to study individual variables.

✔ Customer Ratings Distribution
Visualizations Used:
Histogram
KDE Plot
Boxplot
Insight:
Ratings are approximately normally distributed.
Very little skewness observed.

Skewness value:

0.0095
✔ Quantity Distribution

The distribution of purchased quantity was analyzed using histograms.

Insight:
Most customers purchased medium quantities.
Quantity values are fairly distributed.
✔ Gender Distribution
Insight:
Male and female customers are almost equally distributed.
6️⃣ Branch-wise Sales Analysis

Total sales for each branch were calculated.

Sales by Branch:
Branch	Total Sales
A	106971
B	106837
C	110568
Insight:
Branch C generated the highest sales.
Sales differences between branches are small.
7️⃣ Product Line Analysis

Sales contribution by different product categories was analyzed.

Product Categories:
Fashion accessories
Food and beverages
Electronic accessories
Sports and travel
Health and beauty
Home and lifestyle
Insight:
Product lines contribute differently to revenue.
Some categories generate significantly higher sales.
8️⃣ Payment Method Analysis

Payment methods used by customers were analyzed.

Payment Distribution:
Ewallet
Cash
Credit card
Insight:
Ewallet and cash payments were used most frequently.
Credit cards were slightly less preferred.
9️⃣ Customer Type Analysis

Customer types analyzed:

Member
Normal
Insight:
Customer distribution between members and normal customers is balanced.
🔟 Gross Income vs Ratings Analysis

Scatterplot analysis was performed between:

Gross Income
Customer Ratings
Correlation Value:
-0.0385
Insight:
Very weak negative correlation exists.
Customer ratings do not strongly affect gross income.
1️⃣1️⃣ Time Series Analysis

Gross income trends over time were visualized using line plots.

Insight:
Gross income fluctuates daily.
Some days show noticeable sales spikes.
1️⃣2️⃣ Correlation Analysis

A correlation matrix and heatmap were generated for numerical columns.

Strong Positive Correlations Found:
Variables	Correlation
Total & Gross Income	Strong
Quantity & Total Sales	Strong
Tax & Gross Income	Strong
Weak Correlations:
Ratings with sales-related variables
📈 Visualizations Included

The project contains multiple visualizations:

Histograms
KDE plots
Boxplots
Scatterplots
Line charts
Countplots
Barplots
Heatmaps

These visualizations help in better understanding trends and patterns in the data.

⚠️ Challenges Faced
Module Error

The following error occurred:

ModuleNotFoundError: No module named 'calmap'
Solution

Installed the library using:

pip install calmap

The project was also successfully executed without this optional library.

📁 Project Structure
supermarket-sales-eda/
│
├── supermarket_sales.csv
├── eda_analysis.ipynb
├── README.md
├── requirements.txt
└── images/
▶️ How to Run the Project
Step 1: Clone Repository
git clone https://github.com/your-username/supermarket-sales-eda.git
Step 2: Navigate to Folder
cd supermarket-sales-eda
Step 3: Install Required Libraries
pip install pandas numpy matplotlib seaborn

Optional:

pip install calmap ydata-profiling
Step 4: Launch Jupyter Notebook
jupyter notebook
📌 Final Insights
✔ Customer Insights
Ratings are normally distributed.
Male and female customer participation is balanced.
✔ Business Insights
Branch C performed best in terms of revenue.
Product lines have different revenue contributions.
✔ Financial Insights
Total sales strongly impact gross income.
Quantity sold significantly affects revenue.
✔ Operational Insights
Payment methods are evenly distributed.
Revenue fluctuates across different days.
🔮 Future Enhancements

Future improvements planned for this project:

Create Power BI Dashboard
Build Tableau visualizations
Deploy using Streamlit
Add machine learning prediction models
Generate automated EDA reports
Create sales forecasting system
