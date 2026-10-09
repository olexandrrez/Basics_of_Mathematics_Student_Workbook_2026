# Problem 01: Line Through Two Points

## 1. Original Problem
Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## 2. What We Are Trying to Find
We must determine the parametric vector equation and general Cartesian equation of the 2D line passing through points $A$ and $B$, identify its direction vector $v$ and normal vector $n$, and verify both forms by substituting points $A$ and $B$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Direction Vector**: $v = \overrightarrow{AB} = B - A = (x_B - x_A, y_B - y_A)$.
- **Parametric Form**: $(x, y) = A + t v = (x_A + t v_1, y_A + t v_2)$ for $t \in \mathbb{R}$.
- **Normal Vector**: Any non-zero vector $n = (A, B)$ perpendicular to $v$ ($n \cdot v = 0$). For $v = (v_1, v_2)$, a standard normal is $n = (-v_2, v_1)$ or $(v_2, -v_1)$.
- **General Form**: $A(x - x_0) + B(y - y_0) = 0 \iff Ax + By + C = 0$.

## 4. Step-by-Step Solution

### Step 1: Find a Direction Vector $v$
Subtract point $A=(1, 2)$ from $B=(4, -1)$:
$$v = B - A = (4 - 1, -1 - 2) = (3, -3).$$
We can simplify by dividing by $3$ to use the convenient direction vector:
$$v = (1, -1).$$

### Step 2: Write the Parametric Form
Using point $A=(1, 2)$ and direction $v=(1, -1)$:
$$\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 \\ 2 \end{pmatrix} + t \begin{pmatrix} 1 \\ -1 \end{pmatrix}, \quad t \in \mathbb{R},$$
or parametrically:
$$\begin{cases} x = 1 + t, \\ y = 2 - t. \end{cases}$$

### Step 3: Find a Normal Vector $n$
A normal vector $n = (n_1, n_2)$ must satisfy $n \cdot v = 0$:
$$n_1(1) + n_2(-1) = 0 \implies n_1 - n_2 = 0 \implies n_1 = n_2.$$
Choosing $n_1 = 1$ gives the normal vector:
$$n = (1, 1).$$

### Step 4: Write the General Form
Using normal vector $n = (1, 1)$ and base point $A=(1, 2)$:
$$1(x - 1) + 1(y - 2) = 0 \implies x - 1 + y - 2 = 0 \implies x + y - 3 = 0.$$
(or $x + y = 3$).

### Step 5: Check Both Points in the General Equation
1. Substitute point $A=(1, 2)$:
   $$1 + 2 - 3 = 3 - 3 = 0. \quad (\text{True})$$
2. Substitute point $B=(4, -1)$:
   $$4 + (-1) - 3 = 4 - 4 = 0. \quad (\text{True})$$
Both points satisfy the general equation. In parametric form, $t = 0$ yields point $A$, and $t = 3$ yields $x = 1+3=4, y = 2-3=-1$, which is point $B$.

## 5. Why Each Step Is Valid
- The direction vector accurately captures the orientation connecting $A$ and $B$.
- The dot product $(1, 1) \cdot (1, -1) = 1 - 1 = 0$ confirms that $n$ is orthogonal to the line.
- The general form represents the locus of points whose displacement from $A$ is orthogonal to $n$.

## 6. Final Answer in Words
The direction vector is $v = (1, -1)$ (or $(3, -3)$), and a normal vector is $n = (1, 1)$. The parametric form is $(x, y) = (1, 2) + t(1, -1)$, and the general form is $x + y - 3 = 0$. Substituting points $A(1, 2)$ and $B(4, -1)$ produces $0=0$ in both cases, verifying the equations.

## 7. Quick Verification
- Slope check: $m = \frac{-1 - 2}{4 - 1} = \frac{-3}{3} = -1$.
  Slope-intercept form: $y - 2 = -1(x - 1) \implies y = -x + 3 \implies x + y - 3 = 0$.
  Matches the general form.

## 8. Common Mistakes
- Misidentifying the normal vector from the direction vector: writing $(1, -1)$ as normal instead of $(1, 1)$.
- Sign error in subtracting coordinates for $v$: $-1 - 2 = -3$, not $+1$.

## 9. Short In-Class Explanation (3 Sentences)
We find the direction vector $v = (1, -1)$ by subtracting $A$ from $B$, which gives the parametric equation $(x, y) = (1, 2) + t(1, -1)$. A perpendicular normal vector is $n = (1, 1)$, leading to the general Cartesian equation $x + y - 3 = 0$. Substituting both original points $A(1, 2)$ and $B(4, -1)$ into the general equation yields zero, confirming that both points lie on the line.
