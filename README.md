Exploratory Data Analysis (EDA) on Sales Dataset 📊🛒
Project Overview
This project performs an in-depth Exploratory Data Analysis (EDA) on a sales dataset using Python and its data science ecosystem. The dataset consists of transaction-level purchase details, customer demographics, product categories, and location-based sales insights. Through statistical analysis, data visualization, and feature engineering, we uncover meaningful insights into customer behavior, product trends, and sales performance.

🔍 Objectives of the Project
Data Preprocessing & Cleaning

Handling missing values in categorical and numerical columns.
Removing duplicate entries and inconsistencies.
Encoding categorical variables for better model compatibility.
Standardizing and scaling numerical variables for improved data distribution.
Exploratory Data Analysis (EDA)

Descriptive Statistics: Understanding data distribution, skewness, and kurtosis.
Correlation Analysis: Identifying relationships between key features.
Customer Segmentation: Analyzing user purchase behavior based on demographics.
Sales Trends: Understanding the impact of time, age groups, and city categories.
Feature Engineering

Product Popularity Analysis: Identifying best-selling products.
User Purchase Behavior: Analyzing how users interact with different products.
Purchase Patterns: Creating aggregated purchase metrics per product and user.
Data Visualization for Insights

Sales Trends Over Time (if timestamp is available).
Distribution of Purchase Amounts using histograms and KDE plots.
Purchase Behavior by Age, Gender, and City using boxplots and bar charts.
Top-selling Products and Categories using bar charts and heatmaps.
📂 Dataset Overview
The dataset contains the following key attributes:

Feature	Description
User_ID	Unique identifier for each customer.
Product_ID	Unique identifier for each product.
Gender	Gender of the customer (M/F).
Age	Age group of the customer.
City_Category	City classification (A, B, C).
Stay_In_Current_City_Years	How long the user has lived in their current city.
Product_Category_1, 2, 3	Categorical product classification.
Purchase	Purchase amount in monetary units.
📊 Data Cleaning & Processing Steps
1️⃣ Handling Missing Values
Missing Values in Product_Category_2 & Product_Category_3 were imputed using mode values since they are categorical.
Duplicates were checked and removed where necessary.
2️⃣ Encoding Categorical Variables
Gender: Converted to binary (Male → 1, Female → 0).
Age: Mapped into ordered numerical categories (e.g., 0-17 → 1, 18-25 → 2, etc.).
City_Category: Mapped into numerical values (A → 1, B → 2, C → 3).
Stay_In_Current_City_Years: Converted into integer values.
3️⃣ Feature Engineering
Total_Product_Categories: Number of unique product categories per user.
Purchase_Per_Product: Average purchase amount per product.
Purchase_Per_User: Average purchase per user.
User_Purchase_Count: Total purchases made by each user.
User_Age_Category: Unique combination of User ID and Age group.
4️⃣ Normalization & Scaling
Applied StandardScaler to Purchase, Product_Category_1, Product_Category_2, and Product_Category_3.
Used MinMaxScaler to normalize purchase amounts for better visual representation.
📈 Data Visualization & Insights
1️⃣ Missing Values Heatmap
📌 Objective: To visualize missing data across all columns.
✅ Finding: Missing values were only present in Product_Category_2 and Product_Category_3.

2️⃣ Purchase Distribution Analysis
📌 Objective: To understand how purchase values are distributed.
📊 Visualization: Histogram & KDE plot.
✅ Finding: Purchase amounts show a right-skewed distribution, indicating most purchases are on the lower side.

3️⃣ Correlation Matrix Heatmap
📌 Objective: To identify relationships between numerical features.
📊 Visualization: Correlation heatmap with sns.heatmap().
✅ Finding: Product_Category_1 had a stronger impact on purchase behavior than Product_Category_2 & Product_Category_3.

4️⃣ Age vs Purchase Boxplot
📌 Objective: To analyze the impact of age groups on spending.
📊 Visualization: Boxplot comparison of Age and Purchase.
✅ Finding: The 26-35 age group had the highest median purchase values.

5️⃣ Gender Distribution Analysis
📌 Objective: To compare male vs female buyers.
📊 Visualization: Countplot for gender distribution.
✅ Finding: The dataset is highly imbalanced towards male shoppers.

6️⃣ City Category Analysis
📌 Objective: To analyze sales performance across different city categories.
📊 Visualization: Countplot for city categories.
✅ Finding: Most purchases originated from City Category B.

7️⃣ Purchase Trends Over Time (if timestamp available)
📌 Objective: To analyze purchase patterns over months.
📊 Visualization: Time-series line plot using resample('M').
✅ Finding: There are clear seasonal trends in purchase behavior.

8️⃣ Product Popularity Analysis
📌 Objective: To determine the most frequently bought products.
📊 Visualization: Bar plot for top 20 purchased products.
✅ Finding: A few products account for the majority of purchases.

9️⃣ User Purchase Behavior by City
📌 Objective: To compare spending across city categories.
📊 Visualization: Boxplot of City_Category vs Purchase.
✅ Finding: City B had the highest median purchase amounts.

🔟 Pairplot for Feature Interaction
📌 Objective: To explore relationships between key variables.
📊 Visualization: Seaborn pairplot() on selected features.
✅ Finding: The Purchase feature interacts heavily with Age, City_Category, and Product_Category_1.

🛠️ Technologies & Tools Used
Python: pandas, numpy, matplotlib, seaborn, sklearn, scipy
Data Preprocessing: Handling missing values, encoding categorical variables, feature engineering.
Data Visualization: Heatmaps, histograms, boxplots, bar charts, pair plots.
Statistical Analysis: Skewness, kurtosis, correlation matrix.
📌 Key Takeaways
✅ Most purchases were made by males from City B.
✅ The 26-35 age group had the highest median purchase amounts.
✅ Product_Category_1 had the strongest impact on total purchase behavior.
✅ Sales exhibit seasonal trends, indicating promotional campaigns or festive periods.
✅ Most popular products contribute significantly to overall revenue.

🚀 Future Scope
Perform Machine Learning Models for sales prediction.
Identify customer segments for personalized marketing strategies.
Implement Deep Learning-based recommendations for better user engagement.
