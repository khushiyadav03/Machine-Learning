# Distance Measures in KNN

The core of KNN lies in measuring the distance between data points. The shorter the distance, the more similar the points are considered to be. Two primary distance metrics are used:

---

## Euclidean Distance

Imagine drawing a straight line between two points on a graph. The length of that line is the Euclidean distance. It's the most common distance metric and is derived directly from the Pythagorean theorem.

For two data points, $A = (X_1, Y_1)$ and $C = (X_2, Y_2)$, the Euclidean distance (D) is calculated as:
$$D = \sqrt{(X_2 - X_1)^2 + (Y_2 - Y_1)^2}$$

#### Example:
Let's say point A is (1, 1) and point C is (2, 2).

$D = \sqrt{(2-1)^2 + (2-1)^2}$

$D = \sqrt{(1)^2 + (1)^2}$

$D = \sqrt{1+1}$

$D = \sqrt{2}$

So, the Euclidean distance between (1, 1) and (2, 2) is approximately **1.414**.

---

## Manhattan Distance

Think of navigating a city grid, like Manhattan! You can't go diagonally through buildings; you have to travel along the streets (horizontally or vertically). The Manhattan distance calculates the sum of the absolute differences between the coordinates. 

For two data points, $A = (X_1, Y_1)$ and $C = (X_2, Y_2)$, the Manhattan distance (D) is calculated as:
$$D = |X_1 - X_2| + |Y_1 - Y_2|$$

#### Example:
Using the same points, A = (1, 1) and C = (2, 2):

$D = |1 - 2| + |1 - 2|$

$D = |-1| + |-1|$

$D = 1 + 1$

$D = 2$

The Manhattan distance between (1, 1) and (2, 2) is **2**.

---

## When to Use Which Distance

* **Euclidean Distance** is generally preferred when you want to calculate the shortest straight-line path between two points and when the features have similar scales.

* **Manhattan Distance** is often more suitable for high-dimensional data or when you want to avoid squaring errors for large differences. It's like measuring the path a taxi would take in a city grid, moving only along the axes.

In the context of KNN, once these distances are calculated for all data points relative to a new, unclassified point, the model simply selects the 'K' points with the smallest distances. For classification, it takes a majority vote among these 'K' neighbors. For regression, it averages their values.