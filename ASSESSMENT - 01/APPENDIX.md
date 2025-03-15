# 🍽️ Predicting Customer's Favorite Dish using XGBoost

## 📌 Project Overview
This project aims to build an **XGBoost-based machine learning model** that predicts a customer's favorite dish based on their dining preferences and behavior. The solution applies **data preprocessing, feature engineering, one-hot encoding**, and model training while ensuring the correct handling of time-based data.

## 📂 Dataset
The dataset **dining_info.xlsx** contains:
- **customer_id** – Unique identifier for each customer.
- **transaction_id** – Unique identifier for each transaction.
- **Preferred Cuisine** – The customer's preferred cuisine.
- **dish** – The dish ordered (Target Variable).
- **price_for_1** – Price for one unit of the dish.
- **order_time** – Timestamp of the order.
- **Qty** – Quantity of the dish ordered.
- **stay_duration** – Duration of the customer’s stay.
- **check_in_date** / **check_out_date** – Booking dates.

## 🛠️ Project Workflow
1. **Data Preparation**
   - Split data into:
     - **Feature Extraction Dataset** (Before Jan 1, 2024)
     - **Training Dataset** (Jan 1 – Oct 1, 2024)
     - **Testing Dataset** (Post Oct 1, 2024)
   - Extract meaningful customer preferences for modeling.

2. **Feature Engineering**
   - **Customer-Level Features:** Total transactions, average spend, total quantity ordered.
   - **Cuisine-Level Features:** Average price per cuisine, most preferred cuisine.
   - **Booking-Based Features:** Check-in date, check-out duration, stay duration.

3. **Data Integration**
   - Merge training and test datasets with extracted features.
   - Drop unnecessary columns to prevent data leakage.

4. **Encoding Categorical Data**
   - One-Hot Encoding for **Preferred Cuisine**, customer preferences.
   - Label Encoding for the **dish (target variable)**.

5. **Model Training**
   - **XGBoost Classifier** for multi-class classification.
   - Handle missing values for new customers.
   - Experiment with hyperparameters:
     - **Learning Rate:** 0.01 - 1
     - **Max Depth:** 1 - 5
     - **Estimators:** 50 - 500

6. **Model Evaluation**
   - **Accuracy Score** (Target: ≥13%, Challenge: 20%)
   - **Log Loss** to penalize incorrect high-confidence predictions.
   - **Feature Importance Analysis** to identify key predictors.

## 🚫 Features NOT Allowed in Training & Why
| Feature        | Reason for Exclusion |
|---------------|----------------------|
| transaction_id | No predictive value |
| customer_id | Aggregated behavior used instead |
| order_time | Not known beforehand |
| Qty | Not known beforehand |
