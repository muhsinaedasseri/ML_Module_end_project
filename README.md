# ML_Module_end_project
# 🚗 Car Price Prediction Project

This project aims to build predictive models to estimate the **price of a car** based on various features. The insights will help a Chinese automobile company understand how car pricing works in the **U.S. market**, enabling smarter decisions in design, manufacturing, and marketing strategy.

---

## 📊 Dataset

- Source: Provided by an automobile consulting firm
- Rows: 205
- Target variable: `price`
- Features include: engine size, horsepower, fuel type, car dimensions, brand, etc.

---

## 🎯 Objectives

- Identify key factors influencing car price.
- Compare the performance of various regression models.
- Apply proper preprocessing (e.g., scaling, encoding).
- Interpret the results for actionable business insights.

---

## 🧪 Project Workflow

### 1. **Data Preprocessing**
- Removed unnecessary columns (e.g., `car_ID`)
- Extracted car brand from `CarName` and fixed typos (e.g., "vw" → "volkswagen")
- One-hot encoded categorical features
- Handled missing values and data type conversions

### 2. **Outlier Detection**
Outliers were checked using:
- 🧮 **Z-score** and **IQR method** (optional) for statistical detection  
Findings:
- Outliers exist in `price`, `horsepower`, and `engine-size`, but most are valid data points.
- Not removed, as they reflect real-world premium car prices.

### 3. **Feature Scaling**
- Applied **StandardScaler** to normalize features **only for SVR**, since it's distance-based.
- Tree-based models do not require scaling.

---

## 🤖 Models Used

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)

### ✅ Hyperparameter Tuning
- Performed GridSearchCV for SVR and Random Forest
- Improved model performance (e.g., SVR R² went from negative to **0.959** after tuning and scaling)

---

## 📈 Evaluation Metrics

Each model was evaluated using:

- **R² Score** – how well the model explains the variability
- **MSE** (Mean Squared Error)
- **MAE** (Mean Absolute Error)

### 🔥 Best Model: Random Forest Regressor
| Metric | Value |
|--------|-------|
| R²     | 0.958 |
| MAE    | 1288  |

---

## 🔍 Feature Importance

Top influential features based on Random Forest:
- `engine-size`
- `curb-weight`
- `horsepower`
- `highway-mpg`
- `carwidth`

These features strongly affect how a car is priced in the U.S. market.

---

## 💼 Business Insights

- The company can adjust **design specs (e.g., engine size)** to align with desired price targets.
- **Localizing premium features** may help them compete in higher price segments.
- The model offers a reliable tool to **simulate price scenarios** based on feature changes.

---

## 🛠 Tech Stack

- Python
- pandas, numpy
- seaborn, matplotlib
- scikit-learn

---

## 📂 Project Structure

