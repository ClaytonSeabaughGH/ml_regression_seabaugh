# 🧠 BMI Prediction Using Linear Regression

This project explores how well we can predict an individual’s Body Mass Index (BMI) using basic demographic and lifestyle features like age, sex, and smoking status. We applied various regression models and preprocessing pipelines to identify relationships and improve model performance.

---

## 🎯 Project Goals

- Explore the distribution and relationships between features like age, sex, and smoker status.
- Predict BMI using regression models.
- Evaluate and compare model performance.
- Understand challenges and suggest future improvements.

---

## 📊 Dataset Overview

- **Source**: Insurance dataset with 1,338 samples and the following features:
  - `age` (numerical)
  - `sex` (categorical)
  - `bmi` (numerical) **→ Target**
  - `children` (numerical)
  - `smoker` (categorical)
  - `region` (categorical)
  - `charges` (numerical)

- **Target Variable**: `bmi`

---

## 🔎 Exploratory Data Analysis (EDA)

- **No missing values** in the dataset.
- Used histograms, boxplots, and countplots to visualize:
  - Age distribution
  - BMI spread and outliers
  - Categorical distributions for smoker and sex
- No strong visual correlations were identified between predictors and BMI.

---

## ⚙️ Modeling Workflow

### ✅ Chosen Features
- **Input Features**: `age`, `sex`, `smoker`
- **Target**: `bmi`

### 🔧 Preprocessing
- Handled categorical variables via one-hot encoding
- Applied scaling using `StandardScaler`
- Built pipelines for modular and clean preprocessing

---

## 🤖 Models Used

### 📌 Baseline Linear Regression
- Applied with scaling and encoding
- **R²**: 0.0025
- **MAE**: 0.8140
- **RMSE**: 1.0314

### 📌 Polynomial Regression (Degree=3)
- Included interaction terms and nonlinear relationships
- **R²**: -0.0448 (overfitting)
- **MAE**: 0.8365
- **RMSE**: 1.0556

---

## 📈 Results & Insights

| Model                       | R²     | MAE    | RMSE   |
|----------------------------|--------|--------|--------|
| Linear Regression (scaled) | 0.0025 | 0.8140 | 1.0314 |
| Polynomial Regression (d=3)| -0.0448| 0.8365 | 1.0556 |

- Linear model performed slightly better.
- Polynomial model overfit due to the lack of strong underlying relationships.
- Low R² indicates weak predictive power using only the selected features.

---

## 🧠 Final Reflection

### ✅ What Went Well
- Pipeline design for clean preprocessing and modeling
- Effective evaluation of multiple models
- Insightful EDA to guide modeling decisions

### ⚠️ Challenges
- Features chosen had **low predictive value** for BMI
- Polynomial regression introduced **overfitting**
- Small feature set limited performance

### 🚀 Future Improvements
- Include more relevant health features (diet, exercise, medical history)
- Try regularization (Ridge, Lasso)
- Explore tree-based models like Random Forest or XGBoost
- Perform feature selection or PCA

---

## 🛠️ Technologies Used

- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- Jupyter Notebook

---

## 📌 Author

**Clayton Seabaugh**  
[GitHub](https://github.com/ClaytonSeabaughGH)
