# Estimation of Obesity Levels Based On Eating Habits and Physical Condition

## Project Overview
This project analyzes a dataset related to obesity levels based on individuals' eating habits and physical conditions. Using machine learning and data modeling techniques, the project aims to classify obesity levels by examining lifestyle factors such as food consumption, physical activity, water intake, and family history of overweight.

The analysis includes data preprocessing, exploratory visualization, and the implementation of classification models to estimate obesity categories.

---

## Dataset Source
The dataset used in this project comes from the **UCI Machine Learning Repository** and was accessed using the `ucimlrepo` Python package.

Dataset:  
**Estimation of Obesity Levels Based On Eating Habits and Physical Condition**

The dataset contains demographic, lifestyle, and health-related attributes used to classify individuals into different obesity levels.

---

## Features in the Dataset
The dataset includes variables such as:

- Gender  
- Age  
- Height  
- Weight  
- Family history with overweight  
- Frequency of high-calorie food consumption  
- Vegetable consumption frequency  
- Number of main meals  
- Water consumption  
- Physical activity frequency  
- Time spent using technology devices  
- Smoking habits  
- Alcohol consumption  
- Transportation type  

Target Variable:

**NObeyesdad** – Obesity level classification.

---

## Methodology

### 1. Data Loading
The dataset was imported directly from the UCI repository using the `ucimlrepo` library and converted into Pandas DataFrames for analysis.

### 2. Data Preprocessing
Features were organized into different categories:

**Binary features**
- Gender
- Family history with overweight
- High calorie food consumption
- Smoking
- Calorie consumption monitoring

**Numeric features**
- Age
- Height
- Weight
- Vegetable consumption
- Number of meals
- Water consumption
- Physical activity frequency
- Technology usage time

**Categorical features**
- Eating between meals
- Alcohol consumption
- Transportation type

Categorical variables were encoded and numerical features were scaled using **StandardScaler**.

---

### 3. Exploratory Data Analysis
Initial exploration included visualization of obesity level distributions using bar charts to observe the frequency of each obesity category within the dataset.

---

### 4. Model Development

#### Logistic Regression Model
A **Logistic Regression model** was implemented using a Scikit-learn **Pipeline** with StandardScaler.

Hyperparameter tuning was performed using **GridSearchCV**, testing different values for:

- Regularization strength (C)
- Penalty type (L1, L2)
- Solver algorithms

The best model was selected based on cross-validation performance.

#### Decision Tree Classifier
A **Decision Tree model** was also trained to classify obesity levels.

Key parameters used:
- Criterion: Gini
- Maximum depth
- Minimum samples per leaf

Grid search was used to determine the optimal tree depth.

---

### 5. Model Evaluation
The models were evaluated using:

- **Train/Test Split (80% training, 20% testing)**
- **Classification Report**
- Precision
- Recall
- F1-score
- Accuracy

These metrics help measure how well the models predict obesity categories.

---

## Results
The models demonstrated the ability to classify obesity levels using lifestyle and health-related variables. Logistic Regression provided interpretable coefficients showing how different features influence obesity classification, while the Decision Tree model offered a visual representation of the decision rules used for classification.

Feature coefficient visualizations were also generated to analyze the impact of different variables on each obesity class.

---

## Technologies Used
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- UCI ML Repository API (`ucimlrepo`)

---
