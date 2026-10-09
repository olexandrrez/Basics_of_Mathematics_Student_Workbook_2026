# Problem 11: When Do Matrices Commute?

## 1. Original Problem
Given
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.$$
Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## 2. What We Are Trying to Find
We must determine the necessary and sufficient algebraic constraints on the four entries $a, b, c, d$ of matrix $B$ such that $AB = BA$, and describe the resulting space of commuting matrices.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Commuting Matrices**: Two matrices commute if $AB = BA$.
- **Centralizer of a Matrix**: The set of all matrices that commute with a given matrix $A$ forms a subspace (the centralizer of $A$). We set up the matrix equation $AB - BA = 0$ and equate each entry to zero to solve for the free parameters.

## 4. Step-by-Step Solution

### Step 1: Compute $AB$
$$AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} 1(a)+1(c) & 1(b)+1(d) \\ 0(a)+1(c) & 0(b)+1(d) \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}.$$

### Step 2: Compute $BA$
$$BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a(1)+b(0) & a(1)+b(1) \\ c(1)+d(0) & c(1)+d(1) \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}.$$

### Step 3: Equate Corresponding Entries
For $AB = BA$, all four corresponding entries must be equal:
1. Top-left: $a + c = a \implies c = 0$.
2. Bottom-left: $c = c$ (identically satisfied once $c=0$, $0=0$).
3. Top-right: $b + d = a + b \implies d = a$.
4. Bottom-right: $d = c + d \implies c = 0$ (consistent with equation 1).

### Step 4: Describe the General Form of Matrix $B$
The conditions are:
$$c = 0 \quad \text{and} \quad d = a.$$
The parameters $a$ and $b$ can be chosen as any real numbers ($a, b \in \mathbb{R}$).
Therefore, the general form of all such matrices $B$ is:
$$B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}.$$
This can also be written as:
$$B = a \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} + b \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} = a I + b (A - I).$$

## 5. Why Each Step Is Valid
- Two matrices are equal if and only if their corresponding entries at every coordinate $(i, j)$ are equal.
- Equating entries yields a linear system in the unknowns $a, b, c, d$. Solving this system gives the exact conditions without loss of generality.

## 6. Final Answer in Words
Matrices $A$ and $B$ commute if and only if $c = 0$ and $d = a$, with $a$ and $b$ arbitrary real numbers. The general form of all commuting matrices is $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$, which is an upper-triangular matrix with identical diagonal entries.

## 7. Quick Verification
- Choose test values $a = 3$, $b = 5$, so $B = \begin{pmatrix} 3 & 5 \\ 0 & 3 \end{pmatrix}$.
  $$AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 5 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 5+3 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 8 \\ 0 & 3 \end{pmatrix}.$$
  $$BA = \begin{pmatrix} 3 & 5 \\ 0 & 3 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 3 & 3+5 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 8 \\ 0 & 3 \end{pmatrix}.$$
  $AB = BA$ holds.
- Test a non-conforming matrix with $c=1$: $A \begin{pmatrix}1&0\\1&1\end{pmatrix} = \begin{pmatrix}2&1\\1&1\end{pmatrix} \neq \begin{pmatrix}1&1\\1&2\end{pmatrix}$. Fails as expected.

## 8. Common Mistakes
- Concluding that only scalar multiples of $A$ commute ($B = k A$); this misses the fact that the upper-right entry $b$ is completely independent of $a$.
- Forgetting to check all 4 entries, missing the requirement $c = 0$.

## 9. Short In-Class Explanation (3 Sentences)
We compute $AB$ and $BA$ in terms of the unknown entries $a, b, c, d$ and set the corresponding entries equal to each other. This yields two conditions: $c$ must be zero, and $d$ must equal $a$, while $b$ remains completely free. Consequently, all matrices that commute with $A$ must be upper-triangular with identical entries on the main diagonal.
