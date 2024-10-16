# Problem: Showing the Maximum Growth Rate of Convergent Sums

**Problem Statement:**  
Let $a_1, a_2, \dots$ be positive integers such that $\sum \frac{1}{a_i}$ converges. For each $n$, let $b_n$ denote the number of positive integers $i$ for which $a_i \leq n$. Prove that:

$$
\lim_{n \to \infty} \frac{b_n}{n} = 0
$$

---

### Intuition:

To understand why this statement makes sense, consider the case of the harmonic series $\sum_{i=1}^{\infty} \frac{1}{i}$, which is divergent. In this case, $b_n$ grows proportionally to $n$ because there are approximately $n$ terms where $a_i \leq n$. However, in the given problem, the sum $\sum_{i=1}^{\infty} \frac{1}{a_i}$ converges, which implies that the $a_i$'s must grow sufficiently fast to counterbalance the harmonic-like growth.

The convergence of $\sum \frac{1}{a_i}$ suggests that the sequence $a_i$ grows quickly enough that the number of terms below any given $n$ does not grow as fast as $n$. Therefore, we intuitively expect that $b_n$ grows slower than $n$, leading to the limit $\lim_{n \to \infty} \frac{b_n}{n} = 0$.

---

### Solution Overview:

We will first introduce $d_k$, which represents the number of elements in the sequence equal to $k$. We know that $d_k$ must be finite for each $k$, as otherwise, the sum $\sum \frac{1}{a_i}$ would diverge. We will use the relationship between $b_n$, $b_{n-1}$, and $d_k$ to derive the result.

---

### Step 1: Define $d_k$

Define $d_k$ as the number of elements in the sequence $a_i$ that are equal to $k$. This means:

$$
d_k = b_k - b_{k-1}
$$

Since $\sum_{i=1}^{\infty} \frac{1}{a_i}$ converges, $d_k$ must be finite for each $k$. If $d_k$ were infinite for any $k$, the sum would have an infinite number of terms equal to $\frac{1}{k}$, which would make the series diverge.

---

### Step 2: Express the Sum in Terms of $d_k$

We know that the sum $\sum_{i=1}^{\infty} \frac{1}{a_i}$ can be rewritten as a sum over $k$, where $d_k$ is the number of times $a_i = k$. Therefore, we can write:

$$
\sum_{i=1}^{\infty} \frac{1}{a_i} = \sum_{k=1}^{\infty} d_k \cdot \frac{1}{k}
$$

By substitution, we also know that $d_k = b_k - b_{k-1}$, so we can rewrite the sum as:

$$
\sum_{k=1}^{\infty} (b_k - b_{k-1}) \cdot \frac{1}{k}
$$

This gives us a way to express the convergence condition in terms of $b_k$ and $d_k$.

---

### Step 3: Bound $b_k$

Next, we want to set a lower bound of this series. To do so, we will use the limit we are given. 

$$\lim_{n \rightarrow \infin}\frac{b_n}{n} = L $$

Then, there exists some $N$ such that for $k$ bigger than this $N$, 
$$|\frac{b_n}{n} - L| \leq \epsilon \Rightarrow b_n \geq n (L + \epsilon) = n c$$

---

### Step 4: Sum and Convergence

We now consider the full sum:

$$
\sum_{i=1}^{\infty} \frac{1}{a_i} = \sum_{k=1}^{\infty} d_k \frac{1}{k} = \sum_{k=1}^{\infty} (b_k - b_{k-1}) \cdot \frac{1}{k} \geq \sum_{k=1}^{\infty}\frac{(cn - c(n-1))}{k} = c\sum_{k=1}^{\infty} \frac{1}{k}
$$

So $$\sum_{k=1}^{\infty} \frac{1}{a_i} \geq c \sum_{k=1}^{\infty} \frac{1}{k}$$

But that is $c$ times the harmonic series, so we know that for this to converge $c$ must equal 0. That means, for this to hold for all epsilon, $L$ must be equal to $0$.

---

### Conclusion:

Thus, we have shown that:

$$
\lim_{n \to \infty} \frac{b_n}{n} = 0
$$

This means that the number of integers $i$ for which $a_i \leq n$ grows slower than $n$, which aligns with our intuition that the sequence $a_i$ grows rapidly enough to make the series $\sum \frac{1}{a_i}$ converge.

---

### Citations:
- **[Theorem: Harmonic Series](./Theorems/HarmonicSeries.md)**  
  Used to understand the divergence of the harmonic series and why the sum converges when $L = 0$.
  
- **[Proof Strategy: Bounding and Limits](./ProofStrategies/BoundingLimits.md)**  
  Applied bounding techniques and limits to show the convergence of the series.
