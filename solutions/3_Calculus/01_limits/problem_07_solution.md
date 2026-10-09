# Problem 07: Limit at a Point and Canceling a Factor

## 1. Original Problem
Compute
$$\lim_{x\to3}\frac{x^2-4x+3}{x-3}.$$
Explain why the value of the function at $x=3$ is not needed to compute the limit.

## 2. What We Are Trying to Find
We must:
1. Evaluate the limit of the rational function $f(x) = \frac{x^2-4x+3}{x-3}$ as $x$ approaches the specific point $c = 3$.
2. Resolve the apparent division by zero ($0/0$ indeterminate form) by factoring and canceling.
3. Provide a clear conceptual explanation of why the limit of a function as $x \to c$ is completely independent of the function's value (or lack thereof) at the point $x = c$ itself.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Definition of a Limit at a Point**:
  The statement $\lim_{x \to c} f(x) = L$ means that for every $\epsilon > 0$, there exists a $\delta > 0$ such that:
  $$\text{if } 0 < |x - c| < \delta, \quad \text{then } |f(x) - L| < \epsilon.$$
  Crucially, the condition $0 < |x - c|$ explicitly **excludes** $x = c$. The limit depends strictly on the values of $f(x)$ in a punctured neighborhood of $c$.
- **Cancellation in Punctured Neighborhoods**:
  If two functions $f(x)$ and $g(x)$ agree everywhere on a punctured neighborhood of $c$ ($f(x) = g(x)$ for all $x \neq c$), then:
  $$\lim_{x \to c} f(x) = \lim_{x \to c} g(x).$$

## 4. Step-by-Step Solution

### Step 1: Direct substitution check
Substitute $x = 3$ directly into the expression:
$$\text{Numerator: } 3^2 - 4(3) + 3 = 9 - 12 + 3 = 0,$$
$$\text{Denominator: } 3 - 3 = 0.$$
Direct substitution yields the indeterminate form $\frac{0}{0}$. The function $f(x)$ is not defined at $x = 3$ because division by zero is undefined.

### Step 2: Factor the numerator
The quadratic expression $x^2 - 4x + 3$ has roots satisfying $x_1 + x_2 = 4$ and $x_1 x_2 = 3$, which are $x = 1$ and $x = 3$.
Factor the quadratic:
$$x^2 - 4x + 3 = (x - 1)(x - 3).$$

### Step 3: Rewrite the function and simplify for $x \neq 3$
The function can be written as:
$$f(x) = \frac{(x - 1)(x - 3)}{x - 3}.$$
Since the definition of the limit as $x \to 3$ only considers $x \neq 3$, the factor $(x - 3)$ is non-zero.
Therefore, for all $x \neq 3$:
$$\frac{(x - 1)(x - 3)}{x - 3} = x - 1.$$

### Step 4: Evaluate the limit of the simplified continuous function
Now take the limit as $x \to 3$:
$$\lim_{x\to3}\frac{x^2-4x+3}{x-3} = \lim_{x\to3}(x - 1).$$
Since the linear function $g(x) = x - 1$ is continuous everywhere, we evaluate the limit by direct substitution:
$$\lim_{x\to3}(x - 1) = 3 - 1 = 2.$$

---

### Step 5: Why the value at $x = 3$ is not needed
A limit answers the question: *"What value does $f(x)$ get arbitrarily close to as $x$ gets arbitrarily close to $3$, without ever actually reaching $3$?"*
- In our formal definition, the condition $0 < |x - 3| < \delta$ explicitly rules out the point $x = 3$ itself.
- In fact, $f(3)$ does not exist at all (it is undefined). Yet the limit exists and equals $2$.
- Even if someone arbitrarily defined $f(3) = 100$ or left it undefined, the limit as $x \to 3$ would remain strictly $2$, because the limit depends solely on the surrounding neighborhood, not on the point itself.

## 5. Why Each Step Is Valid
1. **Factoring**: The polynomial identity $(x-1)(x-3) = x^2 - 4x + 3$ is true for all real $x$.
2. **Cancellation**: For any real number $u \neq 0$, $\frac{u}{u} = 1$. Since $x \neq 3$ throughout the limit evaluation, $x - 3 \neq 0$, making division legal.
3. **Continuity of polynomials**: The polynomial $g(x) = x - 1$ is continuous on all of $\mathbb{R}$, so $\lim_{x \to c} g(x) = g(c)$.

## 6. Final Answer in Words
The limit as $x$ approaches $3$ is $2$. Factoring the numerator reveals a common factor of $(x - 3)$, which cancels out for all $x \neq 3$. The value of the function at $x = 3$ is irrelevant because the limit describes the target value that the function approaches in the punctured neighborhood of the point, completely ignoring what happens at the point itself.

## 7. Quick Verification
Construct a table of values approaching $x = 3$ from both sides:
- From the left ($x < 3$):
  - $x = 2.9 \implies f(2.9) = 2.9 - 1 = 1.9$
  - $x = 2.99 \implies f(2.99) = 2.99 - 1 = 1.99$
  - $x = 2.999 \implies f(2.999) = 2.999 - 1 = 1.999$
- From the right ($x > 3$):
  - $x = 3.1 \implies f(3.1) = 3.1 - 1 = 2.1$
  - $x = 3.01 \implies f(3.01) = 3.01 - 1 = 2.01$
  - $x = 3.001 \implies f(3.001) = 3.001 - 1 = 2.001$
As $x$ nears $3$, $f(x)$ unambiguously approaches $2$.

## 8. Common Mistakes
- **Conflating "undefined at a point" with "limit does not exist"**: Concluding that because $f(3) = 0/0$ is undefined, the limit must not exist.
- **Canceling $(x-3)$ without noting $x \neq 3$**: Forgetting that cancellation is valid only because the limit explicitly excludes $x = 3$.
- **Arithmetic sign error in factoring**: Factoring $x^2 - 4x + 3$ as $(x + 1)(x - 3)$ or $(x - 1)(x + 3)$.

## 9. Short In-Class Explanation (3 Sentences)
Substituting $x=3$ directly gives the indeterminate form $0/0$, showing the function is undefined at the point. By factoring the numerator into $(x-1)(x-3)$, we cancel the vanishing factor $(x-3)$ because the limit only inspects $x \neq 3$. This leaves the simplified expression $x-1$, which smoothly approaches $3-1 = 2$ as $x$ nears $3$.
