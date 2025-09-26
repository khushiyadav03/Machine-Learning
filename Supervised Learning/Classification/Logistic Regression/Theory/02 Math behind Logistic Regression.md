# Math behind Logistic Regression

---

## Core Idea

Logistic Regression ek **supervised learning** algorithm hai.

* Mainly **binary classification** ke liye use hota hai (0/1, Yes/No, Spam/Not Spam).
* Ye linear equation ke output ko **Sigmoid function** ke through pass karta hai → jo hamesha probability (0–1 ke beech) deta hai. 
* Fir probability ko threshold (mostly 0.5) se compare karke final class decide hoti hai.

---

## Two Core Equations

### 1. Linear Equation
$$z = W \cdot X + b$$
* **X**: Input features (jaise age, BMI, cholesterol).
* **W (Weights)**: Importance of each feature (model training ke time sikhta hai).
* **b (Bias)**: Constant jo curve ko shift karne me help karta hai.
* Basically, ye ek straight line equation jaisa hi hai (`y = mx + c`).

### 2. Sigmoid Function
$$\hat{y} = \frac{1}{1 + e^{-z}}$$
* **ŷ (y-hat)**: Predicted probability (0 aur 1 ke beech).
* **z**: Linear equation ka output.
* **e**: Euler’s number ≈ 2.718.
* Agar `z` → bada positive number → `ŷ` ≈ 1.
* Agar `z` → bada negative number → `ŷ` ≈ 0.

---

## ⚙️ Step-by-Step Workflow

1.  **Training the Model**:
    * Model dataset use karke **W (weights)** aur **b (bias)** sikhta hai.
    * Optimization algorithm → **Gradient Descent** use hota hai.
2.  **Calculating z**:
    * New input (X) aaya → formula $z = W \cdot X + b$ se ek number nikalta hai.
3.  **Calculating Probability (ŷ)**:
    * `z` ko Sigmoid function me daal ke probability milti hai (0–1 ke beech).
4.  **Assigning Label**:
    * Agar `ŷ > 0.5` → predict **class = 1**.
    * Agar `ŷ < 0.5` → predict **class = 0**.

---

## Worked-Out Example

**Given**:
* `W = 5`
* `b = 10`
* 1 feature: `X`

### Case 1: X = -9
1.  **Calculate z**: $z = (5 \times -9) + 10 = -45 + 10 = -35$
2.  **Calculate Probability**: $\hat{y} = \frac{1}{1 + e^{35}}$ → denominator is huge → `ŷ` ≈ **0**
3.  **Assign Label**: Probability < 0.5 → **Class = 0**

### Case 2: X = 8
1.  **Calculate z**: $z = (5 \times 8) + 10 = 40 + 10 = 50$
2.  **Calculate Probability**: $\hat{y} = \frac{1}{1 + e^{-50}}$ → $e^{-50}$ is almost 0 → `ŷ` ≈ **1**
3.  **Assign Label**: Probability > 0.5 → **Class = 1**

---

### Most Important Takeaway
> **Agar $z = W \cdot X + b$ → bada positive → probability ≈ 1 → class = 1.**
> **Agar $z$ → bada negative → probability ≈ 0 → class = 0.**

Yehi tarika se Logistic Regression data ko do clear classes me separate karta hai.

---

## Quick Recap

### Advantages
* Simple aur efficient.
* Binary classification ke liye perfect.
* Easy to implement.

### Disadvantages
* Complex, non-linear patterns handle nahi kar pata.
* Outliers pe sensitive.
* Zyada features ho gaye to overfit kar sakta hai.