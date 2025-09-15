# Unsupervised Machine Learning

Unsupervised learning algorithms draw inferences from **unlabeled datasets**, enabling:
- Exploratory data analysis  
- Pattern recognition  
- Predictive modeling  

Examples of algorithms include:
- **Apriori**  
- **Gaussian Mixture Models (GMMs)**  
- **Principal Component Analysis (PCA)**  

---

## Common Applications
- Customer segmentation  
- Anomaly detection  
- Recommendation systems  
- Data visualization  
- Dimensionality reduction  

---

## Types of Unsupervised Learning Algorithms

### 1. Clustering Algorithms

#### K-Means Clustering
- Assigns data points into **K groups**.  
- Data points closest to a given **centroid** are clustered under the same category.  
- **K** represents number of clusters (granularity).  
- Applications:
  - Market segmentation  
  - Document clustering  
  - Image segmentation  
  - Image compression  

#### Hierarchical Clustering
- Builds a hierarchy of clusters.  
- Types:
  - **Agglomerative** → Start with individual points, iteratively merge clusters based on similarity until one cluster remains.  
  - **Divisive** → Start with all data points in one cluster, then iteratively divide into smaller clusters.  

#### Probabilistic Clustering
- Solves **density estimation** or “soft” clustering problems.  
- Groups data points based on the **likelihood** they belong to a distribution (e.g., Gaussian Mixture Models).  

---

### 2. Association Algorithms
- Identify **associations between data objects** in large datasets.  
- Example: Market basket analysis (“Customers who bought X also bought Y”).  
- Useful in recommendation systems and pattern discovery.  

---

## Visual Overview

```mermaid
graph TD
    A[Unsupervised Learning] --> B[Clustering]
    A --> C[Association]
    A --> D[Dimensionality Reduction]

    B --> B1[K-Means]
    B --> B2[Hierarchical]
    B --> B3[Probabilistic]

    C --> C1[Market Basket Analysis]
    D --> D1[PCA, Visualization]
