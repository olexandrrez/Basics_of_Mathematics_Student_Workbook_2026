# Problem 01: Matrix Size and Entries

## 1. Original Problem
Given:
$$A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## 2. What We Are Trying to Find
We need to determine the dimensions (rows $\times$ columns) of two rectangular matrices, extract specific entries identified by coordinate indices, and write out a specific row and column as vector objects.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Matrix Dimensions ($m \times n$)**: The size of a matrix is written as $m \times n$, where $m$ is the number of horizontal rows and $n$ is the number of vertical columns.
- **Entry Coordinates ($a_{ij}$)**: In a matrix $A$, $a_{ij}$ denotes the entry in row $i$ and column $j$.
- **Row and Column Vectors**: Slicing along row index $i$ gives a $1 \times n$ row vector, while slicing along column index $j$ gives an $m \times 1$ column vector.

## 4. Step-by-Step Solution

### Step 1: Determine Dimensions
- Matrix $A$ has $2$ rows and $3$ columns, so its size is $2 \times 3$.
- Matrix $B$ has $3$ rows and $2$ columns, so its size is $3 \times 2$.

### Step 2: Read Off Specified Entries
- For $a_{12}$: in matrix $A$, row $1$, column $2$ contains $-1$. So $a_{12} = -1$.
- For $a_{23}$: in matrix $A$, row $2$, column $3$ contains $5$. So $a_{23} = 5$.
- For $b_{21}$: in matrix $B$, row $2$, column $1$ contains $-2$. So $b_{21} = -2$.
- For $b_{32}$: in matrix $B$, row $3$, column $2$ contains $1$. So $b_{32} = 1$.

### Step 3: Extract Row and Column Vectors
- The second row of $A$ ($i=2$) consists of entries $a_{21}=0, a_{22}=4, a_{23}=5$. As a vector, this is:
  $$\mathbf{r}_2(A) = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$$
- The first column of $B$ ($j=1$) consists of entries $b_{11}=1, b_{21}=-2, b_{31}=4$. As a vector, this is:
  $$\mathbf{c}_1(B) = \begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$$

## 5. Why Each Step Is Valid
- Dimensions are counted directly from the grid layout where rows run horizontally and columns run vertically.
- Indices $(i, j)$ refer unambiguously to row $i$ and column $j$ in Cartesian array ordering.
- Row vectors and column vectors preserve the exact ordered components along the respective slice.

## 6. Final Answer in Words
Matrix $A$ has size $2 \times 3$ and matrix $B$ has size $3 \times 2$. The requested entries are $a_{12} = -1$, $a_{23} = 5$, $b_{21} = -2$, and $b_{32} = 1$. The second row of $A$ is $(0, 4, 5)$ and the first column of $B$ is $(1, -2, 4)^T$.

## 7. Quick Verification
- $A$ has $2 \times 3 = 6$ total numbers, matching its appearance. $B$ has $3 \times 2 = 6$ numbers.
- Visually inspecting the bottom-right of $A$ shows $5 = a_{23}$. Inspecting row 2, column 1 of $B$ confirms $-2 = b_{21}$.

## 8. Common Mistakes
- Swapping the row and column order (e.g., calling $A$ a $3 \times 2$ matrix). Remember: Rows first, Columns second ("RC").
- Reading $a_{12}$ as column 1, row 2 instead of row 1, column 2.

## 9. Short In-Class Explanation (3 Sentences)
To find the size of a matrix, count rows first and columns second, giving $2 \times 3$ for $A$ and $3 \times 2$ for $B$. The notation $a_{ij}$ means the entry in row $i$ and column $j$, so $a_{12} = -1$ and $b_{21} = -2$. Slicing across row 2 of $A$ gives $(0, 4, 5)$, and down column 1 of $B$ gives $(1, -2, 4)^T$.
