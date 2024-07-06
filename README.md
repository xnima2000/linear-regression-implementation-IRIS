# 🌟 Linear Regression Implementation

Welcome to the Linear Regression Implementation repository! This project demonstrates a simple yet effective linear regression model using Python's NumPy and pandas libraries. The goal is to provide a clear example of splitting data, training a model, and evaluating its performance.

## 📘 Overview

Suppose we want to fit a linear model on the data that takes the features `f1`, `f2`, and `f4` and predicts the feature `f3` (or `t`). This linear model is defined as follows:

f3 = t = w0 + w1@f1 + w2@f2 + w3@f4

### 🛠️ Training Phase
To form this linear model, we need to estimate the parameters `w0`, `w1`, `w2`, and `w3` using the data.

The Iris dataset consists of three classes (categories). It is better to form a separate linear model for each class. For this purpose, out of 50 data points related to each class, we consider 40 primary data points as training data and 10 final data points as test data.

1. **Form the Training Data Matrix (X matrix)**:
   - We add a column with values of 1 as bias values.
   - The dimensions of the X matrix are 4x40.

2. **Form the Matrix (Vector) `t`**:
   - Using the feature `f3` from class 1.
   - The dimensions of the `t` matrix are 40x1.

To calculate the parameters `w = [w0, w1, w2, w3]^T`, according to the linear regression relations, we use the following formula:

w = (X^T @ X)^-1 @ X^T @ t

By performing these calculations, `w` parameters are obtained.

### 🧪 Test Phase
To test the model, we put the features `f1`, `f2`, and `f4` of the test data in the linear relationship and calculate `t`. The closer the `t` value is to the `f3` characteristic of the test data, the more accurate the regression model is.

The error of this prediction with the MSE criterion is equal to:

1/2 (t - f3)^2

We do the same for the other test data and add or average the prediction errors.

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- NumPy
- pandas
- scikit-learn

### Installation

Clone the repository and install the required libraries:

```bash
git clone https://github.com/xnima2000/linear-regression-implementation.git
cd linear-regression-implementation
pip install -r requirements.txt
```

### Usage

Run the script to see the linear regression in action:

```bash
python script.py
```

## 📊 Description

This script performs the following steps:

1. **Step One**: Load the sample data into a pandas DataFrame.
2. **Step Two**: Split the data into training and testing sets.
3. **Step Three**: Calculate the parameters of the linear regression model.
4. **Step Four**: Make predictions on the test set and calculate the Mean Squared Error (MSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License. See the LICENSE file for details.

---

🌟 Happy Coding!
