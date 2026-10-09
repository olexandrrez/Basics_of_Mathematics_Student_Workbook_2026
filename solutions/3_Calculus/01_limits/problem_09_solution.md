# Problem 09: One-Sided Limits and an Asymptote

## 1. Original Problem
Analyze the left-hand and right-hand limits of
$$f(x)=\frac1{x-2}$$
as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

## 2. What We Are Trying to Find
We must:
1. Compute the right-hand limit $\lim_{x \to 2^+} \frac{1}{x-2}$.
2. Compute the left-hand limit $\lim_{x \to 2^-} \frac{1}{x-2}$.
3. Determine whether the two-sided limit $\lim_{x \to 2} \frac{1}{x-2}$ exists.
4. Interpret the geometric meaning of these one-sided infinite limits on the graph of $f(x)$ and formally specify the vertical asymptote.

## 3. Key Idea or Theorem Needed Before the Calculation
- **One-Sided Limits**:
  - $x \to c^+$ means $x$ approaches $c$ strictly from values greater than $c$ ($x > c$, so $x - c > 0$).
  - $x \to c^-$ means $x$ approaches $c$ strictly from values less than $c$ ($x < c$, so $x - c < 0$).
- **Reciprocal Sign Rule for Infinite Limits**:
  $$\lim_{u \to 0^+} \frac{1}{u} = +\infty, \qquad \lim_{u \to 0^-} \frac{1}{u} = -\infty.$$
- **Existence of Two-Sided Limit**:
  The two-sided limit $\lim_{x \to c} f(x) = L$ exists if and only if both one-sided limits exist and are equal:
  $$\lim_{x \to c^+} f(x) = \lim_{x \to c^-} f(x) = L.$$
- **Vertical Asymptote**:
  The vertical line $x = c$ is a vertical asymptote of $y = f(x)$ if at least one of the one-sided limits as $x \to c$ is $+\infty$ or $-\infty$.

## 4. Step-by-Step Solution

### Step 1: Analyze the right-hand limit as $x \to 2^+$
- As $x \to 2^+$, the argument $x$ is strictly greater than $2$:
  $$x > 2 \implies x - 2 > 0.$$
- As $x$ gets arbitrarily close to $2$, the quantity $(x - 2)$ becomes a positive number arbitrarily close to $0$ (we write $x - 2 \to 0^+$).
- Dividing $1$ by a tiny positive number yields an arbitrarily large positive number:
  $$\lim_{x \to 2^+} \frac{1}{x-2} = \frac{1}{0^+} = +\infty.$$

### Step 2: Analyze the left-hand limit as $x \to 2^-$
- As $x \to 2^-$, the argument $x$ is strictly less than $2$:
  $$x < 2 \implies x - 2 < 0.$$
- As $x$ gets arbitrarily close to $2$, the quantity $(x - 2)$ is negative and arbitrarily close to $0$ (we write $x - 2 \to 0^-$).
- Dividing $1$ by a tiny negative number yields a negative number of arbitrarily large magnitude:
  $$\lim_{x \to 2^-} \frac{1}{x-2} = \frac{1}{0^-} = -\infty.$$

### Step 3: Determine whether the two-sided limit exists
- The right-hand limit is $+\infty$.
- The left-hand limit is $-\infty$.
- Since the two one-sided limits are not equal ($+\infty \neq -\infty$), the **two-sided limit does not exist**:
  $$\lim_{x \to 2} \frac{1}{x-2} \quad \text{does not exist (DNE)}.$$

### Step 4: Geometric interpretation and vertical asymptote
- **Vertical Asymptote**:
  Because the function values diverge to infinity as $x$ approaches $2$, the line:
  $$x = 2$$
  is a **vertical asymptote** of the graph.
- **Graph Behavior**:
  - As you trace the curve from the right approaching $x = 2$, the curve climbs steeply upward toward $+\infty$, hugging the right side of the vertical line $x = 2$.
  - As you trace the curve from the left approaching $x = 2$, the curve plunges steeply downward toward $-\infty$, hugging the left side of the vertical line $x = 2$.
  - The graph is a rectangular hyperbola shifted $2$ units to the right from the standard curve $y = 1/x$.

## 5. Why Each Step Is Valid
1. **Sign analysis**: For $x > 2$, the difference $x - 2$ is positive, so the quotient of positive numbers $1/(x-2)$ must be positive.
2. **Infinite limit definition**: A quotient with a non-zero numerator and a denominator tending to $0$ must diverge in magnitude to infinity.
3. **Criterion for two-sided limits**: By fundamental real analysis, a two-sided limit exists if and only if both directional limits converge to the same value.

## 6. Final Answer in Words
The right-hand limit is $+\infty$, and the left-hand limit is $-\infty$. Because the two one-sided limits have opposite signs and do not agree, the two-sided limit does not exist. Geometrically, the line $x = 2$ is a vertical asymptote where the function shoots upward to $+\infty$ from the right and plunges downward to $-\infty$ from the left.

## 7. Quick Verification
Evaluate $f(x)$ at test points close to $2$:
- Approaching from the right:
  - $f(2.1) = \frac{1}{0.1} = +10$
  - $f(2.01) = \frac{1}{0.01} = +100$
  - $f(2.001) = \frac{1}{0.001} = +1{,}000$ (diverging to $+\infty$).
- Approaching from the left:
  - $f(1.9) = \frac{1}{-0.1} = -10$
  - $f(1.99) = \frac{1}{-0.01} = -100$
  - $f(1.999) = \frac{1}{-0.001} = -1{,}000$ (diverging to $-\infty$).
The numerical signs and magnitudes confirm the analytical one-sided limits.

## 8. Common Mistakes
- **Writing that the two-sided limit is $\infty$**: Forgetting that $+\infty$ and $-\infty$ are fundamentally opposite directions. For $\lim_{x \to c} f(x) = \infty$ to hold, both sides must approach $+\infty$ (like in $\frac{1}{(x-2)^2}$).
- **Forgetting the sign of $x - 2$**: Treating $x \to 2^-$ as approaching $-2$, rather than approaching $+2$ from numbers slightly less than $2$ (such as $1.99$).
- **Confusing vertical and horizontal asymptotes**: Calling the line $y = 2$ the vertical asymptote instead of the vertical line $x = 2$.

## 9. Short In-Class Explanation (3 Sentences)
Approaching $2$ from the right makes $x-2$ a tiny positive number, driving the fraction $\frac{1}{x-2}$ to $+\infty$. Approaching $2$ from the left makes $x-2$ a tiny negative number, driving the fraction to $-\infty$. Because the left and right limits disagree, the two-sided limit does not exist, and the line $x=2$ is a vertical asymptote where the graph branches into opposite infinities.
