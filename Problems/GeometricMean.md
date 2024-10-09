# Problem: Geometric Mean – Minimizing Squared Distances Between Points

Let $P_1, P_2, \dots, P_n$ be points on a plane. Which point $P$ minimizes the sum of the squared distances from $P$ to each of the points $P_i$ on the plane? In other words, minimize the function:

$$
f(P) = \sum_{i=1}^{n} \|P - P_i\|^2
$$

---

### Solution Overview:

We want to minimize the sum of the squared Euclidean distances between a point $P$ and a set of points $P_1, P_2, \dots, P_n$ on the plane.

1. **Set up the Function**:
   The function we aim to minimize is:

   $$
   f(P) = \sum_{i=1}^{n} \|P - P_i\|^2
   $$

   Expanding the squared distance term:

   $$
   f(P) = \sum_{i=1}^{n} \left( (x - x_i)^2 + (y - y_i)^2 \right)
   $$

   where $P = (x, y)$ and $P_i = (x_i, y_i)$.

2. **Find the Critical Points**:
   To minimize $f(P)$, take the partial derivatives with respect to $x$ and $y$ and set them equal to zero.

   - For $x$:
     $$
     \frac{\partial f}{\partial x} = 2 \sum_{i=1}^{n} (x - x_i) = 0 \quad \Rightarrow \quad x = \frac{1}{n} \sum_{i=1}^{n} x_i
     $$

   - For $y$:
     $$
     \frac{\partial f}{\partial y} = 2 \sum_{i=1}^{n} (y - y_i) = 0 \quad \Rightarrow \quad y = \frac{1}{n} \sum_{i=1}^{n} y_i
     $$

   These equations show that the point $P = (x, y)$ that minimizes the sum of squared distances is the **centroid** of the points $P_1, P_2, \dots, P_n$.

3. **Conclusion**:
   The point $P$ that minimizes the sum of squared distances is the centroid, or **mean** of the points. Thus, the point that minimizes the squared distances is:

   $$
   P = \left( \frac{1}{n} \sum_{i=1}^{n} x_i, \frac{1}{n} \sum_{i=1}^{n} y_i \right)
   $$

   This is the **geometric mean** in terms of the coordinates.

### Citations:
- **[Proof Strategy: Derivatives for Optimization](./proof-strategies/derivatives.md)**  
  Used to find the critical points by setting the partial derivatives to zero.
  
- **[Theorem: Centroid Formula](./theorems/centroid-theorem.md)**  
  States that the centroid of a set of points in the plane minimizes the sum of squared Euclidean distances from those points.

