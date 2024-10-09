# Theorem: Monotonicity of Functions

**Statement:**  
A function $f(x)$ is said to be **monotonic** (increasing or decreasing) over a domain if its behavior is consistent in terms of growth (either always increasing or always decreasing). Specifically:

- **Monotonically increasing**: $f(x_1) \leq f(x_2)$ for all $x_1 < x_2$.
- **Monotonically decreasing**: $f(x_1) \geq f(x_2)$ for all $x_1 < x_2$.

Monotonicity can be determined using the **first derivative test**:  
- If $f'(x) \geq 0$ for all $x$ in an interval, then $f(x)$ is monotonically increasing on that interval.
- If $f'(x) \leq 0$ for all $x$ in an interval, then $f(x)$ is monotonically decreasing on that interval.

---

### Proof Strategy: Derivative Analysis

To determine the monotonicity of a function $f(x)$, we often use its first derivative $f'(x)$:

1. **Find $f'(x)$**:  
   Differentiate the function.

2. **Determine the sign of $f'(x)$**:  
   - If $f'(x) > 0$ for all $x$ in a certain interval, then $f(x)$ is strictly increasing on that interval.
   - If $f'(x) < 0$ for all $x$ in a certain interval, then $f(x)$ is strictly decreasing.

3. **Find critical points**:  
   Set $f'(x) = 0$ to find critical points, where the function may change behavior (e.g., from increasing to decreasing).

4. **Analyze behavior around critical points**:  
   Check the sign of $f'(x)$ before and after the critical points to determine where the function is increasing or decreasing.

---

### Example: Monotonicity of $f(x) = \frac{\log(x)}{x}$

Consider the function $f(x) = \frac{\log(x)}{x}$:

1. **Differentiate**:
   $$
   f'(x) = \frac{1 - \log(x)}{x^2}
   $$

2. **Find critical points**:  
   Set $f'(x) = 0$:
   $$
   1 - \log(x) = 0 \quad \Rightarrow \quad x = e
   $$

3. **Determine monotonicity**:  
   - For $x < e$, $f'(x) > 0$, so $f(x)$ is increasing.
   - For $x > e$, $f'(x) < 0$, so $f(x)$ is decreasing.

Thus, $f(x) = \frac{\log(x)}{x}$ is increasing for $x < e$ and decreasing for $x > e$.

---

### Applications:

1. **Inequality Proofs**:  
   - In inequality proofs, monotonicity helps compare values of a function at different points. For instance, if $f(x)$ is increasing and $x_1 < x_2$, then $f(x_1) \leq f(x_2)$, simplifying comparisons.

2. **Optimization**:  
   - Monotonicity is useful in optimization problems. If $f(x)$ is monotonically increasing on an interval, the minimum value occurs at the left endpoint, and the maximum occurs at the right endpoint.

3. **Limit Behavior**:  
   - If $f(x)$ is increasing, its limit as $x \to \infty$ or $x \to 0$ can often be predicted. For example, if $f(x)$ is strictly increasing, $\lim_{x \to \infty} f(x)$ will either approach a constant or tend toward infinity.

---

### General Insights for Monotonicity:

- **Concavity and Monotonicity**:  
   A function's concavity (second derivative) gives further insight into its growth. If $f''(x) > 0$, the function is concave up and, if also increasing, grows faster over time.

- **Logarithmic Functions**:  
   Functions involving logarithms, like $f(x) = \frac{\log(x)}{x}$, often exhibit interesting monotonic behavior because their growth rates slow down as $x$ increases.

- **Exponential and Power Functions**:  
   Monotonicity is especially useful when analyzing exponential functions like $a^b$ versus $b^a$ and functions involving powers or roots.

---

### Example Problem:

In the problem **[Exponential Inequality Comparison](./Problems/ExponentialInequality.md)**, we used the monotonicity of $f(x) = \frac{\log(x)}{x}$ to compare $a^b$ and $b^a$. By showing that $f(x)$ is decreasing for $x > e$, we concluded that $b^a > a^b$ for $n > 8$.

---

### Citations:
- **[Proof Strategy: Derivative Analysis](./ProofStrategies/DerivativeAnalysis.md)**  
  Used to determine the monotonicity of a function via its first derivative.
