# Problem 10: A Polynomial Through Three Points

## 1. Original Problem
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## 2. What We Are Trying to Find
We must determine the three unknown coefficients $a, b, c$ of a quadratic polynomial $p(x) = ax^2 + bx + c$ such that its parabolic graph passes through three given points, set up and solve the resulting $3 \times 3$ linear system, and verify the polynomial on all three points.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Polynomial Interpolation**: For any $n+1$ points with distinct $x$-coordinates, there exists a unique polynomial of degree at most $n$ passing through them (Vandermonde Theorem).
- **Point-Condition Equations**: A curve $y = p(x)$ passes through point $(x_k, y_k)$ if and only if $p(x_k) = y_k$.
- Substituting the three points creates a linear system where the unknown quantities are the coefficients $a, b, c$.

## 4. Step-by-Step Solution

### Step 1: Set Up the Equations from the Points
Substitute each point $(x, y)$ into $p(x) = ax^2 + bx + c$:
1. Point $(0, 1)$:
   $$p(0) = a(0)^2 + b(0) + c = 1 \implies c = 1.$$
2. Point $(1, 3)$:
   $$p(1) = a(1)^2 + b(1) + c = 3 \implies a + b + c = 3.$$
3. Point $(2, 9)$:
   $$p(2) = a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9.$$

### Step 2: Solve the Linear System
We have:
$$\begin{cases} c = 1, \\ a + b + c = 3, \\ 4a + 2b + c = 9. \end{cases}$$
1. Substitute $c = 1$ into the second and third equations:
   $$a + b + 1 = 3 \implies a + b = 2,$$
   $$4a + 2b + 1 = 9 \implies 4a + 2b = 8 \implies 2a + b = 4.$$
2. Subtract the equation $(a + b = 2)$ from $(2a + b = 4)$:
   $$(2a + b) - (a + b) = 4 - 2 \implies a = 2.$$
3. Substitute $a = 2$ back into $a + b = 2$:
   $$2 + b = 2 \implies b = 0.$$
4. We already found $c = 1$.

### Step 3: Write the Polynomial
The coefficients are $a = 2$, $b = 0$, and $c = 1$.
Therefore, the polynomial is:
$$p(x) = 2x^2 + 1.$$

### Step 4: Verification by Direct Substitution
Check all three points:
- For $x = 0$: $p(0) = 2(0)^2 + 1 = 0 + 1 = 1$. Matches $(0, 1)$!
- For $x = 1$: $p(1) = 2(1)^2 + 1 = 2 + 1 = 3$. Matches $(1, 3)$!
- For $x = 2$: $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 8 + 1 = 9$. Matches $(2, 9)$!
All three points lie on the graph of $p(x) = 2x^2 + 1$.

## 5. Why Each Step Is Valid
- Evaluating a polynomial at distinct $x$-coordinates generates a Vandermonde system with non-zero determinant, guaranteeing that the solution for $a, b, c$ is unique.
- The elimination and back-substitution steps are exact algebraic operations.

## 6. Final Answer in Words
The quadratic polynomial is $p(x) = 2x^2 + 1$ (with coefficients $a = 2$, $b = 0$, $c = 1$). Substituting $x = 0, 1, 2$ into $p(x)$ produces the output values $1, 3, 9$, confirming that the parabola passes through all three points.

## 7. Quick Verification
- Second differences test for quadratic functions with equally spaced $x$-values ($h=1$):
  $y$-values: $1, 3, 9$.
  First differences: $3 - 1 = 2$, $9 - 3 = 6$.
  Second difference: $6 - 2 = 4$.
  By calculus / finite differences, the leading coefficient is $a = \frac{\Delta^2 y}{2 h^2} = \frac{4}{2(1)} = 2$.
  Vertex at $x = -b/(2a) = 0$, giving $p(x) = 2x^2 + 1$. Perfectly verified.

## 8. Common Mistakes
- Miscomputing $a(2)^2$ as $2a$ rather than $4a$.
- Forgetting that the linear term coefficient $b$ can be zero.

## 9. Short In-Class Explanation (3 Sentences)
Substituting the three points $(0, 1)$, $(1, 3)$, and $(2, 9)$ into $p(x) = ax^2 + bx + c$ produces a $3 \times 3$ linear system for the coefficients. The first point immediately gives $c = 1$, and solving the remaining two equations yields $a = 2$ and $b = 0$. The resulting polynomial is $p(x) = 2x^2 + 1$, which passes through all three points upon direct substitution.
