# Model Parameters vs. Hyperparameters ⚙️

When we train a machine learning model, there are two types of "settings" we deal with. Understanding them well is very important.

---

## 1. Model Parameters

**In simple words:** These are the settings that the model **learns on its own from the data** during training. They are the "internal" parts of the model. We do not set them directly.

**Analogy:** Imagine you are a student (the model). The knowledge and concepts you form in your brain (like connections between neurons) after studying are your **parameters**. You have learned these from experience (the data).

**Examples & Formulas:**
-   **Weights (w):** Determine how much importance to give to each feature. In linear regression, this is the slope ($m$).
-   **Bias (b):** The model's offset or starting point. In linear regression, this is the intercept ($c$).

The combined formula in a linear model looks like this:
$y = (w_1x_1 + w_2x_2 + \dots) + b$

**Key Point:** The very goal of model training is to find the best possible values for these parameters (weights and bias).

---

## 2. Hyperparameters

**In simple words:** These are the settings that **we, the developers, set before training the model**. They are the "external" settings that control the learning process itself.

**Analogy:** Your study strategy is your **hyperparameters**. For instance, "How many hours will I study every day?" (number of epochs), or "How deeply will I try to understand a topic in one go?" (learning rate). You decide these settings yourself before you start studying.

**Examples & Formulas:**
-   **Learning Rate ($\alpha$):** This determines how much the model adjusts its parameters (weights) in each step.
    -   **Formula (in Gradient Descent):** $w_{\text{new}} = w_{\text{old}} - \alpha \cdot (\text{error\_gradient})$
    -   **Too High:** The model might overshoot the optimal point and never find the best solution. 
    -   **Too Low:** The model will learn very slowly, and training will take a long time. 
-   **Number of Epochs:** How many times the model will go through the entire training dataset.
-   **Number of Layers / Neurons (in Neural Networks):** Defines the architecture of the model.

---

## Summary

| Property          | Model Parameters                        | Hyperparameters                             |
| ----------------- | --------------------------------------- | ------------------------------------------- |
| **Who Sets It?** | The **Model** (from data)               | The **Developer** (before training)         |
| **Purpose** | To make predictions                     | To control the learning process             |
| **Example** | Weights ($w$), Bias ($b$)               | Learning Rate ($\alpha$), Number of Epochs  |
| **Analogy** | The knowledge learned                   | The method of studying                     |

To become a good machine learning engineer, understanding the difference between these two and learning how to "tune" the right hyperparameters is crucial.