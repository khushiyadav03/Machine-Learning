# Loss Function and Cost Function for Logistic Regression

---

## Goal of Logistic Regression

Model ka main kaam:
Input features (`X`) → Linear Equation ($z = W \cdot X + b$) → Sigmoid → Output probability (`ŷ`).

* **ŷ (y-hat)**: Probability ki true label `y = 1` hai.

**Training ka goal**:
Best **W (weights)** aur **b (bias)** find karna jo `ŷ` ko as close as possible kare `y` ke. Ye training process ko guide karte hain **Loss** aur **Cost Functions**.

---

## Loss Function – Error on a Single Example

**Definition**: Ek single data point ke liye prediction kitni galat hai, uska measure.

### Why not use Linear Regression loss?
Linear Regression me simple error = $(y - \hat{y})^2$.
Logistic Regression me agar ye use karenge → graph me multiple dips (local minima) ban jaayenge. **Gradient Descent** confuse ho jaayega aur galat jagah atak sakta hai.



### Solution: Binary Cross-Entropy (Log Loss)
Ye ek **convex** (bowl-shaped) function banata hai → optimization easy ho jaata hai.

**Formula**:
$$L(\hat{y}, y) = -\Big[y \cdot \log(\hat{y}) + (1 - y) \cdot \log(1 - \hat{y})\Big]$$

### Intuition: Two Cases

#### Case 1: True label `y = 1`
Formula simplifies to:
$L = -\log(\hat{y})$
* Agar prediction `ŷ` → 1 (correct) → $\log(\hat{y})$ → 0 → **Loss ≈ 0** (Perfect prediction 👍).
* Agar prediction `ŷ` → 0 (wrong) → $\log(\hat{y})$ → -∞ → **Loss ≫ large** (Model punished 👎).

Model ko reward milta hai jab `ŷ ≈ 1` aur penalty jab galat aur confident hai.

#### Case 2: True label `y = 0`
Formula simplifies to:
$L = -\log(1 - \hat{y})$
* Agar prediction `ŷ` → 0 (correct) → $(1 - \hat{y}) \approx 1$ → $\log(1) = 0$ → **Loss ≈ 0**.
* Agar prediction `ŷ` → 1 (wrong) → $(1 - \hat{y}) \approx 0$ → $\log(0) = -\infty$ → **Loss ≫ large**.

Model ko reward milta hai jab `ŷ ≈ 0` aur penalty jab confidently galat hai.

---

## Loss vs Cost Function

* **Loss Function**: Ek single example ka error.
* **Cost Function**: Puri dataset ka average error.

> Matlab test dene par → ek question ka score = **Loss**, aur poore test ka average = **Cost**.

### Cost Function Formula
$$J(W, b) = \frac{1}{m} \sum_{i=1}^{m} L(\hat{y}^{(i)}, y^{(i)})$$
* **J(W, b)**: Cost function, jo weights aur bias pe depend karta hai.
* **m**: Total training examples.
* **Σ (summation)**: Sab data points ka loss add karke average nikalna.
* **L(...)**: Loss function (binary cross-entropy) har ek example ke liye.

---

## Final Goal of Training

**Gradient Descent** use karke `W` aur `b` aise update karna ki `J(W, b)` minimize ho jaye. Jab Cost Function lowest ho → model ke predictions sabse accurate hote hain poori dataset pe.

## Key Takeaways (One-liners for Revision)
* **Loss** = ek data point ka error.
* **Cost** = sabhi data points ka average error.
* Logistic Regression ke liye → **Binary Cross-Entropy** loss best hai.
* Galti zyada penalty → confidently wrong prediction.
* Optimization ke liye **Convex function** (bowl shape) hona zaroori hai.