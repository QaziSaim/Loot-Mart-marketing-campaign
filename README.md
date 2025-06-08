
# **✨ Marketing Campaign ✨**

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

**Open in Colab**

- [Response Prediction Classification Marketing Campaign.ipynb](https://colab.research.google.com/github/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/blob/main/Response%20Prediction%20Classification%20Marketing%20Campaign.ipynb)

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

**Lotto Mart** is a supermarket operating in the retail sector, selling various types of products such as Fish, Meat, Fruits, Sweet Products, Wines, and Gold Products. Over the past 6 months, the Marketing Team conducted a campaign by distributing discount vouchers to all customers via broadcast messages. However, after the campaign, Lotto Mart faced the following issues:
- **Response rate** from the marketing campaign was low, at approximately 14.91%
- **Inefficient cost** in conducting the marketing campaign
- **Profit not proportional** to the costs incurred

Based on these issues, the Marketing Team requested the data team to analyze the problems. The company aims to create a targeted marketing campaign based on **customer characteristics**. This strategy is expected to **increase response rate**, **minimize costs**, and subsequently **increase profit**.


### **📌 Goals**

The company aims to increase the **response rate** and minimize **marketing campaign costs** to maximize **profit**.

### **📌 Objectives**

Develop a classification model to **predict the group of customers who will respond to the campaign** to **minimize marketing costs and maximize profits** in the next marketing campaign.

### **📌 Business Metrics**

- **Response Rate/RR**
    
    Percentage of total customer responses relative to total delivered campaigns
    
    _**RR Indicator:**_ 30% is good (Efti 2018).
    
- **Net Profit Margin /NPM**
    
    Measures net profit compared to sales. The higher the NPM, the more effective and efficient the marketing campaign (Handayani, Winarningsih 2020).  

    _**NPM Indicator:**_ 5% is low, 10-19% is average, 20% is good (Jayathilaka 2020).
    
- **Return on Investment /ROI**
    
    CLV (Customer Lifetime Value) divided by CAC (Customer Acquisition Cost). Serves as an indicator of company performance and decision-making for investors.

    _**ROI Indicator:**_ 3:1 to 5:1 is good (Manzer 2017).  
        
**📝 References:**

- Efti S. 2018. Sales Benchmarks: The 30/50 rule for cold emailing & cold calling. Accessed May 20, 2023. https://blog.close.com/sales-benchmarks/ 

- Handayani N, Winarningsih S. 2020. The Effect of Net Profit Margin and Return on Equity Toward Profit Growth. Moneter-Jurnal Akuntansi Dan Keuangan 7(2): 198-204. https://doi.org/10.31294/moneter.v7i2.8701.

- Jayathilaka AK. 2020. Operating Profit and Net Profit: Measurements of Profitability. Open Access Library Journal 7(12): 1-11. https://doi.org/10.4236/oalib.1107011.

- Manzer D. 2017. Five insights into measuring marketing ROI. Accessed May 20, 2023. https://growswyft.com/five-insights-to-measure-your-roi/.

## **🕹 Data Description 🕹**

**Marketing Campaign ([link datasets](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign))**

_Boost the profit of a marketing campaign_

A response model can provide a significant boost to the efficiency of a marketing campaign by increasing responses or reducing expenses. 

The objective is to predict who will respond to an offer for a product or service.

**Dataset Description:**

The training dataset contains `2240 samples`. Contains `28 features` and `1 target boolean` variable `"Response"`:

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
- `Education` - Customer’s level of education
- `Marital` - Customer’s marital status
- `Kidhome` - Number of small children in customer’s household
- `Teenhome` - Number of teenagers in customer’s household
- `Income` - Customer’s yearly household income
- `DtCustomer` - Date of customer’s enrollment with the company
- `Recency` - Number of days since the last purchase

**Sales Product Type**

- `MntFishProducts` - Amount spent on fish products in the last 2 years
- `MntMeatProducts` - Amount spent on meat products in the last 2 years
- `MntFruits` - Amount spent on fruit products in the last 2 years
- `MntSweetProducts` - Amount spent on sweet products in the last 2 years
- `MntWines` - Amount spent on wine products in the last 2 years
- `MntGoldProds` - Amount spent on gold products in the last 2 years

**Number of Purchases per Type**

- `NumDealsPurchases` - Number of purchases made with discount
- `NumCatalogPurchases` - Number of purchases made using catalogue
- `NumStorePurchases` - Number of purchases made directly in stores
- `NumWebPurchases` - Number of purchases made through company’s website
- `NumWebVisitsMonth` - Number of visits to company’s website in the last month

**Cost and Revenue**

- `Z_CostContact = 3` (Cost to contact a customer)
- `Z_Revenue = 11` (Revenue after client accepting campaign)

# **💡 Data Understanding 💡**

## **📌 Explore Datasets**

### **Basic Datasets Information**

- The dataset has `29 columns` and `2240 rows` of data
- There are 3 data types: `int64, object, float64`
- The `Income` column has 2216 non-null values, and `24 null/missing values`

**Actions to be taken during Data Pre-Processing:**

- Since the dataset is not large, for `Missing Values` in `Income`, `Imputation` will be performed during the Data Preprocessing stage:
    - Imputation (Median), because the data is Highly Positively Skewed
    - Multivariate Approach (MICE Imputation, KNN Imputer, etc.)

### **Checking Duplicate Rows**

The dataset has no duplicates.

### **Checking Missing Values**

- The `Income` column has `24 null/missing values`, accounting for 1.07% of the total data.

**Actions to be taken during Data Pre-Processing:**

- Since the dataset is not large, for `Missing Values` in `Income`, `Imputation` will be performed during the Data Preprocessing stage:
    - Imputation (Median), because the data is Highly Positively Skewed
    - Multivariate Approach (MICE Imputation, KNN Imputer, etc.)

## **📌 Data Types Information**

**List of Column Types:**

- **Date**

    `Dt_Customer`

- **Categorical** (10 Columns): 
    - `ID` - Nominal
    - `Education` - Ordinal (Levels: Basic - Graduation - 2n Cycle - Master - PhD)
    - `Marital_Status` - Nominal
    - `AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Complain, Response` - Nominal (Binary 0 & 1)

- **Continuous** (18 Columns):

    `Year_Birth, Income, Kidhome, Teenhome, 
    Recency, MntWines, MntFruits, MntMeatProducts, 
    MntFishProducts, MntSweetProducts, MntGoldProds, 
    NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, 
    NumStorePurchases, NumWebVisitsMonth, Z_CostContact, Z_Revenue`

**Change Some Column Data Types**

- We convert categorical data types to `category` so that during exploration and insight generation, they are not treated as numerical data.
- To facilitate the extraction process for `Dt_Customer` or its parts, the date column `object` is changed to `datetime64`.

## **📌 Statistical Summary**

### **Numerical + Date Features**

- **Dt_Customer** 
    - Previously in `string/object` format, the data type was not suitable, so it was changed to `Datetime`.
    - `Dt_Customer` is retained for Business Insight, but it may be dropped as the date of customer enrollment does not affect the prediction model.

- **Year_Birth:**

    - The oldest birth year (min) is `1893`, indicating possible `data entry errors`, so the data needs further processing for `Outliers`.
    - `Feature extraction` may be performed to derive `Age` data based on the current year range of 2014 (as per the data).

- **Household Income:**

    - The `Mean` is `52247.25` and the `Median` is `51381.5`. Since the mean is slightly greater than the median, this indicates a slightly `Right-skewed Distribution`.
    - The range spans from `1730.0 (minimum)` to `666666.0 (maximum)`, a very wide gap, indicating `outliers`. Thus, `Log Transformation/Normalization or Segmentation` is needed for the income data before proceeding to modeling.

- **Recency, Kidhome, Teenhome**

    - The `mean` and `median` are similar, indicating a possible `normal-skewed distribution / bimodal` (to be checked in univariate analysis).
    - `Kidhome` and `Teenhome` have potential for creating a new feature 'Dependents' to better represent the number of dependent family members.

- **Amount of Type Products:**

    Some columns show a significant gap between `Mean and Median` values, such as:

    1. `MntWines`, mean = 303.9, median = 173.5
    2. `MntFruits`, mean = 26.3, median = 8
    3. `MntMeatProducts`, mean = 166.9, median = 67
    4. `MntFishProducts`, mean = 37.5, median = 12
    5. `MntSweetProducts`, mean = 27.06, median = 8
    6. `MntGoldProds`, mean = 44.02, median = 24

    The significant gap between `mean and median` suggests a high number of `outliers` and a `skewed` distribution. Thus, for Data Preprocessing, `Log Transformation` is needed to adjust the skewed data toward normality.

- **Moderately Positively Skewed (Slightly skewed to the right) in columns:**

    `NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth`
    
    The `mean and median` values are not too far apart, but the distribution is likely `skewed` to the right. Further visualization is needed, and for Data Preprocessing, `Log Transformation` is required to adjust the skewed data toward normality.
    
- **Z_CostContact, Z_Revenue**

    The `cost (3)` and `revenue (11)` values are constant, so they will be `dropped during the modeling step` as they do not provide significant information for the prediction model.

### **Categorical Features**

- Too many categories in the `ID` and `Year_Birth` columns.
- In the `ID` data, all values appear only once, indicating no duplicate IDs.
- Many customers were born (`Year_Birth`) in `1976 (age = 38 years)`, totaling 89 people.
- In the `Education` category, "2n Cycle" and "Master" have the same meaning.
- In the `Education` category, the majority of customers have a `Graduation` level of education, totaling 1127 people, significantly higher than other categories.
- In the `Marital Status` category, the majority of customers are married (Married), totaling 864 people.
- In the `Marital Status` category, "Single" and "Alone" have the same meaning.
- In the `Marital Status` category, "Together" and "Married" have the same meaning.
- In the `Marital Status` category, some data is unclear, such as "Absurd" and "YOLO", and it is recommended to combine and replace them with "Others".
- In the `AcceptedCmp(1-5)` categories, the majority of customers did not respond/accept the campaigns.
- In the `Complain` category, the majority of customers never complained about the campaigns.
- The target variable is in the `Response` column, which has a very high imbalance (Imbalanced Data):
    - Did not respond = 1906
    - Responded = 334
    
**Actions to be taken during Data Pre-Processing:**

- Perform `replace data / merge categories with the same meaning` to reduce dimensions and `redundancy in the data`.
- For the `Response` column, the imbalanced category distribution in the target can cause Machine Learning processes to fail. Thus, `Sampling Data (Undersampling/Oversampling/Combined/SMOTE/etc.)` is needed.
- Perform `Feature Encoding` on the `Education` and `Marital_Status` columns for modeling, as they do not yet have numerical representations.

## **📌 Exploratory Data Analysis (EDA)**

### **Uni-variate Analysis**

#### **Individual Boxplot and Violinplot**

**Observations:**

Outliers are present in the columns Year_Birth, Income, MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds, NumDealsPurchases, NumWebPurchases, NumCatalogPurchases, and NumWebVisitsMonth.

- In the `Year_Birth` column, the furthest outlier is below 1900.
- In the `Income` column, the furthest outlier is above $600,000.
- In the `MntWines` column, outliers are at 1200 and above.
- In the `MntFruits` column, outliers are around 80 to 200.
- In the `MntMeatProducts` column, the furthest outlier is around 1,750.
- In the `MntFishProducts` column, outliers are around 125 to above 250.
- In the `MntSweetProducts` column, the furthest outlier is around 250.
- In the `MntGoldProds` column, the furthest outlier is around 350.
- In the `NumDealsPurchases` column, the furthest outlier is at 15.
- In the `NumWebPurchases` column, outliers are around 25.
- In the `NumCatalogPurchases` column, the furthest outlier is above 25.
- In the `NumWebVisitsMonth` column, the furthest outlier is at 20.

**Actions to be taken during Data Pre-Processing:**
- Apply `Log Transformation` for `Feature Scaling` and `Handling Outliers`, which de-emphasizes/minimizes `outliers` and can help achieve a `bell-shaped / normal distribution`. This is the best option due to the limited data of only 2240 rows, avoiding row deletion.
- Alternatively, clean the data by removing `outliers` based on `IQR or Z-score`, but this will reduce the dataset size.

#### **Individual Histogram / Distplot**

Based on the **Boxplot, Distribution, and Violin** charts above, some variables have **outliers** and some have **Skewed Distribution**. The variables are as follows:

1. ***Normal distribution***
    - `Recency` Normal Distribution (Symmetric)
    - `Year_Birth` Moderately Normal Distribution (Symmetric)
    - `NumWebVisitsMonth` Moderately Normal Distribution (Symmetric)
    
2. ***Uniform distribution***  
    - `Z_CostContact` Uniform Distribution - Has only one value
    - `Z_Revenue` Uniform Distribution - Has only one value

3. ***Positive skewed distribution***
    - Income `Income`
    - Amount of Wines Products `MntWines`
    - Amount of Fruits Products `MntFruits`
    - Amount of Meats Products `MntMeatProducts`
    - Amount of Fish Products `MntMeatProducts`
    - Amount of Sweet Products `MntSweetProducts`
    - Amount of Golds Products `MntGoldProds`
    - Number Deals Purchases `NumDealsPurchases`
    - Number Web Purchases `NumWebPurchases`
    - Number Catalog Purchases `NumCatalogPurchases`
    - Number Store Purchases `NumStorePurchases`

4. ***Bimodal distribution***
    - Number of small children in customer's household `Kidhome`
    - Number of teenagers in customer's household `Teenhome`

**Recommendations for data pre-processing:**

Data with `Positive Skewed Distribution` should undergo `Log Transformation` to achieve a normal distribution.

#### **Individual Countplot**

**Observations:**
- Too many categories in the `ID` and `Year_Birth` columns.
- The `Education` and `Marital_Status` columns have some categories with the same and ambiguous values.
    - In the `Education` category, "2n Cycle" and "Master" have the same meaning.
    - In the `Education` category, the majority of customers have a `Graduation` level of education, totaling 1127 people, significantly higher than other categories.
    - In the `Marital Status` category, the majority of customers are married (Married), totaling 864 people.
    - In the `Marital Status` category, "Single" and "Alone" have the same meaning.
    - In the `Marital Status` category, "Together" and "Married" have the same meaning.
    - In the `Marital Status` category, some data is unclear, such as "Absurd" and "YOLO", and it is recommended to combine and replace them with "Others".
- The `Kidhome` and `Teenhome` columns show that the majority of customers have no children or teenagers (value 0).
- The `AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Complain, and Response` columns are dominated by the value 0 (Did not Respond / Complain).
- The target variable is in the `Response` column, which has a very high imbalance (Imbalanced Data):
    - Did not respond = 1906
    - Responded = 334

**Actions to be taken during Data Pre-Processing:**

- Drop the `ID` column for modeling.
- Create a new column `Age` from the `Year_Birth` column to represent the customer’s age.
- Perform `replace data / merge categories with the same meaning` to reduce dimensions and `redundancy in the data`:
    - In the `Education` category, "2n Cycle" and "Master" have the same meaning.
    - In the `Marital Status` category, the majority of customers are married (Married), totaling 864 people.
    - In the `Marital Status` category, "Single" and "Alone" have the same meaning.
    - In the `Marital Status` category, "Together" and "Married" have the same meaning.
    - In the `Marital Status` category, some data is unclear, such as "Absurd" and "YOLO", and it is recommended to combine and replace them with "Others".
- Perform `Label Encoding` on the `Education` column.
- Perform `One Hot Encoding (OHE)` on the `Marital_Status` column.
- For the `Response` column, the imbalanced category distribution in the feature indicates its lack of usefulness. For the target, it can cause Machine Learning processes to fail. Thus, `Sampling Data (Undersampling/Oversampling/Combined/SMOTE/etc.)` is needed.

### **Multivariate Analysis**

#### **Heatmap Correlation**

- **Correlation to Target (Response)**
    - `Top 10 Highly Correlated to Target` as follows, likely the most relevant features to retain:
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

    - The correlation of the **Response** column with other columns is generally low, ranging from `0.00 to 0.33`. Therefore, we set a `threshold at 0.15`. Features with a correlation value `>0.15` are likely to be retained.
    - The correlation of the **Response** column with **AcceptedCmp5** is the highest compared to previous campaign columns.
    - The product offered in the last campaign (**Response**) is somewhat similar to the 5th campaign (**AcceptedCmp5**).
    - Customers tend to be more interested in Wines and Meat, as shown by the correlation of the **Response** column with **MntWines** and **MntMeatProducts**.
    - Customers also prefer purchasing via Catalog (**NumCatalogPurchases**) compared to other methods.
    
- **Complain, Z_CostContact, and Z_Revenue** have potential to be dropped, as they have no correlation compared to other columns.

- **Correlation Between Features**

    - **MntMeatProduct** has a fairly strong positive correlation with **NumCatalogPurchases**, indicating that most meat product purchases are made via catalog (correlation of 0.72). This suggests potential redundancy, so **NumCatalogPurchases** may be dropped as it has a lower correlation with the target (Response).

    Additionally, interesting patterns in feature correlations are as follows:

    - **Year_Birth**
        - **Year_Birth** correlates positively with **Kidhome**, indicating that younger customers tend to have more small children, while it correlates negatively with **Teenhome**, meaning older customers have more teenagers.
    - **Kidhome & Teenhome**
        - Customers with small children (**Kidhome**) tend to have lower **Income**.
        - Customers with small children (**Kidhome**) tend to visit the web more often and make purchases during discounts.
        - Customers with teenagers (**Teenhome**) tend to make more purchases during discounts.
    - **Income**
        - Customers with high **Income** tend to make more purchases.
        - The **Income** column has a fairly strong positive correlation with **MntWines, MntFruits, MntMeatProduct, MntFishProduct, MntSweetProduct, and MntGoldProduct**.
        - The **Income** column has a fairly strong positive correlation with **NumWebPurchases, NumCatalogPurchases, and NumStorePurchases**, while it has a fairly strong negative correlation with **NumWebVisitsPurchases**, indicating that customers with higher income prefer purchasing via Web, Catalog, and Store, while those with lower income tend to visit the web more or make purchases via the web.
    - **Product**
        - The **MntWines** column has a fairly strong positive correlation with **MntMeatProduct**, suggesting that customers buying wine also buy meat.
        - The **MntFruits** column has a fairly strong positive correlation with **MntMeatProduct, MntFishProduct, and MntSweetProduct**, suggesting that customers may buy these products together.
        - **MntMeatProduct** has a fairly strong positive correlation with **NumCatalogPurchases**, indicating that most meat product purchases are made via catalog.
        - **MntWines** is mostly purchased via catalog compared to other purchase methods.
    - **Purchases**
        - The **NumDealsPurchases** column correlates positively with NumWebVisitsMonth, indicating that web visits increase during discounts.
        - The **NumWebVisitsMonth** column has a fairly strong negative correlation with **NumCatalogPurchases and NumStorePurchases**, indicating that when customers visit the web more, purchases via catalog and store decrease.
    - **Additional**
        - Customers buying Wines (**MntWines**) tend to buy Meat (**MntMeatProducts**) and prefer purchasing directly in **Store**, **Catalog**, and **Website**.
        - Some popular **Fruits** combinations include **Fruits** and **Meat**, **Fruits** and **Fish**, or **Fruits** and **Sweet**. Customers also feel more comfortable buying directly in **Store** or via **Catalog** compared to using the Website.
        - The correlation between the 5 product columns is quite high. Thus, customers tend to buy more than one product in a single purchase.
        - **Wines** and **Gold** products are mostly purchased via **Website**. Meanwhile, **Fruits**, **Meat**, **Fish**, and **Sweet** are purchased via **Store** and **Catalog**.
        - Products offered with **Deals** (discounts) are not very appealing to customers, as the correlation with any product column is very low.
        - Customers using **Deals** are mostly those who use the **Website** to buy products.
        
    Based on our initial analysis of features with higher correlations to the target, the results are as follows:

    - `Recency`: Correlation with other features ranges from 0.00 to 0.05

    - `MntWines`: Features correlated with MntWines: 
    
        Income = 0.58, NumCatalogPurchases = 0.64, NumStorePurchases = 0.64

    - `MntMeatProducts`: Features correlated with MntMeatProducts:
    
        NumCatalogPurchases = 0.72, Income = 0.58, MntWines = 0.56

    - `NumCatalogPurchases`: Features correlated with NumCatalogPurchases: 
    
        MntMeatProducts = 0.72, MntWines = 0.64, Income = 0.59

    - `AcceptedCmp3`: Features correlated with AcceptedCmp3: 
    
        MntGoldProducts = 0.12

    - `AcceptedCmp5`: Features correlated with AcceptedCmp5: 
    
        MntWines = 0.47, MntMeatProducts = 0.37, Income = 0.34

    - `AcceptedCmp1`: Features correlated with AcceptedCmp1: 
    
        AcceptedCmp5 = 0.40, MntWines = 0.35, MntMeatProducts = 0.31, NumCatalogPurchases = 0.31

    These results may be used as priority features for determining classification of customer responses.

#### **Box Plot based on Response**

Based on the boxplot analysis above, by adding the `Response` feature as a comparison variable, the following insights can be identified:

Some variables show a significant difference in the median distance between customers who respond and those who do not, such as: `Income`, `Recency`, `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProducts`, `NumberWebPurchases`, `NumberCatalogPurchases`, and `NumberStorePurchases`. Here is the explanation:

- For the `Income` variable, customers who *respond to the campaign* tend to have higher income, with an average income of around 65,000, compared to customers who *do not respond to the campaign*, with an average income of only about 50,000.
- For the `Recency` variable, customers who *respond to the campaign* tend to be more active in shopping, with an average of about 30 days since their last product purchase, compared to customers who *do not respond to the campaign*, with an average of more than 50 days since their last purchase.
- For the `MntWines` variable, customers who *respond to the campaign* tend to buy more wine products, with an average purchase of about $450 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $200 over 2 years.
- For the `MntFruits` variable, customers who *respond to the campaign* tend to buy more fruit products, with an average purchase of more than $20 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $5 over 2 years.
- For the `MntMeatProducts` variable, customers who *respond to the campaign* tend to buy more meat products, with an average purchase of more than $190 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $50 over 2 years.
- For the `MntFishProducts` variable, customers who *respond to the campaign* tend to buy more fish products, with an average purchase of about $25 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $5 over 2 years.
- For the `MntSweetProducts` variable, customers who *respond to the campaign* tend to buy more sweet products, with an average purchase of about $20 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $5 over 2 years.
- For the `MntGoldProducts` variable, customers who *respond to the campaign* tend to buy more gold products, with an average purchase of about $40 over 2 years, compared to customers who *do not respond to the campaign*, with an average purchase of less than $20 over 2 years.
- For the `NumberWebPurchases` variable, customers who *respond to the campaign* tend to buy more products via the web, with an average of 5 purchases, compared to customers who *do not respond to the campaign*, with an average of 3 purchases.
- For the `NumberCatalogPurchases` variable, customers who *respond to the campaign* tend to buy more products via catalog, with an average of 4 purchases, compared to customers who *do not respond to the campaign*, with an average of 1 purchase.
- For the `NumberStorePurchases` variable, customers who *respond to the campaign* tend to buy more products via stores, with an average of 6 purchases, compared to customers who *do not respond to the campaign*, with an average of 5 purchases.

**Simplified based on Amount Product**

For `Response with value 1 (accepted)`, the `Amount` (Purchase Amount) for each product is `higher` than for those who did not respond (value 0).

**Simplified based on Type Purchases**

- For purchases via `Web`, `Catalog`, and `Web`, for `Response with value 1 (accepted)`, the `Purchases` (Number of Purchases) is slightly `higher` than for those who did not respond (value 0).
- For purchases via `Deals / Discount` and `Store`, the values are `not significantly different`.

#### **Count Plot based on Response**

**Simplified based on Status Customer**

- Education
    - `Graduation, PhD, and Master` have a high response count, each with a response ratio > 13.4% (max 20%).
- Marital_Status
    - `Single, Married, Together, and Divorced` have a high response count, but the response vs. no response ratio is < 22.4% (max 50%).
- Kidhome & Teenhome
    - The higher the number of children/teenagers a customer has, the lower the likelihood of the customer responding to the last marketing campaign. Thus, the company should target customers with no children/teenagers. The response vs. no response ratio also decreases.
    
**Simplified based on Campaign/Complain**

- AcceptedCmp columns
    - The highest response tends to come from those who did not accept the campaign.
    - Among those who accepted the campaign, only campaigns 1, 3, 4, and 5 have higher values. The response vs. no response ratio is 33-56%, indicating no significant difference and a fairly balanced ratio.
    - For Accepted Campaign 2, the count is very small, but the response vs. no response ratio is the highest at 66%.

- Complain
    - The highest response tends to come from those with no complaints about the campaign.

## **📌 Feature Engineering / Extraction**

New Calculation, Extraction, and Binning features for business insight:
- Age Customer
- Age Group
- Has Child
- Dependents
- Month Customer
- Spending
- Total Accepted/Responses
- Education and Marital Simplify
- Income Segment
- Conversion Rate
- Total of days/years joined

## **📌 Business Insight**

### **Response Ratio**

- The number of `Responses` is significantly lower than `No Responses`, with a ratio of 14.9%.
- This indicates `data imbalance` in the company’s last (6th) campaign.
- Efforts can be made to improve the marketing campaign process to increase customer responses.

### **Acceptance Rate for each Campaign (1-5)**

From the campaign rates conducted, there was a drastic change from Campaign 1 to Campaign 2 (sharp decline) and Campaign 3 (significant increase). From Campaigns 3-5, the rates are roughly similar, around ~7%. Thus, the company and team need to further identify any patterns in customer purchases.

### **Total Accept Campaign (1-5)**

The majority of customers in the five campaigns did not respond (0), but some potential exists for those who responded once (1) or twice (2), with 325 and 83 customers, respectively.

### **Income vs. Campaign**

Customers with income above $120,000 did not respond to the company’s campaign. Thus, the company should focus campaigns on customers with income below $120,000.

### **Birth Year / Age vs. Response**

The category of customers responding most to the last marketing campaign came from birth years 1970-1975 (39-44 years old) and 1980-1990 (24-34 years old).

If the company must prioritize certain customers, it can target customers born in those years for a campaign.

However, also consider No Responses, as the 1970-1975 birth year range also has a high non-response rate.

### **Age Group vs. Response**

Based on the chart above, the age group responding most to the campaign is `Adult and Senior Adult`, while the lowest is `Young Adult`.

`This means the older a person is, the higher the response rate.`

### **Education vs. Response**

From the pie chart visualization of Education, the customers responding most are those with Graduation and PhD education levels. Thus, the marketing team can focus campaigns on customers with a Graduation education.

### **Marital Status vs Response**

The majority of customers responding based on marital status are Married and Single. Thus, for the next campaign, the company should focus on customers who are married (Married).

For "Absurd" and "YOLO" in the "Others" data, the numbers are very small.

### **Kids and Teens (Dependents) vs. Response**

The higher the number of children/teenagers a customer has, the lower the likelihood of the customer responding to the last marketing campaign. Thus, the company should target customers with no children/teenagers.

From the visualization of Kidhome and Teenhome, the customers responding most are those with no children and no teenagers (0.265403). Thus, the marketing team can focus campaigns on customers with no children and no teenagers.

### **Recency vs. Response**

Based on recency (when the customer last made a purchase), the lower the recency, the higher the likelihood of the customer responding to the company’s last marketing campaign (Response). Thus, the next marketing campaign can focus on customers with low recency.

* Low recency: the time since the customer’s last purchase is not too long.

### **Income vs Response**

The majority of customers responding based on income are those with an income of 80,000. Thus, for the next campaign, the company should focus on people with an income of 80,000.

### **Purchase type vs. Response**

The fewer purchases made (whether with discounts or via web, catalog, or store), the higher the likelihood of the customer responding to the last marketing campaign. Thus, the company can target customers with a low number of purchases.

### **Purchase type vs. Complain**

- Customers with lower Purchases -> High Complaint Numbers, but High Response

    The company should improve service quality so that the response aligns with customer satisfaction to reduce complaints.

- Customers with higher Purchases -> Low Complaint Numbers, but Low Response

    Further review is needed to identify factors causing customers with higher purchases to have a lower response rate.
    
### **Income x Spending for Response**

Income and Spending have a positive correlation with response, where higher income and spending lead to a higher response rate. Thus, the income and spending features should be retained.

### **Income Segment vs. Response**

The higher the income, the more likely to respond to the campaign.

Customers responding to the campaign tend to have higher income, as evidenced by customers with “High” income levels responding more to the campaign.

### **Income Segment vs Product**

Customers with High and Medium income prefer Gold and Fish products. Thus, for campaigns, it is recommended to offer Gold and Fish products to customers with this income level.

### **Income Segment vs Purchase Type**

For campaign creation, it is recommended to use Catalog or Discount forms and target customers with High/Medium income. Alternatively, banners/booths can be set up directly in Stores.

### **Product vs. Response**

Customers responding to the campaign tend to buy more Wines and Meat products. Thus, for the next campaign, Wines and Meat products are recommended as the primary products for responding customers.

### **Total Campaign vs Num Values**

The following insights are obtained based on Total Campaign vs Variables:

- `Income`:
    Customers accepting a total of 4 campaigns tend to have higher income.
- `Kidhome:` 
    Customers not accepting any campaigns have more children.
- `Teenhome`:
    Customers not accepting any campaigns have more teenagers.
- `Recency`:
    Customers accepting a total of 3 campaigns tend to have a longer recency (days since last purchase).
- `MntWines`:
    Customers accepting a total of 4 campaigns tend to buy more wine products.
- `MntFruits`:
    Customers accepting a total of 3 campaigns tend to buy more fruit products.
- `MntMeatProducts`:
    Customers accepting a total of 3 campaigns tend to buy more meat products.
- `MntFishProducts`:
    Customers accepting a total of 3 campaigns tend to buy more fish products.
- `MntSweetProducts`:
    Customers accepting a total of 3 campaigns tend to buy more sweet products.
- `MntGoldProducts:` 
    Customers accepting a total of 3 campaigns tend to buy more gold products.
- `NumDealsPurchases`:
    Customers not accepting any campaigns tend to buy products using discounts more often.
- `NumWebPurchases`:
    Customers accepting a total of 2 and 3 campaigns tend to buy products via the web more often.
- `NumCatalogPurchases`:
    Customers accepting a total of 4 campaigns tend to buy products via catalog more often.
- `NumStorePurchases`:
    Customers accepting a total of 4 campaigns tend to buy products via stores more often.
- `NumWebVisitsMonths`:
    Customers not accepting any campaigns tend to visit the web more often in the last month.

# **🏝 Data Cleansing/Preprocessing 🏝**

## **📌 Handling Missing Value**

```html
Missing values status: True
                     Total Null Values  Percentage Data Type
Income                              24    1.071429     int64
ID                                   0    0.000000     int64
Z_CostContact                        0    0.000000     int64
Complain                             0    0.000000    object
AcceptedCmp2                         0    0.000000    object
AcceptedCmp1                         0    0.000000   float64
AcceptedCmp5                         0    0.000000     int64
AcceptedCmp4                         0    0.000000     int64
AcceptedCmp3                         0    0.000000    object
NumWebVisitsMonth                    0    0.000000     int64
NumStorePurchases                    0    0.000000     int64
NumCatalogPurchases                  0    0.000000     int64
NumWebPurchases                      0    0.000000     int64
NumDealsPurchases                    0    0.000000     int64
Z_Revenue                            0    0.000000     int64
MntGoldProds                         0    0.000000     int64
MntFishProducts                      0    0.000000     int64
MntMeatProducts                      0    0.000000     int64
MntFruits                            0    0.000000     int64
MntWines                             0    0.000000     int64
Recency                              0    0.000000     int64
Dt_Customer                          0    0.000000     int64
Teenhome                             0    0.000000     int64
Kidhome                              0    0.000000     int64
Marital_Status                       0    0.000000     int64
Education                            0    0.000000     int64
Year_Birth                           0    0.000000     int64
MntSweetProducts                     0    0.000000     int64
Response                             0    0.000000     int64
```

Based on the initial analysis, there are missing values in the `Income` column, totaling 24 rows, or 1.07% of the total data.

Methods for handling missing values in the `Income` column include:
- **Drop Rows Missing Values**
- **Imputation Median**
    - `Fillna` or `SimpleImputer`
- **Multivariate Approach**
    - Ensure all data is in numerical form (categorical encoding)
        - `Label Encoding`: `Education`
            - `LabelEncoder` or `Mapping`
        - `One Hot Encoding`: `Marital Status`
            - `get_dummies` or `OneHotEncoder`
    - Drop unimportant columns like the date column `Dt_Customer`
    - Methods:
        - `KNNImputer` or K-Nearest Neighbor
        - `MICE` or Multiple Imputation by Chained Equation      
            - Imputation using MICE with `IterativeImputer`
            - Imputation using MICE with `LightGBM`
            
**Choice Determination:**

- For handling missing values, we use `Imputation using MICE with LightGBM`.

**Imputation using `MICE` with `LightGBM`**

```
import miceforest as mf

# Create kernel. 
kds = mf.ImputationKernel(
  df_ma,
  save_all_iterations=True,
  random_state=100
)

# Run the MICE algorithm
kds.mice(iterations=5, n_estimators=50)

# Return the completed dataset.
df_imputed = kds.complete_data()
df["Income"] = df_imputed["Income"].copy()
df.head()
```

**Conclusion**

Based on the check, the `Income` column has 24 missing values (1.07%). Since our data is limited, we will not drop rows but perform imputation. 

For handling missing values, we use `Imputation using MICE with LightGBM`. MICE imputation can be more efficient using `miceforest` as it is expected to perform better by implementing the `LightGBM` algorithm in the backend for imputation. `LightGBM` is known for high prediction accuracy. Combining it with the `MICE` algorithm makes it a powerful imputation method.

## **📌 Handling Duplicate Rows**

```html
df[df.duplicated(keep=False)].sort_values(by=list(df.columns.values))

df.duplicated().sum()

df.duplicated(subset=["ID"]).sum()

-----------------------------------------
0
```
**Conclusion**

- Based on the check, no duplicate rows were found. Thus, we do not need to handle duplicated data.
- No duplicate customer IDs were found in the subset check.

## **📌 Handling Invalid Values**

```html
===== ID =====
[5524, 2174, 4141, 6182, 5324, 7446, 965, 6177, 4855, 5899, .....]

===== Year_Birth =====
[1957, 1954, 1965, 1984, 1981, 1967, 1971, 1985, 1974, 1950, .....]

===== Education =====
['Graduation', 'PhD', 'Master', 'Basic', '2n Cycle']

===== Marital_Status =====
['Single', 'Together', 'Married', 'Divorced', 'Widow', 'Alone', 'Absurd', 'YOLO']

===== Income =====
[58138.0, 46344.0, 71613.0, 26646.0, 58293.0, 62513.0, 55635.0, 33454.0, 30351.0, 5648.0, .....]

===== Kidhome =====
[0, 1, 2]

===== Teenhome =====
[0, 1, 2]

===== Dt_Customer =====
['2012-09-04', '2014-03-08', '2013-08-21', '2014-02-10', '2014-01-19', '2013-09-09', '2012-11-13', '2013-05-08', '2013-06-06', '2014-03-13', .....]

===== Recency =====
[58, 38, 26, 94, 16, 34, 32, 19, 68, 11, .....]

===== MntWines =====
[635, 11, 426, 173, 520, 235, 76, 14, 28, 5, .....]

===== MntFruits =====
[88, 1, 49, 4, 43, 42, 65, 10, 0, 5, .....]

===== MntMeatProducts =====
[546, 6, 127, 20, 118, 98, 164, 56, 24, 11, .....]

===== MntFishProducts =====
[172, 2, 111, 10, 46, 0, 50, 3, 1, 11, .....]

===== MntSweetProducts =====
[88, 1, 21, 3, 27, 42, 49, 2, 112, 5, .....]

===== MntGoldProds =====
[88, 6, 42, 5, 15, 14, 27, 23, 2, 13, .....]

===== NumDealsPurchases =====
[3, 2, 1, 5, 4, 15, 7, 0, 6, 9, .....]

===== NumWebPurchases =====
[8, 1, 2, 5, 6, 7, 4, 3, 11, 0, .....]

===== NumCatalogPurchases =====
[10, 1, 2, 0, 3, 4, 6, 28, 9, 5, .....]

===== NumStorePurchases =====
[4, 2, 10, 6, 7, 0, 3, 8, 5, 12, .....]

===== NumWebVisitsMonth =====
[7, 5, 4, 6, 8, 9, 20, 2, 3, 1, .....]

===== AcceptedCmp3 =====
[0, 1]

===== AcceptedCmp4 =====
[0, 1]

===== AcceptedCmp5 =====
[0, 1]

===== AcceptedCmp1 =====
[0, 1]

===== AcceptedCmp2 =====
[0, 1]

===== Complain =====
[0, 1]

===== Z_CostContact =====
[3]

===== Z_Revenue =====
[11]

===== Response =====
[1, 0]
```

### **1. Converting `Date` Data**

To facilitate the feature extraction/engineering process, datetime data will be converted to the pandas datetime format.

`df["Dt_Customer"] = pd.to_datetime(df["Dt_Customer"])`

### **2. Simplifying `Marital_Status`**

Replace data / merge categories with the same meaning to reduce dimensions and redundancy in the data.

- Replace categories `Widow`, `Alone`, `Absurd`, and `YOLO` with `Single`.
- Replace category `Together` with `Married`.
- Retain the `Divorced` category.

```html
# Replace categories 'Widow', 'Alone', 'Absurd', 'YOLO' with 'Single'
df['Marital_Status'] = df['Marital_Status'].replace(['Widow', 'Alone', 'Absurd', 'YOLO'],'Single')
# Replace category 'Together' with 'Married'
df['Marital_Status'] = df['Marital_Status'].replace(['Together'],'Married')
```

`df['Marital_Status'].unique()`

'Single', 'Married', 'Divorced'

### **3. Simplifying `Education_Simple`**

The categories `2n Cycle` and `Master` are more or less the same. Thus, rows with the category `2n Cycle` will be replaced with `Master`.

`df['Education'] = df['Education'].replace(['2n Cycle'],'Master')`

**Conclusion**

Based on the check, the `Dt_Customer` column was previously in string/object format, which was not suitable, so it was changed to Datetime for processing in the Feature Engineering stage. For `Marital_Status` and `Education`, data was replaced/merged to reduce dimensions and redundancy.

## **📌 Handling Outliers**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/82cb2648-4896-4e7f-ba2b-1616f1a9d3e5)

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/4510b7f1-cc69-4513-ab42-258f2f7b5f60)
![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/140f65ab-c55b-41b5-a929-4f35c3b8a5bd)
![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/ae73a9b9-a8be-4bcd-8cb5-a9336b619ba5)

Since the `Year_Birth` column has a very distant minimum value in the years `1893-1900` and the `Income` column has a very high maximum value of `$666,666`, rows with these values will be removed to avoid value imbalances. Methods that can be used include:
- **Handling Outliers**
    - IQR (Interquartile Range)
    - Z-Score
- **Manually Trimmed**

**Choice Determination:**

- For this case, we will use the `Manually Trimmed` method to avoid excessive data removal if using Handling Outliers.
- For columns other than `Year_Birth` and `Income` that contain outliers, we will not handle them as they will undergo a `Normal Distribution Transformation` process to reduce outliers.

**Manually Trimmed**

- For the `Year_Birth` column, remove extremely distant values in the years `1893-1900`.
- For the `Income` column, remove the extremely high value of `$666,666`.

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/504e3f4a-97bc-4da6-b8c9-536bb6fc0e49)

**Conclusion**
Based on calculations using `Z-score` and `IQR`, the number of rows removed from `Year_Birth` and `Income` using `IQR` is not much different from `Z-score`:
- IQR:
    - Data before handling outliers: 2240
    - Data after handling outliers (Year_Birth): 2237
    - Data after handling outliers (Income): 2229

- Z_Score:
    - Data before handling outliers: 2240
    - Data after handling outliers (Year_Birth): 2237
    - Data after handling outliers (Income): 2229

However, to minimize data removal, we use `Manually Trimmed` to focus only on extremely high values:

- Data before handling outliers: 2240
- Data after handling outliers (Year_Birth): 2237
- Data after handling outliers (Income): 2236

## **📌 Feature Engineering / Extraction**

We will perform Calculation, Extraction, and Binning features:
- Age Customer
- Age Group
- Has Child
- Dependents
- Month Customer (Lifetime)
- Spending
- Primer and Tersier product
- Total of Purchases
- Total_Cmp (Accepted Campaign 1-5)
- Ever_Accept (Accepted Campaign 1-5)
- Total Revenue
- Income Segment
- Conversion Rate Web
- Month Joined
- Recency Segment

**Create `Age` Column**

Based on the data, the base year is: SAS Institute, 2014.

**Create `Age Group` Column**

[source age group](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.semanticscholar.org%2Fpaper%2FHuman-Age-Group-Classification-Using-Facial-Bhat-V.K.Patil%2F19ddb412336ce633c1fe21544605c7bd65ff8d66&psig=AOvVaw3Sm17zYYJRrkisQVRyg4rf&ust=1684919686463000&source=images&cd=vfe&ved=0CBMQjhxqFwoTCJDXlY2Ni_8CFQAAAAAdAAAAABAI)

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/7f19ab5e-b8db-4728-b83c-d68e14ddf5d7)

Simplified further:
- Young Adult < 30
- Adult 30-45 Years
- Senior Adult > 45 years

**Create `Has_child` Column**

Combine Kidhome and Teenhome into the Has_child feature, where the sum indicates having at least 1 child.

**Create `Dependents` Column**

The number of dependents of the customer, from the sum of Kidhome and Teenhome.

**Create `Lifetime` Column**

How many months the customer has been with the supermarket since their first purchase.

**Create `Spending` Column**

The total purchase amount of each customer across all products.

**Create `Primer and Tersier product` Column**

The purchase amount of each customer for primary and tertiary product groups.

**Create `Total of Purchases` Column**

The total number of purchases by each customer across all purchase methods.

**Create `Total_Cmp` Column**

How many times each customer responded to the 5 campaigns conducted (AcceptedCmp 1 - 5).

**Create `Ever_Accept` Column**

Whether the customer ever accepted a campaign at least once or never at all.

**Create `Total Revenue` Column**

The number of campaigns responded to/accepted (Campaign 1-5) multiplied by revenue = 11.

**Create `Income Segmentation` Column**

- None -> Missing values
- High -> >= q3(68468)
- Medium -> q1(35335) - q3(68468)
- Low -> < q1(35335)

**Create `Conversion Rate Web` Column**

The ratio of Total Purchases to the Number of Website Visitors.

**Create `Month Joined` Column**

Extract the month from the date the customer first shopped.

Note: The year is not used as it may introduce bias due to its increasing value over time, while the month repeats each period.

**Create `Recency_sgmt` Column**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/67179e33-ba86-402d-948a-be1bcc795c79)

Estimated division with a 19-day range:
- 4 score -> half a month
- 3 score -> 1 month
- 2 score -> 1.5 months
- 1 score -> 2 months
- 0 score -> 3 months

#### **Check Extraction Values**

**Categorical (String)**

- Education - Basic, Graduation, Master, PhD
- Marital_Status - Single, Married, Divorced
- Age_group - Young Adult, Adult, Senior Adult
- Income_sgmt - High, Medium, Low

**Categorical (Int)**

- ID
- Kidhome - 0, 1, 2
- Teenhome - 0, 1, 2
- AcceptedCmp1 - 0, 1
- AcceptedCmp2 - 0, 1
- AcceptedCmp3 - 0, 1
- AcceptedCmp4 - 0, 1
- AcceptedCmp5 - 0, 1
- Ever_Accept - 0, 1
- Complain - 0, 1
- Response - 0, 1
- Has_child - 0, 1
- Recency_sgmt - 0, 1, 2, 3, 4

**Numericals**

- Year_Birth = 1940 - 1996
- Income = 1730.0 - 162397.0
- Kidhome = 0 - 2
- Teenhome = 0 - 2
- Recency = 0 - 99
- Age = 18 - 74
- Dependents = 0 - 3
- Lifetime = 1 - 36
- Spending = 5 - 2525
- Primer_purchase = 1 - 1727
- Tersier_purchase = 3 - 1689
- Total_Purchases = 0 - 44
- NumWebVisitsMonth = 0 - 20
- Conversion_rate_web = 0.0 - 43.0
- Total_Cmp = 0 - 4
- Total_revenue = 0 - 44
- Month_joined = 1 - 12

**Numericals (one)**

- Z_CostContact = 3
- Z_Revenue = 11

**Numericals (Product)**

- MntWines = 0 - 1493
- MntFruits = 0 - 199
- MntMeatProducts = 0 - 1725
- MntFishProducts = 0 - 259
- MntSweetProducts = 0 - 263
- MntGoldProds = 0 - 362

**Numericals (Purchases)**

- NumDealsPurchases = 0 - 15
- NumWebPurchases = 0 - 27
- NumCatalogPurchases = 0 - 28
- NumStorePurchases = 0 - 13

**Timestamp**
- Dt_Customer = 2012-07-30 - 2014-06-29

## **📌 Feature Transformation (Numeric)**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/4962331e-fede-4185-9b24-676068f53654)

From the findings, we can determine the transformations to be performed:
- **Scaling and Converting to a Normal Distribution:**
    - Log Transformation
    - Box-Cox Transformation
    - Yeo-Johnson Transformation
    
    **Columns to be transformed in this process:**
        - Conversion_rate_web
        - MntFishProducts
        - MntFruits
        - MntGoldProds
        - MntMeatProducts
        - MntSweetProducts
        - MntWines
        - NumCatalogPurchases
        - NumDealsPurchases
        - NumStorePurchases
        - NumWebPurchases
        - Primer_purchase
        - Spending
        - Tersier_purchase
        - Total_revenue
    
- **Just Scaling:**
    - Normalization
    - Standardization
    
    **Columns to be transformed in this process:**
        - Age
        - Income
        - Lifetime
        - Month_joined
        - NumWebVisitsMonth
        - Recency
        - Total_Purchases
        - Year_Birth

- Columns that **do not require transformation** due to reasonable value ranges:
    - Kidhome
    - Teenhome
    - Dependents
    - Total_Cmp

**Choice Determination:**

- For `Scaling and Converting to a Normal Distribution`, we use `Yeo-Johnson Transformation` because it results in a more normal distribution curve.
- For `Just Scaling`, we use `Normalization` because it is more robust for the algorithms we will use.

**Yeo-Johnson Transformation**

Unlike the Box-Cox transform, it does not require the values for each input variable to be strictly positive.

It supports zero values and negative values. This means we can apply it to our dataset without scaling it first.

```html
pt = PowerTransformer(method='yeo-johnson')
df[log_cols] = pt.fit_transform(df[log_cols])
```

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/2c896c5e-4141-4085-ab20-490fb1d53ac0)

**Normalization**

```html
from sklearn.preprocessing import MinMaxScaler
# create a scaler object
scaler = MinMaxScaler()
# fit and transform the data
df[norm_cols] = pd.DataFrame(scaler.fit_transform(df[norm_cols]), columns=df[norm_cols].columns)
```

**Conclusion**

Based on the check of features processed using the previous transformations, the skewness values now have a more uniform range (not too far apart and not too varied). Thus, the feature transformation techniques we applied are valid.

## **📌 Feature Encoding (Categoric)**

```html
===== Education =====
['Graduation', 'PhD', 'Master', 'Basic']

===== Marital_Status =====
['Single', 'Married', 'Divorced']

===== Age_group =====
['Senior Adult', 'Young Adult', 'Adult']

===== Income_sgmt =====
['Medium', 'High', 'Low']
```
From the findings, we can determine the encoding to be performed:
- **Label Encoding:**
    - LabelEncoder
    - Manually Mapped
    
    **Columns to be processed:**
    - `Education` - Basic (0), Graduation (1), Master (2), PhD (3)
    - `Age_group` - Young Adult (0), Adult (1), Senior Adult (2)
    - `Income_sgmt` - Low (0), Medium (1), High (2)
    
- **One Hot Encoding:**
    - get_dummies
    - OneHotEncoder
    
    **Columns to be processed:**
    - `Marital_Status` - Single, Married, Divorced

**Choice Determination:**

- For `Label Encoding`, we use `Manually Mapped` because we can flexibly determine the order of categorical features.
- For `One Hot Encoding`, we use `OneHotEncoder` because the encoding results are neater and easier to adjust.

**Conclusion**

Based on the check of features processed using the previous encoding, all values are now numeric as assigned. Thus, the feature encoding techniques we applied are valid.

## **📌 Feature Selection**

Several features have been processed using feature selection:
- Drop Unnecessary Feature
- Univariate Selection
    - Anova F-value
    - Variance Threshold
    - Mutual Information
    - SelectKBest
- Feature Importance
- Pearson Correlation
- Drop Redundancy

### **1. Drop Unnecessary Feature**

- Drop the `ID` column because it has many categories and is not useful for modeling.
- Drop the `Year_Birth` column as feature extraction was performed to derive `Age` data based on the current year range of 2014 (as per the data).
- Drop the `Dt_Customer` column because it does not significantly affect the prediction model.
- Drop the `Z_CostContact` (3) and `Z_Revenue` (11) columns because they have only one value, providing no significant information for the prediction model.

### **2. Univariate Selection**

- #### **ANOVA F-value**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/adc3f215-9dd5-424b-b20c-53a61e328c8a)

- #### **Variance Threshold**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/6a369f9b-f13e-46a1-abeb-6fa28a0e960d)

- #### **Mutual information**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/fce9e499-0769-4e3a-b8fa-5c3af1e351e3)

- #### **Scikit-learn’s SelectKBest**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/fdb9ba08-f74b-466a-b576-b8549447682d)

### **3. Feature Importance**

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/03a29c62-7ad0-4c0b-9021-6b11741e4a60)

### **4. Correlation Matrix with Heatmap**

- Correlation states how the features are related to each other or the target variable.
- Correlation can be positive (an increase in one feature value increases the target variable value) or negative (an increase in one feature value decreases the target variable value).
- A heatmap makes it easy to identify which features are most related to the target variable. We will plot a heatmap of correlated features using the seaborn library.
- Check for redundant features in the correlation between features, and drop the one with the lower correlation to the Response (target).

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/0e6b13a0-edf4-4dd1-be56-46092925d577)

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/9f660917-acd4-4669-a6c6-8f116e5520d6)

### **5. Check Data Redundancy**

From the selected features, combining the Top 20, we will recheck for redundancy between features. In this process, we select features with a correlation above a `threshold > 0.70`, then compare their correlation with the target to `drop one of the features`.

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/490e565d-5bb6-4423-928f-e152cf117bd3)

The features to be used in the modeling process are as follows:

```html
['AcceptedCmp1',
 'AcceptedCmp2',
 'AcceptedCmp3',
 'AcceptedCmp4',
 'Dependents',
 'Education',
 'Lifetime',
 'Married',
 'MntGoldProds',
 'NumCatalogPurchases',
 'NumDealsPurchases',
 'NumWebVisitsMonth',
 'Recency',
 'Recency_sgmt',
 'Total_Cmp']
```

## **📌 Data Splitting**

I will split the data into a training set and a testing set with a proportion of 75:25.

```html
# define X and y
X = df.drop(['Response'], axis=1)[feature_importance] #features
y = df['Response'] #target
```

```html
from sklearn.model_selection import train_test_split

# splitting the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, stratify= y, random_state=42)
print(X_train.shape, X_test.shape)
```

## **📌 Handling Imbalanced Data**

The status is highly imbalanced, with 15% Response and 85% No Response. Thus, resampling is needed.

**Note**: When applying machine learning algorithms with imbalanced data, the resulting model will be biased toward the majority class. This means the model will predict the majority class rather than the minority class.

If we want to perform classification, we should first perform a `stratified train_test_split` to maintain the imbalance. This ensures the test and train datasets have the same distribution, and then we should never touch the test set again. Resampling should then be performed only on the training data.

**Summary**: You must apply `SMOTE` after splitting into `training and test`, not before. Doing SMOTE before is invalid and defeats the purpose of having a separate test set.

![image](https://github.com/nurimammasri/Marketing-Campaign-Model-Prediction-by-Datalicious/assets/54845293/499d8c10-193b-45d7-9502-ed1da4604c47)

```html
from imblearn.under_sampling import RandomUnderSampler
from imblearn.over_sampling import RandomOverSampler, SMOTE

....

# Oversampling SMOTE
sm = SMOTE(sampling_strategy=0.5, random_state = 2)
X_balanced_res, y_balanced_res = sm.fit_resample(X_train,y_train)
```

- Before OverSampling, the shape of X_train: (1677, 15)
- Before OverSampling, the shape of y_train: (1677,) 

- Before OverSampling, counts of label '1': 251
- Before OverSampling, counts of label '0': 1426 

