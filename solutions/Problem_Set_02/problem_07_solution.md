# Problem 7: Number of Solutions Depending on a Parameter

## Problem

Discuss the number of solutions of
$$\begin{cases}x+y=2,\\x+ky=k+1\end{cases}$$
for every real $k$, and solve whenever possible.

## Worked Solution

Subtract the first equation from the second. This removes $x$ and gives
$$(k-1)y=k-1.$$

If $k\ne1$, divide by $k-1$ to get $y=1$. The first equation then gives $x=1$, so there is exactly one solution, $(1,1)$.

If $k=1$, both equations reduce to $x+y=2$. They describe the same line, so there are infinitely many solutions:
$$\{(2-t,t):t\in\mathbb R\}.$$

**Conclusion.** For $k\ne1$, the unique solution is $\boxed{(1,1)}$; for $k=1$, there are infinitely many solutions on $x+y=2$. No value of $k$ makes the system inconsistent.

**Check.** $(1,1)$ satisfies both equations for every $k$, including $k=1$.
