# Problem 7: Determinant by Sarrus' Rule

## Problem

Calculate
$$\det\begin{pmatrix}2&1&0\\-1&3&2\\1&0&4\end{pmatrix}$$
using Sarrus' rule. State why this rule is applicable.

## Worked Solution

Sarrus' rule applies to a $3\times3$ determinant. Add the products of the three diagonals running down-right, then subtract the products of the three diagonals running down-left:
$$\det A=(2\cdot3\cdot4+1\cdot2\cdot1+0\cdot(-1)\cdot0)-(0\cdot3\cdot1+2\cdot2\cdot0+1\cdot(-1)\cdot4).$$
The first sum is $24+2+0=26$, and the second is $0+0-4=-4$. Therefore
$$\det A=26-(-4)=\boxed{30}.$$

**Check.** The rule is being used on exactly three rows and three columns, its required matrix size.
