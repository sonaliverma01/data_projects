# Revenue Prediction Using Machine Learning

## Project Overview

This project focuses on predicting **product revenue** using historical transaction data, product class information, and static item attributes. Multiple machine learning models are trained and evaluated to identify the best-performing algorithm for accurate revenue prediction.

### Models Implemented:
- Linear Regression
- Decision Tree
- Random Forest
- Multi-Layer Perceptron (MLP - Neural Network)
- K-Nearest Neighbors (KNN)

---

## Dataset Description

The project uses three primary datasets:

- **`train.csv`**: Contains transaction-level data including `price`, `revenue`, and `competitorPrice`.
- **`class.csv`**: Contains product availability and competitor prices during the classification period.
- **`items.csv`**: Contains static product information such as `salesIndex`, `retail price`, `manufacturer`, etc.

---

## Data Cleaning & Preprocessing

1. **Missing Values & Duplicates**
   - Checked and removed missing values and duplicated rows.
   - Imputed missing `competitorPrice` values using the median.

2. **Outlier Removal**
   - Used the **IQR method** to remove outliers in continuous numerical columns (`price`, `revenue`, `competitorPrice`, etc.).

3. **Merging Datasets**
   - Merged all datasets using `pid` (Product ID).
   - Dropped irrelevant and high-cardinality columns (`lineID`, `manufacturer`, `category`, etc.).

4. **Feature Transformation**
   - One-hot encoded categorical columns like `campaignIndex` and `unit`.
   - Removed highly correlated features (`competitorPrice`, `rrp`) if correlation > 0.9.
   - Filled missing numerical values with the median.

5. **Sampling**
   - Randomly selected 1000 rows to speed up model training and evaluation.

---

## Feature Engineering

- Used **only numerical features** and **one-hot encoded categorical columns** for model training.
- The target variable for prediction is `revenue`.

---

## Models Trained & Evaluation Metrics

Each model is evaluated using the following metrics:

- **MSE**: Mean Squared Error  
- **RMSE**: Root Mean Squared Error  
- **MAE**: Mean Absolute Error  
- **R² Score**: Coefficient of Determination  
- **MAPE**: Mean Absolute Percentage Error  

---

## Author

**Sonal Verma**  
Passionate about data science and machine learning.

---

> 📌 Feel free to explore, clone, and modify the project. Contributions and feedback are welcome!
