# 🛍️ Customer Satisfaction Prediction in E-Commerce

This project uses machine learning to predict whether an e-commerce customer is **satisfied or dissatisfied**, using transactional and behavioral features like delivery timing, shipping cost, product category, and payment value.

---

## 📌 Project Highlights

- **Task**: Binary classification of customer satisfaction  
- **Dataset**: Brazilian E-commerce Public Dataset (Kaggle)  
- **Features**: Delivery, payment, shipping, product metadata  
- **Techniques**: Feature engineering, class imbalance handling, model benchmarking  
- **Models**: Logistic Regression, Random Forest, XGBoost, MLP  
- **Evaluation**: ROC AUC, Weighted Precision, Recall, and F1  

---

## 📊 Class Distribution

### 🔄 Before Binary Classification  
![Review Score Distribution](<Plots/Class Imbalance before Binary Classification.jpg>)

### ✅ After Binary Classification  
![Satisfaction Distribution](<Plots/Class Imbalance after Binary Classification.jpg>)

---

## 🧪 Handling Imbalance

We addressed severe class imbalance by:

- Transforming review scores into binary classes (≤3 → 0, ≥4 → 1)  
- Applying `class_weight='balanced'` in models  
- Using stratified train-test split  
- Evaluating models using **weighted F1 and ROC AUC**

---

## 🧠 Feature Importance

Random Forest revealed top predictors of satisfaction:

- **payment_value**, **freight_value**, **delivery_days**
- Categorical impact: **product_category**, **payment_type**

![Feature Importance](<Plots/Feature Importance - Random Forest.jpg>)

---

## 📦 Delivery & Satisfaction Insights

### 🚚 Satisfaction vs. Delivery Status  
On-time delivery significantly correlates with higher satisfaction.

![Satisfaction vs Delivery](<Plots/Customer Satisfaction vs Delivery Status.jpg>)

### ⏱️ Top Delayed Categories  
Some product categories have high late delivery rates.

![Delay by Category](<Plots/Top 10 product categories by Delay.jpg>)

---

## 💸 Shipping Economics

Categories with higher freight values per order:

![Top Freight Categories](<Plots/Top 20 categories by total freight value.jpg>)

---

## 🤖 Models Used

| Model               | Accuracy | Weighted F1 | ROC AUC |
|--------------------|----------|-------------|---------|
| Logistic Regression | 72.4%    | 72.8%       | 65.9%   |
| Random Forest       | 80.6%    | 77.4%       | 69.9%   |
| XGBoost             | 72.8%    | 73.9%       | 70.1%   |
| MLP Neural Network  | 73.1%    | 73.9%       | 68.9%   |

### 📈 ROC AUC Comparison  
![ROC AUC Curve](<Plots/ROC AUC Curve.jpg>)

---

## 🧠 Key Takeaways

- Delayed deliveries and higher shipping costs are major drivers of dissatisfaction.
- Random Forest performed best overall with high interpretability.
- A balance between accuracy and business explainability is essential.

---

## 📁 Folder Structure

```
customer_satisfaction_prediction/
├── data/              # Preprocessed dataset
├── notebook/          # Jupyter Notebook
├── plots/             # Visualizations
├── models/            # Saved model artifacts (will be uploaded on hugging face shortly...)
└── README.md          # Project documentation
```

---

## 🚀 Future Enhancements

- Integrate sentiment analysis from review text
- Apply TabNet Neural Network for better model performance
- Deploy as a Streamlit dashboard or FastAPI microservice

---

## 🔗 Dataset

Available at [Kaggle: Brazilian E-Commerce Dataset](https://www.kaggle.com/olistbr/brazilian-ecommerce)

---

## 🧠 Author

Built by **Abhishek Malaviya** and team.
Tools: Python, Scikit-learn, XGBoost, Seaborn, Matplotlib, Jupyter
