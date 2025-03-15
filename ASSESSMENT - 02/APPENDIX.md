## 📖 Overview  
This document outlines the implementation of Assessment 2, where a **hotel booking system** was developed with personalized dining recommendations. This system builds on the foundation set in Milestone 1 by incorporating **machine learning** and **database integration** to enhance user experience.  

## 🏗️ System Components  

### 🔹 **User Input Collection**  
- Customers enter their details, including **name, email, check-in/check-out dates, age, number of stayers, preferred cuisine, and booking preferences**.  
- If a **Customer ID** is not provided, a new one is automatically generated.  

### 🔹 **Data Processing & Feature Engineering**  
- Converts **check-in and check-out dates** into **weekday and month indicators**.  
- Combines multiple datasets containing information on **customer preferences, behavior, and loyalty**.  
- Categorical variables are encoded using **OneHotEncoder**, ensuring alignment with the trained model.  

### 🔹 **Machine Learning Model (XGBoost)**  
- The trained **XGBoost model** predicts the top **three personalized dish recommendations**.  
- Uses a **label encoder** to map predictions back to dish names.  

### 🔹 **Database Integration (MongoDB)**  
- Customer booking details are stored in a **MongoDB database** for future reference and analysis.  

### 🔹 **Automated Email Notifications**  
- A **unique discount coupon** is generated for each customer.  
- Booking confirmation and coupon details are sent via **email using SMTP**.  

## 🎯 Implementation Workflow  

1️⃣ **User inputs booking details through a form**  
2️⃣ **Data is preprocessed and transformed into a model-ready format**  
3️⃣ **The trained XGBoost model predicts top dishes**  
4️⃣ **Booking details are stored in MongoDB**  
5️⃣ **Email confirmation with discount code is sent to the customer**  
6️⃣ **A confirmation message is displayed on the web interface**  

## 📊 Key Observations  

✔️ **Accurate dish recommendations** enhance customer satisfaction.  
✔️ **Real-time data storage** in MongoDB ensures seamless tracking of bookings.  
✔️ **Automated email notifications** improve the customer experience.  
✔️ **The web interface is interactive and user-friendly.**  

  
