# Problem 04: Infinitely Many Solutions

## 1. Original Problem
Solve
$$\begin{cases}x+y+z=2,\\2x+2y+2z=4,\\x-y+z=0.\end{cases}$$
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## 2. What We Are Trying to Find
We must determine the complete solution set of the linear system, show that it contains infinitely many solutions due to redundant equations, write the solution in parametric vector form with an explicitly identified free variable, and verify one concrete solution point.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Free Variables and Parameterization**: When row echelon reduction yields fewer non-zero rows (pivots) than variables, the variables without pivot columns are chosen as **free variables** (parameters $t \in \mathbb{R}$).
- **Geometry of Infinitely Many Solutions**: Three planes intersecting along a common line share an infinite continuum of collinear points.

## 4. Step-by-Step Solution

### Step 1: Form the Augmented Matrix
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 2 & 2 & 4 \\ 1 & -1 & 1 & 0 \end{array}\right].$$

### Step 2: Row Reduction
1. Notice that Row 2 is exactly $2 \times$ Row 1.
   Perform $R_2 \leftarrow R_2 - 2R_1$:
   $$(2, 2, 2 \mid 4) - 2(1, 1, 1 \mid 2) = (0, 0, 0 \mid 0).$$
   The second row vanishes entirely.
2. Eliminate $x$ from Row 3 using $R_3 \leftarrow R_3 - R_1$:
   $$(1, -1, 1 \mid 0) - (1, 1, 1 \mid 2) = (0, -2, 0 \mid -2).$$
Swap $R_2$ and $R_3$ to reach standard echelon form:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & -2 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

### Step 3: Identify Pivots and Free Variables
- Pivot in Column 1: $x$ is a leading variable.
- Pivot in Column 2: $y$ is a leading variable (from $-2y = -2$).
- No pivot in Column 3: $z$ is a **free variable**.
Let $z = t$, where $t \in \mathbb{R}$ is an arbitrary parameter.

### Step 4: Express Leading Variables in Terms of Parameter $t$
1. From Row 2:
   $$-2y = -2 \implies y = 1.$$
2. From Row 1:
   $$x + y + z = 2 \implies x + 1 + t = 2 \implies x = 1 - t.$$

### Step 5: Write the Parametric Solution
The general solution in parametric form is:
$$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 - t \\ 1 \\ t \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.$$

### Step 6: Verify a Chosen Parameter Value
Choose $t = 0$. The resulting point is:
$$(x, y, z) = (1, 1, 0).$$
Substitute into all three original equations:
- Equation 1: $1 + 1 + 0 = 2$. ($2 = 2$, True)
- Equation 2: $2(1) + 2(1) + 2(0) = 2 + 2 + 0 = 4$. ($4 = 4$, True)
- Equation 3: $1 - 1 + 0 = 0$. ($0 = 0$, True)
The point $(1, 1, 0)$ satisfies all three equations.

## 5. Why Each Step Is Valid
- Row operations revealed that equation 2 is redundant ($2R_1 = R_2$), reducing the rank of the system to 2 with 3 unknowns.
- A rank-2 system in $\mathbb{R}^3$ has $3 - 2 = 1$ degree of freedom, geometrically defining a line of solutions parameterized by $t$.

## 6. Final Answer in Words
The system has infinitely many solutions. With $z = t$ chosen as the free parameter, the parametric solution is $x = 1 - t$, $y = 1$, and $z = t$ for any real number $t$. Testing $t = 0$ yields the point $(1, 1, 0)$, which satisfies all three equations.

## 7. Quick Verification
- Test another value, e.g. $t = 2 \implies (x, y, z) = (-1, 1, 2)$:
  $-1 + 1 + 2 = 2$ (Eq 1), $2(-1) + 2(1) + 2(2) = 4$ (Eq 2), $-1 - 1 + 2 = 0$ (Eq 3).
  All satisfied.

## 8. Common Mistakes
- Setting $y$ as a free variable when $y$ is actually fixed at $y = 1$.
- Forgetting to write the solution in terms of the parameter $t$.

## 9. Short In-Class Explanation (3 Sentences)
Because the second equation is just twice the first, row elimination produces an entire row of zeros, leaving two independent equations for three unknowns. We set the unpivoted variable $z = t$ as our free parameter, which fixes $y = 1$ and gives $x = 1 - t$. Testing the parameter value $t = 0$ gives the point $(1, 1, 0)$, which satisfies all three equations and confirms the infinite line of solutions.
