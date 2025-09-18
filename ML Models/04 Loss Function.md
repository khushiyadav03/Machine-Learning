# Loss Function

**In simple words:** A **Loss Function** is a formula that tells you how big an error your model made in its prediction.

-   **Low Loss:** This means the model's prediction is very close to the actual value. (👍 Good Model)
-   **High Loss:** This means the model's prediction is far from the actual value. (👎 Bad Model)

The entire goal of training a machine learning model is to **minimize the value of the Loss Function**.

The process is:
1.  The model makes a prediction.
2.  The Loss Function calculates the error between that prediction and the actual value.
3.  The model learns from this error and adjusts itself to reduce the error next time.

Different loss functions are used for different problems. We'll look at the two most common types.

---

## 1. Loss Function for Regression (For Predicting Numbers)

When we need to predict a continuous value (like a house price or salary), the most common loss function is **Mean Squared Error (MSE)**.

**Formula:**
$$
\text{MSE} = \frac{1}{n} \sum (y_{\text{true}} - y_{\text{pred}})^2
$$

**Breaking down the formula in simple terms:**

-   **$(y_{\text{true}} - y_{\text{pred}})$**: This is the simple difference or error between the actual value ($y_{\text{true}}$) and the model's prediction ($y_{\text{pred}}$).
-   **$(\dots)^2$**: We **square** this error. This has two benefits:
    -   It turns negative errors into positive ones (because an error is an error, whether it's -2 or +2).
    -   It penalizes larger errors more heavily (a square of 2 is 4, but a square of 10 is 100).
-   **$\sum(\dots)$**: We calculate this squared error for every data point and then **sum** them all up. $\sum$ (Sigma) is the symbol for sum.
-   **$\frac{1}{n} \times \dots$**: Finally, we take the **average (mean)** of all these squared errors. Here, `n` is the total number of data points.

So, MSE simply means the "average of all the squared errors."

---

## 2. Loss Function for Classification (For Predicting Categories)

When we need to predict a category (like 'Cat' vs. 'Dog', or 'Spam' vs. 'Not Spam'), the most common loss function is **Cross-Entropy Loss** (or Log Loss).

Its formula looks a bit complex, but the concept is very simple.

**Intuition:**
In classification, the model predicts a probability (e.g., "there's a 90% chance this is a 'Cat'"). Cross-Entropy Loss penalizes the model heavily when it is very **confident** in the **wrong** prediction.

**Example:**
-   **Case 1:** The actual picture is a **Cat**. The model predicts a 90% (0.9) chance of it being a Cat.
    -   The model is correct and confident. **The loss will be very low.**
-   **Case 2:** The actual picture is a **Cat**. The model predicts a 10% (0.1) chance of it being a Cat (meaning a 90% chance it's a Dog).
    -   The model is wrong and very confident in its wrong answer. **The loss will be very high.**

Cross-Entropy just ensures that the model not only makes the right prediction but is also confident about it.

---

## Summary

The **Loss Function** is the model's "report card," telling it how badly it's performing. The entire process of model training is driven by trying to make this "bad score" as low as possible.