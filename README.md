# ⚽ Football Player Value Prediction

This project focuses on predicting the market value of football players based on their performance metrics, physical attributes, and contract details. By analyzing a comprehensive dataset of professional players, the goal is to develop a predictive model that can estimate player values — aiding clubs and scouts in identifying undervalued talent and making informed transfer decisions.

---

## 📊 Dataset Overview

The dataset includes **3,120 football players** with a wide range of features, including:

- **Player Attributes:** Overall rating, potential, growth, attacking and skill metrics  
- **Physical Characteristics:** Height, weight, age  
- **Contract Details:** Contract start and end years, team affiliation  
- **Player Position:** Detailed and grouped positions (Goalkeeper, Defender, Midfielder, Forward)  
- **Market Values:** Player value, wage, release clause (monetary values converted and standardized)  

> ✅ The dataset was clean with no missing values and required preprocessing to standardize columns, extract and convert contract dates, and clean monetary values.

---

## 🧹 Data Preprocessing

- ✅ Removed empty columns and standardized column names  
- 🔍 Extracted player names and positions, including the number of playable positions  
- 🔄 Converted contract dates to numeric format and cleaned erroneous entries  
- 💰 Converted monetary values from strings with '€', 'K', and 'M' to numeric values  
- ⚖️ Created age brackets and mapped detailed positions to core position groups  

---

## 🔍 Exploratory Data Analysis

### Key Insights:

- 📈 Strong correlations between player value and attributes like **overall rating**, **potential**, and **international reputation**  
- 📊 **Defenders'** height and reputation influence their market value  
- 🎯 **Midfielders'** overall rating and age brackets show clear trends in value distribution  
- 🔄 Visualizations highlighted differences in value across core positions and age groups  

---

## 🤖 Machine Learning Task: Regression for Player Value Prediction

The modeling focused on **midfielders**, using features such as:

- Overall rating  
- Age  
- Growth  
- Attacking and skill metrics  
- International reputation  

### Models Implemented:

- **Linear Regression:** Baseline model with moderate performance  
- **Random Forest Regressor:** Improved performance with hyperparameter tuning via `GridSearchCV`  

### 🔝 Best Model: Random Forest Regressor

| Metric | Score (RMSE) |
|--------|--------------|
| RMSE   | ~5,000,000   |

> 📌 Feature importance analysis revealed that **overall rating**, **potential**, and **growth** were among the most influential predictors.

---

## 💡 Insights & Recommendations

- 🔍 **Player overall rating and potential** are the most decisive factors in determining market value.  
- 🎯 Clubs can leverage such predictive models to identify **undervalued players**, optimizing transfer strategies and investments.  
- 📉 **Contract details and physical attributes** also contribute, but to a lesser extent compared to performance metrics.  

---

## 🚀 Future Work

- Extend modeling to **other positions** (e.g., goalkeepers, defenders, forwards)  
- Incorporate **temporal contract dynamics**  
- Explore **advanced models** like Gradient Boosting or Neural Networks for improved accuracy  
