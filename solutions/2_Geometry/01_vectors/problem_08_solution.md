# Problem 08: Linear Combination and Checking the Result

## 1. Original Problem
Check whether $w=(5,1)$ can be written as
$$w=au+bv,$$
where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## 2. What We Are Trying to Find
We must determine whether vector $w$ can be expressed as a linear combination of vectors $u$ and $v$, find the scalar weights $a$ and $b$ by solving the resulting system of equations, reconstruct $w$ to verify, and explain the geometric meaning of this decomposition in $\mathbb{R}^2$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Linear Combination in $\mathbb{R}^2$**: $w = a u + b v$ means:
  $$a \begin{pmatrix} 1 \\ 1 \end{pmatrix} + b \begin{pmatrix} 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix}.$$
- **Basis Property**: Two non-zero vectors in $\mathbb{R}^2$ form a basis for $\mathbb{R}^2$ if and only if they are not collinear (their determinant is non-zero). If they form a basis, **any** vector $w \in \mathbb{R}^2$ can be uniquely written as their linear combination.

## 4. Step-by-Step Solution

### Step 1: Set Up the Linear System
Write the vector equation componentwise:
$$\begin{cases} 1a + 2b = 5, \\ 1a - 1b = 1. \end{cases}$$

### Step 2: Solve for $a$ and $b$
Subtract the second equation from the first:
$$(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = \frac{4}{3}.$$
Substitute $b = 4/3$ into the second equation:
$$a - \frac{4}{3} = 1 \implies a = 1 + \frac{4}{3} = \frac{7}{3}.$$
So the coefficients are $a = 7/3$ and $b = 4/3$.

### Step 3: Reconstruct $w$ from $a$ and $b$
Evaluate $au + bv$ using the found coefficients:
$$au + bv = \frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = \left(\frac{7}{3}, \frac{7}{3}\right) + \left(\frac{8}{3}, -\frac{4}{3}\right) = \left(\frac{7+8}{3}, \frac{7-4}{3}\right) = \left(\frac{15}{3}, \frac{3}{3}\right) = (5, 1) = w.$$
The reconstructed vector matches $w$ exactly.

### Step 4: Geometric Meaning of the Coefficients
- Vectors $u = (1, 1)$ and $v = (2, -1)$ are non-parallel (their determinant is $1(-1) - 1(2) = -3 \neq 0$), so they define a valid coordinate grid spanning the entire 2D plane $\mathbb{R}^2$.
- The existence and uniqueness of coefficients $a = 7/3$ and $b = 4/3$ means that to reach point $(5, 1)$ starting from the origin:
  1. We travel $7/3$ units along the direction of vector $u$.
  2. From there, we travel $4/3$ units along the direction of vector $v$.
The coefficients represent the **coordinates of $w$ in the non-orthogonal basis $\{u, v\}$**.

## 5. Why Each Step Is Valid
- Matrix determinant $\det[u \mid v] = -3 \neq 0$ guarantees that the linear system has a unique solution.
- Algebraic substitution and fraction arithmetic solve the system rigorously.

## 6. Final Answer in Words
Vector $w$ can be written as a linear combination of $u$ and $v$ with coefficients $a = 7/3$ and $b = 4/3$: $w = \frac{7}{3}u + \frac{4}{3}v$. Reconstructing the combination yields $(15/3, 3/3) = (5, 1)$, verifying the result. Geometrically, because $u$ and $v$ are not parallel, they form a basis for $\mathbb{R}^2$, and the coefficients $7/3$ and $4/3$ represent the coordinates of $w$ in this new coordinate system.

## 7. Quick Verification
- Check Cramer's rule:
  $D = \det\begin{pmatrix}1&2\\1&-1\end{pmatrix} = -1 - 2 = -3$.
  $D_a = \det\begin{pmatrix}5&2\\1&-1\end{pmatrix} = -5 - 2 = -7 \implies a = -7/(-3) = 7/3$.
  $D_b = \det\begin{pmatrix}1&5\\1&1\end{pmatrix} = 1 - 5 = -4 \implies b = -4/(-3) = 4/3$.
  Cramer's rule yields the exact same coefficients.

## 8. Common Mistakes
- Subtracting equations incorrectly: $(2b) - (-b) = 3b$, not $b$.
- Forgetting to reconstruct $w$ to verify the solution.

## 9. Short In-Class Explanation (3 Sentences)
Setting up the system of equations for the components gives $a + 2b = 5$ and $a - b = 1$, which solves to $a = 7/3$ and $b = 4/3$. Reconstructing $\frac{7}{3}(1, 1) + \frac{4}{3}(2, -1)$ yields $(5, 1)$, verifying the combination. Geometrically, because $u$ and $v$ are non-parallel, they form a basis for the plane, and the coefficients tell us how far to move along each direction to reach $w$.
