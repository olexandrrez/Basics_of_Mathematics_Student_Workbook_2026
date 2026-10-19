# Problem 5: An Exponential Function with a Maximum

## 1. Original Problem
Analyze monotonicity and extrema of $f(x)=xe^{-x}$. Find its behavior as $x\to\infty$ and explain the graph's right side.

## 2. What We Are Trying to Find
We locate the critical point and use derivative signs to classify it, then compute the limit controlling the graph at large positive inputs.

## 3. Key Idea or Theorem Needed Before the Calculation
Use product rule for $xe^{-x}$ and chain rule for $e^{-x}$. Exponential decay dominates polynomial growth as $x\to\infty$.

## 4. Step-by-Step Solution
Differentiate:
$$f'=e^{-x}+x(-e^{-x})=e^{-x}(1-x).$$
Because $e^{-x}>0$, the sign is that of $1-x$. The function increases for $x<1$ and decreases for $x>1$, giving a global maximum at $x=1$ with height $f(1)=1/e$.

As $x\to\infty$, rewrite $xe^{-x}=x/e^x$. The exponential grows faster than $x$, so this quotient tends to zero; values remain positive, hence the limit is $0^+$.

## 5. Why Each Step Is Valid
The sign change is positive to negative, so the critical point is a maximum. Together with $f(x)\to-\infty$ as $x\to-\infty$ and $f(x)\to0$ on the right, this is global.

## 6. Final Answer in Words
Increasing on $(-\infty,1)$, decreasing on $(1,\infty)$, with global maximum $(1,1/e)$. The graph approaches horizontal asymptote $y=0$ from above as $x\to\infty$.

## 7. Quick Verification
$f(1)=e^{-1}$, and for $x>1$ the derivative is negative while the values stay positive, so the right branch descends toward zero.

## 8. Common Mistakes
- Differentiating $e^{-x}$ as $e^{-x}$ instead of $-e^{-x}$.
- Claiming the limit is negative because of the exponent's minus sign; the function is positive for $x>0$.

## 9. Short In-Class Explanation
The derivative is $e^{-x}(1-x)$, so it changes from positive to negative at 1. The function peaks at $1/e$ and then decays toward zero because exponential growth in the denominator dominates $x$.
