# Problem 12: Exponential Function Limit

## 1. Original Problem
Compute
$$\lim_{x\to0}(1+3x)^{1/x}.$$
Connect the result with the limit from Exercise 5 and show the appropriate transformation.

## 2. What We Are Trying to Find
We must:
1. Compute the limit of the indeterminate exponential expression $f(x) = (1 + 3x)^{1/x}$ as $x$ approaches $0$.
2. Note that as $x \to 0$, the base $(1 + 3x) \to 1$ while the exponent $1/x \to \pm\infty$, creating the classic indeterminate form $1^\infty$.
3. Connect this expression directly to the fundamental definition of Euler's number $e$ from Exercise 5, demonstrating the appropriate substitution and exponent transformation.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Fundamental Limit Defining $e$**:
  From Exercise 5, the sequence limit is:
  $$\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e.$$
  For continuous real variables, this takes the equivalent forms:
  $$\lim_{t \to \infty} \left(1 + \frac{1}{t}\right)^t = e, \qquad \lim_{u \to 0} (1 + u)^{1/u} = e.$$
- **Power of a Power Law**:
  $$(A^B)^C = A^{B \cdot C}.$$
  We can manipulate the exponent $\frac{1}{x}$ into the required reciprocal form $\frac{1}{3x}$ by writing:
  $$\frac{1}{x} = \frac{3}{3x} = \frac{1}{3x} \cdot 3.$$
- **Continuity of Power Functions**:
  If $\lim_{x \to c} g(x) = L > 0$, then $\lim_{x \to c} [g(x)]^k = L^k$.

## 4. Step-by-Step Solution

### Step 1: Identify the indeterminate form
As $x \to 0$:
- Base: $1 + 3x \to 1 + 0 = 1$.
- Exponent: $\frac{1}{x} \to \pm\infty$.
This is the indeterminate form $1^\infty$.

### Step 2: Introduce the change of variable
Let $u = 3x$.
- As $x \to 0$, we have $u = 3(0) = 0$.
- Solving for $x$ gives $x = \frac{u}{3}$, so:
  $$\frac{1}{x} = \frac{3}{u} = \frac{1}{u} \cdot 3.$$

### Step 3: Rewrite the expression in terms of $u$
Substitute $3x = u$ and $\frac{1}{x} = \frac{3}{u}$:
$$(1 + 3x)^{1/x} = (1 + u)^{3/u}.$$
Using the exponent rule $(A^B)^C = A^{B \cdot C}$:
$$(1 + u)^{3/u} = \left[ (1 + u)^{1/u} \right]^3.$$

### Step 4: Apply the fundamental limit
As $x \to 0$, $u \to 0$. Recall the fundamental limit:
$$\lim_{u \to 0} (1 + u)^{1/u} = e.$$
Because the cubic function $h(y) = y^3$ is continuous on all of $\mathbb{R}$:
$$\lim_{x \to 0} (1 + 3x)^{1/x} = \lim_{u \to 0} \left[ (1 + u)^{1/u} \right]^3 = \left[ \lim_{u \to 0} (1 + u)^{1/u} \right]^3 = e^3.$$

---

### Step 5: Alternative transformation via natural logarithms
We can also evaluate the limit using the exponential-logarithmic identity $A^B = e^{B \ln A}$:
$$(1 + 3x)^{1/x} = \exp\left( \frac{\ln(1 + 3x)}{x} \right).$$
Now analyze the exponent as $x \to 0$:
$$\lim_{x \to 0} \frac{\ln(1 + 3x)}{x} = \lim_{x \to 0} 3 \cdot \frac{\ln(1 + 3x)}{3x}.$$
Since $\lim_{u \to 0} \frac{\ln(1 + u)}{u} = 1$:
$$\lim_{x \to 0} \frac{\ln(1 + 3x)}{x} = 3 \cdot 1 = 3.$$
By continuity of the exponential function $e^t$:
$$\lim_{x \to 0} (1 + 3x)^{1/x} = e^3.$$
Both methods confirm the identical result.

## 5. Why Each Step Is Valid
1. **Change of variable**: The substitution $u = 3x$ is a continuous bijection mapping the neighborhood of $x = 0$ to the neighborhood of $u = 0$.
2. **Algebra of exponents**: $(a^b)^c = a^{bc}$ holds for all positive bases $a > 0$ and real exponents $b, c$.
3. **Limit of continuous compositions**: The function $f(t) = t^3$ is continuous everywhere, so $\lim [g(x)]^3 = [\lim g(x)]^3$.

## 6. Final Answer in Words
The limit as $x$ approaches $0$ is $e^3$. By setting $u = 3x$, the exponent $\frac{1}{x}$ is rewritten as $\frac{1}{u} \times 3$, allowing the expression to be factored into $[(1+u)^{1/u}]^3$. Since the inner term approaches Euler's number $e$ by the fundamental limit from Exercise 5, cubing the result produces $e^3$.

## 7. Quick Verification
- Compute numerical values for small $x$:
  - $e^3 \approx 20.085537$.
  - For $x = 0.1$: $(1 + 0.3)^{10} = (1.3)^{10} \approx 13.7858$.
  - For $x = 0.01$: $(1 + 0.03)^{100} = (1.03)^{100} \approx 19.2186$.
  - For $x = 0.001$: $(1 + 0.003)^{1000} = (1.003)^{1000} \approx 19.9955$.
  - For $x = 0.0001$: $(1 + 0.0003)^{10000} \approx 20.0765$.
The values rapidly converge to $e^3 \approx 20.0855$.

## 8. Common Mistakes
- **Assuming $1^\infty = 1$**: Incorrectly claiming that since the base is $1$, raising $1$ to any power gives $1$. The base is not identically $1$; it only approaches $1$ while the power approaches infinity.
- **Forgetting to cube the base**: Identifying the limit as $e$ or $3e$ instead of $e^3$.
- **Misplacing the factor of $3$**: Writing $\frac{1}{x} = \frac{1}{3} \cdot \frac{1}{3x}$ instead of $3 \cdot \frac{1}{3x}$.

## 9. Short In-Class Explanation (3 Sentences)
The limit has the indeterminate form $1^\infty$, which signals the classical definition of Euler's number $e$. By writing the exponent $\frac{1}{x}$ as $\frac{3}{3x}$, we restructure the expression into $[(1+3x)^{1/(3x)}]^3$. The term inside the brackets approaches $e$ as $3x \to 0$, so cubing this limit yields $e^3$.
