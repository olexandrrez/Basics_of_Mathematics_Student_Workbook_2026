# Problem 3: Cramer's Rule for a 2×2 System

## Problem

Solve
$$\begin{cases}2x+y=7,\\x-y=2\end{cases}$$
using Cramer's rule. Check the condition for using the rule.

## Worked Solution

The coefficient matrix is $A=\begin{pmatrix}2&1\\1&-1\end{pmatrix}$, whose determinant is
$$\Delta=2(-1)-1(1)=-3\ne0.$$
Thus the system has a unique solution and Cramer's rule applies. Replacing the first column with the constants gives
$$\Delta_x=\det\begin{pmatrix}7&1\\2&-1\end{pmatrix}=-7-2=-9,$$
so $x=\Delta_x/\Delta=3$. Replacing the second column gives
$$\Delta_y=\det\begin{pmatrix}2&7\\1&2\end{pmatrix}=4-7=-3,$$
so $y=\Delta_y/\Delta=1$.

**Answer and check:** $(x,y)=\boxed{(3,1)}$. Substitution yields $2(3)+1=7$ and $3-1=2$.
