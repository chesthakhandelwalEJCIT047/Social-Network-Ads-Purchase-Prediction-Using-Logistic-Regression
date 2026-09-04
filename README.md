# 📊 Social Network Ads – Purchase Prediction

A beginner-friendly **Machine Learning classification project** that uses **Logistic Regression** to predict whether a user will purchase a product based on their age.

---

## 📌 Project Overview

This project demonstrates a simple implementation of **Logistic Regression** using Python and Scikit-learn.

The **Social Network Ads dataset** is used to analyze the relationship between a user's **Age** and their purchasing decision. After preprocessing the dataset, Logistic Regression is trained to classify whether a user is likely to purchase a product.

The project is implemented in a **Jupyter Notebook** and is suitable for understanding the basic workflow of a Machine Learning classification problem.

---

## 🎯 Objective

The primary goal of this project is to build a Logistic Regression model that can predict:

* `0` → User does not purchase the product
* `1` → User purchases the product

The model uses **Age** as the input feature.

---

## 🔄 Machine Learning Workflow

The project follows these major steps:

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Feature Selection
   ↓
Data Visualization
   ↓
Train-Test Split
   ↓
Logistic Regression
   ↓
Model Evaluation
   ↓
Prediction
```

---

## 🗂️ Dataset

The project uses the **Social Network Ads dataset**.

The original dataset contains information such as:

* User ID
* Gender
* Age
* Estimated Salary
* Purchased

For this implementation, unnecessary columns are removed and the model focuses on:

### Feature

`Age`

### Target

`Purchased`

---

## 🧹 Data Preprocessing

The following preprocessing operations are performed:

### 1. Remove User ID

The `User ID` column is removed because it does not provide useful information for predicting purchasing behavior.

```python
data.drop(columns=["User ID"], inplace=True)
```

### 2. Remove Gender

The `Gender` column is also removed from the dataset.

```python
data.drop(columns=["Gender"], inplace=True)
```

### 3. Remove Salary

The salary-related column is removed so that the final model focuses on age.

---

## 📈 Data Visualization

A scatter plot is created to visualize the relationship between **Age** and **Purchased**.

```python
sns.scatterplot(x="Age", y="Purchased", data=data)
plt.show()
```

This visualization helps in understanding how purchasing behavior changes with age.

---

## 🤖 Machine Learning Model

### Logistic Regression

The project uses **Logistic Regression** from Scikit-learn.

```python
from sklearn.linear_model import LogisticRegression

lr = LogisticRegression()
lr.fit(x_train, y_train)
```

Logistic Regression is suitable for this problem because the target variable is binary:

```text
0 → Not Purchased
1 → Purchased
```

---

## ✂️ Train-Test Split

The dataset is divided into training and testing sets using an **80:20 split**.

```python
from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x, y,
    test_size=0.2,
    random_state=42
)
```

* **80%** → Training data
* **20%** → Testing data

`random_state=42` is used to make the split reproducible.

---

## 📊 Model Evaluation

The trained model is evaluated using the test dataset:

```python
lr.score(x_test, y_test) * 100
```

The resulting value represents the model's **classification accuracy on the test data**.

---

## 🔮 Prediction

After training the model, it can be used to make predictions for new users.

For example:

```python
lr.predict([[50]])
```

This predicts whether a **50-year-old user** is likely to purchase the product according to the trained model.

---

## 🛠️ Technologies & Libraries

The project is built using:

* 🐍 **Python**
* 📓 **Jupyter Notebook**
* 🧮 **NumPy**
* 🐼 **Pandas**
* 📊 **Matplotlib**
* 📈 **Seaborn**
* 🤖 **Scikit-learn**

---

## 📁 Project Structure

```text
Social-Network-Ads-Logistic-Regression/
│
├── Social_Network_Ads.csv
├── Untitled8.ipynb
└── README.md
```

---

## 💡 Key Learning Outcomes

Through this project, I learned how to:

* Load and explore a dataset using Pandas
* Perform basic data preprocessing
* Select relevant features
* Visualize data using Seaborn
* Split data into training and testing sets
* Implement Logistic Regression
* Evaluate a classification model
* Make predictions using a trained Machine Learning model

---

## 🚀 Future Improvements

This project can be further improved by:

* Using additional relevant features such as salary
* Comparing Logistic Regression with other classification algorithms
* Adding a confusion matrix
* Calculating precision, recall, and F1-score
* Plotting the Logistic Regression decision boundary
* Performing feature scaling
* Hyperparameter tuning
* Comparing multiple models to determine the best-performing algorithm

---

## 📌 Conclusion

This project provides a simple and practical introduction to **binary classification using Logistic Regression**.

By using the user's age as a feature, the model attempts to predict their purchasing decision. Although this is a basic implementation, it demonstrates the fundamental Machine Learning workflow from **data preprocessing and visualization to model training, evaluation, and prediction**.

---

## 👩‍💻 Author

**Cheshta Khandelwal**

If you found this project useful, feel free to ⭐ the repository!
