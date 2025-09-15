# Supervised Machine Learning

Supervised machine learning is a type of machine learning where the model is trained on a **labeled dataset** (i.e., the target or outcome variable is known).  

For instance, if data scientists were building a model for **tornado forecasting**, the input variables might include:
- Date  
- Location  
- Temperature  
- Wind flow patterns  
- Other weather features  

The output would be the **actual tornado activity recorded** for those days.

---

## Applications of Supervised Learning
- Risk assessment  
- Image recognition  
- Predictive analytics  
- Fraud detection  

---

## Types of Algorithms

### 1. Regression Algorithms
- Predict **continuous output values** by identifying relationships between features.  
- Example outputs: **temperature, salary, house price**  
- Common algorithms:
  - Linear Regression  
  - Random Forest Regression  
  - Gradient Boosting  

---

### 2. Classification Algorithms
- Predict **categorical output variables**.  
- Example outputs: “**spam**” or “**not spam**”, “**disease present**” or “**absent**”  
- Common algorithms:
  - Logistic Regression  
  - K-Nearest Neighbors (KNN)  
  - Support Vector Machines (SVMs)  

---

### 3. Naïve Bayes Classifiers
- Useful for **large datasets**.  
- Belong to the family of **generative learning algorithms** (model input distribution of a given class).  
- Variants can also accommodate **regression + classification** tasks.  
- Example: Decision Trees  

---

### 4. Neural Networks
- Inspired by the **human brain** with many connected processing nodes.  
- Applications:
  - Natural language translation  
  - Image recognition  
  - Speech recognition  
  - Image generation  

---

### 5. Random Forest Algorithms
- Combine the results of multiple **decision trees** to predict:
  - Continuous values (**regression**)  
  - Categories (**classification**)  

---

## Visual Overview

```mermaid
graph TD
    A[Supervised Learning] --> B[Regression]
    A --> C[Classification]
    A --> D[Naïve Bayes]
    A --> E[Neural Networks]
    A --> F[Random Forest]

    B --> B1[Continuous Outputs]
    C --> C1[Categorical Outputs]
    D --> D1[Generative Models]
    E --> E1[NLP, Vision, Speech]
    F --> F1[Ensemble of Trees]
