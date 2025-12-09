#  House Price Predictor (Scikit-learn Linear Regression)

## Project Goal
The goal of this project is to develop a simple **Supervised Machine Learning Regression model** to predict the selling price of a house based on its features using the popular `scikit-learn` library.

The specific task is to predict the **price** column using all other available features in the provided dataset.

---

##  Dataset & Features

* **Data Source:** `Housing.csv`
* **Target Variable ($\mathbf{y}$):** **price** (Continuous integer)
* **Features ($\mathbf{X}$):** All other columns, including numerical features like **area**, **bedrooms**, **bathrooms**, and various **categorical variables** (e.g., **mainroad**, **furnishingstatus**).

---

##  Methodology (Machine Learning Workflow)

The project followed a standard machine learning pipeline:

### 1. Data Preprocessing

* **One-Hot Encoding:** All categorical (string/object) features (like `mainroad`, `guestroom`, `furnishingstatus`) were converted into numerical binary columns using `pandas.get_dummies`. This step is crucial for the Linear Regression model. 
* **Feature/Target Separation:** The dataset was split into the feature matrix (**X**) and the target vector (**y**).

### 2. Model Training

* **Train-Test Split:** The data was divided into an **80% training set** and a **20% testing set** to ensure the model's performance is evaluated on unseen data.
* **Model Selection:** A simple **Linear Regression** model was chosen for the initial baseline prediction.
* **Fitting:** The model was trained (`model.fit`) using only the training data (**X**_train, **y**_train).

### 3. Evaluation

The trained model was used to predict prices on the test set. Performance was measured using common regression metrics.

---

## Results

The model's performance on the unseen test data is summarized below:

| Metric | Value | Interpretation |
| :---|:---|:--- |
| **R-squared ($R^2$) Score** | **0.6529** | The model explains about **65.29%** of the variability in house prices. |
| **Mean Absolute Error (MAE)** | **970,043.40** | On average, the model's price prediction is off by approximately **$\text{\textdollar}970,000$**. |
| **Root Mean Squared Error (RMSE)** | **1,324,506.96** | The square root of the average squared difference between predicted and actual values. |
