# Problem 06: From a Sequence to a Function — Limit at Infinity

## 1. Original Problem
Compute
$$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.$$
Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

## 2. What We Are Trying to Find
We must:
1. Compute the limit of the rational function $f(x) = \frac{3x^2-x+1}{5x^2+4x-2}$ as the continuous real variable $x$ tends to positive infinity ($x \to \infty$).
2. Compare the algebraic steps with Exercise 1 (which used a discrete integer sequence $a_n$).
3. Explain mathematically what changes when transitioning from a discrete sequence index $n \in \mathbb{N}$ to a continuous variable $x \in \mathbb{R}$, and what fundamental principles remain invariant.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Factoring the Highest Power for Continuous Functions**:
  Just like sequences, as $x \to \infty$, polynomials are dominated by their highest-degree terms. Factoring $x^2$ normalizes the expression:
  $$\lim_{x \to \infty} \frac{1}{x^p} = 0 \quad (\text{for any } p > 0).$$
- **Heine's Definition of Function Limits**:
  A function limit $\lim_{x \to \infty} f(x) = L$ holds if and only if for *every* sequence of real numbers $(x_n)$ such that $x_n \to \infty$, the sequence of function values satisfies $\lim_{n \to \infty} f(x_n) = L$.

## 4. Step-by-Step Solution

### Step 1: Identify the leading power
Both the numerator $P(x) = 3x^2 - x + 1$ and denominator $Q(x) = 5x^2 + 4x - 2$ are quadratic polynomials of degree $2$. The highest power is $x^2$.

### Step 2: Factor out $x^2$ from numerator and denominator
For $x > 0$:
$$P(x) = x^2 \left(3 - \frac{x}{x^2} + \frac{1}{x^2}\right) = x^2 \left(3 - \frac{1}{x} + \frac{1}{x^2}\right),$$
$$Q(x) = x^2 \left(5 + \frac{4x}{x^2} - \frac{2}{x^2}\right) = x^2 \left(5 + \frac{4}{x} - \frac{2}{x^2}\right).$$

### Step 3: Cancel the common factor $x^2$
Since $x \to \infty$, we are considering large $x > 0$, so $x^2 \neq 0$:
$$\frac{3x^2 - x + 1}{5x^2 + 4x - 2} = \frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}}.$$

### Step 4: Evaluate the limit of each rational term as $x \to \infty$
As the real variable $x$ increases without bound:
- $\lim_{x \to \infty} \frac{1}{x} = 0$
- $\lim_{x \to \infty} \frac{1}{x^2} = 0$
- $\lim_{x \to \infty} \frac{4}{x} = 0$
- $\lim_{x \to \infty} \frac{2}{x^2} = 0$

### Step 5: Compute the limit of the quotient
Using the limit quotient law:
$$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2} = \frac{\lim_{x\to\infty}\left(3 - \frac{1}{x} + \frac{1}{x^2}\right)}{\lim_{x\to\infty}\left(5 + \frac{4}{x} - \frac{2}{x^2}\right)} = \frac{3 - 0 + 0}{5 + 0 - 0} = \frac{3}{5}.$$

---

### Step 6: Comparison — What Stays the Same vs. What Changes

#### What Stays the Same:
1. **Algebraic mechanism**: Factoring the dominant power of the variable ($x^2$ or $n^2$) remains the exact same algebraic technique.
2. **Dominance principle**: Terms with lower powers become infinitesimally small compared to the highest power and vanish in the limit.
3. **Limit value**: The final result is simply the ratio of the leading coefficients $\frac{a_2}{b_2} = \frac{3}{5}$.

#### What Changes:
1. **Domain of the argument**:
   - In Exercise 1, the variable $n$ is an integer restricted to the discrete set of natural numbers $\mathbb{N} = \{1, 2, 3, \dots\}$. It approaches infinity by taking discrete steps of size $+1$.
   - In Exercise 6, the variable $x$ is a continuous real number moving through $\mathbb{R}$. It passes continuously through all rational and irrational values ($x = \pi, \sqrt{17}, 100.456, \dots$).
2. **Topological requirement**:
   - For a sequence, convergence requires that terms $a_n$ enter any interval $(L - \epsilon, L + \epsilon)$ for all integer indices $n > N$.
   - For a function, $f(x)$ must enter and remain within the interval for *all* real numbers $x > M$. Heine's theorem proves that the continuous limit implies the sequence limit for any chosen sequence $x_n \to \infty$.

## 5. Why Each Step Is Valid
1. **Factoring $x^2$**: Valid for all $x \neq 0$ by the distributive property of real numbers.
2. **Reciprocal limit for real variables**: By the Archimedean property, for any $\epsilon > 0$, choosing $M = 1/\epsilon$ ensures that for all real $x > M$, $|1/x| < \epsilon$, proving $\lim_{x \to \infty} 1/x = 0$.
3. **Quotient rule**: The limit of the denominator is $5 \neq 0$, making the quotient rule applicable.

## 6. Final Answer in Words
The limit of the function as $x$ approaches infinity is $\frac{3}{5}$. The calculation method is algebraically identical to the sequence case because factoring the dominant term $x^2$ eliminates lower-order terms; the only difference is that $x$ varies continuously over all real numbers rather than taking discrete integer steps.

## 7. Quick Verification
- At $x = 100$:
  $$f(100) = \frac{3(10000) - 100 + 1}{5(10000) + 400 - 2} = \frac{29901}{50398} \approx 0.5933.$$
- At $x = 10{,}000$:
  $$f(10000) = \frac{3(10^8) - 10^4 + 1}{5(10^8) + 4(10^4) - 2} \approx \frac{299990001}{500039998} \approx 0.599932.$$
The values rapidly converge to $\frac{3}{5} = 0.6$.

## 8. Common Mistakes
- **Confusing discrete and continuous limits**: Believing that continuous limits require different algebraic identities, leading students to avoid standard factoring.
- **Forgetting that $x$ can take non-integer values**: Assuming that functions only exist at integer values like sequences.
- **Applying l'Hôpital's rule unnecessarily**: While l'Hôpital's rule is applicable, factoring $x^2$ is more fundamental, faster, and establishes the growth hierarchy directly.

## 9. Short In-Class Explanation (3 Sentences)
To find the limit of a rational function as $x \to \infty$, we factor out $x^2$ from the numerator and denominator, exactly as we did with $n^2$ for sequences. As $x$ grows without bound through the real numbers, all terms with $x$ in the denominator approach zero. This isolates the ratio of the leading coefficients, giving $\frac{3}{5}$.
