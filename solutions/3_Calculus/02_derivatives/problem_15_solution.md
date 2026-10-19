# Problem 15: The Difference Quotient as a Check

## 1. Original Problem
Choose a function and point with a derivative, compute the derivative exactly, and evaluate the difference quotient for $h=1,0.1,0.01$. Compare and explain why samples are not a proof.

## 2. What We Are Trying to Find
We will compare finite secant slopes near a chosen point with the tangent slope defined as their limit.

## 3. Key Idea or Rule Needed Before the Calculation
The derivative at $x_0$ is $\lim_{h\to0}[f(x_0+h)-f(x_0)]/h$. A few values can illustrate this limiting process, but cannot replace it.

## 4. Step-by-Step Solution
Choose $f(x)=x^2$ and $x_0=1$. The power rule gives $f'(1)=2$. Compute the quotient algebraically:
$$\frac{f(1+h)-f(1)}h=\frac{(1+h)^2-1}{h}=\frac{2h+h^2}{h}=2+h.$$
For $h=1$, it is 3; for $h=0.1$, it is 2.1; for $h=0.01$, it is 2.01. These values approach 2.

## 5. Why Each Step Is Valid
The expansion of $(1+h)^2$ is exact, and cancellation is valid for the nonzero increments used. Taking the limit of $2+h$ as $h\to0$ yields 2, matching the derivative.

## 6. Final Answer in Words
The exact derivative is 2 at $x_0=1$, and the three requested secant slopes are 3, 2.1, and 2.01.

## 7. Quick Verification
The simplified quotient has limit 2 directly, so the numerical trend is consistent with the derivative definition.

## 8. Common Mistakes
- Treating the quotient for one finite $h$ as the derivative itself.
- Claiming a few values prove convergence for every sufficiently small increment.

## 9. Short In-Class Explanation
For $x^2$ at 1, the difference quotient simplifies to $2+h$. The sample values approach 2 and its limit is 2, which agrees with the derivative. The limit, not the finite list, is the proof.
