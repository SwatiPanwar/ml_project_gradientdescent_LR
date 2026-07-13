# ml_project_gradientdescent_LR
This project implements Linear Regression from scratch using Gradient Descent to understand how ML algorithms learn weights internally.

# 📊 Student Performance Prediction using Linear Regression & Gradient Descent

## 🚀 Project Overview

This project focuses on predicting a student's **Post Semester GPA** using academic behavior and AI usage patterns.

The main objective of this project is to understand the complete Machine Learning workflow:

**Data Understanding → Data Preparation → Feature Scaling → Model Training → Gradient Descent → Prediction → Evaluation**

This project implements Linear Regression from scratch using **Gradient Descent** to understand how ML algorithms learn weights internally.

---

# 🎯 Problem Statement

Can we predict a student's future GPA based on:

* Previous academic performance
* Traditional study habits
* Generative AI usage patterns

### Target Variable:

```
Post_Semester_GPA
```

### Features Used:

```
Pre_Semester_GPA
Traditional_Study_Hours
Weekly_GenAI_Hours
```

---

# 🧠 Machine Learning Concept Used

## Linear Regression

Linear Regression tries to learn the relationship:

[
y = w_1x_1+w_2x_2+w_3x_3+b
]

Where:

* X = Input Features
* y = Target Output
* w = Weights learned by the model
* b = Bias

The model learns the best values of weights and bias to minimize prediction error.

---

# 🔥 Gradient Descent Implementation

Instead of directly using sklearn's Linear Regression, this project implements Gradient Descent manually to understand the internal working of ML models.

## Gradient Descent Flow:

```
Initialize Weights
        |
        ↓
Make Prediction
        |
        ↓
Calculate Error
        |
        ↓
Calculate Gradient
        |
        ↓
Update Weights
        |
        ↓
Repeat Until Loss Reduces
```

---

# 🏗️ Complete ML Workflow

## Super Trick:

```
D → E → F → S → M → L → P → E
```

Remember:

**"Data Explore Features Scale Model Learn Predict Evaluate"**

---

# 1️⃣ Data Loading

Dataset is loaded using Pandas.

```python
pd.read_csv()
```

Purpose:

* Convert CSV data into DataFrame
* Start data analysis

---

# 2️⃣ Data Understanding (EDA)

Before building a model, understand the data.

### Check Dataset Information:

```python
df.info()
```

Provides:

* Column names
* Data types
* Missing values

### Statistical Summary:

```python
df.describe()
```

Provides:

* Mean
* Minimum
* Maximum
* Standard deviation

---

# 3️⃣ Feature Selection

Machine Learning needs:

## Input (X)

Features used for prediction:

```
Pre_Semester_GPA
Traditional_Study_Hours
Weekly_GenAI_Hours
```

## Output (y)

Target:

```
Post_Semester_GPA
```

Remember:

```
X = Explanation variables

y = Your answer
```

---

# 4️⃣ Data Visualization

Visualization helps understand relationships.

### Scatter Plot:

Examples:

```
Pre GPA vs Post GPA

Study Hours vs Post GPA

AI Hours vs Post GPA
```

Purpose:

* Find patterns
* Understand relationships
* Detect trends

---

# 5️⃣ Correlation Analysis

Correlation tells how strongly features are related.

Range:

```
+1  → Strong Positive Relationship

 0  → No Relationship

-1  → Strong Negative Relationship
```

Example:

```
Pre GPA  → High correlation with Post GPA
```

---

# 6️⃣ Train-Test Split

Dataset is divided into:

```
Training Data  → Model Learning

Testing Data   → Model Evaluation
```

Flow:

```
Complete Dataset

       |
       ↓

80% Training

20% Testing
```

---

# 7️⃣ Feature Scaling

## Why Scaling?

Different features have different ranges.

Example:

```
GPA = 3.5

Study Hours = 30
```

Gradient Descent may learn slowly if features are not scaled.

Solution:

```python
StandardScaler()
```

Scaling makes features comparable.

---

# 8️⃣ Model Architecture

## Class Creation

```python
class LinearRegressionGD:
```

Concept:

```
Class = Blueprint

Object = Actual Model
```

---

## Model Initialization

```python
__init__()
```

Purpose:

Store initial settings:

```
Learning Rate

Epochs
```

---

# 9️⃣ Model Training (fit function)

```python
model.fit(X_train,y_train)
```

Meaning:

"Model, learn from this data."

Inside fit():

## Step 1:

Find number of samples and features:

```
n_samples
n_features
```

---

## Step 2:

Initialize weights:

```
weights = [0,0,0]
```

Starting assumption:

Model knows nothing.

---

## Step 3:

Initialize bias:

```
bias = 0
```

---

## Step 4:

Gradient Descent Loop

Repeat for multiple epochs:

```
Prediction

↓

Error Calculation

↓

Gradient Calculation

↓

Weight Update
```

---

# 🔟 Prediction

Formula:

[
Prediction = XW+b
]

Implementation:

```
np.dot(X,weights)+bias
```

## np.dot()

Purpose:

Matrix multiplication.

Example:

```
Feature × Weight
```

---

# 1️⃣1️⃣ Weight Update

Gradient Descent Formula:

[
New Weight = Old Weight - Learning Rate × Gradient
]

Meaning:

The model improves itself by reducing mistakes.

---

# 1️⃣2️⃣ Model Evaluation

Performance is checked using:

## MSE

Measures average squared error.

## RMSE

Shows prediction error in original units.

Lower error = Better model.

---

# 📈 Result Visualization

## Actual vs Predicted Graph

Purpose:

Compare:

```
Actual GPA

vs

Predicted GPA
```

A good model has points close to the ideal line.

---

# 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

# 📂 Project Structure

```
Student-Performance-Prediction/

│
├── dataset/
│   └── student_data.csv
│
├── LinearRegression_GD.ipynb
│
├── README.md
│
└── requirements.txt
```

---

# 💡 Key Learnings

Through this project, I understood:

✅ Complete ML workflow
✅ Feature selection
✅ Data visualization
✅ Feature scaling
✅ Linear Regression mathematics
✅ Gradient Descent optimization
✅ Weight and bias learning
✅ Model evaluation

---

# 🧠 Final ML Memory Trick

Every Machine Learning Project follows:

```
Understand Data
        ↓
Prepare Data
        ↓
Train Model
        ↓
Learn Patterns
        ↓
Predict Output
        ↓
Evaluate Performance
        ↓
Improve Model
```

---

## Future Improvements

* Add more features
* Compare with sklearn Linear Regression
* Try Random Forest Regressor
* Perform Hyperparameter Tuning
* Deploy as an ML application

---

# 👩‍💻 Author

Swati Panwar

Machine Learning Journey 🚀
