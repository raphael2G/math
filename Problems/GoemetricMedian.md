# Problem: Geometric Median

Let $P_1, P_2, \dots, P_n$ be points on a line, not necessarily distinct. Which point(s) $P$ on the line minimize the sum of distances $\sum_{i=1}^{n} |P - P_i|$?

---

### Solution Overview:

We want to minimize the function $f(P)$ that represents the sum of distances between the point $P$ and the given points $P_1, P_2, \dots, P_n$. This can be written as:

$$
f(P) = \sum_{i=1}^{n} |P - P_i|
$$

To solve this, we use the following steps:

1. **Split the Sum to Handle the Absolute Values:**
   Break the sum into two parts:
   - The part where $P \geq P_i$ for some points.
   - The part where $P < P_i$ for the remaining points.

   We can define $f(P)$ more clearly by considering the contribution of points to the left and right of $P$.

2. **Find the Derivative:**
   Consider the derivative of $f(P)$ with respect to $P$. Since the function involves absolute values, the derivative will change based on whether $P$ is to the left or right of each $P_i$. We examine where the derivative equals zero:
   
   - For $P$ less than a given $P_i$, the derivative is $-1$.
   - For $P$ greater than $P_i$, the derivative is $+1$.

3. **Condition for Minimization:**
   The derivative $f'(P)$ will equal zero when the number of points on the left of $P$ equals the number of points on the right of $P$. This happens when $P$ is the **median** of the points. Therefore, the value of $P$ that minimizes $f(P)$ is the median of the set of points $P_1, P_2, \dots, P_n$.

### Conclusion:

The point $P$ that minimizes the sum of distances $\sum_{i=1}^{n} |P - P_i|$ is the **median** of the points $P_1, P_2, \dots, P_n$. If $n$ is odd, this is the middle point. If $n$ is even, any point between the two middle points minimizes the sum.

### Key Insight:

The sum of absolute differences is minimized when the number of points to the left and right of $P$ is equal, which occurs at the median.

