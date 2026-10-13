Project Details Repository Link
Project Report
CUSTOMER BEHAVIOR ANALYSIS FOR RETAIL BUSINESS
(Using Python, MySQL Workbench, and Power BI)
1. Abstract
Customer behavior analysis plays an important role in helping retail and e-commerce companies understand purchasing
trends, customer preferences, and business performance. This project focuses on analyzing customer transaction data to
uncover valuable business insights that can improve revenue generation, customer retention, and marketing
effectiveness.
The project involves data cleaning and exploratory data analysis using Python, storing and querying cleaned data using
MySQL Workbench, and developing interactive dashboards using Power BI. Various business questions related to
revenue generation, discounts, customer segmentation, subscription behavior, product performance, and demographic
contribution were analyzed.
The results of this project help businesses make data-driven decisions regarding inventory management, customer
targeting, discount optimization, and subscription strategies.
2. Introduction
In the modern retail industry, businesses generate huge volumes of customer transaction data daily. Analyzing this data
helps organizations understand customer purchasing behavior and improve operational efficiency.
Retail companies often face challenges such as:
• Low customer retention
• Ineffective marketing campaigns
• Poor understanding of customer demand
• Weak customer segmentation
• Inefficient discount strategies
This project aims to solve these business challenges by applying data analytics techniques using Python, MySQL
Workbench, and Power BI.
3. Problem Statement
The retail company wants to understand customer purchasing behavior to:
• Increase overall revenue
• Improve customer retention
• Optimize discount and promotional strategies
• Identify high-performing products and categories
• Understand customer demographics
• Improve subscription and loyalty programs
The company currently possesses raw transactional data but lacks meaningful insights that can support strategic
business decisions.
Project Details Repository Link
Saurabh Kumar (Click here to view All Projects) Follow me on:
4. Project Objectives
The main objectives of this project are:
1. Perform data cleaning and preprocessing using Python.
2. Conduct Exploratory Data Analysis (EDA).
3. Store cleaned data in MySQL Workbench.
4. Solve business problems using SQL queries.
5. Create interactive dashboards in Power BI.
6. Generate actionable business insights.
5. Tools & Technologies Used
Tool Purpose
Python Data Cleaning & EDA
Pandas Data Manipulation
NumPy Numerical Computation
Matplotlib & Seaborn Visualization
MySQL Workbench Database Storage & SQL Analysis
Power BI Dashboard & Reporting
CSV Dataset Data Source
6. Dataset Overview
The dataset used in this project is a structured retail/e-commerce dataset containing customer transaction information.
Dataset Characteristics
Feature Description
Type Retail / E-commerce
Nature Structured (Tabular)
Level Customer Transaction Level
Data Types
Numerical Columns
• Age
• Purchase Amount
• Previous Purchases
• Review Rating
Categorical Columns
• Gender
• Category
• Payment Method
• Season
Project Details Repository Link
• Subscription Status
• Shipping Type
7. Data Dictionary
Column Name Description
Customer ID Unique customer identifier
Age Age of customer
Gender Customer gender
Item Purchased Product purchased
Category Product category
Purchase Amount Amount spent
Location Customer location
Size Product size
Color Product color
Season Season of purchase
Review Rating Product rating
Subscription Status Subscription membership
Shipping Type Delivery method
Discount Applied Whether discount applied
Previous Purchases Past purchase count
Payment Method Payment mode
Frequency of Purchases Buying frequency
8. Methodology
The project followed the below workflow:
1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis
4. Data Export to MySQL Workbench
5. SQL Query Analysis
6. Power BI Dashboard Development
7. Business Insight Generation
9. Data Cleaning & Preprocessing using Python
The dataset contained inconsistencies, missing values, and duplicate records that required cleaning before analysis.
Project Details Repository Link
Saurabh Kumar (Click here to view All Projects) Follow me on:
9.1 Data Loading
The dataset was loaded using Pandas.
import pandas as pd
df = pd.read_csv("customer_shopping_behavior.csv")
9.2 Initial Data Exploration
The following functions were used:
df.head()
df.info()
df.describe()
df.isnull().sum()
Purpose:
• Understand dataset structure
• Identify missing values
• Check data types
• Detect inconsistencies
9.3 Category Consistency Correction
Incorrect category mappings between products and categories were identified and corrected using dictionary mapping.
Purpose:
• Improve analysis accuracy
• Ensure proper product categorization
9.4 Missing Value Handling
Size Column
Different strategies were used:
• Electronics → Not Applicable
• Accessories → Free Size
• Clothing → Mode value
Review Rating
Missing ratings were filled using product-level mean ratings.
Purchase Amount
Filled using average purchase amount.
Previous Purchases
Missing values replaced with 0.
Purpose:
• Preserve data quality
• Maintain realistic business logic
9.5 Duplicate Removal
Project Details Repository Link
Saurabh Kumar (Click here to view All Projects) Follow me on:
Duplicate customer records were identified and removed.
df.drop_duplicates(inplace=True)
Purpose:
• Prevent double counting
• Improve reporting accuracy
9.6 Column Standardization
df.columns = df.columns.str.replace(" ","_")
df.columns = df.columns.str.lower()
Purpose:
• SQL-friendly naming
• Easy Power BI integration
10. Data Export to MySQL Workbench
After cleaning, the processed dataset was exported to MySQL Workbench for SQL-based analysis.
Why MySQL Workbench?
• Easy database management
• Efficient SQL querying
• Better integration for analysis workflows
Connection Process
Python libraries used:
pip install mysql-connector-python sqlalchemy
Example connection:
from sqlalchemy import create_engine
engine = create_engine("mysql+mysqlconnector://root:password@localhost/customer_analysis")
df.to_sql("customer_data", engine, if_exists="replace", index=False)
11. Exploratory Data Analysis (EDA)
EDA was performed to identify patterns, trends, and relationships in customer purchasing behavior.
Main analysis areas:
• Revenue analysis
• Customer segmentation
• Product performance
• Discount impact
• Subscription analysis
• Age-group contribution
• Shipping behavior
12. Business Questions & SQL Analysis
12.1 Which category generates the highest revenue?
Electronics generated the highest revenue (~$486K).
Business Insight
Project Details Repository Link
Saurabh Kumar (Click here to view All Projects) Follow me on:
Electronics products contribute significantly to company revenue and should receive focused inventory and marketing
investment.
12.2 Are discounts increasing purchase value?
Customers using discounts spent more on average ($219) compared to non-discount purchases ($182).
Business Insight
Discount campaigns positively influence customer spending behavior.
12.3 Revenue by Gender
• Male: ~$391K
• Female: ~$352K
• Other: ~$251K
Business Insight
Male customers contributed the highest overall revenue.
12.4 Top Rated Products
Highest-rated products:
• Gloves
• Sandals
• Boots
Lowest-rated products:
• Phone
• Headphones
• Watch
Business Insight
High-rated products can be promoted more aggressively, while low-rated products may require quality improvement.
12.5 Subscription Analysis
Subscribed customers spend significantly more than non-subscribers.
Customer Type Avg Spend
Subscribers $270
Non-Subscribers $166
Business Insight
Subscription programs improve customer lifetime value.
12.6 Customer Segmentation
Project Details Repository Link
Customers were divided into:
• Loyal Customers
• Returning Customers
• New Customers
Results:
• Loyal Customers: 3085
• Returning Customers: 1354
• New Customers: 561
Business Insight
Loyal customers form the major revenue-driving segment.
12.7 Revenue Contribution by Age Group
Age Group Revenue
51+ Highest
36–50 Second Highest
26–35 Moderate
18–25 Lowest
Business Insight
Older customers contribute the highest revenue.
13. Power BI Dashboard
Interactive dashboards were created to visualize business insights.
Dashboard Features
• KPI Cards
• Revenue Analysis
• Category Analysis
• Customer Segmentation
• Shipping Insights
• Seasonal Analysis
• Payment Method Analysis
• Product Ratings
Key KPIs
KPI Value
Total Customers 5000
Unique Items 30
Project Details Repository Link
KPI Value
Total Spend 994K
Average Spend 198
Average Rating 3.62
14. Key Findings
1. Electronics is the highest revenue-generating category.
2. Discounts increase average purchase value.
3. Subscribers spend significantly more than non-subscribers.
4. Loyal customers contribute major repeat revenue.
5. Customers aged 51+ generate the highest revenue.
6. Standard shipping is the most frequently used shipping type.
7. Debit cards are the most preferred payment method.
15. Business Recommendations
Marketing Recommendations
• Increase targeted discounts for high-spending customers.
• Promote subscription programs aggressively.
Product Recommendations
• Invest more in electronics inventory.
• Improve quality of low-rated products.
Customer Retention Recommendations
• Reward loyal customers with exclusive benefits.
• Create personalized campaigns for returning customers.
Sales Strategy Recommendations
• Target older age groups with premium offerings.
• Optimize seasonal campaigns based on demand trends.
16. Conclusion
This project successfully analyzed customer purchasing behavior using Python, MySQL Workbench, and Power BI.
The analysis provided valuable insights into:
• Customer spending habits
• Product performance
• Discount effectiveness
• Customer loyalty
• Subscription behavior
The project demonstrates how data analytics can help retail businesses make smarter decisions, improve customer
retention, optimize marketing strategies, and increase profitability.
Project Details Repository Link

17. Future Scope
Future improvements may include:
• Machine Learning-based customer prediction
• Recommendation systems
• Sales forecasting
• Real-time dashboard integration
• Customer churn prediction
18. References
• Python Documentation
• Pandas Documentation
• MySQL Workbench Documentation
• Microsoft Power BI Documentation 
