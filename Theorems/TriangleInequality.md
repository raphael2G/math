## Theorem: Triangle Inequality

**Statement:**  
For any real numbers \( x \) and \( y \), the following holds:
\[
|x + y| \leq |x| + |y|
\]
This also extends to vectors in Euclidean space:  
For vectors \( \mathbf{u} \) and \( \mathbf{v} \) in \( \mathbb{R}^n \), the inequality holds:
$$\|\mathbf{u} + \mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|$$

**Proof Sketch:**  
- Consider the properties of the absolute value function and norms.  
- Apply the definition of the absolute value:
  \[
  |x + y|^2 = (x + y)^2 \quad \text{and expand:} \quad x^2 + 2xy + y^2
  \]
- Using the fact that \( 2xy \leq 2|x||y| \), it follows that:
  \[
  |x + y|^2 \leq (|x| + |y|)^2
  \]
- Taking square roots of both sides yields the desired result.

**Applications:**
- The Triangle Inequality is fundamental in proving bounds and is often used in distance-based arguments, such as in geometry, analysis, and functional spaces.
- Commonly used in problems involving sequences, limits, and inequalities.

**Extended Form (Generalized Triangle Inequality):**
For real numbers \( x_1, x_2, \dots, x_n \), we have:
\[
|x_1 + x_2 + \cdots + x_n| \leq |x_1| + |x_2| + \cdots + |x_n|
\]

**Example Problem:**
Prove that for any complex numbers \( z_1 \) and \( z_2 \), the following inequality holds:
\[
|z_1 + z_2| \leq |z_1| + |z_2|
\]

**Solution:**
- Recall that \( |z| = \sqrt{z \bar{z}} \).
- By applying the Triangle Inequality to the real and imaginary components of the complex numbers, the result follows directly from the standard form of the inequality.

**Tags:** Inequalities, Absolute Value, Euclidean Space, Vector Norms

