# Problem 6: Classifying Two Linear Systems

## Problem

Classify each system and give its solution set when it exists:

**(a)** $\begin{cases}x+2y=3,\\2x+4y=6.\end{cases}$

**(b)** $\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}$

## Worked Solution

### (a)

The second equation is exactly twice the first, so it imposes no new condition. There are infinitely many solutions on the line $x+2y=3$. Setting $y=t$ gives $x=3-2t$:
$$\boxed{\{(3-2t,t):t\in\mathbb R\}}.$$
This is a consistent dependent system.

### (b)

Twice the first equation would give $2x+4y=6$, but the second equation says $2x+4y=7$. Subtracting them yields $0=1$, a contradiction. The system is inconsistent and has no solutions:
$$\boxed{\varnothing}.$$

**Check.** In (a) the equations describe the same line; in (b) they have the same left-hand side after scaling but different right-hand sides.
