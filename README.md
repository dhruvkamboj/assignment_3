# Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model 📊

**Assignment-1**  
**UCS654**

_Submitted by:_  
**Dhruv Kamboj**  
**102303645**  
**3C45**

---

## 🎯 Objective

The objective of this assignment is to **learn the parameters of a probability density function (PDF)** after applying a **roll-number-based non-linear transformation** to real-world air quality data.

The task demonstrates:

- Non-linear data transformation
- Parameter estimation
- Learning a probability distribution from real data

---

## 📥 Dataset

The dataset contains air quality measurements across Indian cities.  
For this assignment, the **NO₂ (Nitrogen Dioxide)** feature is used as the input variable \( x \).

**Dataset Link:**  
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

---

## 🧩 Problem Formulation

### Step-1: Non-Linear Transformation

Each value of \( x \) is transformed using:

$$
z = x + a_r \sin(b_r x)
$$

Where:

$$
a_r = 0.05 \times (r \bmod 7)
$$

$$
b_r = 0.3 \times ((r \bmod 5) + 1)
$$

and  

r = university roll number(102303645).


---

### Step-2: Probability Density Function

The transformed data (z) is modeled using the PDF:

$$
\hat{p}(z) = c \cdot e^{-\lambda (z-\mu)^2}
$$

Where:

- μ → mean (center of distribution)
- λ → spread parameter
- c → scaling constant

---

## ⚙️ Parameter Estimation Method

Parameters were estimated using **Maximum Likelihood Estimation (MLE)**, which for a Gaussian-shaped distribution is equivalent to computing:

- Sample mean
- Sample variance

from the transformed data.

### Computation formulas

$$
\mu = \text{mean}(z)
$$

$$
\sigma^2 = \text{variance}(z)
$$

$$
\lambda = \frac{1}{2\sigma^2}
$$

$$
c = \frac{1}{\sqrt{2\pi\sigma^2}}
$$


---

## 🧮 Estimated Parameters

Using the given roll number and dataset, the following values were obtained:

| Parameter | Value |
|----------|------|
| μ (mu) | **25.804484510102007** |
| λ (lambda) | **0.0014602636800887954** |
| c | **0.02155960031650373** |

---

## 🧠 Interpretation & Insights

- The transformed data follows a **Gaussian-like distribution**.
- The mean $$\( \mu \approx 25.8 \)$$ represents the central tendency of the transformed NO₂ values.
- The small value of $$\( \lambda \)$$ indicates a **relatively wide distribution**.
- The scaling constant $$\( c \)$$ ensures the function behaves like a proper probability density.

---

## 📝 Conclusion

This assignment demonstrates how **probability density functions can be learned from real-world data** using parameter estimation techniques.

By applying a **roll-number-based non-linear transformation** and using **maximum likelihood estimation**, the parameters of the distribution were successfully learned.

---

## ✅ Key Takeaway

> Estimation techniques like MLE allow us to determine the most likely parameters of a probability model directly from observed data.

---

⭐ *This project illustrates the practical use of statistical estimation in modeling real-world datasets.*
