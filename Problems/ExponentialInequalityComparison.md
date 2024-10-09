# Problem: Exponential Inequality Comparison

Given $n > 8$, let $a = \sqrt{n}$ and $b = \sqrt{n+1}$. Which is greater, $a^b$ or $b^a$?

---

### Solution Overview:

We are asked to compare $a^b$ and $b^a$, where $a = \sqrt{n}$ and $b = \sqrt{n+1}$. To solve this, we assume $a^b > b^a$ and then analyze the behavior of the logarithmic form.

---

### Step 1: Assume $a^b > b^a$

Start by assuming $a^b > b^a$. Taking the natural logarithm of both sides, we get:

$$
\log(a^b) > \log(b^a)
$$

Using the logarithmic rule $\log(x^y) = y \log(x)$, this simplifies to:

$$
b \log(a) > a \log(b)
$$

This can be rewritten as:

$$
\frac{\log(a)}{a} > \frac{\log(b)}{b}
$$

Note, this can only be done since we know both a and b are positive

### Step 2: Define the Function $f(x)$

Let’s define the function $f(x)$ as:

$$
f(x) = \frac{\log(x)}{x}
$$

We want to analyze the behavior of $f(x)$ to determine whether $\frac{\log(a)}{a} > \frac{\log(b)}{b}$.

### Step 3: Analyze the Derivative of $f(x)$

To understand how $f(x)$ behaves, we compute its derivative:

$$
f'(x) = \frac{1 - \log(x)}{x^2}
$$

For $f'(x)$ to be positive, we need:

$$
1 - \log(x) > 0 \quad \Rightarrow \quad \log(x) < 1 \quad \Rightarrow \quad x < e
$$

Since $a = \sqrt{n}$ and $b = \sqrt{n+1}$ with $n > 8$, both $a$ and $b$ are greater than $e$. This means $f'(x) < 0$ for $x > e$, implying that $f(x)$ is **monotonically decreasing** for $x > e$.

### Step 4: Compare $f(a)$ and $f(b)$

Since $f(x)$ is decreasing for $x > e$ and $b = \sqrt{n+1} > a = \sqrt{n}$, we know that:

$$
f(b) < f(a)
$$

Thus:

$$
\frac{\log(b)}{b} < \frac{\log(a)}{a}
$$

This contradicts our assumption that $a^b > b^a$. Therefore, $b^a > a^b$.

---

### Conclusion:

We conclude that:

$$
b^a > a^b
$$

In other words, $\sqrt{n+1}^{\sqrt{n}} > \sqrt{n}^{\sqrt{n+1}}$ for $n > 8$.

### Citations:
  
- **[Theorem: Monotonicity of $f(x) = \frac{\log(x)}{x}$](../Theorems/Monotonicity.md)**  
  The monotonicity of $f(x) = \frac{\log(x)}{x}$ was critical to completing the proof.
