# Problem 05: The Classical Limit Leading to the Number $e$

## 1. Original Problem
Compute
$$\lim_{n\to\infty}\left(1+\frac1n\right)^n.$$
Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

## 2. What We Are Trying to Find
We must:
1. State the exact definition and analytical value of the fundamental limit $\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n$.
2. Calculate numerical values of the sequence $e_n = \left(1+\frac{1}{n}\right)^n$ for several increasing values of $n$.
3. Compare the numerical trend with the mathematical constant $e \approx 2.7182818\dots$.
4. Provide a sound epistemological explanation for why evaluating a finite collection of terms does not constitute a valid mathematical proof of convergence.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Definition of Euler's Number $e$**:
  The mathematical constant $e$ is formally defined as:
  $$e = \lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n \approx 2.718281828459\dots$$
- **Monotone Convergence Theorem**:
  Every sequence of real numbers that is both monotonically increasing and bounded above converges to a finite limit.
  For $e_n = \left(1+\frac{1}{n}\right)^n$:
  - $e_n < e_{n+1}$ for all $n \ge 1$ (strictly increasing).
  - $e_n < 3$ for all $n \ge 1$ (bounded above).
  Therefore, the limit exists by theorem.
- **Binomial Expansion of $e_n$**:
  $$\left(1+\frac{1}{n}\right)^n = \sum_{k=0}^n \binom{n}{k}\frac{1}{n^k} = 1 + 1 + \frac{1}{2!}\left(1-\frac{1}{n}\right) + \frac{1}{3!}\left(1-\frac{1}{n}\right)\left(1-\frac{2}{n}\right) + \dots$$

## 4. Step-by-Step Solution

### Step 1: Compute numerical values for increasing $n$
Let $e_n = \left(1 + \frac{1}{n}\right)^n$:
- For $n = 1$:
  $$e_1 = \left(1 + \frac{1}{1}\right)^1 = 2^1 = 2.000000$$
- For $n = 2$:
  $$e_2 = \left(1 + \frac{1}{2}\right)^2 = (1.5)^2 = 2.250000$$
- For $n = 5$:
  $$e_5 = \left(1 + \frac{1}{5}\right)^5 = (1.2)^5 = 2.488320$$
- For $n = 10$:
  $$e_{10} = \left(1 + \frac{1}{10}\right)^{10} = (1.1)^{10} \approx 2.593742$$
- For $n = 100$:
  $$e_{100} = \left(1 + \frac{1}{100}\right)^{100} = (1.01)^{100} \approx 2.704814$$
- For $n = 1{,}000$:
  $$e_{1000} = \left(1 + \frac{1}{1000}\right)^{1000} = (1.001)^{1000} \approx 2.716924$$
- For $n = 10{,}000$:
  $$e_{10000} = \left(1 + \frac{1}{10000}\right)^{10000} \approx 2.718146$$

### Step 2: Compare observed behavior with the limit value
- The values are strictly increasing:
  $$2.0 < 2.25 < 2.488 < 2.594 < 2.705 < 2.717 < 2.718.$$
- The growth progressively slows down: the jump from $n=1$ to $n=2$ is $+0.25$, whereas from $n=100$ to $n=1000$ it is only $+0.012$.
- The values approach the transcendental constant $e = 2.718281828\dots$ from below.

### Step 3: Analytical justification of convergence
Using the binomial expansion:
$$e_n = 1 + 1 + \frac{1}{2!}\left(1 - \frac{1}{n}\right) + \frac{1}{3!}\left(1 - \frac{1}{n}\right)\left(1 - \frac{2}{n}\right) + \dots + \frac{1}{n!}\left(1-\frac{1}{n}\right)\dots\left(1-\frac{n-1}{n}\right).$$
1. As $n$ increases to $n+1$, every existing factor $\left(1 - \frac{k}{n}\right)$ increases because $\frac{k}{n+1} < \frac{k}{n}$, and a new positive term is added to the sum. Thus, $e_n < e_{n+1}$ (monotonicity).
2. Since each bracket is strictly less than $1$:
   $$e_n < 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \dots + \frac{1}{n!} < 1 + 1 + \frac{1}{2} + \frac{1}{4} + \dots + \frac{1}{2^{n-1}} < 1 + 2 = 3.$$
3. Because $e_n$ is strictly increasing and bounded above by $3$, the Monotone Convergence Theorem guarantees that the limit exists. By definition, this limit is $e$.

### Step 4: Why a few values do not constitute a proof
1. **Finite samples cannot speak for infinity**: Calculating values for $n = 1, 2, 10, 1000$ only tests four points out of infinitely many integers. A sequence could easily appear to approach a limit initially, only to oscillate wildly or diverge for $n > 10^9$.
   - *Example*: The sequence $a_n = \left(1 + \frac{1}{n}\right)^n + \sin(n \pi / 1000)$ behaves almost identically to $e_n$ for small $n$, but oscillates forever.
2. **Numerical approximations hide exact targets**: From numerical terms alone, one cannot determine whether the limit is a rational number like $2.718$ or an irrational number like $e$.
3. **Observation versus deductive necessity**: Mathematics demands deductive certainty that holds for *all* $n$ beyond any threshold $\epsilon > 0$. A finite table provides intuition, but only a rigorous theorem (such as the Monotone Convergence Theorem or an $\epsilon$-$N$ proof) establishes the existence of the limit.

## 5. Why Each Step Is Valid
1. **Binomial theorem**: True for any real $a, b$ and integer $n$: $(a+b)^n = \sum \binom{n}{k}a^{n-k}b^k$.
2. **Comparison with geometric series**: The factorial satisfies $k! \ge 2^{k-1}$ for all $k \ge 1$, allowing the upper bound to be controlled by a convergent geometric progression summing to $3$.
3. **Monotone convergence**: The completeness axiom of the real numbers guarantees that any non-empty set bounded above possesses a least upper bound (supremum), which serves as the limit of an increasing bounded sequence.

## 6. Final Answer in Words
The limit is Euler's number $e \approx 2.71828$. Numerical calculations show the sequence strictly increasing from $2.0$ toward $2.718$, but evaluating finite terms is not a proof because numerical samples cannot guarantee behavior for all infinitely many indices or distinguish an exact irrational limit from a nearby rational approximation. A formal proof requires showing that the sequence is strictly increasing and bounded above.

## 7. Quick Verification
- Difference from $e$:
  - $|e - e_{10}| = |2.71828 - 2.59374| = 0.1245$.
  - $|e - e_{100}| = |2.71828 - 2.70481| = 0.0135$.
  - $|e - e_{1000}| = |2.71828 - 2.71692| = 0.00136$.
The error shrinks proportionally to $\frac{e}{2n}$, confirming steady convergence.

## 8. Common Mistakes
- **Applying power rules incorrectly**: Concluding that because $1 + 1/n \to 1$, $1^n = 1$, so the limit is $1$. The base approaches $1$ while the exponent approaches $\infty$, forming the indeterminate form $1^\infty$.
- **Believing $e$ is equal to $2.718$**: Treating $e$ as a terminating decimal rather than an irrational, transcendental number.
- **Thinking computer calculations prove a limit**: Forgetting that floating-point arithmetic has rounding errors and can never inspect infinitely many terms.

## 9. Short In-Class Explanation (3 Sentences)
The sequence $(1+1/n)^n$ defines the fundamental mathematical constant $e$, which is approximately $2.71828$. Computing values for increasing $n$ shows the terms steadily growing and leveling off, giving strong intuition that a limit exists. However, a table of numbers is not a proof; rigorous mathematical certainty requires proving the sequence is monotonic and bounded using the Monotone Convergence Theorem.
