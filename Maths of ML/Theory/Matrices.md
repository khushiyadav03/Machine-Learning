# Matrices: Theory and Concepts ▦

## 1. Matrix Kya Hai? (What is a Matrix?)

Agar vector ek line (row ya column) of numbers hai, toh matrix numbers ka ek poora grid ya table hai. Isme rows aur columns dono hote hain.



---

## 2. Machine Learning me Matrices Kyun Sabse Important Hain?

Yeh sabse zaroori concept hai. Aapka poora dataset ek matrix hi hota hai!

* **Rows:** Har row ek single data point (ek vector) ko represent karti hai. Jaise, ek patient ki details.
* **Columns:** Har column ek feature ko represent karta hai. Jaise, Age, Blood Pressure, Weight.

#### Example Dataset as a Matrix:

| Age (Feature 1) | Blood Pressure (Feature 2) | Has Diabetes (Target) |
| :-------------- | :------------------------- | :-------------------- |
| 45              | 140                        | 1                     |
| 23              | 120                        | 0                     |
| 51              | 155                        | 1                     |

Toh jab hum kehte hain "model ko data par train karna hai", iska matlab hai ki hum is matrix par mathematical operations kar rahe hain.

---

## 3. Matrix ke Formulas aur Properties

### Shape (Dimensions)

Yeh batata hai ki matrix me kitni rows aur columns hain. Ise `(rows, columns)` likha jaata hai. Upar wale example ka shape `(3, 3)` hai.

### Transpose of a Matrix ($A^T$)

Matrix ka transpose karna matlab uski rows ko columns me aur columns ko rows me badal dena.

**Example:**
Agar Matrix `A` hai (Shape: 2 rows, 3 columns):

[[1, 2, 3],
[4, 5, 6]]


Toh `A` ka Transpose $A^T$ hoga (Shape: 3 rows, 2 columns):
[[1, 4],
[2, 5],
[3, 6]]


---

# Matrix Operations: Formulas and Intuition

### 1. Matrix Addition and Scalar Multiplication

Yeh bilkul vectors ki tarah hi kaam karte hain.

* **Addition:** Corresponding elements add ho jaate hain. (Dono matrices ka shape same hona zaroori hai).
* **Scalar Multiplication:** Matrix ke har element ko ek single number se multiply kar diya jaata hai.

### 2. Matrix Multiplication (The Most Important Operation)

Yeh simple element-wise multiplication nahi hai. Yeh data ko transform karne ka ek powerful tarika hai.

> **Golden Rule:** Do matrix `A` aur `B` ko multiply karne ke liye (`A @ B`), pehli matrix (`A`) ke **columns** ka number doosri matrix (`B`) ke **rows** ke number ke barabar hona chahiye.

**Formula:** $(m \times n) \ @ \ (n \times p) \ \rightarrow \ (m \times p)$

Matlab: Agar ek matrix ka shape `(3, 4)` hai aur doosri ka `(4, 5)`, to multiplication possible hai. Resulting matrix ka shape `(3, 5)` hoga. Agar pehli ka shape `(3, 4)` aur doosri ka `(2, 5)` hai, to multiplication possible nahi hai.

#### ML me Use:

* **Neural Networks:** Yeh neural networks ki jaan hai. Jab data ek layer se doosri layer me jaata hai, to woh ek weight matrix se multiply hota hai. Yahi process "learning" ka core hai, jahan model data ko ek useful representation me transform karta hai.

### 3. Special Matrices

#### Identity Matrix (I)

Yeh matrix world ka "1" hai. Yeh ek square matrix (rows = columns) hoti hai jiske diagonal me `1`s hote hain aur baaki sab jagah `0`s.
[[1, 0, 0],
[0, 1, 0],
[0, 0, 1]]

Kisi bhi matrix `A` ko Identity matrix `I` se multiply karne par `A` hi waapis milta hai.
$A \ @ \ I = A$

#### Zero Matrix

Yeh matrix world ka "0" hai. Iske saare elements `0` hote hain.
