# Dehli Indian Housing Part 2: Predicting Price with Size Using Linear Regression

## Project Overview
This project focuses on building a **Linear Regression model** to predict rental prices based on house size using the Delhi Indian Housing dataset. It is a continuation of the exploratory data analysis conducted in Part 1 and aims to deepen understanding of regression modeling, evaluation metrics, and the relationship between house size and rental price.

## Contact Details
- Email: dumisanimukuchura@gmail.com
- LinkedIn: https://www.linkedin.com/in/dumisani-maxwell-mukuchura-4859b7170/

## Objectives
- Prepare data by cleaning and exploring key columns.
- Build a Linear Regression model to predict rental prices (`price_approx_usd`) from house sizes (`house_size_in_sqft`).
- Evaluate the model's performance using baseline comparisons and metrics like Mean Absolute Error (MAE).
- Communicate the model as a mathematical equation and visualize its predictions.

---

## Dataset Description
The dataset contains housing rental details in Delhi, India. Below are the key columns used:

| Column              | Description                                |
|---------------------|--------------------------------------------|
| `house_size_in_sqft`| House size in square feet                 |
| `price_approx_usd`  | Rental price in US Dollars                |

The data was further cleaned and filtered during preprocessing to remove outliers and ensure reliable analysis.

---

## Key Steps

### **1. Data Preparation**
- Imported and cleaned the dataset.
- Removed outliers using the Interquartile Range (IQR) for `house_size_in_sqft`.
- Created a feature matrix (`X_Train`) and a target vector (`y_train`) for training.

### **2. Data Exploration**
- Analyzed the relationship between house size and price using visualizations:\n
  - Scatter plot showing the positive correlation.
  - Histogram and boxplot for the distribution of house sizes.
- Verified statistical summaries to identify trends and anomalies.

### **3. Data Splitting**
- Split the dataset into:\n
  - **Training set**: Used to train the model.
  - **Test set**: Used to evaluate model performance on unseen data.

### **4. Model Building**
#### **Baseline**
- Established a baseline by predicting the mean price for all houses.
- Calculated the **Mean Absolute Error (MAE)** for the baseline:\n
  - Baseline MAE: `$1651.68`

#### **Linear Regression**
- Trained a Linear Regression model using `sklearn`.
- Evaluated the model on:\n
  - **Training data**: MAE = `$1544.43`
  - **Test data**: MAE = `$1191.67`

### **5. Model Communication**
- Represented the model as a mathematical equation:\n

housing_price_in_usd = 0.72 * house_size_in_sqft + 1389.38

- Visualized the linear model against the data points in a scatter plot.

### **6. Conclusion**
The Linear Regression model significantly outperformed the baseline, reducing the prediction error. This demonstrates the importance of incorporating meaningful features like house size into predictive models.

---

## Tools and Libraries Used
- **Python**
- **Pandas** and **NumPy**: Data manipulation and numerical operations.
- **Matplotlib**: Data visualization.
- **scikit-learn**: Machine learning algorithms and evaluation metrics.

---

## How to Run the Project
1. **Set Up the Environment**:
 - Install required libraries: `pandas`, `numpy`, `matplotlib`, `scikit-learn`.
 - Ensure the dataset (`Dehli-Indian-Housing-Clean-Data.csv`) is in the `data` directory.
2. **Run the Jupyter Notebook**:
 - Execute cells sequentially to preprocess data, build the model, and evaluate results.
3. **Analyze Results**:
 - Review metrics and visualizations to understand model performance.