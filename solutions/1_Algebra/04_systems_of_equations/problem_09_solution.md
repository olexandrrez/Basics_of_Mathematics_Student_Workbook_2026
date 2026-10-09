# Problem 09: A System from a Sum Condition

## 1. Original Problem
Find numbers $x,y$ satisfying
$$x+y=10,\qquad 2x+5y=32.$$
Solve the system and explain geometrically why the solution is unique.

## 2. What We Are Trying to Find
We must determine the values of numbers $x$ and $y$ that satisfy both given linear relations, compute the intersection point algebraically, and explain geometrically why there is exactly one solution.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Linear System as Intersection of Lines**: Each linear equation in two variables $ax + by = c$ describes a straight line in the Cartesian plane $\mathbb{R}^2$.
- **Geometric Uniqueness Condition**: Two lines in $\mathbb{R}^2$ have a unique intersection point if and only if they are not parallel (their slopes are distinct, or equivalently, their normal vectors are linearly independent).
- **Determinant Criterion**: $\det\begin{pmatrix}1 & 1 \\ 2 & 5\end{pmatrix} \neq 0$.

## 4. Step-by-Step Solution

### Step 1: Solve the System Algebraically
Given:
$$\begin{cases} x + y = 10, \\ 2x + 5y = 32. \end{cases}$$
Express $x$ from Equation 1:
$$x = 10 - y.$$
Substitute into Equation 2:
$$2(10 - y) + 5y = 32.$$
Expand and simplify:
$$20 - 2y + 5y = 32 \implies 20 + 3y = 32 \implies 3y = 32 - 20 = 12 \implies y = 4.$$
Now substitute $y = 4$ back into the expression for $x$:
$$x = 10 - 4 = 6.$$
The solution is $(x, y) = (6, 4)$.

### Step 2: Geometric Explanation of Uniqueness
Write both lines in slope-intercept form $y = mx + b$:
- Line 1: $x + y = 10 \implies y = -x + 10$.
  Slope: $m_1 = -1$.
  $y$-intercept: $(0, 10)$.
- Line 2: $2x + 5y = 32 \implies 5y = -2x + 32 \implies y = -\frac{2}{5}x + \frac{32}{5} = -0.4x + 6.4$.
  Slope: $m_2 = -\frac{2}{5} = -0.4$.
  $y$-intercept: $(0, 6.4)$.

**Why the solution is unique**:
The slopes are different:
$$m_1 = -1 \neq -0.4 = m_2.$$
In the Euclidean plane, two straight lines with different slopes are non-parallel. Any two non-parallel lines in $\mathbb{R}^2$ intersect at exactly one single geometric point.
Alternatively, the normal vectors $n_1 = (1, 1)$ and $n_2 = (2, 5)$ are linearly independent because:
$$\det\begin{pmatrix} 1 & 1 \\ 2 & 5 \end{pmatrix} = (1)(5) - (1)(2) = 5 - 2 = 3 \neq 0.$$
Because the determinant is non-zero, the lines cannot be parallel or coincident, guaranteeing a unique point of intersection at $(6, 4)$.

## 5. Why Each Step Is Valid
- Substitution is an exact algebraic method that reduces the system to a single linear equation in one unknown.
- The Euclidean geometry axiom guarantees that non-parallel coplanar lines meet at exactly one point.

## 6. Final Answer in Words
The numbers are $x = 6$ and $y = 4$. Geometrically, the two equations represent straight lines with different slopes ($m_1 = -1$ and $m_2 = -0.4$), which ensures that the lines are not parallel and therefore intersect at exactly one unique point in the plane, $(6, 4)$.

## 7. Quick Verification
- Check Equation 1: $6 + 4 = 10$. (True)
- Check Equation 2: $2(6) + 5(4) = 12 + 20 = 32$. (True)
Both equations are satisfied.

## 8. Common Mistakes
- Arithmetic error when distributing: writing $2(10 - y) = 20 - y$ instead of $20 - 2y$.
- Explaining uniqueness merely by stating "we found numbers" rather than referring to the non-parallel slopes of the lines.

## 9. Short In-Class Explanation (3 Sentences)
We substitute $x = 10 - y$ into the second equation to get $20 + 3y = 32$, which yields $y = 4$ and $x = 6$. Geometrically, each equation represents a straight line in the coordinate plane. Because the lines have different slopes of $-1$ and $-2/5$, they are not parallel and must intersect at exactly one unique point, $(6, 4)$.
