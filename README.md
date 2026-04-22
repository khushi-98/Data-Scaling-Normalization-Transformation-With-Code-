# Data-Scaling-Normalization-Transformation-With-Code-

# 📘 Data Scaling, Normalization & Transformation (Complete Guide)

A complete guide to **data preprocessing techniques in Machine Learning**, including **Scaling, Normalization, and Transformation** with clear **definitions, formulas, and explanations**.

---

## 🚀 Overview

In Machine Learning, the **scale and distribution of features** directly impact model performance.

Algorithms like:
- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)
- Neural Networks
- Linear Models

are **sensitive to feature scaling**.

👉 If features are not scaled properly:
- Larger values dominate  
- Models become biased  
- Accuracy decreases  

---

## ⚠️ Why Data Scaling Matters

### Example:
- Income → 30,000 to 10,00,000  
- Age → 0 to 100  

👉 Income dominates → Age ignored ❌  

### Problems:
- Wrong predictions  
- Biased model  
- Slow training  
- Poor accuracy  

---

# 🧪 Techniques

---

## 🔹 1. Min-Max Scaling

**Definition:**  
Min-Max Scaling rescales feature values to a fixed range, usually **[0, 1]**.

**Formula:**
```

X_scaled = (X - X_min) / (X_max - X_min)

```

**Where:**
- X = Original value  
- X_min = Minimum value  
- X_max = Maximum value  

**Use Case:**
- Fixed range data  
- No extreme outliers  

**Limitation:**
- Sensitive to outliers  

---

## 🔹 2. Standardization (Z-Score)

**Definition:**  
Standardization transforms data so that it has:
- Mean = 0  
- Standard Deviation = 1  

**Formula:**
```

Z = (X - μ) / σ

```

**Where:**
- μ = Mean  
- σ = Standard deviation  

**Use Case:**
- Normally distributed data  
- Used in SVM, Logistic Regression  

---

## 🔹 3. Robust Scaling

**Definition:**  
Robust Scaling uses **median and interquartile range (IQR)**, making it resistant to outliers.

**Formula:**
```

X_scaled = (X - Median) / IQR

```

**Where:**
```

IQR = Q3 - Q1

```

**Use Case:**
- Data with outliers  

---

## 🔹 4. Log Transformation

**Definition:**  
Log transformation applies a logarithmic function to reduce skewness and compress large values.

**Formula:**
```

X_transformed = log(X)

```

**Use Case:**
- Right-skewed data  

**Note:**
- Works only for positive values  

---

## 🔹 5. Power Transformations

**Definition:**  
Power transformations modify the distribution of data to make it more **normal-like** and stabilize variance.

---

### 🔸 Box-Cox Transformation (Only Positive Data)

**Formula:**
```

X(λ) = (X^λ - 1) / λ      if λ ≠ 0
X(λ) = log(X)             if λ = 0

```

---

### 🔸 Yeo-Johnson Transformation

**Formula:**
```

For X ≥ 0:
X(λ) = ((X + 1)^λ - 1) / λ       if λ ≠ 0
X(λ) = log(X + 1)                if λ = 0

For X < 0:
X(λ) = - [(-X + 1)^(2 - λ) - 1] / (2 - λ)   if λ ≠ 2

```

---

## 🔹 6. Normalization

**Definition:**  
Normalization scales each **data point (row)** so that its magnitude equals 1.

**Difference:**
- Scaling → Column-wise  
- Normalization → Row-wise  

---

### 🔸 L1 Normalization

**Definition:**  
Ensures the sum of absolute values equals 1.

**Formula:**
```

||x||₁ = |x₁| + |x₂| + ... + |xₙ|
x_normalized = x / ||x||₁

```

---

### 🔸 L2 Normalization

**Definition:**  
Ensures the vector length equals 1.

**Formula:**
```

||x||₂ = sqrt(x₁² + x₂² + ... + xₙ²)
x_normalized = x / ||x||₂

```

---

## 📊 Final Summary

| Technique        | Best For              |
|-----------------|----------------------|
| Min-Max         | Fixed range           |
| Standardization | Normal distribution   |
| Robust Scaling  | Outliers              |
| Log Transform   | Skewed data           |
| Box-Cox         | Positive data         |
| Yeo-Johnson     | Any data              |
| L1 Norm         | Sparse data           |
| L2 Norm         | Distance-based models |

---

## 🎯 Conclusion

✔ Improves model accuracy  
✔ Faster convergence  
✔ Balanced feature contribution  

👉 **Good preprocessing = Better Machine Learning models**

---

## 🛠️ Requirements

```

pip install numpy pandas scikit-learn

```

---

## ⭐ Support

If you found this helpful:

- ⭐ Star this repository  
- 🍴 Fork it  
- 📢 Share with others  

---

## 📌 Connect

- YouTube: @learn.pywithradhe  
- Instagram: @learn.pywithradhe  
- Telegram: https://t.me/learnpywithradhe  
```
