# 📈 Sales Prediction Using Machine Learning

This project predicts **product sales** based on advertising budgets using **Linear Regression**. The dataset includes advertising costs across TV, Radio, and Newspaper. The model helps businesses understand how advertising spend impacts sales.

---

## 📊 Dataset Overview

- **File**: `advertising.csv`
- **Columns**:
  - `TV`: Budget for TV advertisements
  - `Radio`: Budget for Radio advertisements
  - `Newspaper`: Budget for Newspaper advertisements
  - `Sales`: Number of units sold (target)

---

## 🔧 Technologies Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 📌 Project Workflow

### 1. Data Cleaning & Preprocessing
- Removed unnecessary features (`Newspaper`)
- Handled outliers using IQR method
- Applied `StandardScaler` to normalize data

### 2. Exploratory Data Analysis (EDA)
- Correlation heatmaps
- Pairplots and distribution plots

### 3. Feature Engineering
- Added interaction feature: `TV * Radio` (optional)
- Selected the most impactful features

### 4. Model Building
- Used **Linear Regression**
- Train-test split: 80% training / 20% testing

### 5. Evaluation Metrics
| Metric | Value |
|--------|-------|
| R² Score | **0.9079** |
| MAE      | 1.2670 |
| MSE      | 2.8466 |
| RMSE     | 1.6872 |

### 6. Prediction
```python
# Input sample: TV = 150, Radio = 25
new_data = np.array([[150, 25]])
new_data_scaled = scaler.transform(new_data)
predicted_sales = model.predict(new_data_scaled)
print(f"Predicted Sales: {predicted_sales[0]:.2f}")




---
