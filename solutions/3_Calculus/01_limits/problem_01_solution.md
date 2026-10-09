# Problem 01: Dominant Terms in a Sequence

## 1. Original Problem
Compute
$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.$$
Explain why the highest-degree terms determine the result.

## 2. What We Are Trying to Find
We are asked to evaluate the limit of the rational sequence $a_n = \frac{4n^2-3n+1}{2n^2+5n-7}$ as the integer index $n$ tends to infinity ($n \to \infty$), and to give a rigorous conceptual explanation for why only the leading terms ($4n^2$ and $2n^2$) dictate the limiting value.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Factoring the Highest Power**:
  For rational expressions as $n \to \infty$, factor out the highest power of $n$ present in both the numerator and denominator:
  $$\frac{P(n)}{Q(n)} = \frac{n^k \left(a_k + \frac{a_{k-1}}{n} + \dots\right)}{n^m \left(b_m + \frac{b_{m-1}}{n} + \dots\right)}.$$
- **Limit of Reciprocal Powers**:
  For any real power $p > 0$:
  $$\lim_{n \to \infty} \frac{1}{n^p} = 0.$$
- **Arithmetic Laws of Limits (Quotient and Sum Rule)**:
  If $\lim u_n = U$ and $\lim v_n = V$ with $V \neq 0$, then $\lim \frac{u_n}{v_n} = \frac{U}{V}$.

## 4. Step-by-Step Solution

### Step 1: Identify the highest degree
Both the numerator $P(n) = 4n^2 - 3n + 1$ and the denominator $Q(n) = 2n^2 + 5n - 7$ are quadratic polynomials of degree $2$. The highest power of $n$ is $n^2$.

### Step 2: Factor out $n^2$ from numerator and denominator
Factor $n^2$ from the numerator:
$$4n^2 - 3n + 1 = n^2 \left(4 - \frac{3n}{n^2} + \frac{1}{n^2}\right) = n^2 \left(4 - \frac{3}{n} + \frac{1}{n^2}\right).$$

Factor $n^2$ from the denominator:
$$2n^2 + 5n - 7 = n^2 \left(2 + \frac{5n}{n^2} - \frac{7}{n^2}\right) = n^2 \left(2 + \frac{5}{n} - \frac{7}{n^2}\right).$$

### Step 3: Cancel the common factor $n^2$
For all $n \ge 1$, $n \neq 0$, so we cancel $n^2$:
$$\frac{4n^2 - 3n + 1}{2n^2 + 5n - 7} = \frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}.$$

### Step 4: Evaluate the limit of each individual term
As $n \to \infty$:
- $\lim_{n \to \infty} \frac{3}{n} = 3 \cdot 0 = 0$
- $\lim_{n \to \infty} \frac{1}{n^2} = 0$
- $\lim_{n \to \infty} \frac{5}{n} = 5 \cdot 0 = 0$
- $\lim_{n \to \infty} \frac{7}{n^2} = 7 \cdot 0 = 0$

### Step 5: Apply limit laws to evaluate the quotient
$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{\lim_{n\to\infty}\left(4 - \frac{3}{n} + \frac{1}{n^2}\right)}{\lim_{n\to\infty}\left(2 + \frac{5}{n} - \frac{7}{n^2}\right)} = \frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2.$$

### Step 6: Explanation of why dominant terms determine the result
As $n$ grows exceedingly large (e.g., $n = 10^6$):
- $4n^2 = 4 \times 10^{12}$
- $3n = 3 \times 10^6$
- $1 = 1$

The term $4n^2$ is one million times larger than $3n$ and four trillion times larger than $1$. Relative to $n^2$, the terms $-3n$ and $+1$ become an infinitesimally small fraction of the total value. Formally, dividing by $n^2$ shows that $\frac{3n}{n^2} = \frac{3}{n} \to 0$ and $\frac{1}{n^2} \to 0$. Thus, lower-order terms vanish in the limit, leaving only the leading coefficients $\frac{4}{2} = 2$.

## 5. Why Each Step Is Valid
1. **Factoring $n^2$**: Distributive law of real numbers allows factoring any non-zero quantity from a sum.
2. **Canceling $n^2$**: Since $n$ approaches $+\infty$, $n > 0$, ensuring $n^2 \neq 0$; division by non-zero preserves expression value.
3. **Limit of reciprocal powers**: By the Archimedean property of real numbers, for any $\epsilon > 0$, there exists $N$ such that $1/n < \epsilon$ for all $n > N$.
4. **Quotient rule for limits**: Since the denominator's limit is $2 \neq 0$, the limit of the quotient equals the quotient of the limits.

## 6. Final Answer in Words
The limit of the sequence as $n$ approaches infinity is $2$. The highest-degree terms dominate because all lower-degree terms, when scaled relative to $n^2$, approach zero as $n$ grows without bound.

## 7. Quick Verification
Evaluate $a_n$ for large values of $n$:
- For $n = 10$: $a_{10} = \frac{4(100) - 30 + 1}{2(100) + 50 - 7} = \frac{371}{243} \approx 1.5267$.
- For $n = 100$: $a_{100} = \frac{40000 - 300 + 1}{20000 + 500 - 7} = \frac{39701}{20493} \approx 1.9373$.
- For $n = 1000$: $a_{1000} = \frac{4000000 - 3000 + 1}{2000000 + 5000 - 7} = \frac{3997001}{2004993} \approx 1.9935$.
The sequence values approach $2$ as $n$ increases.

## 8. Common Mistakes
- **Evaluating as $\frac{\infty}{\infty}$ and declaring the limit undefined**: The symbol $\frac{\infty}{\infty}$ is an indeterminate form, meaning algebraic manipulation is required, not that the limit does not exist.
- **Dropping lower-degree terms without factoring**: Writing $\frac{4n^2-3n+1}{2n^2+5n-7} = \frac{4n^2}{2n^2}$ directly as an equality, which is algebraically false for finite $n$. One must factor out $n^2$ and evaluate limits.
- **Incorrectly dividing terms**: Writing $\frac{3n}{n^2} = 3n$ instead of $\frac{3}{n}$.

## 9. Short In-Class Explanation (3 Sentences)
To evaluate the limit of this rational sequence, we factor out the highest power of $n$, which is $n^2$, from both the numerator and denominator. When we cancel $n^2$, all lower-order terms become fractions with $n$ in the denominator, which vanish to zero as $n$ goes to infinity. This leaves only the ratio of the leading coefficients, yielding $\frac{4}{2} = 2$.
