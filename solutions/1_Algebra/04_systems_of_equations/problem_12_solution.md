# Problem 12: Homogeneous System

## 1. Original Problem
Solve
$$\begin{cases}x+2y-z=0,\\2x+4y-2z=0,\\x-y+2z=0.\end{cases}$$
Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## 2. What We Are Trying to Find
We must determine the complete solution set of a homogeneous linear system (where all right-hand side constants are zero), express the solution space in parametric vector form, and explain why the trivial zero vector is guaranteed to be a solution for any homogeneous system.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Homogeneous Linear System**: A system of the form $Ax = 0$.
- **The Trivial Solution**: The zero vector $x = 0 = (0, 0, \dots, 0)^T$ always satisfies $Ax = 0$ because multiplying any matrix by the zero vector yields zero: $A \cdot 0 = 0$.
- **Non-trivial Solutions**: A homogeneous system has non-trivial (non-zero) solutions if and only if $\det A = 0$ (or equivalently, $\operatorname{rank}(A) < n$).

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix
$$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right].$$

### Step 2: Perform Row Elimination
1. Notice that Row 2 is exactly $2 \times$ Row 1.
   Perform $R_2 \leftarrow R_2 - 2R_1$:
   $$(2, 4, -2 \mid 0) - 2(1, 2, -1 \mid 0) = (0, 0, 0 \mid 0).$$
   Row 2 is entirely zero.
2. Eliminate $x$ from Row 3 using $R_3 \leftarrow R_3 - R_1$:
   $$(1, -1, 2 \mid 0) - (1, 2, -1 \mid 0) = (0, -3, 3 \mid 0).$$
Swap $R_2$ and $R_3$:
$$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & -3 & 3 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

### Step 3: Identify Free Variables and Parameterize
- Pivot in Col 1 ($x$) and Col 2 ($y$).
- Col 3 ($z$) has no pivot; therefore, $z$ is a free variable.
Let $z = t$, where $t \in \mathbb{R}$.

1. From Row 2:
   $$-3y + 3z = 0 \implies -3y + 3t = 0 \implies 3y = 3t \implies y = t.$$
2. From Row 1:
   $$x + 2y - z = 0 \implies x + 2t - t = 0 \implies x + t = 0 \implies x = -t.$$

### Step 4: Write Solution in Parametric Form
$$\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} -t \\ t \\ t \end{pmatrix} = t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.$$

### Step 5: Explain Why $(0, 0, 0)$ Always Satisfies a Homogeneous System
In any homogeneous system $Ax = 0$:
- Each equation has the form $a_{i1} x_1 + a_{i2} x_2 + \dots + a_{in} x_n = 0$.
- Substituting $x_1 = 0, x_2 = 0, \dots, x_n = 0$ into the left-hand side gives:
  $$a_{i1}(0) + a_{i2}(0) + \dots + a_{in}(0) = 0 + 0 + \dots + 0 = 0.$$
Because every term is multiplied by zero, the sum is identically zero, which matches the right-hand side $0$ regardless of the coefficients.
In our parametric solution, setting $t = 0$ yields $(x, y, z) = (0, 0, 0)$, verifying that the trivial solution is included in the solution subspace.

## 5. Why Each Step Is Valid
- Homogeneous systems are always consistent (the zero vector is always in the kernel).
- Since the rank is $2 < 3$, the null space has dimension $3 - 2 = 1$, forming a line through the origin spanned by $(-1, 1, 1)^T$.

## 6. Final Answer in Words
The solutions form a one-dimensional line parameterized by $t \in \mathbb{R}$: $x = -t$, $y = t$, and $z = t$, or vectorially $t(-1, 1, 1)^T$. The point $(0, 0, 0)$ always satisfies any homogeneous system because multiplying any set of coefficients by zero always sums to zero.

## 7. Quick Verification
- Check $(x, y, z) = (-1, 1, 1)$ (for $t = 1$):
  - Eq 1: $-1 + 2(1) - 1 = -1 + 2 - 1 = 0$. (True)
  - Eq 2: $2(-1) + 4(1) - 2(1) = -2 + 4 - 2 = 0$. (True)
  - Eq 3: $-1 - 1 + 2(1) = -2 + 2 = 0$. (True)
  All satisfied.

## 8. Common Mistakes
- Claiming that because the system has infinitely many solutions, $(0,0,0)$ is not a solution (it is always the base solution at $t=0$).
- Sign error in Row 1: writing $x = t$ instead of $x = -t$.

## 9. Short In-Class Explanation (3 Sentences)
Because the second equation is twice the first, the system reduces to two independent equations, leaving $z = t$ as a free parameter that gives the line of solutions $(-t, t, t)^T$. The zero vector $(0, 0, 0)$ always satisfies every homogeneous system because multiplying any coefficients by zero produces a sum of zero. Here, that trivial solution simply corresponds to choosing parameter value $t = 0$.
