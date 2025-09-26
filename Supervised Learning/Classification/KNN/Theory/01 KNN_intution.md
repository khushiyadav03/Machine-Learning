# K-Nearest Neighbors (KNN) Basics

KNN ek supervised machine learning algorithm hai jo new data point ko classify ya predict karta hai based on uske K closest neighbors. Closeness measure hoti hai distance formula se.

## Key Points

* **Supervised Learning**: Training data labeled hona chahiye (matlab classes ya values already pata hain).
* **Versatile**: Classification (categories like ‘dog’ or ‘cat’) aur Regression (continuous value like salary) dono ke liye use hota hai.
* **Non-linear Data**: Linear regression ki tarah line fit karne ki zaroorat nahi; predictions local neighborhood ke basis par hoti hain.
* **‘K’ Value**: Ye user-defined number hai jo decide karta hai ki kitne nearest neighbors consider honge prediction ke liye. Sahi K choose karna bahut important hai.

---

## ⚙️ KNN Kaise Kaam Karta Hai: Intuition

KNN ka core idea: similar cheezein paas mein hoti hain.

### Classification Example

Loan applicants ko classify karna hai based on loan amount aur annual income:

1.  **New Data Point**: Ek naya applicant (red dot) ko classify karna hai.
2.  **Set K**: Maan lo K = 5 (odd number to avoid tie).
3.  **Find Nearest Neighbors**: 5 closest points find karo (distance formula: Euclidean ya Manhattan).
4.  **Vote**: Neighbors ke classes count karo. Example: 3 green, 2 blue.
5.  **Assign Class**: Majority class assign kar do. Red dot → “green” (will not repay).

### Regression Example

Salary predict karna hai based on years of experience:

1.  **New Data Point**: Ek person ki experience ke basis pe salary predict karni hai.
2.  **Set K**: K = 5.
3.  **Find Nearest Neighbors**: 5 closest people with similar experience.
4.  **Average**: Neighbors ki salaries ka mean calculate karo.
5.  **Assign Value**: Ye average new person ki predicted salary ban jati hai.

---

## ✅ Advantages aur ❌ Disadvantages

### Advantages

* **Chhote Datasets ke liye Best**: Low features wale small datasets pe acha perform karta hai.
* **Multi-purpose**: Classification aur regression dono ke liye.
* **Multi-class Problems easy**: More than 2 categories ke liye naturally kaam karta hai.
* **Flexible Distance Metrics**: Euclidean, Manhattan etc. choose kar sakte ho.

### Disadvantages

* **K choose karna critical**: Galat K → poor predictions.
* **Large datasets me slow**: Har point ka distance calculate karna padta hai → computationally expensive.
* **Imbalanced Data me biased**: Majority class ke favor me predictions ho sakti hain.
* **Outliers pe sensitive**: Outliers distance ko skew kar dete hain → wrong predictions.