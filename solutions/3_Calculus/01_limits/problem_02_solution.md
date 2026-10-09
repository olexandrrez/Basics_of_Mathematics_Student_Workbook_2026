# Problem 02: Different Growth Rates

## 1. Original Problem
Compute
$$\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.$$
Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

## 2. What We Are Trying to Find
We must:
1. Compute the limit of the first sequence $a_n = \frac{3n+1}{n^2+4}$ as $n \to \infty$.
2. Compute the limit of the second sequence $b_n = \frac{2n^3-n}{5n^2+1}$ as $n \to \infty$.
3. Compare the growth rate of the numerator versus the denominator in both cases.
4. Formulate a general rule governing the limit of any rational sequence $\frac{P(n)}{Q(n)}$ based on the relationship between $\deg(P)$ and $\deg(Q)$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Degree Comparison Theorem for Rational Sequences**:
  Let $P(n) = a_k n^k + \dots$ and $Q(n) = b_m n^m + \dots$ be polynomials with $a_k \neq 0, b_m \neq 0$:
  - If $\deg(P) < \deg(Q)$ ($k < m$): the denominator grows strictly faster than the numerator, and $\lim_{n \to \infty} \frac{P(n)}{Q(n)} = 0$.
  - If $\deg(P) = \deg(Q)$ ($k = m$): numerator and denominator grow at the same rate, and $\lim_{n \to \infty} \frac{P(n)}{Q(n)} = \frac{a_k}{b_m}$.
  - If $\deg(P) > \deg(Q)$ ($k > m$): the numerator grows strictly faster than the denominator, and the sequence diverges to $\pm\infty$ (specifically, $\operatorname{sgn}(a_k/b_m) \cdot \infty$).

## 4. Step-by-Step Solution

### Part 1: Computing $\lim_{n\to\infty}\frac{3n+1}{n^2+4}$
1. **Identify degrees**: Numerator degree is $1$; denominator degree is $2$.
2. **Factor out highest power of denominator ($n^2$)**:
   $$\frac{3n + 1}{n^2 + 4} = \frac{n^2 \left(\frac{3}{n} + \frac{1}{n^2}\right)}{n^2 \left(1 + \frac{4}{n^2}\right)} = \frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}}.$$
3. **Take limits of individual terms**:
   - $\lim_{n \to \infty} \frac{3}{n} = 0$, $\lim_{n \to \infty} \frac{1}{n^2} = 0$.
   - $\lim_{n \to \infty} \left(1 + \frac{4}{n^2}\right) = 1 + 0 = 1$.
4. **Apply the quotient rule**:
   $$\lim_{n\to\infty}\frac{3n+1}{n^2+4} = \frac{0 + 0}{1 + 0} = \frac{0}{1} = 0.$$

---

### Part 2: Computing $\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}$
1. **Identify degrees**: Numerator degree is $3$; denominator degree is $2$.
2. **Factor out $n^2$ (highest power of denominator)**:
   $$\frac{2n^3 - n}{5n^2 + 1} = \frac{n^2 \left(2n - \frac{1}{n}\right)}{n^2 \left(5 + \frac{1}{n^2}\right)} = \frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}}.$$
3. **Analyze behavior as $n \to \infty$**:
   - The numerator is $2n - \frac{1}{n}$. Since $2n \to +\infty$ and $\frac{1}{n} \to 0$, the numerator tends to $+\infty$.
   - The denominator is $5 + \frac{1}{n^2} \to 5 + 0 = 5 > 0$.
4. **Conclude divergence to infinity**:
   $$\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1} = \frac{+\infty}{5} = +\infty.$$
   The sequence diverges to positive infinity (it has no finite limit).

---

### Part 3: General Observation on Polynomial Degrees
Comparing a rational sequence $\frac{P(n)}{Q(n)}$:
1. **Case $\deg(P) < \deg(Q)$**: The denominator grows by an order of magnitude faster than the numerator. After dividing by the highest power, the numerator approaches $0$ while the denominator approaches a non-zero constant, giving limit $0$.
2. **Case $\deg(P) > \deg(Q)$**: The numerator outpaces the denominator. After dividing by the highest power of the denominator, an uncancelled positive power of $n$ remains in the numerator, causing the ratio to diverge to $+\infty$ or $-\infty$.
3. **Case $\deg(P) = \deg(Q)$**: The growth rates are perfectly balanced; the powers of $n$ cancel completely, leaving the ratio of the leading coefficients $\frac{a_{\text{lead}}}{b_{\text{lead}}}$.

## 5. Why Each Step Is Valid
1. **Factoring $n^2$**: Factoring the dominant denominator term normalizes the denominator to a non-zero finite limit ($1$ in Part 1, $5$ in Part 2).
2. **Arithmetic limit of $\frac{0}{c}$**: For any non-zero real number $c$, $\frac{0}{c} = 0$.
3. **Infinite limit rule**: If $u_n \to +\infty$ and $v_n \to c > 0$, then their quotient $\frac{u_n}{v_n}$ grows without bound toward $+\infty$.

## 6. Final Answer in Words
The first limit is $0$, and the second sequence diverges to $+\infty$. In general, for a quotient of polynomials, if the denominator has a higher degree, the limit is $0$; if the degrees are equal, the limit is the ratio of leading coefficients; and if the numerator has a higher degree, the sequence diverges to $\pm\infty$.

## 7. Quick Verification
- For $a_n = \frac{3n+1}{n^2+4}$: at $n = 100$, $a_{100} = \frac{301}{10004} \approx 0.0301$; at $n = 1000$, $a_{1000} = \frac{3001}{1000004} \approx 0.0030$. Values decrease toward $0$.
- For $b_n = \frac{2n^3-n}{5n^2+1}$: at $n = 100$, $b_{100} = \frac{1999900}{50001} \approx 39.997$; at $n = 1000$, $b_{1000} \approx 400$. Values grow linearly with $n$ toward $+\infty$.

## 8. Common Mistakes
- **Writing $\frac{\infty}{\infty} = 1$**: Assuming identical symbols mean identical values, ignoring the polynomial degrees.
- **Claiming the second limit does not exist without specifying $+\infty$**: While not converging to a real number, it is standard in calculus to specify that it diverges specifically to $+\infty$.
- **Factoring $n^3$ from the first fraction**: Overcomplicating algebra by factoring powers larger than either polynomial requires.

## 9. Short In-Class Explanation (3 Sentences)
In the first sequence, the denominator has degree $2$ while the numerator has degree $1$, so the denominator grows much faster and pulls the quotient to $0$. In the second sequence, the numerator has degree $3$ and the denominator degree $2$, which leaves a factor of $n$ in the numerator and causes the sequence to diverge to $+\infty$. In general, the limit of a rational sequence is determined solely by comparing the degrees of the numerator and denominator.
