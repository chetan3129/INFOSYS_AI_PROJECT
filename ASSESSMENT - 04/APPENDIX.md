# 📊 Assignment 4: Hotel Guests Dashboard with Dash, Plotly, and Streamlit  


## 🎯 Objective  
The goal of this assignment is to **store, process, and visualize** three datasets (**Booking Data, Dining Info, and Reviews Data**) using **MongoDB, Pandas, Dash, and Plotly**.  

---

## 📌 **Tasks & Implementation Steps**  

### **Step 1: Load and Store Data in MongoDB**  
- Ensure **MongoDB** is running locally or use **MongoDB Atlas** for cloud storage.  
- Read the following datasets:  
  1. **Booking Data**  
  2. **Dining Info Data**  
  3. **Reviews Data**  
- Store each dataset in **separate MongoDB collections**.  
- Verify data integrity by retrieving a few records from MongoDB.  

📌 **Tools Used:** `pymongo` for inserting and retrieving data.  

---

### **Step 2: Read Data from MongoDB into Pandas**  
- Connect to MongoDB and fetch each dataset.  
- Convert data into **Pandas DataFrames** for processing.  
- Perform necessary **data cleaning and transformation**:  
  - Handle missing values.  
  - Convert date columns to **datetime format**.  
  - Ensure numerical fields are correctly formatted.  

📌 **Tools Used:** `pandas`, `pymongo`  

---

### **Step 3: Build Interactive Dashboards Using Dash & Plotly**  

💡 **Use Dash to create an interactive web application** with the following dashboards:  

#### 📊 **Dashboard 1: Hotel Booking Insights**  
- **Bookings Trend Over Time**: Line chart showing daily hotel bookings.  
- **Preferred Cuisine Analysis**: Popular cuisines among customers.  
- **Average Length of Stay**: Weekly and monthly stay duration analysis.  

#### 🍽️ **Dashboard 2: Dining Insights**  
- **Average Dining Cost by Cuisine**: Pie chart of cost distribution.  
- **Customer Count Over Time**: Trends in dining visits.  

#### 📝 **Dashboard 3: Reviews Analysis**  
- **Sentiment Analysis**: Pie chart showing **positive, neutral, and negative** reviews.  
- **Rating Distribution**: Histogram of review ratings.  
- **Word Cloud of Customer Feedback** (Optional NLP Visualization).  

📌 **Tools Used:** `Dash`, `Plotly`, `pandas`, `MongoDB`  

---

### **Step 4: Integrate Everything into Streamlit**  
- Combine all **Dash visualizations** into a **Streamlit web application**.  

### **Addition to Assignment 2: Real-Time Sentiment Analysis**  
- Implement **a sentiment analyzer** in the **real-time review UI page**.  
- Use a **pretrained sentiment detector** (e.g., `TextBlob`) to calculate **sentiment scores**.  
- If a customer **currently staying at the hotel** submits a **negative review**, trigger an **email alert** to the manager containing:  
  - **Room number**  
  - **Review text**  
  - **Sentiment score**  

📌 **Tools Used:** `Streamlit`, `TextBlob`, `smtplib` (for email alerts).  

---


### **1️⃣ Install Dependencies**  
Run the following command to install required packages:  
```sh
pip install pymongo pandas dash plotly streamlit textblob openpyxl
