# 🏠 House Price Prediction Analysis

This repository contains a comprehensive study of various Machine Learning models applied to the **Housing Dataset** from Kaggle. The goal is to predict house prices based on features like area, bedrooms, bathrooms, and location perks.

## 📋 Project Workflow
1.  **Data Preprocessing**: 
    * Categorical variables handled via `OneHotEncoder`.
    * Numerical features scaled using `StandardScaler`.
2.  **Feature Engineering**: 
    * Applied `PolynomialFeatures` to capture non-linear relationships.
3.  **Model Selection**: 
    * Tested Linear, Polynomial, SVR, Decision Tree, and Random Forest models.

---

## 📊 Performance Comparison

Here is the final evaluation of all models tested during the project:

| Model | Train R² Score | Test R² Score | Conclusion |
| :--- | :---: | :---: | :--- |
| **Polynomial Regression (Deg 3)** | **0.93** | **0.93** | **🏆 Best Fit (Winner)** |
| **Random Forest** | 0.94 | 0.61 | Overfitting |
| **Linear Regression** | 0.68 | 0.66 | Underfitting |
| **Support Vector Regression (SVR)**| 0.77 | 0.59 | Moderate |
| **Decision Tree** | 0.75 | 0.48 | Severe Overfitting |

---

## 💡 Key Findings

* **Polynomial Wins**: The relationship between house features and price in this dataset is highly non-linear. The Degree 3 Polynomial model perfectly captured this without losing generalization.
* **The Overfitting Trap**: Tree-based models (Decision Tree & Random Forest) performed exceptionally well on training data but failed to generalize to the test set, showing the importance of model pruning and cross-validation.
* **Target Scaling**: For SVR, scaling the target variable ($y$) was a game-changer. Without it, the model failed to converge (negative R²).



---

## 🛠️ Tech Stack
* **Language**: Python
* **Libraries**: `scikit-learn`, `pandas`, `numpy`, `matplotlib`

## 🏁 How to Run
1. Clone the repo: `git clone https://github.com/your-username/house-price-prediction.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook/script to see the results.

---
*Created with Zahra Ardalan.*
