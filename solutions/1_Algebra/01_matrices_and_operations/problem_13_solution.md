# Problem 13: A Recurrence Written in Matrix Form

## 1. Original Problem
Let
$$F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.$$
Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence
$$0,1,1,2,3,5,8,\ldots$$
and describe the relationship you observe. Then compute
$$F\begin{pmatrix}a\\b\end{pmatrix}$$
and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## 2. What We Are Trying to Find
We need to calculate powers $F^2, F^3, F^4, F^5$ of the Fibonacci transition matrix, connect its entries to the Fibonacci numbers, and analyze how multiplying a state vector $(a, b)^T$ by $F$ generates the next term in the recurrence relation.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Fibonacci Sequence**: Defined by $F_0 = 0, F_1 = 1, F_2 = 1, F_3 = 2, F_4 = 3, F_5 = 5, F_6 = 8, F_7 = 13$, with the recurrence $F_{k+1} = F_k + F_{k-1}$.
- **Matrix Representation of Linear Recurrences**: A second-order recurrence $x_{k+1} = x_k + x_{k-1}$ can be rewritten as a first-order vector system:
  $$\begin{pmatrix} x_{k+1} \\ x_k \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} x_k \\ x_{k-1} \end{pmatrix}.$$

## 4. Step-by-Step Solution

### Step 1: Compute the Matrix Powers
- Given $F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$.
- Compute $F^2$:
  $$F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1)+1(1) & 1(1)+1(0) \\ 1(1)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}.$$
- Compute $F^3$:
  $$F^3 = F^2 F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2+1 & 2+0 \\ 1+1 & 1+0 \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}.$$
- Compute $F^4$:
  $$F^4 = F^3 F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3+2 & 3+0 \\ 2+1 & 2+0 \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}.$$
- Compute $F^5$:
  $$F^5 = F^4 F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5+3 & 5+0 \\ 3+2 & 3+0 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}.$$

### Step 2: Compare with the Fibonacci Sequence
The standard Fibonacci sequence is $F_0=0, F_1=1, F_2=1, F_3=2, F_4=3, F_5=5, F_6=8$.
Comparing with our computed matrices:
- $F^1 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} F_2 & F_1 \\ F_1 & F_0 \end{pmatrix}$.
- $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} F_3 & F_2 \\ F_2 & F_1 \end{pmatrix}$.
- $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} = \begin{pmatrix} F_4 & F_3 \\ F_3 & F_2 \end{pmatrix}$.
- $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} F_5 & F_4 \\ F_4 & F_3 \end{pmatrix}$.
- $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix} = \begin{pmatrix} F_6 & F_5 \\ F_5 & F_4 \end{pmatrix}$.
In general, $F^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}$.

### Step 3: Compute $F \begin{pmatrix} a \\ b \end{pmatrix}$ and Explain the Mechanism
$$F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1(a) + 1(b) \\ 1(a) + 0(b) \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}.$$
**Explanation of the recurrence step**:
- The top entry $a+b$ computes the sum of the two preceding terms, producing the next Fibonacci term.
- The bottom entry $a$ shifts the most recent term down to be remembered for the subsequent step.
Thus, multiplying by $F$ precisely advances the sequence by one step.

## 5. Why Each Step Is Valid
- Matrix multiplication computes the row dot products $(1 \cdot a + 1 \cdot b)$ and $(1 \cdot a + 0 \cdot b)$, directly embodying the linear shift operator for Fibonacci recurrence.
- By associativity, $F^n$ advances the state vector by $n$ steps.

## 6. Final Answer in Words
The powers are $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$, $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$, $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$, and $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$. The entries in $F^n$ are consecutive Fibonacci numbers: $\begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}$. Multiplying by $\begin{pmatrix} a \\ b \end{pmatrix}$ yields $\begin{pmatrix} a+b \\ a \end{pmatrix}$, which replaces the pair of terms with their sum and the newer term.

## 7. Quick Verification
- Compute $\det(F) = 1(0) - 1(1) = -1$.
  By the determinant product rule, $\det(F^n) = (\det F)^n = (-1)^n$.
  For $F^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}$, its determinant is:
  $$F_{n+1} F_{n-1} - F_n^2 = (-1)^n.$$
  This is Cassini's Identity for Fibonacci numbers. For $n=3$: $F_4 F_2 - F_3^2 = 3(1) - 2^2 = 3 - 4 = -1 = (-1)^3$. Perfect consistency.

## 8. Common Mistakes
- Misaligning indices of the Fibonacci numbers (e.g., claiming the top-left entry of $F^3$ is $F_3$ rather than $F_4$).
- Misunderstanding how the state vector $(a, b)^T$ updates, confusing which entry represents the newer term.

## 9. Short In-Class Explanation (3 Sentences)
The powers of $F$ yield matrices whose entries are consecutive Fibonacci numbers, with $F^5$ having entries $8, 5, 5, 3$. Multiplying $F$ by a vector $(a, b)^T$ produces $(a+b, a)^T$, which adds the two terms to create the next number while keeping the previous term. This shows that matrix powers allow us to compute terms of recurrence relations using matrix algebra.
