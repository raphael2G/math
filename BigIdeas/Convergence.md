# Big Idea: Convergence

**Description:**  
Convergence (in my understanding) is about infinite series, sums, the existence of limits, and related. Below discusses interesting and fundamental ideas related to convergence. 

---

### Big Ideas:

1. **Telescoping**:  
   $$\sum^{\infin}_{i=1} (\frac{1}{i} - \frac{1}{i+1}) = [insert \ expansion \ here]$$

   However, notice the following is the sum of two divergent series
   $$\sum^{\infin}_{i=1} \frac{1}{i} - \sum^{\infin}_{i=1} \frac{1}{i+1}$$

   Let's think about what this is really saying. Go on for infinity adding this thing, and then go on for infinity subtracting this thing. It doesn't really make sense. 

   Further, let's take another example. 
   $$\sum^{\infin}_{i=1} (2^i - 2^{i+1}) = [insert \ expansion \ here]$$

   Can we just telescope this? 

   Notice that each term is going to be negative, and we are adding bigger and bigger negative things. How could we possible say this is 2 when we are only adding negative terms together

   This brings an interesting point. We can't (always) change the order of infinitie series, because then we are changing the series itself. 

   To investigate when we can, let's break down the definition of an infinite sum

   $$\sum^{\infin}_{i=1} (2^i - 2^{i+1}) = \lim _{n\rightarrow \infin} \sum_{i=1}^n(2^i - 2^{i+1})$$

   Notice we can find a closed form solution of this finite summation

   $$\sum^{\infin}_{i=1} (2^i - 2^{i+1}) = \lim _{n\rightarrow \infin} (2 - 2^{n+1}) \neq 2$$

   Notice, 
   



2. **Insight 2**:  
   [Continue explaining other important observations or strategies related to the big idea.]

3. **Insight 3**:  
   [Further explain the broader implications or connections this idea has to other areas of mathematics.]

---

### Applications:

- **Application 1**:  
  [Describe a situation where this big idea is applied. For example, explain how the concept is used in proofs, inequalities, or problem-solving strategies.]

- **Application 2**:  
  [Describe another example, preferably in a different domain or problem type.]

---

### Example Problem:

- **[Example Problem: Problem Name](./Problems/ExampleProblem.md)**  
  [Link to a problem where this big idea is used. Provide a brief description of how the big idea plays a central role in solving the problem.]

---

### Related Theorems or Proof Strategies:

- **[Theorem 1: Related Theorem](./Theorems/RelatedTheorem.md)**  
  [Mention any theorems that are connected to this big idea.]

- **[Proof Strategy: Relevant Strategy](./ProofStrategies/RelevantStrategy.md)**  
  [Mention any proof strategies commonly used alongside this big idea.]
