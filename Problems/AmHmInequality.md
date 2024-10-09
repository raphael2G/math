# Problem: AM - HM Inequality

**Problem Statement:**  
Prove that for all positive real numbers $a$, $b$, and $c$, the following inequality holds:

$$
\frac{9}{a + b + c} \leq 2 \left( \frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a} \right)
$$

---

### Solution Overview:

1. **Intuition**:  
   The first thing to notice is the similarity between the two denominators. My first thought was to try and get them to look like eachother. However, this proves more difficult than first apepar because it is a sum, and not a product. 

2. **Realization**: 
    The big insight is noticing that the RHS is summing a bunhc of harmonics, which makes me think of the Harmonic Mean. Therefore, I wondier if this is a QM-AM-GM-HM inequality. 

$$?? \geq \frac{1}{\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a}}$$

The question is just what? 

We know we want to get a + b + c, and I realize that by adding up all of the denominators, you get two times this, so this makes me think of AM.

$$\frac{a + b + b + c + c + a}{3} \geq \frac{3}{\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a}}$$

$$\frac{2(a + b + c)}{3} \geq \frac{3}{\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a}}$$

$$\frac{2(a + b + c)}{3} \geq \frac{3}{\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a}}$$

$$2(\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a}) \geq \frac{9}{a + b + c}$$

$$\frac{9}{a + b + c} \leq 2(\frac{1}{a + b} + \frac{1}{b + c} + \frac{1}{c + a})$$

---

### Conclusion:

The big insight for this problem was idenitifying the sum of harmonics, which allows me to think of the AM - HM inequality. 

### Citations:
- **[Theorem: QM-AM-GM-HM](./Theorems/QM-AM-GM-HM.md)**  
  Useful inequality for common mathematical patterns


