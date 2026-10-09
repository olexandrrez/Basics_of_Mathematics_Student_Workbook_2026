# Problem 07: Classifying a Second-Degree Equation

## 1. Original Problem
Determine the type of object described by:
1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

## 2. What We Are Trying to Find
For each of the four given quadratic equations, we must identify the geometric curve it represents in the Cartesian plane $\mathbb{R}^2$ by examining the signs and degrees of the variables, and provide an algebraic proof for why the fourth equation has no real solutions.

## 3. Key Idea or Theorem Needed Before the Calculation
- **General Second-Degree Curves in Standard Position**:
  - $A x^2 + B y^2 = C$ with $A, B, C > 0$: **Ellipse** (a circle if $A = B$).
  - $A x^2 - B y^2 = C$ with $A, B, C > 0$: **Hyperbola**.
  - $A x^2 + D y = 0$ or $B y^2 + C x = 0$ (one variable squared, the other linear): **Parabola**.
  - Sum of non-negative terms equal to a strictly negative constant: **Empty set** (no real points), because for all real $u \in \mathbb{R}$, $u^2 \ge 0$.

## 4. Step-by-Step Solution

### Item 1: $4x^2 + 9y^2 = 36$
1. Divide both sides by $36$:
   $$\frac{4x^2}{36} + \frac{9y^2}{36} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1.$$
2. Both $x$ and $y$ are squared with positive, unequal coefficients ($a^2 = 9 \neq 4 = b^2$).
3. **Conclusion**: This is an **ellipse** centered at $(0, 0)$ with horizontal semi-major axis $a = 3$ and vertical semi-minor axis $b = 2$.

### Item 2: $x^2 - y^2 = 1$
1. The equation is already in canonical form:
   $$\frac{x^2}{1^2} - \frac{y^2}{1^2} = 1.$$
2. Both variables are squared, but their coefficients have opposite signs ($+1$ for $x^2$, $-1$ for $y^2$).
3. **Conclusion**: This is an **equilateral (rectangular) hyperbola** centered at $(0, 0)$ with vertices at $(\pm 1, 0)$ and asymptotes $y = \pm x$.

### Item 3: $x^2 - 4y = 0$
1. Solve for the linear variable $y$:
   $$4y = x^2 \implies y = \frac{1}{4}x^2.$$
2. One variable ($x$) is squared, while the other ($y$) appears only to the first power.
3. **Conclusion**: This is a **parabola** with vertex at $(0, 0)$, axis of symmetry along the $y$-axis ($x = 0$), opening upwards.

### Item 4: $x^2 + y^2 + 1 = 0$
1. Rearrange by moving the constant to the right-hand side:
   $$x^2 + y^2 = -1.$$
2. **Analysis of real points**:
   - For every real number $x \in \mathbb{R}$, we have $x^2 \ge 0$.
   - For every real number $y \in \mathbb{R}$, we have $y^2 \ge 0$.
   - Therefore, the sum of two squares is always non-negative:
     $$x^2 + y^2 \ge 0.$$
   - However, the equation demands that $x^2 + y^2 = -1$, which is strictly less than $0$.
   - Since a non-negative number ($x^2 + y^2 \ge 0$) can never equal a strictly negative number ($-1$), there exist no real numbers $x, y$ that satisfy this equation.
3. **Conclusion**: This equation represents the **empty set** $\emptyset$ in $\mathbb{R}^2$ (an imaginary circle).

## 5. Why Each Step Is Valid
1. **Division by constants**: Multiplying or dividing both sides by a non-zero real number preserves algebraic equivalence.
2. **Conic signatures**: Quadratic forms in standard position are uniquely characterized by the signs of the quadratic coefficients: $(+, +)$ is elliptic, $(+, -)$ is hyperbolic, and one zero coefficient with a linear term is parabolic.
3. **Non-negativity of real squares**: The square of any real number is non-negative ($u^2 \ge 0$ for all $u \in \mathbb{R}$). The sum of two non-negative numbers cannot be negative, proving the impossibility of real solutions for $x^2 + y^2 = -1$.

## 6. Final Answer in Words
1. $4x^2+9y^2=36$ is an **ellipse** centered at the origin with semiaxes $3$ and $2$.
2. $x^2-y^2=1$ is a **hyperbola** centered at the origin opening along the $x$-axis.
3. $x^2-4y=0$ is a **parabola** opening upward with vertex at the origin.
4. $x^2+y^2+1=0$ describes the **empty set** (no real points), because the left side is the sum of two non-negative squares and a positive one, which strictly exceeds zero for all real coordinates $(x, y)$.

## 7. Quick Verification
- For $4x^2+9y^2=36$: $(3, 0) \implies 4(9)+0=36$ (valid real point).
- For $x^2-y^2=1$: $(1, 0) \implies 1-0=1$ (valid real point).
- For $x^2-4y=0$: $(2, 1) \implies 4-4(1)=0$ (valid real point).
- For $x^2+y^2+1=0$: even at the absolute minimum $(x, y) = (0, 0)$, $0^2+0^2+1 = 1 \neq 0$. Any other real pair gives an even larger sum $> 1$.

## 8. Common Mistakes
- **Confusing parabolas with hyperbolas**: Not noticing that $x^2 - 4y = 0$ has only one squared term, making it a parabola rather than a hyperbola.
- **Calling $x^2+y^2=-1$ a circle of radius $-1$**: A radius must be a positive real distance; a negative squared radius means the geometric locus in $\mathbb{R}^2$ contains zero points.
- **Failing to isolate $1$ on the right side**: Misidentifying semiaxes before dividing by $36$ in Item 1.

## 9. Short In-Class Explanation (3 Sentences)
We classify second-degree curves by examining the degrees and signs of the terms: two positive squares give an ellipse, opposite signs give a hyperbola, and a single square with a linear term gives a parabola. For the last equation, $x^2+y^2=-1$ cannot hold for any real numbers because squares of real numbers are always non-negative. Thus, the fourth equation contains no real points and describes the empty set.
