# Problem 06: A System with a Parameter — Which Cases Actually Occur?

## 1. Original Problem
Analyze, depending on the parameter $a$, the system
$$\begin{cases}x+y=2,\\ax+ay=4.\end{cases}$$
Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## 2. What We Are Trying to Find
We must determine the number of solutions to the linear system across all values of parameter $a \in \mathbb{R}$, determine which of the three standard linear system outcomes occur, identify the specific parameter values for each case, and explain why the remaining case is mathematically impossible.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Parallel Line Analysis**: The left-hand sides are $x+y$ and $a(x+y)$. The normal vectors are $(1, 1)$ and $(a, a) = a(1, 1)$.
- For $a\neq0$, the normal vectors are parallel, so the two equations represent parallel lines. At $a=0$, the second equation is the impossible equation $0=4$, so it represents no line.
- Two lines in the plane that are parallel can either be:
  - **Identical (coincident)**: Infinitely many solutions.
  - **Distinct (parallel and disjoint)**: No solution.
- They can **never** intersect at a single point, because non-parallel lines require linearly independent normal vectors.

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix and Perform Elimination
$$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ a & a & 4 \end{array}\right].$$
Perform $R_2 \leftarrow R_2 - a R_1$:
- Left-hand side: $(a, a) - a(1, 1) = (a-a, a-a) = (0, 0)$.
- Right-hand side: $4 - a(2) = 4 - 2a$.
The reduced matrix is:
$$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 4 - 2a \end{array}\right].$$

### Step 2: Analyze Based on the Value of $4 - 2a$
The second equation has reduced to:
$$0x + 0y = 4 - 2a \iff 0 = 4 - 2a.$$

- **Case 1: $4 - 2a = 0 \implies a = 2$**
  When $a = 2$, the second row becomes $[0 \; 0 \mid 0]$.
  The second equation becomes $0 = 0$, which is trivially true.
  The system reduces to the single equation $x + y = 2$.
  With $y = t \in \mathbb{R}$, we get $x = 2 - t$.
  Therefore, for $a = 2$, the system has **infinitely many solutions**.

- **Case 2: $a \neq 2$**
  When $a \neq 2$, the second row is $[0 \; 0 \mid c]$ where $c = 4 - 2a \neq 0$.
  This represents the equation $0 = 4 - 2a \neq 0$, which is an impossible contradiction. Geometrically, if $a\neq0$, the original second equation is the line $x+y=4/a$: it is distinct and parallel to $x+y=2$. If $a=0$, it reduces to $0=4$ and has no points, rather than representing a line.
  Therefore, for all $a \neq 2$, the system has **no solution**.

### Step 3: Explain Why "Exactly One Solution" Cannot Occur
For a $2 \times 2$ system to have exactly one solution, the coefficient matrix $A = \begin{pmatrix} 1 & 1 \\ a & a \end{pmatrix}$ must have non-zero determinant:
$$\det A = (1)(a) - (1)(a) = a - a = 0.$$
Notice that $\det A = 0$ for **every** real value of $a$.
Because the determinant is identically zero regardless of $a$, the rows of $A$ are always linearly dependent, and the rank of $A$ is at most 1.
A rank of 2 is required for a unique solution. Since rank 2 is impossible here, the case of **exactly one solution never occurs**.

## 5. Why Each Step Is Valid
- Row operation $R_2 \leftarrow R_2 - aR_1$ is valid for all $a \in \mathbb{R}$.
- The identity $\det A = 0$ holds identically on $\mathbb{R}$, proving that the linear transformation is permanently non-invertible.

## 6. Final Answer in Words
The system has infinitely many solutions when $a = 2$ (the two equations describe the same line $x+y=2$). For $a\neq0,2$, it has no solution because the lines $x+y=2$ and $x+y=4/a$ are distinct and parallel. At $a=0$, the second equation is the impossible equation $0=4$. The case of exactly one solution never occurs for any real value of $a$ because the determinant of the coefficient matrix is identically zero for all $a$.

## 7. Quick Verification
- Test $a = 2$: System is $x+y=2$ and $2x+2y=4$. Dividing the second equation by 2 gives $x+y=2$. Identical lines $\implies$ infinitely many solutions.
- Test $a = 0$: System is $x+y=2$ and $0 = 4$. Contradiction $\implies$ no solution.
- Test $a = 1$: System is $x+y=2$ and $x+y=4$. Contradiction $2 = 4 \implies$ no solution.

## 8. Common Mistakes
- Assuming that varying a parameter must produce all three cases (unique, infinite, none).
- Dividing by $a$ before checking $a=0$, which introduces an invalid singularity.

## 9. Short In-Class Explanation (3 Sentences)
Subtracting $a$ times the first row from the second row reduces the second equation to $0 = 4 - 2a$. When $a = 2$, this becomes $0 = 0$, meaning the equations describe the same line and there are infinitely many solutions. For $a\neq2$, it is a contradiction; geometrically, when $a\neq0$ the lines are distinct and parallel, while at $a=0$ the second equation is $0=4$. A unique solution never occurs because the determinant is zero for every $a$.
