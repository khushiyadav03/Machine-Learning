# Gradient Descent for Logistic Regression

---

## Goal of Gradient Descent

Logistic Regression ka accuracy weights (**W**) aur bias (**b**) pe depend karta hai. Training ka main goal hai **W** aur **b** ki best values find karna jo model ke predictions ko true labels ke sabse close le aaye.

* **Cost Function**: Ye ek single number calculate karta hai → poore dataset ka total error.
    * **High cost** → predictions galat (far from true values).
    * **Low cost** → predictions accurate.
* **Gradient Descent ka purpose**: **W** aur **b** aise update karna ki **Cost Function** minimum ho.

---

## Hill Analogy – Samajhne ka Tarika ⛰️

Imagine the Cost Function as a U-shaped valley or hill.

* **Hill**: The U-shaped curve represents the **Cost Function**.
* **Your Position**: Your current **W** aur **b** values.
* **Bottom of Hill**: The global minimum → cost is lowest → best parameters.



The step-by-step process is:

1.  **Start Somewhere**: Random **W** aur **b** se start karo.
2.  **Check the Slope**: Gradient calculate karo → ye steepest downhill direction bataata hai.
3.  **Take a Small Step**: **W** aur **b** ko thoda adjust karo → downhill.
4.  **Repeat**: Slope check + step repeat karo jab tak tum bottom tak na pahunch jao.

---

## Math Behind Gradient Descent

### Update Rules
$$W_{\text{new}} = W_{\text{old}} - (\alpha \cdot dW)$$
$$b_{\text{new}} = b_{\text{old}} - (\alpha \cdot db)$$

**Components**:
* **α (alpha) = Learning Rate**: Ek small number (e.g., 0.01) jo step size control karta hai.
    * Too big → overshoot kar sakte ho.
    * Too small → convergence bahut slow hoga.
* **dW, db = Derivatives**: Ye Cost Function ka slope hai with respect to **W** aur **b**. Ye direction batata hai ki downhill kaunsi side hai.

### Derivative Formulas for Logistic Regression
$$dW = \frac{1}{m} \sum_{i=1}^{m} (\hat{y}^{(i)} - y^{(i)}) \cdot x^{(i)}$$
$$db = \frac{1}{m} \sum_{i=1}^{m} (\hat{y}^{(i)} - y^{(i)})$$

* **m**: Total training examples.
* **ŷ (y-hat)**: Predicted probability.
* **y**: True label.
* **x**: Input feature.

**Intuition**: Ye formulas batate hain ki Cost Function ka slope kaisa hai aur kis direction me **W** aur **b** ko adjust karna hai.

---

## Summary of Essential Equations

1.  **Linear Equation**:
    $z = W \cdot X + b$

2.  **Sigmoid Function**:
    $$\hat{y} = \frac{1}{1 + e^{-z}}$$

3.  **Derivatives (Slope)**:
    $dW = \frac{1}{m} \sum (\hat{y} - y) \cdot x$
    $db = \frac{1}{m} \sum (\hat{y} - y)$

4.  **Gradient Descent Update Rules**:
    $W = W - (\alpha \cdot dW)$
    $b = b - (\alpha \cdot db)$

---

## Step-by-Step Training Loop (Conceptual)

Initialize W, b randomly

Repeat for a number of iterations (or until convergence):

Forward Propagation
Calculate z = W·X + b
Calculate ŷ = sigmoid(z)

Backward Propagation (Calculate Derivatives)
Calculate dW, db using derivative formulas

Update Parameters
Update W = W - α·dW
Update b = b - α·db

Optional: Monitor progress
Calculate Cost J(W,b)

Stop when the Cost Function stops decreasing → **W** aur **b** optimized hain.

---

## Key Takeaways

* **Gradient Descent** ek optimization algorithm hai jo trial & error se best parameters find karta hai.
* **Slope (gradient)** batata hai ki kis direction me step lena hai.
* **Learning Rate** step size control karta hai.
* Jab **Cost Function minimum** hota hai, tab **best W & b** milte hain, jisse predictions sabse accurate hote hain.
* Ye ek iterative process hai jo **global minimum** par converge hota hai.
