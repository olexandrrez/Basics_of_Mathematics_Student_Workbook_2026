# Problem 07: Identity Matrix, Zero Matrix, and Powers

## 1. Original Problem
For
$$A=\begin{pmatrix}2&1\\0&2\end{pmatrix}$$
compute
$$AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.$$
Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## 2. What We Are Trying to Find
We must evaluate operations involving the identity matrix $I$, the zero matrix $0$, and repeated matrix powers $A^2$ and $A^3$, describe their algebraic properties, and find the general formula for $A^n$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Identity Matrix $I$**: Acts as the multiplicative identity: $AI = IA = A$ for any compatible square matrix. Here, $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$.
- **Zero Matrix $0$**: Acts as the additive identity: $A + 0 = A$. Here, $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$.
- **Matrix Powers**: $A^k = A^{k-1} A$ with $A^1 = A$. For triangular matrices of this form, the diagonal entries are powered, and the superdiagonal entry exhibits a clear binomial or linear pattern.

## 4. Step-by-Step Solution

### Step 1: Compute $AI$, $IA$, and $A+0$
- $AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2(1)+1(0) & 2(0)+1(1) \\ 0(1)+2(0) & 0(0)+2(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A$.
- $IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1(2)+0(0) & 1(1)+0(2) \\ 0(2)+1(0) & 0(1)+1(2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A$.
- $A+0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A$.

### Step 2: Compute $A^2$
$$A^2 = A \cdot A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2(2)+1(0) & 2(1)+1(2) \\ 0(2)+2(0) & 0(1)+2(2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}.$$

### Step 3: Compute $A^3$
$$A^3 = A^2 \cdot A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4(2)+4(0) & 4(1)+4(2) \\ 0(2)+4(0) & 0(1)+4(2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}.$$

### Step 4: Describe the Roles and Pattern
- **Role of $I$ and $0$**: $I$ is the neutral element for matrix multiplication (leaving any matrix unchanged under multiplication), while $0$ is the neutral element for matrix addition (leaving any matrix unchanged under addition).
- **Pattern in Powers**:
  - For $n=1$: $A = \begin{pmatrix} 2^1 & 1 \cdot 2^0 \\ 0 & 2^1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$.
  - For $n=2$: $A^2 = \begin{pmatrix} 2^2 & 2 \cdot 2^1 \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$.
  - For $n=3$: $A^3 = \begin{pmatrix} 2^3 & 3 \cdot 2^2 \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$.
  In general, for any integer $n \ge 1$:
  $$A^n = \begin{pmatrix} 2^n & n 2^{n-1} \\ 0 & 2^n \end{pmatrix}.$$

## 5. Why Each Step Is Valid
- The identity matrix consists of the standard basis vectors as columns, which reproduce each column of $A$ unchanged under multiplication.
- Associativity of matrix multiplication allows computing $A^3$ as $A^2 A$.
- Writing $A = 2I + N$ where $N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$ commutes with $2I$, the binomial theorem gives $A^n = (2I)^n + n(2I)^{n-1}N + 0$, explaining the exact formula $n 2^{n-1}$ for the upper-right entry.

## 6. Final Answer in Words
$AI = A$, $IA = A$, and $A+0 = A$. The second and third powers are $A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$ and $A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$. The identity matrix $I$ acts as the number 1 in multiplication, and the zero matrix acts as 0 in addition. The general $n$-th power has $2^n$ on the main diagonal and $n 2^{n-1}$ in the upper-right corner.

## 7. Quick Verification
- Check $n=1$: $1 \cdot 2^0 = 1$, which gives $A$.
- Compute $A^4$ from formula: $2^4 = 16$, upper-right entry $4 \cdot 2^3 = 32$.
  Check by multiplication: $A^3 A = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 16 & 8 + 24 \\ 0 & 16 \end{pmatrix} = \begin{pmatrix} 16 & 32 \\ 0 & 16 \end{pmatrix}$. Matches perfectly.

## 8. Common Mistakes
- Thinking $A^2$ is formed by squaring each entry individually (which would incorrectly give $\begin{pmatrix} 4 & 1 \\ 0 & 4 \end{pmatrix}$).
- Guessing the top-right entry in $A^3$ is simply $1^3 = 1$ rather than performing matrix multiplication.

## 9. Short In-Class Explanation (3 Sentences)
Multiplying by the identity matrix leaves $A$ unchanged, and adding the zero matrix also leaves $A$ unchanged, showing they are the neutral elements of multiplication and addition. Computing successive powers reveals that $A^2 = \begin{pmatrix}4&4\\0&4\end{pmatrix}$ and $A^3 = \begin{pmatrix}8&12\\0&8\end{pmatrix}$. In general, the diagonal entries grow as $2^n$ while the upper-right entry grows as $n \cdot 2^{n-1}$.
