# **✨ Marketing Campaign prediction and Customer Segmentation ✨**

<img src="https://raw.githubusercontent.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/main/assets/banner.png">

## **⚙ Work Environment ⚙**

- **Tools**

[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)

[![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/blob/main/Response%20Prediction%20Classification%20Marketing%20Campaign.ipynb)

- **Programming Language**

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

- **Libraries**

[Requirements Text](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/blob/main/requirements.txt)

- **Dataset**

[Marketing campaign](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign "Marketing campaign dataset from Kaggle")

## **💻 Script 💻**

## **📍 Table of Content 📍**
<!--ts-->
* **Business Understanding**
    * [Problem Statement](#-business-understanding-)
    * [Roles](#-roles)
    * [Goals](#-goals)
    * [Objectives](#-objectives)
    * [Business Metrics](#-business-metrics)
* **Data Preparation**
    * [Data Description](#-data-description-)
* **Data Understanding**
    * [Exploring Datasets](#-data-understanding-)
    * [Data Types Information](#-data-types-information)
    * [Statistical Summary](#-statistical-summary)
    * [EDA (Exploratory Data Analysis)](#-exploratory-data-analysis-eda)
    * [Feature Engineering / Extraction (Business Insight)](#-feature-engineering--extraction)
    * [Business Insight](#-business-insight)
* **Data Cleansing/Preprocessing**
    * [Handling Missing Values](#-handling-missing-value)
    * [Handling Duplicated Rows](#-handling-duplicate-rows)
    * [Handling Invalid Values](#-handling-invalid-values)
    * [Handling Outliers](#-handling-outliers)
    * [Feature Engineering / Extraction](#-feature-engineering--extraction-1)
    * [Feature Transformation (Numeric)](#-feature-transformation-numeric)
    * [Feature Encoding (Categoric)](#-feature-encoding-categoric)
    * [Feature Selection](#-feature-selection)
    * [Data Splitting](#-data-splitting)
    * [Handling Imbalanced Data](#-handling-imbalanced-data)
<!--te-->

## **⛳ Business Understanding ⛳**

### **📌 Problem Statement**

Here's the translated content:

### **📌 Problem Statement**

**Lotto Mart** is a supermarket in the retail sector, selling various types of products such as Fish, Meat, Fruits, Sweet Products, Wines, and Gold Products. Over the past 6 months, the Marketing Team conducted a campaign involving the distribution of discount vouchers to all customers via Broadcast Message. However, after the campaign, Lotto Mart faced several issues as follows:
- The **response rate** of the marketing campaign was low, approximately 14.91%.
- **Inefficient costs** associated with conducting the marketing campaign.
- **Profit was not proportional** to the costs incurred.

Based on these issues, the Marketing Team asked the data team to analyze the problems that occurred. The company aims to create a targeted marketing campaign tailored to the **characteristics of customers**. This strategy is expected to **increase the response rate**, **minimize costs**, and ultimately **increase profit**.

### **📌 Goals**

The company aims to increase the **response rate** and minimize **marketing campaign costs** to maximize **profit**.

### **📌 Objectives**

Create a classification model to **predict customer groups that will respond to the campaign** in order to **minimize marketing expenses and maximize profits** in the next marketing campaign.

### **📌 Business Metrics**

- **Response Rate (RR)**
    
    The percentage of total customer responses relative to the total delivered campaigns.
    
    _**RR Indicator:**_ 30% is considered good (Efti 2018).
    
- **Net Profit Margin (NPM)**
    
    Measures net profit compared to sales. The larger the NPM, the more effective and efficient the marketing campaign performance (Handayani, Winarningsih 2020).  

    _**NPM Indicator:**_ 5% is low, 10-19% is average, 20% is good (Jayathilaka 2020).
    
- **Return on Investment (ROI)**
    
    CLV (Customer Lifetime Value) divided by CAC (Customer Acquisition Cost). It serves as an indicator of company performance and assists investors in decision-making. 

    _**ROI Indicator:**_ A ratio of 3:1 to 5:1 is considered good (Manzer 2017).  
        
**📝 References:**

- Efti S. 2018. Sales Benchmarks: The 30/50 rule for cold emailing & cold calling. Accessed on May 20, 2023. [Link](https://blog.close.com/sales-benchmarks/)

- Handayani N, Winarningsih S. 2020. The Effect of Net Profit Margin and Return on Equity Toward Profit Growth. Moneter-Journal of Accounting and Finance 7(2): 198-204. [DOI](https://doi.org/10.31294/moneter.v7i2.8701).

- Jayathilaka AK. 2020. Operating Profit and Net Profit: Measurements of Profitability. Open Access Library Journal 7(12): 1-11. [DOI](https://doi.org/10.4236/oalib.1107011).

- Manzer D. 2017. Five insights into measuring marketing ROI. Accessed on May 20, 2023. [Link](https://growswyft.com/five-insights-to-measure-your-roi/).

## **🕹 Data Description 🕹**

**Marketing Campaign ([link to datasets](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign))**

_Boost the profit of a marketing campaign_

A response model can significantly enhance the efficiency of a marketing campaign by increasing responses or reducing costs.

The objective is to predict who will respond to an offer for a product or service.

**Dataset Description:**

The training dataset contains `2240 samples`. It includes `28 features` and `1 target boolean` variable `"Response"`.


**Accepted/Responses Campaign**

- `AcceptedCmp1` - 1 if customer accepted the offer in the 1st campaign, 0 otherwise
- `AcceptedCmp2` - 1 if customer accepted the offer in the 2nd campaign, 0 otherwise
- `AcceptedCmp3` - 1 if customer accepted the offer in the 3rd campaign, 0 otherwise
- `AcceptedCmp4` - 1 if customer accepted the offer in the 4th campaign, 0 otherwise
- `AcceptedCmp5` - 1 if customer accepted the offer in the 5th campaign, 0 otherwise
- `Response (target)` - 1 if customer accepted the offer in the last campaign, 0 otherwise
- `Complain` - 1 if customer complained in the previous 2 years

**Customer Information**

- `ID` - Customer's id
- `Year_Birth` - Customer's year of birth
- `Education` - customer’s level of education
- `Marital` - customer’s marital status
- `Kidhome` - number of small children in customer’s household
- `Teenhome` - number of teenagers in customer’s household
- `Income` - customer’s yearly household income
- `DtCustomer` - date of customer’s enrolment with the company
- `Recency` - number of days since the last purchase

**Sales Product Type**

- `MntFishProducts` - amount spent on fish products in the last 2 years
- `MntMeatProducts` - amount spent on meat products in the last 2 years
- `MntFruits` - amount spent on fruits products in the last 2 years
- `MntSweetProducts` - amount spent on sweet products in the last 2 years
- `MntWines` - amount spent on wine products in the last 2 years
- `MntGoldProds` - amount spent on gold products in the last 2 years

**Number of Purchases per Type**

- `NumDealsPurchases` - number of purchases made with discount
- `NumCatalogPurchases` - number of purchases made using catalogue
- `NumStorePurchases` - number of purchases made directly in stores
- `NumWebPurchases` - number of purchases made through company’s web site
- `NumWebVisitsMonth` - number of visits to company’s web site in the last month

**Cost and Revenue**

- `Z_CostContact = 3` (Cost to contact a customer)
- `Z_Revenue = 11` (Revenue after client accepting campaign)


# **💡 Data Understanding 💡**

## **📌 Explore Datasets**

### **Basic Datasets Information**

Here's the translated content:

- The dataset has `29 columns` and `2240 rows` of data.
- There are 3 data types: `int64, object, float64`.
- The `Income` column has 2216 non-null values, and `24 null/missing values`.

**Steps to take during Data Pre-Processing:**

- Since the data volume is not very large, `Missing Values` in the `Income` column will be handled through `Imputation` during Data Preprocessing:
    - Imputation using the `Median` due to a highly positive skew.
    - Multivariate approaches (MICE Imputation, KNN Imputer, etc.).

### **Checking Duplicate Rows**

The dataset does not contain duplicates.

### **Checking Missing Values**

- The `Income` column has `24 null/missing values`, which is 1.07% of the total data.

**Steps to take during Data Pre-Processing:**

- Given the limited data, `Missing Values` in the `Income` column will be addressed using `Imputation`:
    - Imputation using the `Median` due to high positive skewness.
    - Multivariate approaches (MICE Imputation, KNN Imputer, etc.).

## **📌 Data Types Information**

**List of Column Types:**

- **Date**:
  
    `Dt_Customer`

- **Categorical** (10 Columns):
    - `ID` - Nominal
    - `Education` - Ordinal (Levels: Basic - Graduation - 2nd Cycle - Master - PhD)
    - `Marital_Status` - Nominal
    - `AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Complain, Response` - Nominal (Binary 0 & 1)

- **Continuous** (18 Columns):

    `Year_Birth, Income, Kidhome, Teenhome, 
    Recency, MntWines, MntFruits, MntMeatProducts, 
    MntFishProducts, MntSweetProducts, MntGoldProds, 
    NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, 
    NumStorePurchases, NumWebVisitsMonth, Z_CostContact, Z_Revenue`

**Change in Column Data Types:**

- Categorical data types are changed to `category` to prevent them from being treated as numerical data during exploration and analysis.
- To facilitate data extraction, the `Dt_Customer` date column, currently an `object`, is converted to `datetime64`.

Here's the translated content:

## **📌 Statistical Summary**

### **Numerical + Date Features**

- **Dt_Customer**
    - Initially stored as a `string/object`, the data type is not suitable, so it will be changed to `Datetime`.
    - `Dt_Customer` will be retained for business insight but may be dropped as the date a customer joined does not impact the predictive model.

- **Year_Birth:**
    - The earliest birth year (min) is `1893`, indicating possible `data entry errors`, so this data needs further processing for `outliers`.
    - Potential `feature extraction` will be done to derive `Age` data based on the current year range, 2014 (as per the data).

- **Household Income:**
    - The `mean` is `52247.25`, and the `median` is `51381.5`. This suggests that the mean is greater than the median, indicating a `right-skewed distribution`.
    - The `range` is significantly large (from `1730.0` to `666666.0`), suggesting the presence of `outliers`, necessitating `Log Transformation/Normalization or Segmentation` of the income data before moving on to modeling.

- **Recency, Kidhome, Teenhome**
    - The `mean` and `median` are `similar`, indicating a `normal-skewed or bimodal distribution (to be checked in univariate analysis)`.
    - The `Kidhome` and `Teenhome` features could potentially be combined into a new feature 'Dependents' to represent the number of dependent family members.

- **Amount of Type Products:**

    Some columns show summaries where the `mean` and `median` are significantly different, such as:

    1. `MntWines`, mean = 303.9, median = 173.5
    2. `MntFruits`, mean = 26.3, median = 8
    3. `MntMeatProducts`, mean = 166.9, median = 67
    4. `MntFishProducts`, mean = 37.5, median = 12
    5. `MntSweetProducts`, mean = 27.06, median = 8
    6. `MntGoldProds`, mean = 44.02, median = 24

    These discrepancies suggest a high number of `outliers` and a `skewed distribution`, so `Log Transformation` should be applied in Data Preprocessing to make the data more normally distributed.

- **Moderately Positively Skewed (slightly skewed to the right) columns:**

    `NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth`

    Although the `mean` and `median` differences are not substantial, these columns may still show a `right-skewed distribution`. Further visualization is needed, and `Log Transformation` should be applied during Data Preprocessing to normalize the data.

- **Z_CostContact, Z_Revenue**
    
    The values for `cost (3)` and `revenue (11)` are constant, so they will be `dropped during the modeling step` as they do not contribute significantly to the predictive model.

### **Categorical Features**

- The columns `ID` and `Year_Birth` have too many unique categories.
- Each `ID` appears only once, so there are no duplicate IDs in the data.
- Most customers were born in `1976 (age = 38 years)`, with 89 individuals in that category.
- In the `Education` category, "2n Cycle" and "Master" have similar meanings.
- Most customers fall under the `Education` category of `Graduation` (1127 individuals), which is significantly larger than other categories.
- In `Marital Status`, most customers are `Married` (864 individuals).
- The `Marital Status` categories "Single" and "Alone" have similar meanings.
- The `Marital Status` categories "Together" and "Married" have similar meanings.
- Some entries in `Marital Status`, such as "Absurd" and "YOLO," are unclear and should be grouped and renamed as "Others."
- In the `AcceptedCmp(1-5)` category, most customers did not respond/accept the campaigns.
- In the `Complain` category, most customers did not file any complaints related to the campaigns.
- The `Response` target column is highly imbalanced:
    - Did not respond = 1906
    - Responded = 334

**Steps to take during Data Pre-Processing:**

- `Replace or merge data with similar meanings` to reduce dimensionality and `eliminate redundancy`.
- Due to the imbalanced `Response` target column, machine learning processes might fail, so `Data Sampling (Undersampling/Oversampling/Combined/SMOTE, etc.)` is needed.
- `Feature Encoding` will be applied to the `Education` and `Marital_Status` columns for modeling, as they lack numerical representation.


## **📌 Exploratory Data Analysis (EDA)**

### **Univariate Analysis**

#### **Individual Boxplot and Violinplot**

**Observations:**

There are outliers in the columns Year_Birth, Income, MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds, NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, and NumWebVisitsMonth.

- In the `Year_Birth` column, the farthest outlier is below 1900.
- In the `Income` column, the farthest outlier is above $600,000.
- In the `MntWines` column, outliers are present above 1200.
- In the `MntFruits` column, outliers range between 80 and 200.
- In the `MntMeatProducts` column, the farthest outlier is around 1,750.
- In the `MntFishProducts` column, outliers range from 125 to above 250.
- In the `MntSweetProducts` column, the farthest outlier is around 250.
- In the `MntGoldProds` column, the farthest outlier is around 350.
- In the `NumDealsPurchases` column, the farthest outlier is at 15.
- In the `NumWebPurchases` column, outliers are around 25.
- In the `NumCatalogPurchases` column, the farthest outlier is above 25.
- In the `NumWebVisitsMonth` column, the farthest outlier is at 20.

**Actions to take during Data Pre-Processing:**
- Apply `Log Transformation` for `Feature Scaling` and `Handling Outliers`, as this transformation de-emphasizes/minimizes `outliers` and can help achieve a `bell-shaped/normal distribution`. This is particularly suitable because the dataset is limited to only 2240 rows, making it the best choice without removing data rows.
- Alternatively, clean the data by removing `outliers` based on `IQR or Z-score`, but this will reduce the available data.

#### **Individual Histogram / Distplot**

Based on the **Boxplot, Distribution, and Violin** charts above, several variables contain **outliers** and some have a **Skewed Distribution**. Below are some of the identified variables:

1. ***Normal distribution***
   - `Recency`: Normal Distribution (Symmetric)
   - `Year_Birth`: Moderately Normal Distribution (Symmetric)
   - `NumWebVisitsMonth`: Moderately Normal Distribution (Symmetric)

2. ***Uniform distribution***  
   - `Z_CostContact`: Uniform Distribution - Contains only one value.
   - `Z_Revenue`: Uniform Distribution - Contains only one value.

3. ***Positive skewed distribution***
   - `Income`
   - `MntWines`
   - `MntFruits`
   - `MntMeatProducts`
   - `MntFishProducts`
   - `MntSweetProducts`
   - `MntGoldProds`
   - `NumDealsPurchases`
   - `NumWebPurchases`
   - `NumCatalogPurchases`
   - `NumStorePurchases`

4. ***Bimodal distribution***
   - `Kidhome`
   - `Teenhome`

**Pre-processing recommendations:**

Apply `Log Transformation` to features with a `Positive Skewed Distribution` to normalize the data.

#### **Individual Countplot**

**Observations:**
- There are too many categories in the `ID` and `Year_Birth` columns.
- The `Education` and `Marital_Status` columns have categories with similar or ambiguous values.
  - In `Education`, "2n Cycle" and "Master" have the same meaning.
  - In `Education`, most customers are in the `Graduation` category (1127 people), creating an imbalance.
  - In `Marital_Status`, most customers are `Married` (864 people).
  - In `Marital_Status`, "Single" and "Alone" have similar meanings.
  - In `Marital_Status`, "Together" and "Married" have similar meanings.
  - In `Marital_Status`, ambiguous categories like "Absurd" and "YOLO" should be grouped as "Others".
- Most customers in `Kidhome` and `Teenhome` do not have children or teenagers (value 0).
- The `AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Complain, and Response` columns are dominated by value 0 (No Response/Complaint).
- The target column, `Response`, is highly imbalanced:
  - No response = 1906
  - Response = 334

**Actions to take during Data Pre-Processing:**

- Drop the `ID` column for modeling purposes.
- Create a new `Age` column from `Year_Birth` to represent the customer's age.
- Consolidate categories with similar meanings to reduce dimensions and data redundancy:
  - Merge "2n Cycle" and "Master" in `Education`.
  - In `Marital_Status`, merge "Single" and "Alone".
  - Merge "Together" and "Married" in `Marital_Status`.
  - Replace ambiguous data like "Absurd" and "YOLO" with "Others".
- Apply `Label Encoding` to the `Education` column.
- Apply `One-Hot Encoding (OHE)` to the `Marital_Status` column.
- For the `Response` column, consider resampling techniques (e.g., `Undersampling`, `Oversampling`, `Combined`, `SMOTE`) to handle imbalanced data for machine learning model training.


### **Multivariate Analysis**

#### **Heatmap Correlation**

- **Correlation with Target (Response)**
    - `Top 10 features with high correlation to the target` are as follows, indicating these features might be the most relevant and should be retained:
        - `AcceptedCmp5` - 0.32 - Positive
        - `AcceptedCmp1` - 0.29 - Positive
        - `AcceptedCmp3` - 0.25 - Positive
        - `MntWines` - 0.24 - Positive
        - `MntMeatProducts` - 0.23 - Positive
        - `NumCatalogPurchases` - 0.22 - Positive
        - `Recency` - 0.19 - Negative
        - `AcceptedCmp4` - 0.17 - Positive
        - `AcceptedCmp2` - 0.16 - Positive
        - `Teenhome` - 0.15 - Negative

    - The correlation between the **Response** column and other columns is generally low. The correlation between features and the target ranges from `0.00 to 0.33`. Therefore, a `threshold of 0.15` was set. The features above that threshold are likely to be retained.
    - The correlation between the **Response** column and **AcceptedCmp5** is the highest among previous campaign columns.
    - The products offered in the last campaign (column **Response**) are somewhat similar to campaign 5 (**AcceptedCmp5**).
    - Customers tend to be more interested in wines and meats, as shown by the correlation between **Response** and **MntWines** and **MntMeatProducts**.
    - Customers also prefer purchasing through catalogs (column **NumCatalogPurchases**) compared to other methods.
    
- **Complain, Z_CostContact, and Z_Revenue** are potential candidates for removal as they show no correlation compared to other columns.

- **Feature Correlations**

    - **MntMeatProduct** has a significant positive correlation with **NumCatalogPurchases**, indicating that most meat product purchases are made through catalogs (correlation 0.72). This suggests potential data redundancy, so **NumCatalogPurchases** could be dropped as it has a lower correlation to the target (response).

    Additionally, some interesting patterns were found in feature correlations:

    - **Year_Birth**
        - **Year_Birth** correlates positively with **Kidhome**, indicating that younger customers tend to have more young children, while **Teenhome** correlates negatively, suggesting older customers have more teenagers.
    - **Kidhome & Teenhome**
        - Customers with **Kidhome** (young children) tend to have lower **Income**.
        - Customers with **Kidhome** are more likely to visit websites and make purchases during discounts.
        - Customers with **Teenhome** (teenagers) tend to make more purchases during discounts.
    - **Income**
        - Customers with higher **Income** tend to make more purchases.
        - **Income** correlates positively with **MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, and MntGoldProducts**.
        - **Income** also correlates positively with **NumWebPurchases, NumCatalogPurchases, and NumStorePurchases**, while correlating negatively with **NumWebVisits**. This suggests that higher-income customers prefer to purchase via web, catalog, and store, while lower-income customers visit the web more frequently or make purchases online.
    - **Products**
        - **MntWines** correlates positively with **MntMeatProducts**, suggesting customers often buy wines and meat together.
        - **MntFruits** correlates with **MntMeatProducts, MntFishProducts, and MntSweetProducts**, indicating these products are often bought together.
        - **MntMeatProducts** shows a strong correlation with **NumCatalogPurchases**, indicating most meat purchases are through catalogs.
        - **MntWines** is most frequently purchased through catalogs.
    - **Purchases**
        - **NumDealsPurchases** correlates positively with **NumWebVisitMonth**, showing that web visits increase during discount periods.
        - **NumWebVisitMonth** has a negative correlation with **NumCatalogPurchases** and **NumStorePurchases**, indicating that when customers visit the web more, catalog and store purchases decrease.
    - **Additional Insights**
        - Customers who purchase wines (**MntWines**) also tend to buy meat (**MntMeatProducts**) and prefer shopping in stores, catalogs, or on the web.
        - Combinations of **Fruits** and other products like **Meat, Fish, and Sweets** are popular among customers, who prefer buying these in stores or through catalogs rather than the web.
        - The correlation among the five product columns is quite high, indicating customers often buy multiple products in one shopping trip.
        - **Wines** and **Gold** products are more often bought online, while **Fruits, Meat, Fish, and Sweets** are bought in stores or via catalogs.
        - Discounted deals are not very appealing, as shown by the low correlation between **Deals** and product columns.
        - Customers who use **Deals** are more likely to shop online.

    Based on the initial feature analysis, here are the significant correlations with the target:

    - **Recency**: Correlations with other features range from 0.00 to 0.05.

    - **MntWines**: Correlates with:
    
        Income = 0.58, NumCatalogPurchases = 0.64, NumStorePurchases = 0.64.

    - **MntMeatProducts**: Correlates with:
    
        NumCatalogPurchases = 0.72, Income = 0.58, MntWines = 0.56.

    - **NumCatalogPurchases**: Correlates with:
    
        MntMeatProducts = 0.72, MntWines = 0.64, Income = 0.59.

    - **AcceptedCmp3**: Correlates with:
    
        MntGoldProducts = 0.12.

    - **AcceptedCmp5**: Correlates with:
    
        MntWines = 0.47, MntMeatProducts = 0.37, Income = 0.34.

    - **AcceptedCmp1**: Correlates with:
    
        AcceptedCmp5 = 0.40, MntWines = 0.35, MntMeatProducts = 0.31, NumCatalogPurchases = 0.31.

    These findings could be prioritized for feature selection in customer response classification.

#### **Box Plot based on Response**

Analysis of the box plot comparing features with the `Response` variable reveals the following insights:

Certain variables show significant differences between customers who responded and those who did not, based on the median distance. These variables include `Income`, `Recency`, `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProducts`, `NumberWebPurchases`, `NumberCatalogPurchases`, and `NumberStorePurchases`.
Key findings:

- **Income**: Customers who *responded to the campaign* generally have higher incomes, with an average of around $65,000, compared to non-responders, whose average income is around $50,000.
- **Recency**: Customers who *responded* tend to be more active, with the average number of days since their last purchase being around 30, compared to non-responders, whose last purchase was over 50 days ago.
- **MntWines**: Customers who *responded* bought more wine, with an average purchase amount of about $450 over two years, compared to non-responders, who spent less than $200.
- **MntFruits**: Responders bought more fruits, with an average purchase of over $20 over two years, compared to non-responders, who bought less than $5 worth.
- **MntMeatProducts**: Responders bought more meat products, averaging over $190 over two years, compared to non-responders, who spent less than $50.
- **MntFishProducts**: Responders spent around $25 on fish over two years, compared to non-responders, who spent less than $5.
- **MntSweetProducts**: Responders spent around $20 on sweets over two years, compared to non-responders, who spent less than $5.
- **MntGoldProducts**: Responders spent around $40 on gold products over two years, compared to non-responders, who spent less than $20.
- **NumberWebPurchases**: Responders made an average of 5 web purchases, while non-responders averaged 3.
- **NumberCatalogPurchases**: Responders made an average of 4 catalog purchases, while non-responders averaged 1.
- **NumberStorePurchases**: Responders made an average of 6 store purchases, while non-responders averaged 5.

**Simplified by Purchase Amount**

Responders (value 1) show higher purchase amounts across all product categories compared to non-responders (value 0).

**Simplified by Purchase Type**

- For web, catalog, and store purchases, responders (value 1) show slightly higher purchase amounts than non-responders (value 0).
- Purchases via **Deals/Discounts** and in-store purchases do not show significant differences.

#### **Count Plot based on Response**

**Simplified based on Customer Status**

- **Education**
    - Customers with `Graduation, PhD, and Master` degrees have higher response counts, each showing a response ratio greater than 13.4% (up to 20% max).
  
- **Marital_Status**
    - `Single, Married, Together, and Divorced` statuses have higher response counts, but the response vs. no-response ratio is less than 22.4% (up to 50% max).

- **Kidhome & Teenhome**
    - As the number of children or teenagers a customer has increases, the likelihood of them responding to the latest marketing campaign decreases. Therefore, it’s better for the company to target customers without children or teenagers. Additionally, the response vs. no-response ratio decreases as the number of children/teenagers increases.

**Simplified based on Campaign/Complaint**

- **AcceptedCmp columns**
    - The highest response rates tend to be from customers who did not accept a campaign.
    - For customers who accepted campaigns, only Campaigns 1, 3, 4, and 5 have higher response counts. The response vs. no-response ratio ranges from 33% to 56%, which means there is not a significant difference, and the comparison is relatively balanced.
    - Campaign 2, while having a very small number of responses, has the highest response vs. no-response ratio at 66%.

- **Complain**
    - The highest response rates tend to come from customers who did not have complaints about the campaign.
# 📌 Feature Engineering / Extraction
New Calculation, Extraction, and Binning features for business insight :
- Age Customer
- Age Group
- Has Child
- Dependents
- Month Customer
- Spending
- Total Accepted/Responses
- Education and Marital Simplify
- Income Segment
- Convertion Rate
- Total of days/years joined
