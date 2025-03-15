# 🏨 Assessment 3: Hotel Review Analysis System  

## 📌 Overview  
This assessment focuses on developing a **hotel review analysis system** by integrating:  
- **Together AI embeddings** for text processing.  
- **Pinecone** for vector storage and similarity search.  
- **Streamlit** for an interactive user interface.  

The system enables **real-time review submissions, sentiment analysis, review retrieval, and managerial insights**.  

---

## 📂 **System Components**  

### **1️⃣ Customer Review Submission UI**  
- Customers submit hotel reviews in real time.  

### **2️⃣ Sentiment Analysis**  
- **TextBlob** computes the sentiment score.  
- If a **negative review** is submitted and the customer is still at the hotel:  
  - An **automated email** is sent to the manager with:  
    - **Room number**  
    - **Review text**  
    - **Sentiment score**  

### **3️⃣ Manager Review Analysis UI**  
Built using **Streamlit**, this dashboard allows managers to:  
- **Query customer reviews** based on specific topics.  
- **Retrieve relevant reviews** using **Pinecone similarity search**.  
- **Summarize customer sentiments** using **Together AI**.  
- **Generate a word cloud** of frequently mentioned words.  
- **Download sentiment analysis reports** in `.txt` format.  

---

## 🚀 **Implementation Steps**  

### **1️⃣ Install Dependencies**  
```sh
pip install streamlit textblob pinecone-client together pandas numpy
