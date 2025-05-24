# 📊 Telco Customer Churn Prediction

This project applies and compares several machine learning algorithms to predict customer churn using the popular **Telco Customer Churn** dataset from Kaggle.

## 💡 Objective

To identify customers who are likely to cancel their subscription (churn) and compare the performance of different classification models to support decision-making for retention strategies.

---

## 📁 Project Structure

- `notebook/`: Contains the complete analysis notebook (`telco_churn_analysis.ipynb`)
- `data/`: Information on the dataset origin and format (not included directly)
- `images/`: Key plots (confusion matrices, ROC curves, etc.)
- `reports/`: Final summary or presentation-ready content
- `README.md`: Project documentation
- `requirements.txt`: Python dependencies

---

## 🛠️ Methods Applied

- Exploratory Data Analysis (EDA)
- Handling missing values and outliers
- Feature encoding (binary + one-hot)
- Class balancing using **SMOTE**
- Standardization with **StandardScaler**
- Train/Test split with stratification
- Evaluation with **classification report**, **AUC**, **confusion matrix**
- **Cross-validation (5-fold)** to estimate generalization

---

## 🤖 Models Compared

| Model           | F1 (CV) | Accuracy | Recall (Churn) | AUC    |
|----------------|---------|----------|----------------|--------|
| Decision Tree  | 0.589   | 0.72     | 0.73           | 0.799  |
| KNN            | 0.567   | 0.70     | 0.61           | 0.761  |
| Naive Bayes    | 0.571   | 0.65     | **0.86**       | 0.795  |
| SVM            | **0.612** | **0.77** | 0.64           | **0.815** |
| MLP            | 0.556   | 0.77     | 0.58           | 0.806  |

> Full analysis and metrics are available in the notebook.

---

## 📈 Key Insights

- **SVM** and **MLP** achieved the best balanced performance.
- **Naive Bayes** had the highest churn recall, useful for high-risk detection.
- **Decision Tree** is a good interpretable baseline with decent recall.

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/telco-customer-churn.git
cd telco-customer-churn
```
### 2. Install the required packages
```bash
pip install -r requirements.txt
```
### 3. Launch notebook
```bash
jupyter notebook notebook/telco_churn_analysis.ipynb
```
