# Online Shopping Dataset - Data Analysis

## About the Project 📊
This project analyzes the Online Shopping Dataset to explore and understand customer behavior. It involves handling missing data, cleaning the dataset, performing statistical analyses, and creating visualizations to derive meaningful insights.

## Table of Contents 📂
Key Features <br />
Technologies Used <br />
Dataset Description <br />
Data Preprocessing and Analysis <br />
Results <br />
Kaggle Notebook

## ✨ Key Features

- Missing Value Handling: <br />
Identification and imputation of missing data using forward fill (ffill) and other custom strategies.<br />

- Feature Engineering: <br />
  - Creation of new features such as Total Prices and Total Spend. <br />
  - Mapping and filling missing SKU, Product Description values using a group-based dictionary.

- Data Visualization:
  - Missing value heatmaps and bar charts using missingno.

- Data Cleaning:
  - Dropping irrelevant columns.
  - Ensuring the dataset is consistent and ready for advanced analysis.

## 🛠️ Technologies Used
- Programming Languages: Python
- Libraries:
  - pandas: Data manipulation and analysis
  - numpy: Numerical operations
  - matplotlib and seaborn: Data visualization
  - missingno: Visualization of missing data
  - calendar: Handling and formatting date-related data

## 📊 Dataset Features
### The dataset includes the following information:

- CustomerID: Customer ID
- Gender: Customer Gender
- Product_SKU: Product Stock Code
- Avg_Price: Average Product Price
- Quantity: Quantity of Product Purchased
- Offline_Spend and Online_Spend: Online and offline spending
- Delivery_Charges: Delivery Charges
- Transaction_Date: Transaction Date <br />
There are 20+ columns and 10000+ rows in total.

## 🔍 Data Preprocessing and Analysis 
- Handling Missing Values:
  - Bar plots and heatmaps reveal missing value distribution.
  - Methods such as fillna (forward fill) and custom mapping functions are used for imputation.
  
- Feature Engineering:
New columns like Total Prices (calculated from price and quantity) and Total Spend (offline + online spend) are added.

- Cleaning:
Unnecessary columns (e.g., Unnamed: 0) are removed for clarity.

- Visualization:
  - Heat map and bar charts of missing values.
  - Grouping and visualization of spending trends on a monthly basis.
 
## 📊 Results
### Missing Values
The missing values was succseffuly integrated to data.  <br />
To deal with missing values several methods were used:
  - For IDs: random numbers are generated to fill missing values.
  - The box-plots generated to determine wheter to use mean values or medians for numerical data (if there is outliers median value is used, otherwise mean value is used to fill NaN values).
  - For categorical variables mode of the data is used to fill NaN values, with some exceptions:
    - For Product_SKU and Product_Description, when data examined these two categories were related therefore a method is defined to fill the NaN values.
   
  ### Data Analysis
- Histograms are used to visualize the distribution of a single variable by dividing the data into intervals (bins) and counting the number of observations that fall into each bin. They provide a clear way to understand the underlying frequency distribution of data, making it easier to observe patterns, trends, and outliers.  <br />
In this data the histograms gave informations about spending habits, pricing and quantity.
- Spending Habits: Both Offline_Spend and Online_Spend indicate a skew toward lower spending.
- Pricing: The Avg_Price distribution suggests that lower-priced products are more common.
- Quantity: Most transactions involve low item counts.
![image](https://github.com/user-attachments/assets/6f2161a5-b605-41d9-a893-dc74a35e8b24)

- Boxplot summarize the distribution of a dataset visually by showing its central tendency, spread, and potential outliers. They provide a quick snapshot of data variation and symmetry. <br />
Here it is observed that Total Prices has so many outliers, which is after cleaned and the cleaned version of the data used in next steps.
![image](https://github.com/user-attachments/assets/6fca421e-0c42-4680-8ce7-d232be41543e)

- Bar charts prepared for showing top 10 products that have been purchased the most, measured by the total quantity sold. <br />
As result the top product was "Google 22 oz Water Bottle". <br />
This charts can give idea about sales strategy insight which can focus promotional campaigns or ensuring stock availability for these high-demand products could maximize sales and customer satisfaction. <br />
This type of analysis can help bussinesses identiy their most popular products.

-Gender based analysis done with both piechart and bar graphs. It showed that female customers are the primers buyers in the dataset. The most purchased product by women is "Maze Pen", closely followed by "Google 22 oz Water Bottle". <br />
This type of analysis can give an idea about buying trends based on gender. 

- Product category frequency analysis is done. This analysis can highlight key trends in product category.

- Monthly Spending Analysis (Total, Online, and Offline) is done. This analysis provides insights into spending behaviors across months and channels, allowing businesses to align operations and marketing strategies.

- Correlation Matrix: <br />
![image](https://github.com/user-attachments/assets/f3b3ea0f-8fca-4598-92df-221f405d2441) <br />
This heatmap visualizes the pairwise correlations between numerical columns in the dataset. The strength and direction of the correlation are represented by the colors and values in the matrix. <br />
This matrix provides insights into the relationships between variables, enabling data-driven strategies for revenue optimization.

### Feature Engineering
Feature engineering is the process of selecting, modifying, or creating new features (variables) from raw data to improve the performance of a machine learning model.  <br />
In this study the analysis also indicates a feature engineering. For a market it is importent to know the best product, the best audience and the best time for taking accounts to gain more and satisfying the customer.  <br />
In a story such as to improve the gain of the market the following features should also be known.
- total spend by category: Understanding spending habits across product categories.
- Coupon Status: Analyzing the impact and utilization of promotional offers.
- purchasing frequency of users: Identifying loyal customers and predicting repeat purchases.
- analyze the total amount spent by combining users' online and offline purchases : Combining users' online and offline transactions for comprehensive spending analysis.
- average price for each product category: Evaluating pricing strategies and customer preferences across categories.
These engineered features play a key role in refining the market’s strategic decisions and ensuring customer satisfaction while maximizing profitability.

## 📂 Kaggle Notebook
You can access the analysis file of the project on Kaggle from the link below:  <br />
[Kaggle Notebook Link](https://www.kaggle.com/code/karinmanto/onlineshoppingdataset-dataanalysis)


