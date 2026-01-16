# Crop Water Requirement Prediction Using Linear Regression (Machine Learning)

This project builds a **regression** model to predict the **water requirement for crops** based on weather conditions like **temperature, humidity, and rainfall**. It follows the standard ML workflow:

**Problem Statement → Selection of Data → Collection of Data → EDA → Train/Test Split → Model Selection → Evaluation Metric**

---

## Problem Statement
Farmers need the right amount of water for crops depending on climate conditions.  
The goal of this project is to predict the **water required (mm)** using weather features.

**Input Features:**
- `Temperature_C`
- `Humidity_%`
- `Rainfall_mm`

**Output:**
- Predicted `Water_Required_mm`

---

## Selection of Data
**Dataset Type Used:** Structured tabular dataset (numeric features)

Why this dataset is suitable:
- Clear regression target (`Water_Required_mm`)
- Weather inputs are numeric and practical for prediction
- Good beginner project to understand regression workflow

---

## Collection of Data
In this project, the dataset is created inside the code as a sample dictionary and converted into a DataFrame using `pandas`.  
(The same workflow works with real agriculture/weather datasets loaded using `pd.read_csv()`.)

---

## EDA (Exploratory Data Analysis)
EDA is kept simple to confirm the dataset before training:
- Preview the dataset (`df.head()`)
- Confirm feature columns and target column
- Understand value ranges for temperature, humidity, rainfall, and water requirement

---

## Dividing Training and Testing
The dataset is split using `train_test_split`:
- Training set: model learns relationships
- Testing set: model is evaluated on unseen data

---

## Model Selection
**Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)

Why Linear Regression:
- Simple baseline model for regression
- Easy to train and interpret for beginners
- Works well when relationships are roughly linear

---

## Evaluation Metric (Used in this Project)
This project uses **R² Score** (`r2_score`) to evaluate model performance.

Simple meaning:
- R² shows how well the model fits the test data
- Higher R² means predictions are closer to actual values

Used in code:
- `r2_score(y_test, y_pred)`

---

## Main Libraries Used (and why)

1. `pandas`  
   - Creates and manages the dataset as a DataFrame.

2. `numpy`  
   - Supports numerical operations and array handling.

3. `sklearn.model_selection.train_test_split`  
   - Splits the dataset into training and testing sets.

4. `sklearn.linear_model.LinearRegression`  
   - Trains the regression model.

5. `sklearn.metrics.r2_score`  
   - Evaluates model performance using R² score.

---

## Output
- Printed **R² Score** for model performance
- Predicted water requirement for a new weather input (example: `[33, 65, 50]`)

---

## Developer
Grishma C.D
