# Problem 10: Ticket Sales as a Linear System

## Problem

A workshop sells 30 tickets. A standard ticket costs 12 currency units and a student ticket costs 8. Revenue is 304. Form a linear system, solve it, and check that the answer is meaningful.

## Worked Solution

Let $s$ be the number of standard tickets and $t$ the number of student tickets. The total-ticket condition and the revenue condition give
$$\begin{cases}s+t=30,\\12s+8t=304.\end{cases}$$
Multiply the first equation by $8$ to express the revenue from 30 student-price tickets:
$$8s+8t=240.$$
Subtract this equation from the revenue equation. The difference $4s=64$ gives $s=16$. Then $t=30-16=14$.

**Answer:** $\boxed{16}$ standard tickets and $\boxed{14}$ student tickets.

**Meaningfulness check.** The counts are nonnegative whole numbers and sum to $16+14=30$. Their revenue is $12(16)+8(14)=192+112=304$, as required.
