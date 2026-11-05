# Problem 8: Solutions of a Homogeneous System

## Problem

Find all solutions of
$$\begin{cases}x+2y-z=0,\\2x+4y-2z=0.\end{cases}$$
Express the solution as a linear combination of two vectors.

## Worked Solution

The second equation is twice the first, so there is only one independent condition. Rearranging the first gives $z=x+2y$. Let the free variables be $x=s$ and $y=t$. Then
$$\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}s\\t\\s+2t\end{pmatrix}=s\begin{pmatrix}1\\0\\1\end{pmatrix}+t\begin{pmatrix}0\\1\\2\end{pmatrix},\qquad s,t\in\mathbb R.$$

**Answer:** $\boxed{(x,y,z)=s(1,0,1)+t(0,1,2)}$ for arbitrary real $s,t$.

**Check.** Each spanning vector satisfies $x+2y-z=0$, and therefore also satisfies the second equation, which is its double. Their independent free parameters describe every choice of $x$ and $y$.
