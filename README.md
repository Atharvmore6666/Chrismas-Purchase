# Chrismas-Purchase
This project focuses on analyzing and predicting customer purchase behavior during the Chrismas sales. Using the provided dataset, we aim to identify key factors influencing purchase amounts and build predictive models to estimate purchase values.

# Black Friday Purchase Prediction

## Project Overview
This project focuses on analyzing and predicting customer purchase behavior during Black Friday sales. Using transactional data, we aim to identify factors influencing purchase amounts and build machine learning models to predict purchase values accurately.

---

## Motivation
Understanding customer behavior during Black Friday sales helps retailers:
- Optimize marketing strategies
- Improve inventory management
- Enhance the shopping experience

Leveraging machine learning allows us to uncover insights and establish a predictive framework.

---

## Dataset Description
The dataset includes transactional data from Black Friday sales. Below is an overview:

| Column Name                | Description                               | Data Type    |
|----------------------------|-------------------------------------------|--------------|
| User_ID                   | Unique identifier for each user          | int64        |
| Product_ID                | Unique identifier for each product       | object       |
| Gender                    | Gender of the user                       | object       |
| Age                       | Age group of the user                    | object       |
| Occupation                | Occupation code of the user              | int64        |
| City_Category             | Category of the city                     | object       |
| Stay_In_Current_City_Years| Years of stay in the current city         | object       |
| Marital_Status            | Marital status of the user (0 or 1)       | int64        |
| Product_Category_1        | Product category code (primary)          | int64        |
| Product_Category_2        | Product category code (secondary)        | float64      |
| Product_Category_3        | Product category code (tertiary)         | float64      |
| Purchase                  | Purchase amount                          | int64        |

---

## Data Preprocessing
1. **Handling Missing Values:**
   - Imputed `Product_Category_2` with its median.
   - Dropped `Product_Category_3` due to excessive missing values.

2. **Label Encoding:**
   - Encoded categorical columns like `Gender`, `Age`, and `City_Category`.

3. **Feature Selection:**
   - Dropped irrelevant columns: `User_ID`, `Product_ID`, `Product_Category_3`.

4. **Target Variable:**
   - The target for prediction is `Purchase`.

---

## Exploratory Data Analysis

### Key Insights:
- **Purchase Distribution:** Purchase amounts follow a nearly normal distribution.
- **Demographics:** 
  - Male users dominate purchases.
  - Buyers mostly belong to City Category B.
  - Age group 26-35 is the highest purchasing segment.
- **Product Impact:** Specific product categories significantly influence purchase amounts.

---

## Model Building

### Implemented Models:
1. **Linear Regression**
   - RMSE: 4711.49
   - R² Score: 0.107
2. **KNN Regressor**
   - RMSE: 3273.01
   - R² Score: 0.569
3. **XGBoost Regressor**
   - RMSE: 2974.48
   - R² Score: 0.644

### Results:
- **Best Model:** XGBoost Regressor achieved the lowest RMSE and highest R².

---

## Conclusion
- Customer purchase amounts can be predicted effectively, with XGBoost delivering the best results.
- Influential factors include `Age`, `City_Category`, and `Product_Category_1`.

### Future Directions:
- Perform advanced feature engineering.
- Experiment with deep learning models for further improvement.

---

