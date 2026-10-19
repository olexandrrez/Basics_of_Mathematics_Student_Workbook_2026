# Problem 14: Continuity and Differentiability

## 1. Original Problem
For $f(x)=x^2$ if $x\ge0$ and $f(x)=ax$ if $x<0$, find when it is continuous, when one-sided derivatives exist and agree, and when it is differentiable at zero.

## 2. What We Are Trying to Find
We compare the two pieces at their joining point. Continuity concerns matching values; differentiability also requires matching one-sided slopes.

## 3. Key Idea or Rule Needed Before the Calculation
Continuity at zero requires $\lim_{x\to0^-}f(x)=f(0)=\lim_{x\to0^+}f(x)$. One-sided derivatives are limits of difference quotients with $h$ approaching from the corresponding side.

## 4. Step-by-Step Solution
Since $f(0)=0$, the right limit of $x^2$ is zero. The left limit of $ax$ is also zero for every fixed $a$. Thus the function is continuous for all real $a$.

For the right derivative,
$$f'_+(0)=\lim_{h\to0^+}\frac{h^2-0}{h}=\lim_{h\to0^+}h=0.$$
For the left derivative,
$$f'_-(0)=\lim_{h\to0^-}\frac{ah-0}{h}=a.$$
Both exist for all $a$, but they agree only when $a=0$. Hence the function is differentiable at zero exactly for $a=0$.

## 5. Why Each Step Is Valid
The two formulas apply on opposite sides of the joining point. Continuity is satisfied because both pieces meet at value zero. A derivative exists at the join only when the one-sided derivatives match.

## 6. Final Answer in Words
The function is continuous for every $a$. Both one-sided derivatives exist for every $a$, and the function is differentiable at zero only when $a=0$.

## 7. Quick Verification
When $a=0$, both pieces have horizontal slope at the origin. When $a\ne0$, the left slope is $a$ while the right slope is zero, creating a corner or kink despite continuity.

## 8. Common Mistakes
- Assuming continuity automatically implies differentiability.
- Computing the left derivative with the right-hand formula.

## 9. Short In-Class Explanation
Both pieces tend to zero at the join, so continuity holds for all $a$. The right slope is zero and the left slope is $a$. They agree only when $a=0$, which is exactly the differentiable case.
