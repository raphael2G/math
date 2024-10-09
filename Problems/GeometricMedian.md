# Problem: Geometric Median

Let $P_1, P_2, \dots, P_n$ be points on a line, not necessarily distinct. Which point(s) $P$ on the line minimize the sum of distances $\sum_{i=1}^{n} |P - P_i|$?

---

### Solution Overview:

This function is inherently a minimization problem. Therefore, let's create some function which we want to minimize. 

$$
f(P) = \sum_{i=1}^{n} |P - P_i|
$$

As with all minimizations probelms, let's look for critical points. 

$$
f(P) = \sum_{i=1}^{k} P-P_i + \sum_{i=k+1}^{n} P_i - P
$$

where $k$ is the number of points to the left of P. 

Notice then that 

$$f'(P) = k - (n-k)$$

It is now clear that the critical points of $f$ will be when there are an equal number of points on the left and right of $P$. 

Therefore, when $n$ is odd, there is a single point at which $f$ is minimized, but when $n$ is even, any point in between the $k$th and $k+1$th point for $n = 2k$ will minimize $f$. 

Notice that this is because $f$ is convex we can rewrite $f$ in terms of the number of points on the left of $P$, so $$f'(k) = k - (n - k) = 2k - n$$

meaning $$f''(k) = 2 > 0$$ 




### Conclusion:

The point $P$ that minimizes the sum of distances $\sum_{i=1}^{n} |P - P_i|$ is the **median** of the points $P_1, P_2, \dots, P_n$. If $n$ is odd, this is the middle point. If $n$ is even, any point between the two middle points minimizes the sum.

### Key Insight:

The sum of absolute differences is minimized when the number of points to the left and right of $P$ is equal, which occurs at the median.

