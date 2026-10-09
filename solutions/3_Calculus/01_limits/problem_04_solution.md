# Problem 04: Powers and Oscillation

## 1. Original Problem
Analyze
$$\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.$$
For each sequence, describe the type of behavior and justify your answer.

## 2. What We Are Trying to Find
We must determine the convergence or divergence of four fundamental sequences:
1. $a_n = \left(\frac{2}{3}\right)^n$
2. $b_n = \left(\frac{3}{2}\right)^n$
3. $c_n = (-1)^n$
4. $d_n = \frac{(-1)^n}{n}$

For each sequence, we must identify whether it converges, diverges to infinity, or oscillates, and justify each conclusion using convergence theorems.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Geometric Sequence Theorem**:
  For the sequence $q^n$ where $q \in \mathbb{R}$:
  - If $|q| < 1$, then $\lim_{n \to \infty} q^n = 0$ (converges to $0$).
  - If $q = 1$, then $\lim_{n \to \infty} q^n = 1$ (constant, converges to $1$).
  - If $q > 1$, then $\lim_{n \to \infty} q^n = +\infty$ (diverges to $+\infty$).
  - If $q \le -1$, then $q^n$ diverges by oscillation (no limit).
- **Squeeze Theorem (Sandwich Theorem)**:
  If $|a_n| \le b_n$ for all $n$ and $\lim_{n \to \infty} b_n = 0$, then $\lim_{n \to \infty} a_n = 0$.

## 4. Step-by-Step Solution

### Sequence 1: $a_n = \left(\frac{2}{3}\right)^n$
- **Base analysis**: Here $q = \frac{2}{3}$.
- Notice that $|q| = \frac{2}{3} < 1$.
- Each successive term is obtained by multiplying the previous term by $\frac{2}{3} < 1$, making the terms strictly positive, strictly decreasing, and bounded below by $0$:
  $$a_1 = \frac{2}{3} \approx 0.667, \quad a_2 = \frac{4}{9} \approx 0.444, \quad a_3 = \frac{8}{27} \approx 0.296, \dots$$
- By the Geometric Sequence Theorem with $|q| < 1$:
  $$\lim_{n \to \infty} \left(\frac{2}{3}\right)^n = 0.$$
- **Behavior**: **Converges monotonically to $0$**.

---

### Sequence 2: $b_n = \left(\frac{3}{2}\right)^n$
- **Base analysis**: Here $q = \frac{3}{2} = 1.5 > 1$.
- Each term is $1.5$ times the preceding term, so the sequence is strictly increasing:
  $$b_1 = 1.5, \quad b_2 = 2.25, \quad b_3 = 3.375, \quad b_4 \approx 5.06, \dots$$
- Using Bernoulli's Inequality: $\left(1 + 0.5\right)^n \ge 1 + 0.5n$. As $n \to \infty$, $1 + 0.5n \to \infty$.
- **Behavior**: **Diverges to $+\infty$** (unbounded growth).

---

### Sequence 3: $c_n = (-1)^n$
- **Term evaluation**:
  $$c_1 = -1, \quad c_2 = +1, \quad c_3 = -1, \quad c_4 = +1, \dots$$
- The sequence alternates indefinitely between $-1$ (for odd $n$) and $+1$ (for even $n$).
- Consider two subsequences:
  - Even subsequence: $c_{2k} = (-1)^{2k} = 1 \implies \lim_{k \to \infty} c_{2k} = 1$.
  - Odd subsequence: $c_{2k-1} = (-1)^{2k-1} = -1 \implies \lim_{k \to \infty} c_{2k-1} = -1$.
- Since the two subsequences have distinct limits ($1 \neq -1$), the full sequence cannot converge to any single number.
- Furthermore, its terms are bounded ($|c_n| = 1$), so it does not diverge to $\pm \infty$.
- **Behavior**: **Diverges by finite oscillation** (no limit exists).

---

### Sequence 4: $d_n = \frac{(-1)^n}{n}$
- **Term evaluation**:
  $$d_1 = -1, \quad d_2 = \frac{1}{2} = 0.5, \quad d_3 = -\frac{1}{3} \approx -0.333, \quad d_4 = \frac{1}{4} = 0.25, \dots$$
- The sign of $d_n$ alternates with each step, but the absolute magnitude $|d_n|$ shrinks:
  $$|d_n| = \left|\frac{(-1)^n}{n}\right| = \frac{1}{n}.$$
- We apply the Squeeze Theorem:
  $$-\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}.$$
- Since $\lim_{n \to \infty} \left(-\frac{1}{n}\right) = 0$ and $\lim_{n \to \infty} \frac{1}{n} = 0$, both bounding sequences converge to $0$.
- **Behavior**: **Converges to $0$ with damped oscillation**.

## 5. Why Each Step Is Valid
1. **Geometric limit rule**: For $|q| < 1$, the terms become arbitrarily small because $(1/|q|)^n > 1 + n(1/|q| - 1)$ by Bernoulli's inequality, forcing $q^n \to 0$.
2. **Subsequence theorem**: A sequence converges if and only if all its subsequences converge to the same limit. Distinct limits for odd and even indices disprove convergence.
3. **Squeeze theorem**: If a sequence is trapped between two bounds that share the same limit, it must converge to that exact same limit, regardless of any alternating sign.

## 6. Final Answer in Words
1. $\left(\frac{2}{3}\right)^n$ converges monotonically to $0$ because the common ratio has absolute value strictly less than $1$.
2. $\left(\frac{3}{2}\right)^n$ diverges to $+\infty$ because the common ratio exceeds $1$.
3. $(-1)^n$ diverges by oscillation because its terms alternate between $-1$ and $+1$ without settling on a single value.
4. $\frac{(-1)^n}{n}$ converges to $0$ by the Squeeze Theorem; although its signs oscillate, its amplitude $\frac{1}{n}$ decreases to zero.

## 7. Quick Verification
- For $a_n$: $\left(\frac{2}{3}\right)^{10} \approx 0.0173 \to 0$.
- For $b_n$: $\left(\frac{3}{2}\right)^{10} \approx 57.665 \to \infty$.
- For $c_n$: $c_{99} = -1$, $c_{100} = +1$ (never converges).
- For $d_n$: $d_{100} = 0.01$, $d_{101} = -0.0099$ (trapped within $[-0.01, 0.01]$ of $0$).

## 8. Common Mistakes
- **Assuming any oscillating sequence diverges**: Concluding that $\frac{(-1)^n}{n}$ does not converge simply because $(-1)^n$ oscillates. Oscillation of sign does not prevent convergence if the amplitude tends to zero.
- **Confusing $\frac{2}{3}$ and $\frac{3}{2}$**: Mixing up which fraction is greater than or less than $1$.
- **Claiming $(-1)^n$ diverges to infinity**: It is bounded between $-1$ and $1$, so it never tends to $\infty$; it diverges purely due to oscillation.

## 9. Short In-Class Explanation (3 Sentences)
A geometric sequence converges to zero if its base has magnitude less than one, like $(2/3)^n$, and diverges to infinity if its base is greater than one, like $(3/2)^n$. The sequence $(-1)^n$ diverges because it endlessly bounces between two different values, never settling on a single limit. In contrast, $(-1)^n/n$ converges to zero because the shrinking denominator $n$ squeezes the oscillating terms to zero.
