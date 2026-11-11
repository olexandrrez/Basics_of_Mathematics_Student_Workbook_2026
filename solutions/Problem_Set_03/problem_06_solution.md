# Problem 6: Cross Product and Perpendicularity

## Problem

For $u=(1,2,0)$ and $v=(0,1,3)$, compute $u\times v$ and check that the result is perpendicular to both vectors.

## Worked Solution

Using the component formula
$$u\times v=(u_2v_3-u_3v_2,\ u_3v_1-u_1v_3,\ u_1v_2-u_2v_1),$$
we obtain
$$u\times v=(2\cdot3-0\cdot1,\ 0\cdot0-1\cdot3,\ 1\cdot1-2\cdot0)=\boxed{(6,-3,1)}.$$

Check perpendicularity using dot products:
$$u\cdot(u\times v)=1(6)+2(-3)+0(1)=0,$$
$$v\cdot(u\times v)=0(6)+1(-3)+3(1)=0.$$
Both are zero, so the cross product is perpendicular to both original vectors.
