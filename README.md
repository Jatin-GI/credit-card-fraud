# 💳 Credit Card Fraud Detection

This project focuses on detecting fraudulent credit card transactions using **unsupervised machine learning techniques** on an imbalanced dataset. Fraud detection is a critical real-world application where the aim is to detect rare fraudulent activities from a large set of normal transactions.

---

## 📌 Problem Overview

- The dataset contains credit card transactions by European cardholders in September 2013.
- The main challenge is the **extreme class imbalance**:
  - Normal Transactions: 284,315
  - Fraudulent Transactions: 492

---

## 📊 Dataset Summary

- **Rows:** 284,807 transactions
- **Columns:** 31 (30 numerical features + target)
- **Target:** `Class`  
  - `0` = Normal Transaction  
  - `1` = Fraudulent Transaction

The dataset has been anonymized using **Principal Component Analysis (PCA)** to protect confidentiality. Only the `Time` and `Amount` columns are unaltered.

📂 Dataset Source: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

---

## 🚀 Technologies Used

- Python 🐍
- Pandas & NumPy 📊
- Matplotlib & Seaborn 📈
- Scikit-learn 🤖
- Jupyter Notebook

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked for **missing values** (Result: No missing data ✅)
- Visualized **class imbalance** using bar plots.
- Plotted **transaction amount distributions** for both Fraud and Normal classes using histograms with logarithmic scaling.
- Generated a **correlation heatmap** to identify relationships between features.

Key Findings:
- Fraud transactions are extremely rare (~0.17%)
- Fraud transaction amounts tend to be lower on average but have significant variation.

---

## ⚙ Machine Learning Approach: Unsupervised Anomaly Detection

Since this is an **unsupervised anomaly detection problem** (very limited fraud labels), three algorithms were used:

| Algorithm              | Description                              | Performance Summary                               |
|------------------------|------------------------------------------|--------------------------------------------------|
| **Isolation Forest** 🏝  | Anomaly detection by isolating outliers  | Best performer: F1-Score ~0.26                    |
| **Local Outlier Factor** 🌳 | Detects local density anomalies          | Struggled with high imbalance                     |
| **One-Class SVM** ⚙     | SVM boundary-based anomaly detection      | Poor accuracy, too many false positives (70% acc) |

---

## 📝 Implementation Highlights

1. **Data Sampling:**  
   Used 10% of the full dataset to speed up model training and testing.

2. **Class Distribution Plot:**  
   Bar plot showing severe imbalance between Fraud (1) and Normal (0).

3. **Transaction Amount Distribution:**  
   Histograms showing that fraud amounts are generally lower.

4. **Correlation Heatmap:**  
   Seaborn heatmap to visualize correlations between anonymized features.

5. **Model Training & Evaluation:**  
   Evaluated models using:
   - **Accuracy Score**
   - **Precision**
   - **Recall**
   - **F1-Score**

---

## 📈 Evaluation Metrics (on 10% sampled data)

| Model                   | Accuracy | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) |
|-------------------------|----------|-------------------|----------------|------------------|
| **Isolation Forest**     | 99.74%   | 0.26              | 0.27           | 0.26             |
| **Local Outlier Factor** | 99.65%   | 0.02              | 0.02           | 0.02             |
| **One-Class SVM**        | 70.09%   | 0.00              | 0.37           | 0.00             |

➡ **Isolation Forest** performed the best overall in detecting fraudulent transactions.

---

## 🖥 How to Run the Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Jatin-GI/credit-card-fraud.git
   cd credit-card-fraud
2. (Optional) Create Virtual Environment:
   python -m venv venv
   venv\Scripts\activate    # On Windows
   source venv/bin/activate # On Mac/Linux
3. Install Dependencies:
   pip install -r requirements.txt


## ✅ Key Takeaways

- Unsupervised learning techniques like **Isolation Forest** and **Local Outlier Factor** are effective when labeled fraud data is scarce.
- The project highlights the challenge of working with **extremely imbalanced datasets**, a common scenario in real-world fraud detection.
- Visualizations such as **class distribution plots**, **transaction amount histograms**, and **correlation heatmaps** help in better understanding the underlying data patterns.
- **Isolation Forest** achieved the best balance between detecting fraud and minimizing false alarms.
- Even simple models can provide valuable results when combined with **good exploratory data analysis** and **careful evaluation**.

---

## 🚀 Future Improvements

- Implement **SMOTE (Synthetic Minority Over-sampling Technique)** or other **resampling methods** to better handle class imbalance.
- Explore **Autoencoder-based anomaly detection** or other **deep learning techniques** for improved detection accuracy.
- Evaluate **ensemble approaches** that combine multiple models to increase robustness.
- Develop a **real-time streaming fraud detection pipeline** using tools like Apache Kafka or Spark Streaming.
- Deploy the trained model as a **web service (API)** for real-time use cases.

---

## 🤝 Contributions

Contributions are welcome!  
If you'd like to improve this project, feel free to:

- ⭐ Star the repository
- 🐛 Report issues
- 🔀 Submit pull requests

Please ensure your code follows good practices and includes clear explanations and documentation.

---

## 📜 License

This project is licensed for **educational and research purposes only**.  
All content is provided "as-is" without any warranties or guarantees.  
Please ensure you use the provided code responsibly, especially when applying it to real-world financial or sensitive data scenarios.

---
    
