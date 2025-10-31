# Salary Prediction in Norway  

An end-to-end machine learning workflow for predicting developer salaries in Norway.  
This project was developed between June - October 2025.  

---

## 1. Project Overview  

This study investigates whether developer salaries in Norway can be predicted from survey data, or whether they are influenced by external and subjective factors that go beyond measurable variables.  

The project applies a complete machine learning pipeline — from raw data to model optimization — and evaluates the predictive capacity of different regression algorithms using real-world salary data collected from Norwegian developers (Kaggle, 2024).  

**Main objectives:**  
- Explore salary trends by gender, region, experience, and job field  
- Clean, encode, and scale survey data for model readiness  
- Train and evaluate multiple regression models  
- Optimize hyperparameters to improve predictive accuracy  
- Reflect on the interpretability and limitations of salary prediction  

---

## 2. Methodology  

**Workflow summary:**  
1. **Exploratory Data Analysis (EDA):** Salary distribution and variable correlations  
2. **Preprocessing:** Encoding categorical variables, scaling numeric features, removing duplicates  
3. **Model Development:** Linear Regression, Random Forest Regressor, Support Vector Regressor (SVR)  
4. **Model Optimization:** Hyperparameter tuning using RandomizedSearchCV  
5. **Evaluation Metrics:** Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R²  

**Tools and Libraries:**  
Python, pandas, numpy, matplotlib, scikit-learn  

---

## 3. Results  

| Model | MAE (NOK) | RMSE (NOK) | R² |
|:------|-----------:|------------:|:---:|
| Linear Regression | 157,744 | 237,759 | 0.40 |
| Random Forest (baseline) | 139,240 | 218,958 | 0.49 |
| Random Forest (tuned) | **134,745** | **212,175** | **0.52** |
| SVR (baseline) | 215,581 | 312,950 | -0.05 |
| SVR (tuned) | 178,245 | 278,522 | 0.17 |

**Interpretation:**  
The Random Forest Regressor (tuned) achieved the best performance, explaining approximately 52% of the variance in salaries.  
While the model captures major trends, high residual error indicates that salary levels are also shaped by non-quantifiable variables such as negotiation skills, company context, and interpersonal factors.  

---

## 4. Repository Structure  

| File | Description |
|------|--------------|
| `salary-prediction.ipynb` | Full Jupyter Notebook with code implementation and visualizations |
| `norway-2024-salaries.csv` | Dataset used for model training |
| `Report CARLOS TORRES.pdf` | Full academic report including EDA, preprocessing, models, tuning, and analysis |
| `README.md` | Documentation and project summary |

---

## 5. Key Takeaways  

- The project demonstrates an end-to-end data science pipeline from data cleaning to model evaluation.  
- Random Forest outperforms linear and kernel-based methods on structured salary data.  
- Despite optimization, predictive accuracy remains moderate, confirming that salary determination involves both measurable and unmeasurable factors.  
- The workflow and methodology can be easily adapted for similar regression-based prediction problems.  

---

## 6. Author  

**Carlos Torres González**  
Machine Learning Graduate – Noroff School of Technology and Digital Media  
Oslo, Norway  
[LinkedIn](https://linkedin.com/in/CarlosTorresML)

---

> “Data can approximate reality, but it can never fully capture the human complexity behind it.”  
> — Carlos Torres González
