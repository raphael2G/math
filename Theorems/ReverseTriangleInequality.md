# Theorem: Reverse Triangle Inequality

**Statement:**  
For any real numbers (or vectors in a normed space) $x$ and $y$, the following inequality holds:

$$
||x| - |y|| \leq |x - y|
$$

This is known as the **Reverse Triangle Inequality** and it complements the regular triangle inequality.

In my opinion, the most intuitive way to think about this problem is: 

$$dist(x, y) \geq |dist(x, z) - dist(z, y)|$$

That is, the distance between any two points is greater than or equal to the difference between any two points and their some intermediate value.

---

### Proof Sketch:

1. **Want to Show** $|x| - |y| \leq |x - y| \land |x| - |y| \geq -|x - y|$

2. **Showing** $|A| - |B| \leq |A - B|$
By the triangle inequality, we know $|A + B| - |B| \leq  |A|$
Let $A = x - y$ and $B = y$. Then, |x| 

---

### Applications:

- **Distance in Normed Spaces**:  
  The reverse triangle inequality helps provide a lower bound for the difference between the magnitudes of two vectors or real numbers. It is often used in analysis and geometry to reason about distances in Euclidean space and other normed spaces.

- **Approximation**:  
  The inequality is useful in bounding errors in numerical approximations where the difference between magnitudes needs to be estimated.

---

### Example:

- Suppose $x = 5$ and $y = 3$. Then we can calculate:
  $$
  ||5| - |3|| = |5 - 3| = 2
  $$
  and
  $$
  |5 - 3| = 2
  $$
  Thus, the reverse triangle inequality holds with equality in this case.

- For vectors $x = (1, 2)$ and $y = (3, 4)$ in $\mathbb{R}^2$, we can similarly compute the magnitudes and differences to see that the inequality holds.

---

### Citations:
- **[Proof Strategy: Triangle Inequality](./TriangleInequality.md)**  
  The reverse triangle inequality directly follows from applying the triangle inequality to both $x$ and $y$.
