# Problem 02: A Line in Space

## 1. Original Problem
Given
$$L:(x,y,z)=(2,-1,3)+t(1,2,-2).$$
State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

## 2. What We Are Trying to Find
We must extract a base point and direction vector from the parametric line equation in $\mathbb{R}^3$, test if point $P = (4, 3, -1)$ belongs to line $L$, and evaluate the spatial coordinates of the point on $L$ where parameter $t = -1$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Parametric Form of a 3D Line**: $L: \mathbf{r}(t) = P_0 + t v$, where $P_0$ is a fixed point on the line and $v$ is the direction vector along the line.
- **Point-Inclusion Test**: A point $P$ lies on the line if and only if there exists a **single unique scalar $t$** that simultaneously satisfies all three coordinate equations:
  $$x_P = x_0 + t v_1, \quad y_P = y_0 + t v_2, \quad z_P = z_0 + t v_3.$$
  If different coordinates require conflicting values of $t$, the point does not lie on the line.

## 4. Step-by-Step Solution

### Step 1: Identify Base Point and Direction Vector
From the equation $(x,y,z) = (2,-1,3) + t(1,2,-2)$:
- **Base Point (for $t=0$)**: $P_0 = (2, -1, 3)$.
- **Direction Vector**: $v = (1, 2, -2)$.

### Step 2: Check Whether $P = (4, 3, -1)$ Lies on $L$
Set $(x, y, z) = (4, 3, -1)$ in the coordinate equations:
$$\begin{cases} 4 = 2 + 1t \\ 3 = -1 + 2t \\ -1 = 3 - 2t \end{cases}$$
1. From the $x$-equation:
   $$4 = 2 + t \implies t = 2.$$
2. Test $t = 2$ in the $y$-equation:
   $$-1 + 2(2) = -1 + 4 = 3.$$
   This matches $y = 3$!
3. Test $t = 2$ in the $z$-equation:
   $$3 - 2(2) = 3 - 4 = -1.$$
   This matches $z = -1$!
Since $t = 2$ satisfies all three coordinates simultaneously, point $P = (4, 3, -1)$ **lies on line $L$**.

### Step 3: Find the Point Corresponding to $t = -1$
Substitute $t = -1$ into the parametric equation:
$$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} + (-1) \begin{pmatrix} 1 \\ 2 \\ -2 \end{pmatrix} = \begin{pmatrix} 2 - 1 \\ -1 - 2 \\ 3 - (-2) \end{pmatrix} = \begin{pmatrix} 1 \\ -3 \\ 3 + 2 \end{pmatrix} = \begin{pmatrix} 1 \\ -3 \\ 5 \end{pmatrix}.$$
The point corresponding to $t = -1$ is $Q = (1, -3, 5)$.

## 5. Why Each Step Is Valid
- In $\mathbb{R}^3$, a line is a 1-dimensional manifold; each value of parameter $t$ bijectively indexes a single point in space.
- Agreement across all three coordinate equations confirms that $P$ is collinear with $P_0$ along direction $v$.

## 6. Final Answer in Words
A point on the line is $(2, -1, 3)$ and its direction vector is $(1, 2, -2)$. The point $P = (4, 3, -1)$ lies on line $L$ because setting $t = 2$ satisfies all three coordinate equations simultaneously. For $t = -1$, the corresponding point on the line is $(1, -3, 5)$.

## 7. Quick Verification
- Check vector $\overrightarrow{P_0 P}$:
  $$P - P_0 = (4 - 2, 3 - (-1), -1 - 3) = (2, 4, -4) = 2(1, 2, -2) = 2v.$$
  Since $\overrightarrow{P_0 P}$ is a scalar multiple of $v$, $P$ lies on the line.
- Check vector $\overrightarrow{P_0 Q}$ for $t = -1$:
  $$Q - P_0 = (1 - 2, -3 - (-1), 5 - 3) = (-1, -2, 2) = -1(1, 2, -2) = -1v.$$
  Verified.

## 8. Common Mistakes
- Checking $t = 2$ only in the first equation and concluding the point lies on the line without checking $y$ and $z$.
- Arithmetic sign error in computing $3 - (-2) = 5$ for the $z$-coordinate when $t = -1$.

## 9. Short In-Class Explanation (3 Sentences)
The line has base point $(2, -1, 3)$ and direction vector $(1, 2, -2)$. Point $P = (4, 3, -1)$ lies on the line because the parameter value $t = 2$ produces the correct coordinates across all three axes. Substituting $t = -1$ into the parametric equation yields the coordinates $(1, -3, 5)$ for that specific point on the line.
