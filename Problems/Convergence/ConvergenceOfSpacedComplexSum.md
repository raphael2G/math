# Problem: Converging Complex Series

**Problem Statement:**  
Let $z_1, z_2, z_3, \ldots$ be non-zero complex numbers with the property that $|z_i - z_j| > 1 \ \forall i, j$. Prove that:

$$
\sum_{i=1}^{\infty} \frac{1}{z_i^3}
$$

converges.

---

### Solution Overview:

We are tasked with proving that the series $\sum_{i=1}^{\infty} \frac{1}{z_i^3}$ converges. There are two common approaches to proving the convergence of a series: 

- **Bounding and Monotonicity**: This involves showing that the series is bounded and the terms are decreasing in magnitude.
- **Cauchy Criterion**: For a series to converge, the difference between the $N$th partial sum and the tail of the series must be arbitrarily small for sufficiently large $N$.

Let’s begin by exploring the **Cauchy criterion** before moving to **bounding and monotonicity** to complete the proof.

---

### Step 1: Cauchy Criterion

The Cauchy criterion states that for any $\epsilon > 0$, there exists an $N$ such that for all $n > N$, the difference between the $N$th partial sum and the $n$th partial sum is less than $\epsilon$. In terms of our series, this means we can make the tail sum arbitrarily small:

$$
\left| \sum_{i=N+1}^{n} \frac{1}{z_i^3} \right| < \epsilon \quad \forall n > N.
$$

One way to bound the tail is to find the largest element in the tail and use this to estimate the sum. However, attempting this leads to complications because the minimum value of $|z_i|$ in the tail could change arbitrarily as $n$ increases, making it hard to directly apply the Cauchy criterion.

---

### Step 2: Absolute Convergence via Bounding and Monotonicity

Since the Cauchy approach is difficult to manage, we switch to the **absolute convergence** test. A series converges absolutely if the series of absolute values converges, i.e., if:

$$
\sum_{i=1}^{\infty} \left| \frac{1}{z_i^3} \right| = \sum_{i=1}^{\infty} \frac{1}{|z_i|^3}
$$

converges.

To apply this, we will first establish a bound on the magnitude of $|z_i|$. 

---

### Step 3: Rearranging the Sequence

Let’s consider the points $z_1, z_2, z_3, \ldots$ ordered such that their distances from the origin are non-decreasing:

$$
|z_1| \leq |z_2| \leq |z_3| \leq \cdots.
$$

This ordering is valid because of the commutativity of addition—whether we sum the terms in increasing or decreasing order, the result will be the same. Thus, ordering by magnitude provides an upper bound on any other possible ordering of the sequence.

---

### Step 4: Bounding \( |z_i| \)

Given that $|z_i - z_j| > 1$ for all $i \neq j$, we can model the points as non-overlapping circles of radius $\frac{1}{2}$. The total area covered by $N$ such circles is:

$$
A_{\text{total}} = N \cdot \pi \left( \frac{1}{2} \right)^2 = \frac{N\pi}{4}.
$$

Assuming optimal packing, the radius \( r \) of the circle containing all $N$ points satisfies:

$$
\pi r^2 \geq \frac{N\pi}{4} \quad \Rightarrow \quad r \geq \frac{\sqrt{N}}{2}.
$$

Thus, the distance of the $(N+1)$th point from the origin must satisfy:

$$
|z_{N+1}| \geq \frac{\sqrt{N}}{2}.
$$

This provides a lower bound for the magnitude of each point as the number of points increases.

---

### Step 5: Rewriting the Series

Using this bound, we can now rewrite the sum:

$$
\sum_{i=1}^{\infty} \left| \frac{1}{z_i^3} \right| = \sum_{i=1}^{\infty} \frac{1}{|z_i|^3}.
$$

Applying the lower bound \( |z_i| \geq \frac{\sqrt{i}}{2} \) for all $i$, we get:

$$
\sum_{i=1}^{\infty} \frac{1}{|z_i|^3} \leq \sum_{i=1}^{\infty} \frac{1}{\left( \frac{\sqrt{i}}{2} \right)^3} = 8 \sum_{i=1}^{\infty} \frac{1}{i^{1.5}}.
$$

---

### Step 6: Convergence of the p-Series

The sum:

$$
\sum_{i=1}^{\infty} \frac{1}{i^{1.5}}
$$

is a **p-series** with \( p = 1.5 > 1 \), which is known to converge. Therefore, the series \( \sum_{i=1}^{\infty} \frac{1}{|z_i|^3} \) also converges, proving that:

$$
\sum_{i=1}^{\infty} \frac{1}{z_i^3}
$$

converges **absolutely**, and hence, the original series converges.

---

### Conclusion:

Here were the main insights used in this proof

1. Thinking about the distance constraint as adding balls of certain area, and thinking about the sums of those areas
2. Reorganizing the sequence to upper bound sequences of any other order
3. Manipulations on absolute values with complex numbers


### Citations:
- **[Big Idea: Convergence](../../BigIdeas/Convergence.md)**  
  Brief explanation of how this theorem was used in the solution.
