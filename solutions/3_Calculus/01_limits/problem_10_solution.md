# Problem 10: Continuity of a Piecewise Function

## 1. Original Problem
Find $a$ so that
$$f(x)=\begin{cases}ax+1,&x<2,\\x^2-1,&x\ge2\end{cases}$$
is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

## 2. What We Are Trying to Find
We must determine the value of the parameter $a \in \mathbb{R}$ that makes the piecewise function $f(x)$ continuous at the boundary point $x = 2$. To do this rigorously, we must explicitly calculate and compare three distinct mathematical quantities:
1. The left-hand limit: $\lim_{x \to 2^-} f(x)$.
2. The right-hand limit: $\lim_{x \to 2^+} f(x)$.
3. The function value at the point: $f(2)$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Three-Part Definition of Continuity**:
  A function $f(x)$ is continuous at a point $x = c$ if and only if all three of the following conditions hold:
  1. $f(c)$ is defined.
  2. $\lim_{x \to c} f(x)$ exists, which requires:
     $$\lim_{x \to c^-} f(x) = \lim_{x \to c^+} f(x).$$
  3. The limit equals the function value:
     $$\lim_{x \to c} f(x) = f(c).$$
  Combining these into a single master condition:
  $$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2).$$

## 4. Step-by-Step Solution

### Step 1: Calculate the function value $f(2)$
According to the piecewise formula, for $x \ge 2$, $f(x)$ is defined by the formula $x^2 - 1$.
Since $x = 2$ satisfies the condition $x \ge 2$:
$$f(2) = 2^2 - 1 = 4 - 1 = 3.$$

### Step 2: Calculate the right-hand limit $\lim_{x \to 2^+} f(x)$
For $x > 2$, the function is governed by $f(x) = x^2 - 1$.
Since $x^2 - 1$ is a polynomial, it is continuous:
$$\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (x^2 - 1) = 2^2 - 1 = 3.$$
Notice that the right-hand limit automatically agrees with the function value $f(2) = 3$.

### Step 3: Calculate the left-hand limit $\lim_{x \to 2^-} f(x)$
For $x < 2$, the function is governed by the linear expression $f(x) = ax + 1$.
Taking the limit as $x \to 2^-$:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} (ax + 1) = a(2) + 1 = 2a + 1.$$

### Step 4: Enforce the continuity condition
For $f$ to be continuous at $x = 2$, the left-hand limit must equal the common value of the right-hand limit and the function value:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2).$$
Substitute our computed expressions:
$$2a + 1 = 3.$$

### Step 5: Solve for the parameter $a$
Subtract $1$ from both sides:
$$2a = 3 - 1 = 2.$$
Divide by $2$:
$$a = 1.$$

---

### Step 6: Explicit Comparison of the Three Quantities
When $a = 1$:
1. **Left-hand limit**:
   $$\lim_{x \to 2^-} f(x) = 1(2) + 1 = 3.$$
2. **Right-hand limit**:
   $$\lim_{x \to 2^+} f(x) = 2^2 - 1 = 3.$$
3. **Function value**:
   $$f(2) = 2^2 - 1 = 3.$$

All three quantities are identically equal to $3$:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2) = 3.$$
The left piece (the line $y = x + 1$) and the right piece (the parabola $y = x^2 - 1$) meet seamlessly at the point $(2, 3)$, without any jump or hole.

## 5. Why Each Step Is Valid
1. **Piecewise evaluation**: The piecewise definition partitions the real line into disjoint sets $(-\infty, 2)$ and $[2, \infty)$. Evaluating each limit using the formula governing that half-line is mathematically necessary.
2. **Continuity of polynomial components**: Both $ax + 1$ and $x^2 - 1$ are polynomials and therefore continuous on their respective intervals, allowing their limits at $2$ to be calculated by substitution.
3. **Definition of continuity**: Equating the left-hand limit to the right-hand limit and the function value is the definitive mathematical criterion for continuity at a point.

## 6. Final Answer in Words
The function is continuous at $x = 2$ if and only if $a = 1$. The function value is $f(2) = 3$, the right-hand limit is $3$, and the left-hand limit is $2a + 1$. Setting $2a + 1 = 3$ gives $a = 1$, ensuring all three quantities equal $3$ and eliminating any discontinuity.

## 7. Quick Verification
- Let $a = 1$.
- Evaluate slightly to the left: $f(1.999) = 1(1.999) + 1 = 2.999$.
- Evaluate at the point: $f(2.000) = 2^2 - 1 = 3.000$.
- Evaluate slightly to the right: $f(2.001) = (2.001)^2 - 1 = 4.004001 - 1 = 3.004001$.
The values are continuous with no jump across $x = 2$.
- If $a$ were different, e.g., $a = 2$: the left limit would be $2(2)+1 = 5 \neq 3$, producing a jump discontinuity of size $2$.

## 8. Common Mistakes
- **Checking only that the two formulas are equal without stating limits**: Simply setting $2a+1 = 3$ without distinguishing between the left-hand limit, right-hand limit, and function value.
- **Using the wrong formula for $f(2)$**: Trying to evaluate $f(2)$ using $ax + 1$, ignoring the inequality $x \ge 2$ in the second branch.
- **Arithmetic slips**: Solving $2a + 1 = 3$ and writing $a = 2$ or $a = 4$.

## 9. Short In-Class Explanation (3 Sentences)
For the function to be continuous at $x=2$, the left-hand limit, right-hand limit, and function value must all be equal. The function value and right-hand limit both evaluate to $2^2-1 = 3$, while the left-hand limit equals $2a+1$. Setting $2a+1 = 3$ yields $a=1$, which seamlessly joins the line and parabola at the point $(2, 3)$.
