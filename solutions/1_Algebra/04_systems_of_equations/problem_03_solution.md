# Problem 03: Inconsistent System

## 1. Original Problem
Solve or show that the system is inconsistent:
$$\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}$$
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## 2. What We Are Trying to Find
We must determine if the system of two equations has any solution by applying Gaussian elimination, identify the contradictory row in the augmented matrix, and explain the geometric and algebraic meaning of inconsistency.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Rouché-Capelli Theorem**: A linear system is consistent if and only if the rank of the coefficient matrix equals the rank of the augmented matrix: $\operatorname{rank}(A) = \operatorname{rank}([A \mid b])$.
- **Contradiction Condition**: If row elimination produces a row of the form $[0 \; 0 \mid c]$ where $c \neq 0$, the corresponding equation is $0x + 0y = c$, which is an impossible statement ($0 = c$). The system is inconsistent and has no solution.

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix
$$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right].$$

### Step 2: Perform Elimination
Eliminate $x$ from Row 2 using $R_2 \leftarrow R_2 - 2R_1$:
- Left-hand side: $(2, 4) - 2(1, 2) = (2-2, 4-4) = (0, 0)$.
- Right-hand side: $7 - 2(3) = 7 - 6 = 1$.
The augmented matrix becomes:
$$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right].$$

### Step 3: Interpret the Resulting Row
Row 2 represents the equation:
$$0x + 0y = 1 \iff 0 = 1.$$
Because $0 = 1$ is mathematically impossible for any choice of real numbers $x$ and $y$, no pair $(x, y)$ can ever satisfy the second equation.
Therefore, the system is **inconsistent** (it has no solution).

### Step 4: Geometric Interpretation
Write each equation in slope-intercept form $y = mx + b$:
- Equation 1: $x + 2y = 3 \implies y = -\frac{1}{2}x + \frac{3}{2}$.
- Equation 2: $2x + 4y = 7 \implies y = -\frac{1}{2}x + \frac{7}{4}$.
Both lines have the exact same slope $m = -1/2$, meaning they are **parallel**.
However, their $y$-intercepts are different ($3/2 = 1.5$ vs $7/4 = 1.75$), meaning they are **distinct parallel lines**.
Because two parallel lines never intersect, there are no common points, which geometrically explains why the system has no solution.

## 5. Why Each Step Is Valid
- Elementary row operations preserve the equivalence of equations; any solution of the original system must satisfy the reduced system.
- The rank of $A$ is $1$, but the rank of $[A \mid b]$ is $2$; by the Rouché-Capelli theorem, unequal ranks strictly imply inconsistency.

## 6. Final Answer in Words
The system is inconsistent and has no solution. After performing the row operation $R_2 \leftarrow R_2 - 2R_1$, the second row becomes $[0 \; 0 \mid 1]$, which translates to the impossible equation $0 = 1$. Geometrically, the two equations represent parallel lines that never intersect.

## 7. Quick Verification
- Multiply the first equation by 2: $2(x + 2y) = 2(3) \implies 2x + 4y = 6$.
  The system states $2x + 4y = 6$ and $2x + 4y = 7$ simultaneously.
  Subtracting them gives $0 = 1$, an immediate contradiction.

## 8. Common Mistakes
- Misinterpreting $[0 \; 0 \mid 1]$ as infinitely many solutions (confusing it with $[0 \; 0 \mid 0]$).
- Claiming that $x=0, y=0$ is a solution.

## 9. Short In-Class Explanation (3 Sentences)
Subtracting twice the first row from the second row reduces the augmented matrix to have a second row of $[0 \; 0 \mid 1]$. This corresponds to the equation $0 = 1$, which is impossible for any values of $x$ and $y$. Geometrically, the two equations describe distinct parallel lines with the same slope that never intersect, so the system has no solution.
