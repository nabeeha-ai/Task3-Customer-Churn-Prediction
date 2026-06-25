# Task 3: Customer Churn Prediction (Bank Customers)

> **DevelopersHub Corporation — Data Science & Analytics Internship**

---

## Objective

Predict whether a bank customer is likely to **leave (churn)** the bank based on their personal and account information. Early identification of at-risk customers allows banks to take proactive retention measures before losing them.

---

## Dataset

**Churn Modelling Dataset**

| Detail | Info |
|--------|------|
| Records | 10,000 customers |
| Features | 13 input features |
| Target | `Exited` (1 = Churned, 0 = Stayed) |
| Churn Rate | ~26% |

### Features Used

| Feature | Description |
|---------|-------------|
| `CreditScore` | Customer's credit score |
| `Geography` | Country — France, Germany, Spain |
| `Gender` | Male / Female |
| `Age` | Customer's age |
| `Tenure` | Years with the bank |
| `Balance` | Account balance |
| `NumOfProducts` | Number of bank products used |
| `HasCrCard` | Has credit card (1 = Yes, 0 = No) |
| `IsActiveMember` | Active member (1 = Yes, 0 = No) |
| `EstimatedSalary` | Estimated annual salary |
| **`Exited`** | **Target variable** |

---

## Approach

### 1. Exploratory Data Analysis (EDA)
- Analyzed churn distribution across geography, gender, age groups
- Visualized how balance, salary, credit score relate to churn
- Examined churn rates by number of products and membership activity
- Generated correlation heatmap to identify key relationships

### 2. Data Preprocessing
- Dropped irrelevant columns (`RowNumber`, `CustomerId`, `Surname`)
- Applied **Label Encoding** for `Gender`
- Applied **One-Hot Encoding** for `Geography`
- Applied **StandardScaler** for feature scaling (Logistic Regression)
- Train-Test Split: **80% train / 20% test** (stratified)

### 3. Model Training
Three classification models were trained and compared:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

### 4. Evaluation
- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- Feature Importance Analysis

---

## Results

| Model | Accuracy |
|-------|----------|
| Logistic Regression | ~79% |
| Decision Tree | ~83% |
| **Random Forest** | **~86%** |

**Best Model: Random Forest Classifier (~86% accuracy)**

---

## Key Insights

1. **Age** is the strongest predictor of churn — customers aged **40–60** are most at risk
2. **Germany** has the highest churn rate among all regions
3. **Female customers** churn more than male customers
4. **Inactive members** are significantly more likely to churn
5. Customers with **3–4 products** show unexpectedly high churn rates
6. Customers with **zero balance** are also a high-risk group

---

## Repository Structure

```
Task3-Customer-Churn-Prediction/
│
├── Task3_Customer_Churn_Prediction.ipynb   # Main Jupyter Notebook
├── Churn_Modelling.csv                     # Dataset
└── README.md                               # Project documentation
```

---

## Libraries Used

```python
pandas, numpy, matplotlib, seaborn, scikit-learn
```

---

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/Task3-Customer-Churn-Prediction.git

# 2. Navigate to folder
cd Task3-Customer-Churn-Prediction

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# 4. Open the notebook
jupyter notebook Task3_Customer_Churn_Prediction.ipynb
```

---

## Author

Nabeeha Shakeel
Data Science & Analytics Intern — DevelopersHub Corporation
