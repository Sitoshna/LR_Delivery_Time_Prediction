
# 📦 Delivery Time Estimation Using Linear Regression

This project aims to analyze food delivery data and predict delivery time (in minutes) using **Linear Regression**. It involves data preprocessing, exploratory data analysis (EDA), feature selection using **RFE**, model building, evaluation, and residual diagnostics.

---

## 📁 Project Structure

```
.
├── LR_Delivery_Time_Estimation_Starter.ipynb  # Main notebook for analysis and modeling
├── porter_data_1.csv                          # Input dataset (assumed location)
├── model.pkl (optional)                       # Trained model (if exported)
└── README.md                                  # Project documentation
```

---

## 🔍 Problem Statement

Predict the **delivery time** of an order based on several factors including:
- Number of items
- Day and hour of order
- Other operational/categorical data

---

## 🔧 Steps Performed

### ✅ 1. Data Preprocessing
- Converted date columns to datetime format
- Extracted `order_hour` and `order_day`
- Converted object columns to categorical
- Created target variable: `time_taken_mins`
- Dropped unnecessary columns

### ✅ 2. Exploratory Data Analysis (EDA)
- Plotted distributions of numerical and categorical features
- Analyzed outliers using boxplots
- Visualized relationships using scatter plots and correlation heatmaps

### ✅ 3. Outlier Handling
- Used IQR method to cap or remove outliers

### ✅ 4. Feature Selection
- Applied **Recursive Feature Elimination (RFE)** with Linear Regression
- Compared performance across different feature counts
- Selected top-performing feature subset

### ✅ 5. Model Building
- Trained linear regression models with and without feature scaling
- Compared scaled vs unscaled performance

### ✅ 6. Evaluation
- Used the following metrics:
  - **R² (Coefficient of Determination)**
  - **MAE (Mean Absolute Error)**
  - **RMSE (Root Mean Squared Error)**

### ✅ 7. Residual Analysis
- Residual vs predicted plot
- Histogram and KDE of residuals
- Q-Q plot to check normality

---

## 🧠 Key Insights

- Features like `total_items`, `order_hour`, and `order_day` significantly impact delivery time.
- RFE helped reduce overfitting and improved model generalization.
- Residual plots confirmed model assumptions reasonably hold.

---

## 📊 Requirements

Install required Python libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels
```

---

## 🧪 Run the Notebook

You can run the notebook using:

```bash
jupyter notebook LR_Delivery_Time_Estimation_Starter.ipynb
```


