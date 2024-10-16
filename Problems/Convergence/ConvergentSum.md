# Problem: Convergence of $\sum_{i=1}^{\infty}(a_i - b_i)^2$

**Problem Statement:**  
Given that $\sum_{i=1}^{\infty} a_i^2$ and $\sum_{i=1}^{\infty} b_i^2$ both converge, show that $\sum_{i=1}^{\infty} (a_i - b_i)^2$ also converges.

---

### Solution Overview:

We are tasked with proving that if the series $\sum_{i=1}^{\infty} a_i^2$ and $\sum_{i=1}^{\infty} b_i^2$ converge, then the series $\sum_{i=1}^{\infty} (a_i - b_i)^2$ also converges. We will prove this by splitting the sum and analyzing each component.

---

### Step 1: Expand and Split the Sum

We start by expanding the expression $(a_i - b_i)^2$:

$$
(a_i - b_i)^2 = a_i^2 - 2a_ib_i + b_i^2
$$

Thus, we can rewrite the series as:

$$
\sum_{i=1}^{\infty} (a_i - b_i)^2 = \sum_{i=1}^{\infty} a_i^2 - 2 \sum_{i=1}^{\infty} a_i b_i + \sum_{i=1}^{\infty} b_i^2
$$

Since $\sum_{i=1}^{\infty} a_i^2$ and $\sum_{i=1}^{\infty} b_i^2$ both converge by assumption, it remains to show that $\sum_{i=1}^{\infty} a_i b_i$ converges. If this term converges, then the entire sum will converge.

---

### Step 2: Prove Convergence of $\sum_{i=1}^{\infty} a_i b_i$

There are a few ways of proving convergence. One way is to show the sequence is cauchy, but we really don't know anything about how the terms relate to eachother. Another way is to show the sum is monotonic and bounded. 

To make it monotonic, we can simply consider the **absolute value** of each element in the sum $\sum_{i=1}^{\infty} |a_i b_i|$. This will let us prove the series is absolutely convergent, thus convergent. We know this is increasing since it is a sum of positive reals.  

Now need to prove that $\sum_{i=1}^{\infty} |a_i b_i|$ is bounded. 

---

### Step 3: Apply the Cauchy-Schwarz Inequality

To prove absolute convergence, we will use the **Cauchy-Schwarz Inequality**, which states:

$$a_ib_i \leq \sqrt{a_i^2} \sqrt{b_i^2}$$

Since this holds for all $i \in \mathbb{Z}^+$

$$
\sum_{i=1}^{\infty} |a_i b_i| \leq \left( \sum_{i=1}^{\infty} a_i^2 \right)^{\frac{1}{2}} \left( \sum_{i=1}^{\infty} b_i^2 \right)^{\frac{1}{2}}
$$

Since both $\sum_{i=1}^{\infty} a_i^2$ and $\sum_{i=1}^{\infty} b_i^2$ are finite (convergent by assumption), it follows that:

$$
\sum_{i=1}^{\infty} |a_i b_i| \text{ converges} \quad \Rightarrow \quad \sum_{i=1}^{\infty} a_i b_i \text{ converges}
$$

---

### Step 4: Conclusion

Thus, $\sum_{i=1}^{\infty} a_i b_i$ converges, which implies that:

$$
\sum_{i=1}^{\infty} (a_i - b_i)^2 = \sum_{i=1}^{\infty} a_i^2 - 2 \sum_{i=1}^{\infty} a_i b_i + \sum_{i=1}^{\infty} b_i^2
$$

converges, since all components of the sum are convergent. Therefore, the series $\sum_{i=1}^{\infty} (a_i - b_i)^2$ converges.

---

### Citations:
- **[Theorem: Cauchy-Schwarz Inequality](./Theorems/CauchySchwarzInequality.md)**  
  Used to prove that $\sum_{i=1}^{\infty} a_i b_i$ converges.
  
- **[Proof Strategy: Series Convergence](./ProofStrategies/SeriesConvergence.md)**  
  We used a combination of splitting the sum and applying absolute convergence to prove the result.
