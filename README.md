# Medical Cost Prediction Using Linear Regression

This project explores the factors associated with individual medical insurance charges and builds a **Linear Regression** model to predict medical costs.

The project demonstrates a complete machine learning workflow, from exploratory data analysis and preprocessing to model training, evaluation, and interpretation.

## Project Overview

The main objective is to investigate how demographic and lifestyle-related features are associated with medical insurance charges and to build a model that can predict the expected medical cost for an individual.

The project focuses on understanding both the **machine learning concepts** and the practical implementation of a regression workflow using Python and scikit-learn.

## Dataset

The dataset contains **1,338 observations** and **7 variables** describing individuals and their medical insurance charges.

### Features

| Feature    | Description                          |
| ---------- | ------------------------------------ |
| `age`      | Age of the individual                |
| `sex`      | Biological sex                       |
| `bmi`      | Body Mass Index                      |
| `children` | Number of children/dependents        |
| `smoker`   | Whether the individual is a smoker   |
| `region`   | Residential region                   |
| `charges`  | Individual medical insurance charges |

### Target

The target variable is:

`charges`

Because `charges` is a continuous numerical variable, this is a **regression problem**.

## Machine Learning Workflow

The notebook follows these main steps:

1. Load and inspect the dataset
2. Perform exploratory data analysis
3. Analyze relationships between features and medical charges
4. Visualize numerical and categorical variables
5. Understand simple linear regression
6. Implement a simple linear model manually
7. Calculate RMSE manually
8. Build Linear Regression models using scikit-learn
9. Encode categorical variables
10. Standardize numerical features
11. Split the data into training and testing sets
12. Train the final Linear Regression model
13. Evaluate the model using RMSE and R²
14. Compare actual and predicted charges
15. Interpret model coefficients
16. Discuss limitations and possible improvements

## Exploratory Data Analysis

The analysis investigates several relationships in the dataset, including:

* Age and medical charges
* BMI and medical charges
* Smoking status and medical charges
* Sex and medical charges
* Region and medical charges
* Number of children and medical charges
* Correlations between numerical variables

One of the most noticeable patterns in the dataset is the substantial difference in medical charges between smokers and non-smokers.

The analysis also suggests a positive relationship between age and medical charges.

## Data Preprocessing

The dataset contains both numerical and categorical variables.

### Binary Encoding

The following variables are converted into numerical representations:

* `smoker`: `no = 0`, `yes = 1`
* `sex`: `male = 0`, `female = 1`

### One-Hot Encoding

The `region` variable is converted using one-hot encoding.

This avoids assigning an artificial numerical ordering to the different regions.

### Feature Scaling

The numerical features:

* `age`
* `bmi`
* `children`

are standardized using `StandardScaler`.

## Models

Several models are explored throughout the notebook.

### Simple Linear Regression

A model using `age` as the only predictor is built to demonstrate the basic idea of:

`ŷ = wx + b`

The notebook also includes a manually defined prediction function and RMSE calculation to build intuition about how linear regression works.

### Multiple Linear Regression

Additional numerical features are then introduced:

* Age
* BMI
* Number of children

Finally, categorical variables are encoded and included in the final model.

### Final Model

The final Linear Regression model uses:

* Age
* BMI
* Number of children
* Sex
* Smoking status
* Region

## Model Evaluation

The final model is evaluated using a separate test set.

### Metrics

**Root Mean Squared Error (RMSE)**

RMSE measures the typical magnitude of prediction errors in the same units as medical charges.

Lower RMSE indicates better predictive performance.

**R² Score**

R² measures the proportion of variation in medical charges explained by the model.

A higher R² generally indicates that the model explains more of the variation in the target.

Both training and testing metrics are reported to examine how well the model generalizes to unseen data.

## Key Findings

The analysis indicates that:

* Age has a positive relationship with medical charges.
* BMI provides additional predictive information.
* Smoking status is a particularly important predictor of medical charges.
* Categorical variables can be incorporated into linear regression through encoding.
* A train/test split provides a more realistic evaluation of model performance than evaluating only on training data.
* Linear regression provides a useful baseline for understanding the relationships in this dataset.

## Limitations

This project uses a relatively simple Linear Regression model.

Medical charges may contain nonlinear relationships and interactions between variables that a basic linear model cannot fully capture.

Additionally, the dataset describes statistical relationships and should not be used to interpret the model's coefficients as proof of causal relationships.

## Future Improvements

Possible improvements include:

* Polynomial features
* Interaction terms
* Ridge Regression
* Lasso Regression
* Decision Trees
* Random Forests
* Gradient Boosting
* Cross-validation
* Hyperparameter tuning
* Comparison of multiple regression models

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
Medical_Charges_LinearRegression/
│
├── Medical_Charges_LinearRegression.ipynb
├── medical-charges.csv
└── README.md
```

## How to Run

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd Medical_Charges_LinearRegression
```

### 2. Install the required libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Open the notebook

```bash
jupyter notebook Medical_Charges_LinearRegression.ipynb
```

Run the notebook cells from top to bottom.

## Author

**Muhammadsodiq Doniyorbekov**
