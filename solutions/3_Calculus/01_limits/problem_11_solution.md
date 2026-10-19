# Problem 11: An n-th Root

## 1. Original Problem
Compute
$$\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.$$
Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

## 2. What We Are Trying to Find
We must evaluate the limit of the sequence $a_n = \sqrt[n]{5^n + 2^n} = (5^n + 2^n)^{1/n}$ as $n \to \infty$. We need to identify which exponential base dominates, execute the algebraic simplification, and explain why handling exponential bases under an $n$-th root differs structurally from evaluating quotients of polynomials.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Dominance in Exponential Bases**:
  For positive bases $a > b > 0$, the exponential $a^n$ grows incomparably faster than $b^n$:
  $$\lim_{n \to \infty} \left(\frac{b}{a}\right)^n = 0.$$
  Here, $5 > 2$, so $5^n$ dominates $2^n$.
- **Factoring the Dominant Base from an $n$-th Root**:
  $$\sqrt[n]{a^n \cdot X} = a \sqrt[n]{X} = a X^{1/n}.$$
- **Squeeze Theorem for $n$-th Roots**:
  For any positive constant $c > 0$:
  $$\lim_{n \to \infty} c^{1/n} = \lim_{n \to \infty} \sqrt[n]{c} = 1.$$
  If $L \le a_n \le U_n$ and both bounds converge to $L$, then $a_n \to L$.

## 4. Step-by-Step Solution

### Step 1: Identify the dominant term
Between $5^n$ and $2^n$, the base $5$ is strictly larger than $2$.
As $n$ grows, $\frac{2^n}{5^n} = \left(\frac{2}{5}\right)^n \to 0$.
Therefore, $5^n$ is the dominant term.

### Step 2: Factor $5^n$ out of the sum inside the radical
$$5^n + 2^n = 5^n \left(1 + \frac{2^n}{5^n}\right) = 5^n \left(1 + \left(\frac{2}{5}\right)^n\right).$$

### Step 3: Extract $5^n$ from under the $n$-th root
Using the radical property $\sqrt[n]{u \cdot v} = \sqrt[n]{u} \cdot \sqrt[n]{v}$:
$$\sqrt[n]{5^n + 2^n} = \sqrt[n]{5^n \left(1 + \left(\frac{2}{5}\right)^n\right)} = \sqrt[n]{5^n} \cdot \sqrt[n]{1 + \left(\frac{2}{5}\right)^n}.$$
Since $5 > 0$, $\sqrt[n]{5^n} = 5$. Thus:
$$a_n = 5 \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n}.$$

### Step 4: Evaluate the limit using the Squeeze Theorem
We can bound the inner term for all $n \ge 1$:
$$1 < 1 + \left(\frac{2}{5}\right)^n \le 1 + \frac{2}{5} = \frac{7}{5} < 2.$$
Taking the $n$-th root preserves inequalities:
$$1^{1/n} < \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n} \le 2^{1/n}.$$
Multiplying through by $5$:
$$5 < \sqrt[n]{5^n + 2^n} \le 5 \cdot 2^{1/n}.$$

Now evaluate the bounding limits as $n \to \infty$:
- Lower bound: $\lim_{n \to \infty} 5 = 5$.
- Upper bound: $\lim_{n \to \infty} 5 \cdot 2^{1/n} = 5 \cdot 2^0 = 5 \cdot 1 = 5$.

By the Squeeze Theorem:
$$\lim_{n\to\infty}\sqrt[n]{5^n+2^n} = 5.$$

---

### Step 5: Why the transformation looks different from polynomial quotients
1. **Nature of dominance**:
   - In a quotient of polynomials $\frac{P(n)}{Q(n)}$, the variable $n$ is in the **base** ($n^2, n^3$), and degrees are compared by subtraction ($n^3/n^2 = n$).
   - In $\sqrt[n]{5^n+2^n}$, the variable $n$ is in the **exponent** ($5^n, 2^n$). The ratio $\left(\frac{2}{5}\right)^n$ converges to zero exponentially, much faster than any power of $1/n$.
2. **Action of the outer operator**:
   - In polynomial quotients, factoring $n^k$ cancels out via division: $\frac{n^k}{n^k} = 1$.
   - Here, the expression is enclosed by an $n$-th root (power $1/n$). Factoring $5^n$ requires applying the identity $(5^n)^{1/n} = 5$, pulling a constant $5$ completely outside the radical, while the remaining bracket has base approaching $1$ and exponent approaching $0$ ($1^0 = 1$).

## 5. Why Each Step Is Valid
1. **Factoring $5^n$**: True by the distributive property of real numbers.
2. **Power of product**: $(u \cdot v)^{1/n} = u^{1/n} \cdot v^{1/n}$ for all positive real numbers $u, v$.
3. **Limit of $c^{1/n}$**: For any positive constant $c > 0$, $\ln(c^{1/n}) = \frac{\ln c}{n} \to 0$, so $c^{1/n} = e^{(\ln c)/n} \to e^0 = 1$.
4. **Squeeze theorem**: Since the sequence is trapped between two sequences that both converge to $5$, its limit must be $5$.

## 6. Final Answer in Words
The limit of $\sqrt[n]{5^n+2^n}$ as $n \to \infty$ is $5$. The term $5^n$ completely dominates $2^n$ because $(2/5)^n$ vanishes to zero. The transformation differs from polynomial quotients because instead of canceling powers via algebraic fraction division, we extract $5^n$ through the $n$-th root as $(5^n)^{1/n} = 5$, leaving a residual term whose $n$-th root tends to $1$.

## 7. Quick Verification
Calculate numerical values for several integers $n$:
- For $n = 1$: $\sqrt[1]{5^1 + 2^1} = 7$.
- For $n = 2$: $\sqrt{25 + 4} = \sqrt{29} \approx 5.385$.
- For $n = 5$: $\sqrt[5]{3125 + 32} = \sqrt[5]{3157} \approx 5.010198$.
- For $n = 10$: $\sqrt[10]{5^{10} + 2^{10}} = \sqrt[10]{9765625 + 1024} \approx 5.000052426$.
The sequence rapidly approaches $5$ from above.

## 8. Common Mistakes
- **Distributing the $n$-th root over addition**: Writing $\sqrt[n]{5^n+2^n} = \sqrt[n]{5^n} + \sqrt[n]{2^n} = 5 + 2 = 7$. Radicals do not distribute over addition!
- **Thinking the limit is $\infty$**: Seeing $5^n \to \infty$ and assuming the $n$-th root cannot tame the exponential growth.
- **Forgetting why $(1+(2/5)^n)^{1/n} \to 1$**: Overlooking that $(1+0)^0 = 1^0 = 1$.

## 9. Short In-Class Explanation (3 Sentences)
Because $5$ is larger than $2$, the term $5^n$ grows exponentially faster and completely dominates the sum inside the radical. Factoring out $5^n$ allows us to extract it from the $n$-th root as $(5^n)^{1/n} = 5$. The remaining factor $(1+(2/5)^n)^{1/n}$ approaches $1^0 = 1$, giving the final limit of $5$.
