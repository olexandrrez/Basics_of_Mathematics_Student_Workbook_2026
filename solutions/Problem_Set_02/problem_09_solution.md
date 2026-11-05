# Problem 9: A Rectangular Linear System

## Problem

Solve the rectangular system
$$\begin{cases}x+y=3,\\2x-y=0,\\3x=3.\end{cases}$$
Explain why three equations in two unknowns need not be inconsistent.

## Worked Solution

The third equation immediately gives $x=1$. Substituting into $2x-y=0$ gives $2-y=0$, so $y=2$. The first equation is then satisfied because $1+2=3$.

Thus the system is consistent and has the unique solution
$$\boxed{(x,y)=(1,2)}.$$

Three equations in two unknowns need not contradict one another: an equation may be redundant or may agree with the solution determined by the others. Here the third equation fixes $x$, the second fixes $y$, and the first is a compatible check.

**Check.** Substituting $(1,2)$ gives $1+2=3$, $2-2=0$, and $3(1)=3$.
