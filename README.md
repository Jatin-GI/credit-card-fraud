# Credit Card Fraud Detection

This project aims to detect fraudulent credit card transactions using Machine Learning techniques. The dataset contains transactions made by credit cards in September 2013 by European cardholders.

## 📂 Project Structure

credit-card-fraud/
├── fraud_detection.ipynb
├── dataset.csv
└── README.md


## 🚀 Technologies Used

- Python
- Jupyter Notebook
- Scikit-learn
- Pandas
- Matplotlib / Seaborn

## 📝 Dataset

The dataset is highly unbalanced, with fraud cases representing only a small fraction of all transactions. It contains numerical input variables which are the result of a PCA transformation for confidentiality.

- **Features:** V1, V2, ..., V28
- **Amount:** Transaction Amount
- **Time:** Seconds elapsed between transactions
- **Class:** Target variable (1 = Fraud, 0 = Not Fraud)

## 🔍 Steps Performed

1. Data Exploration & Visualization
2. Data Preprocessing
3. Handling Imbalanced Data
4. Model Training:
   - Logistic Regression
   - Decision Tree
   - Random Forest
5. Model Evaluation (Accuracy, Precision, Recall, F1-Score)

## ⚙ How to Run

1. Clone this repository:
git clone https://github.com/Jatin-GI/credit-card-fraud.git

2. Navigate to the project directory:
cd credit-card-fraud

3. Install required libraries:
pip install -r requirements.txt

4. Open and run the Jupyter Notebook:
jupyter notebook fraud_credit_card.ipynb


## 📊 Results

- Achieved high precision in detecting fraudulent transactions.
- Visualizations help in understanding the distribution of fraud vs. non-fraud cases.

## 📌 Note

This project is for educational purposes only. The dataset used is anonymized to protect user confidentiality.

---

✅ Contributions and suggestions are welcome!


