# Problem 14: A System of Equations and the Determinant

## 1. Original Problem
Consider the system $Ax=b$, where
$$A=\begin{pmatrix}1&2\\k&4\end{pmatrix}.$$
For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

## 2. What We Are Trying to Find
We must determine the values of the parameter $k$ for which the system $Ax = b$ possesses a unique solution for every right-hand side vector $b$. For the exceptional value of $k$, we must analyze the singular system and provide specific numerical vectors $b$ that produce infinitely many solutions (consistency) and no solution (inconsistency).

## 3. Key Idea or Theorem Needed Before the Calculation
- **Cramer's Theorem / Invertibility Theorem**: A linear system $Ax = b$ with a square matrix $A$ has a unique solution for every vector $b$ if and only if $\det A \neq 0$.
- **Singular System Analysis ($\\det A = 0$)**: When $\det A = 0$, the rows of $A$ are proportional:
  - If the components of $b$ satisfy the exact same proportion as the rows of $A$, the equations are redundant and there are **infinitely many solutions**.
  - If the components of $b$ do not satisfy that proportion, the equations are contradictory and there is **no solution**.

## 4. Step-by-Step Solution

### Step 1: Compute $\det A$
$$A = \begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix} \implies \det A = (1)(4) - (2)(k) = 4 - 2k.$$

### Step 2: Determine Condition for a Unique Solution
The system has exactly one solution for every $b$ if and only if $\det A \neq 0$:
$$4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2.$$
Therefore, for all $k \in \mathbb{R} \setminus \{2\}$, the system has a unique solution for any choice of $b$.

### Step 3: Analyze the Exceptional Value $k = 2$
When $k = 2$, the matrix is:
$$A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}.$$
The system of equations is:
$$\begin{cases} x + 2y = b_1, \\ 2x + 4y = b_2. \end{cases}$$
Notice that the left-hand side of the second equation is exactly twice the left-hand side of the first equation:
$$2(x + 2y) = 2x + 4y.$$

### Step 4: Construct Examples for $k = 2$
- **Case A: Infinitely Many Solutions**
  For consistency, the right-hand side must satisfy the same proportionality: $b_2 = 2 b_1$.
  Choose $b_1 = 1$, which requires $b_2 = 2(1) = 2$.
  Vector: $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$.
  The system becomes:
  $$\begin{cases} x + 2y = 1, \\ 2x + 4y = 2. \end{cases}$$
  Dividing the second equation by 2 gives $x + 2y = 1$, which is identical to the first.
  Setting $y = t$ as a free parameter, the solutions are $(1 - 2t, t)$ for any $t \in \mathbb{R}$ (infinitely many solutions).

- **Case B: No Solution**
  Choose a vector $b$ where $b_2 \neq 2 b_1$.
  Choose $b_1 = 1$ and $b_2 = 5$.
  Vector: $b = \begin{pmatrix} 1 \\ 5 \end{pmatrix}$.
  The system becomes:
  $$\begin{cases} x + 2y = 1, \\ 2x + 4y = 5. \end{cases}$$
  Multiplying the first equation by 2 yields $2x + 4y = 2$.
  Comparing with the second equation gives $2 = 5$, a contradiction.
  Therefore, there is no solution.

## 5. Why Each Step Is Valid
- When $\det A \neq 0$, the inverse $A^{-1}$ exists and uniquely solves $x = A^{-1}b$.
- When $\det A = 0$, Rouché-Capelli theorem establishes that the system is consistent if and only if $\operatorname{rank}(A) = \operatorname{rank}([A \mid b])$, which here requires $b_2 = 2b_1$.

## 6. Final Answer in Words
The system has exactly one solution for every $b$ if and only if $k \neq 2$. For $k = 2$, the right-hand side $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ yields infinitely many solutions (the two equations describe the same line), while $b = \begin{pmatrix} 1 \\ 5 \end{pmatrix}$ yields no solution (the two equations describe parallel, disjoint lines).

## 7. Quick Verification
- For $k = 3$: $\det A = 4 - 2(3) = -2 \neq 0$. The unique solution for $b=(1,2)^T$ is found by Cramer's rule: $x = \frac{4(1)-2(2)}{-2} = 0$, $y = \frac{1(2)-3(1)}{-2} = \frac{-1}{-2} = 1/2$. A unique solution exists.
- For $k = 2$, $b=(1,2)^T$: point $(1, 0)$ satisfies both $1+0=1$ and $2+0=2$. Point $(-1, 1)$ satisfies both $-1+2=1$ and $-2+4=2$. Multiple solutions confirmed.

## 8. Common Mistakes
- Stating that $k=2$ always means no solution, ignoring the possibility of infinitely many solutions when $b$ is proportional.
- Forgetting to provide a concrete numerical vector $b$ for each case.

## 9. Short In-Class Explanation (3 Sentences)
The determinant of the coefficient matrix is $4 - 2k$, which is non-zero whenever $k \neq 2$, ensuring a unique solution for every right-hand side vector. When $k = 2$, the two equations have parallel left-hand sides because the second row is twice the first. Choosing $b = (1, 2)^T$ creates two identical equations with infinitely many solutions, whereas choosing $b = (1, 5)^T$ creates the contradiction $2 = 5$, yielding no solution.
