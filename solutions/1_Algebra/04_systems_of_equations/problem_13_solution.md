# Problem 13: Does Every Equation Add New Information?

## 1. Original Problem
Consider the system
$$x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.$$
Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## 2. What We Are Trying to Find
We must determine whether the three given equations are linearly independent or whether one equation is redundant, demonstrate the algebraic dependence explicitly, solve the system, and describe the resulting solution set.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Linear Redundancy of Equations**: An equation in a linear system adds no new information if it is a linear combination of the remaining equations.
- **Algebraic Test**: If subtracting Equation 2 from Equation 1 reproduces Equation 3 identically, then Equation 3 is mathematically redundant.

## 4. Step-by-Step Solution

### Step 1: Test for Linear Dependence Among the Equations
Look at the three equations:
$$(1) \quad x_1 + x_2 = 10,$$
$$(2) \quad x_2 + x_3 = 8,$$
$$(3) \quad x_1 - x_3 = 2.$$
Subtract Equation (2) from Equation (1):
$$(x_1 + x_2) - (x_2 + x_3) = 10 - 8.$$
Simplify the left-hand side:
$$x_1 + x_2 - x_2 - x_3 = x_1 - x_3.$$
Simplify the right-hand side:
$$10 - 8 = 2.$$
The resulting equation is:
$$x_1 - x_3 = 2.$$
This is **identically Equation (3)**!
Therefore:
$$\text{Equation (3)} = \text{Equation (1)} - \text{Equation (2)}.$$
Equation (3) adds zero new information: any values of $(x_1, x_2, x_3)$ that satisfy Equations (1) and (2) are automatically guaranteed to satisfy Equation (3).

### Step 2: Solve the System
Because Equation (3) follows from the first two, the system has only 2 independent equations for 3 variables:
$$\begin{cases} x_1 + x_2 = 10, \\ x_2 + x_3 = 8. \end{cases}$$
Choose $x_3 = t \in \mathbb{R}$ as the free parameter.
1. From Equation (2):
   $$x_2 = 8 - x_3 = 8 - t.$$
2. From Equation (1):
   $$x_1 = 10 - x_2 = 10 - (8 - t) = 2 + t.$$

### Step 3: Write the Solution in Parametric Form
$$\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 2 + t \\ 8 - t \\ t \end{pmatrix} = \begin{pmatrix} 2 \\ 8 \\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.$$

## 5. Why Each Step Is Valid
- If $L_1(x) = b_1$ and $L_2(x) = b_2$, then $(L_1 - L_2)(x) = b_1 - b_2$ is an algebraic identity satisfied by all solutions.
- Since the rank of the system is 2 and there are 3 variables, the solution set is a 1-dimensional line.

## 6. Final Answer in Words
Not all three equations are necessary: the third equation is redundant because subtracting the second equation from the first yields $x_1 - x_3 = 2$, which is exactly the third equation. The system has infinitely many solutions parameterized by $x_3 = t$: $x_1 = 2 + t$, $x_2 = 8 - t$, and $x_3 = t$ for any $t \in \mathbb{R}$.

## 7. Quick Verification
- Check Equation (3) with the parametric solution:
  $$x_1 - x_3 = (2 + t) - t = 2.$$
  It holds identically for every $t$!
- Test $t = 0$: $(x_1, x_2, x_3) = (2, 8, 0)$.
  $2 + 8 = 10$ (Eq 1), $8 + 0 = 8$ (Eq 2), $2 - 0 = 2$ (Eq 3). All satisfied.

## 8. Common Mistakes
- Assuming that because there are 3 equations with 3 unknowns, the system must have a single unique solution.
- Failing to write out the explicit calculation $(x_1 + x_2) - (x_2 + x_3) = 10 - 8$ proving the redundancy.

## 9. Short In-Class Explanation (3 Sentences)
Subtracting the second equation from the first gives $(x_1 + x_2) - (x_2 + x_3) = 10 - 8$, which simplifies directly to $x_1 - x_3 = 2$. Because this matches the third equation exactly, the third equation adds no new information and is redundant. Therefore, the system has only two independent constraints, resulting in an infinite line of solutions parameterized by $(2+t, 8-t, t)^T$.
