# Problem 15: Classifying Three Systems

## 1. Original Problem
For each of the following systems, perform only as much elimination as necessary to recognize its type:
1. $\begin{cases}x+y=2,\\x-y=0,\end{cases}$
2. $\begin{cases}x+y=2,\\2x+2y=4,\end{cases}$
3. $\begin{cases}x+y=2,\\2x+2y=5.\end{cases}$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## 2. What We Are Trying to Find
We must classify each of the three systems into one of the three fundamental categories of linear systems (unique solution, infinitely many solutions, or no solution) by performing minimal row elimination and justifying each conclusion from the resulting echelon structure.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Classification Criteria in Row Echelon Form**:
  1. **Exactly One Solution**: Full rank ($2$ pivots for $2$ variables).
  2. **Infinitely Many Solutions**: Consistent system with fewer pivots than variables (contains a row $[0 \; 0 \mid 0]$ with a free variable).
  3. **No Solution**: Inconsistent system containing a contradiction row $[0 \; 0 \mid c]$ where $c \neq 0$.

## 4. Step-by-Step Solution

### System 1
$$\begin{cases} x + y = 2, \\ x - y = 0. \end{cases}$$
1. Set up the augmented matrix:
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 1 & -1 & 0 \end{array}\right].$$
2. Perform $R_2 \leftarrow R_2 - R_1$:
   $$(1, -1 \mid 0) - (1, 1, 2) = (0, -2 \mid -2).$$
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -2 & -2 \end{array}\right].$$
- **Analysis**:
  There are two non-zero rows and two pivot positions (Row 1 Col 1, and Row 2 Col 2).
  Since the rank of the coefficient matrix equals the number of variables ($2 = 2$) and there are no contradiction rows, the system is consistent with no free variables.
- **Classification**: **Exactly one unique solution** (specifically, $y = 1$ and $x = 1$).

### System 2
$$\begin{cases} x + y = 2, \\ 2x + 2y = 4. \end{cases}$$
1. Set up the augmented matrix:
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & 2 & 4 \end{array}\right].$$
2. Perform $R_2 \leftarrow R_2 - 2R_1$:
   $$(2, 2 \mid 4) - 2(1, 1 \mid 2) = (0, 0 \mid 0).$$
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 0 \end{array}\right].$$
- **Analysis**:
  Row 2 is $[0 \; 0 \mid 0]$, representing $0 = 0$.
  The system is consistent, but there is only $1$ pivot for $2$ variables.
  Variable $y$ is free ($y = t$), giving $x = 2 - t$.
- **Classification**: **Infinitely many solutions**.

### System 3
$$\begin{cases} x + y = 2, \\ 2x + 2y = 5. \end{cases}$$
1. Set up the augmented matrix:
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & 2 & 5 \end{array}\right].$$
2. Perform $R_2 \leftarrow R_2 - 2R_1$:
   $$(2, 2 \mid 5) - 2(1, 1 \mid 2) = (0, 0 \mid 1).$$
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 1 \end{array}\right].$$
- **Analysis**:
  Row 2 is $[0 \; 0 \mid 1]$, which translates to the impossible equation $0 = 1$.
- **Classification**: **No solution** (inconsistent).

## 5. Why Each Step Is Valid
- A single elementary row operation reduces each $2 \times 2$ system to row echelon form.
- The structure of the second row directly signals the classification: a pivot on the left means unique solution; all zeros means infinite solutions; a pivot on the right means no solution.

## 6. Final Answer in Words
System 1 has exactly one solution because elimination yields a full-rank upper-triangular matrix with two pivots. System 2 has infinitely many solutions because elimination produces the consistent row $[0 \; 0 \mid 0]$, leaving one free variable. System 3 has no solution because elimination produces the contradictory row $[0 \; 0 \mid 1]$, meaning the lines are parallel and disjoint.

## 7. Quick Verification
- Check lines geometrically:
  - System 1: lines $y = -x + 2$ and $y = x$ have slopes $-1$ and $1$ (perpendicular $\implies$ one intersection).
  - System 2: lines $y = -x + 2$ and $y = -x + 2$ have identical slopes and intercepts (coincident $\implies$ infinite intersections).
  - System 3: lines $y = -x + 2$ and $y = -x + 2.5$ have identical slopes but different intercepts (parallel $\implies$ zero intersections).

## 8. Common Mistakes
- Doing unnecessary full elimination or inverting matrices when a single row operation suffices.
- Confusing $[0 \; 0 \mid 0]$ (infinite solutions) with $[0 \; 0 \mid 1]$ (no solution).

## 9. Short In-Class Explanation (3 Sentences)
In System 1, row elimination leaves pivots in both columns, giving exactly one unique solution at $(1, 1)$. In System 2, subtracting twice the first row eliminates the second row completely into zeros, which leaves a free variable and infinitely many solutions. In System 3, the same operation produces the contradiction $0 = 1$, which proves that the parallel lines never intersect and the system has no solution.
