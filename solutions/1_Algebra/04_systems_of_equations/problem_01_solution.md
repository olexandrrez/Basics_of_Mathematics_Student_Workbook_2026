# Problem 01: From a System to a Matrix

## 1. Original Problem
Write the system
$$\begin{cases}2x-y+z=4,\\x+3y-2z=1,\\3x+y+z=7.\end{cases}$$
in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## 2. What We Are Trying to Find
We must convert a system of three linear equations in three variables into standard matrix-vector notation $Ax = b$, clearly identifying the coefficient matrix $A$, unknown vector $x$, and constant vector $b$, and explain how matrix multiplication reconstructs each original equation row by row.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Matrix Representation of a Linear System**: A system of linear equations
  $$\sum_{j=1}^n a_{ij} x_j = b_i \quad (i=1, \dots, m)$$
  is compactly written as $Ax = b$, where:
  - $A = (a_{ij})$ is the $m \times n$ **coefficient matrix** containing the coefficients of the unknowns.
  - $x = (x_1, \dots, x_n)^T$ is the $n \times 1$ **vector of unknowns**.
  - $b = (b_1, \dots, b_m)^T$ is the $m \times 1$ **right-hand side vector** of constants.
- **Row-by-Vector Dot Product**: By the definition of matrix-vector multiplication, the $i$-th row of $A$ dotted with $x$ produces the left-hand side of equation $i$.

## 4. Step-by-Step Solution

### Step 1: Align Coefficients and Variables
Align the system in standard order for variables $x, y, z$:
$$\begin{array}{rrrrrcc}
2x & - & 1y & + & 1z & = & 4 \\
1x & + & 3y & - & 2z & = & 1 \\
3x & + & 1y & + & 1z & = & 7
\end{array}$$

### Step 2: Extract the Coefficient Matrix $A$
Collect the coefficients of $x$ (col 1), $y$ (col 2), and $z$ (col 3):
$$A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}.$$

### Step 3: Define the Vector of Unknowns and the Right-Hand Side Vector
- Vector of unknowns:
  $$\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}.$$
- Right-hand side vector:
  $$\mathbf{b} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.$$

### Step 4: Write the Compact Matrix Equation
$$Ax = b \iff \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.$$

### Step 5: Explain Row Correspondence
Matrix-vector multiplication performs dot products row by row:
- Row 1 times $x$: $\begin{pmatrix} 2 & -1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = 2x - y + z$. Setting this equal to the first entry of $b$ gives $2x - y + z = 4$ (Equation 1).
- Row 2 times $x$: $\begin{pmatrix} 1 & 3 & -2 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = x + 3y - 2z$. Setting this equal to the second entry of $b$ gives $x + 3y - 2z = 1$ (Equation 2).
- Row 3 times $x$: $\begin{pmatrix} 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = 3x + y + z$. Setting this equal to the third entry of $b$ gives $3x + y + z = 7$ (Equation 3).
Each horizontal row of matrix $A$ stores the weights of the variables for that specific equation, and the matching entry in vector $b$ holds its constant target value.

## 5. Why Each Step Is Valid
- Matrix-vector multiplication is defined as $(Ax)_i = \sum_{j} A_{ij} x_j$, which identically reproduces linear equations.
- Vector equality requires equality at each coordinate, faithfully representing the simultaneous conditions of the system.

## 6. Final Answer in Words
The system in matrix form is $\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}$. The coefficient matrix is $A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}$, the vector of unknowns is $x = (x, y, z)^T$, and the right-hand side vector is $b = (4, 1, 7)^T$. Row $i$ corresponds to equation $i$ because multiplying row $i$ by the column of variables computes the left-hand side of equation $i$.

## 7. Quick Verification
- Multiplying Row 2: $1(x) + 3(y) - 2(z) = x + 3y - 2z = 1$, which matches the original second equation.
- Check dimensions: $A$ is $3 \times 3$, $x$ is $3 \times 1$, product is $3 \times 1$, matching $b$ ($3 \times 1$).

## 8. Common Mistakes
- Misplacing negative signs when copying coefficients (e.g., writing $+1$ instead of $-1$ for $-y$ in row 1).
- Writing the right-hand side as a row vector rather than a column vector.

## 9. Short In-Class Explanation (3 Sentences)
We extract the coefficients of $x, y, z$ into the matrix $A$, place the variables into vector $x$, and place the constants into vector $b$, forming $Ax = b$. Multiplying any row of $A$ by the vector $x$ produces the left-hand side of the corresponding equation. Thus, each row of the matrix encodes the coefficients of one linear equation in the system.
