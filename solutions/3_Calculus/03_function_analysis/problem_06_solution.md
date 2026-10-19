# Problem 6: A Logarithmic Function

## 1. Original Problem
Analyze domain, zero and monotonicity of $f(x)=\ln x-x+1$. Explain why the domain comes first.

## 2. What We Are Trying to Find
We determine where the formula is real, find its zero, and use a derivative sign chart to locate the maximum and describe behavior.

## 3. Key Idea or Theorem Needed Before the Calculation
The logarithm requires positive input. Once the domain is known, use $f'=1/x-1$ and inspect its sign on that domain.

## 4. Step-by-Step Solution
The domain is $x>0$. Differentiate:
$$f'(x)=\frac1x-1=\frac{1-x}{x}.$$
On the domain $x$ is positive, so the derivative is positive for $0<x<1$, zero at 1, and negative for $x>1$. Thus $f$ increases and then decreases, attaining a maximum at $x=1$. The value is $f(1)=0$. Since this is the maximum, it is also the only zero. As $x\to0^+$, $\ln x$ tends to $-\infty$; as $x\to\infty$, the term $-x$ dominates, so $f\to-\infty$ at both domain ends.

## 5. Why Each Step Is Valid
A derivative sign chart applies only where the function exists. The maximum value zero means all other values are below zero, establishing uniqueness of the zero.

## 6. Final Answer in Words
Domain $(0,\infty)$; unique zero and global maximum at $x=1$; increasing on $(0,1)$ and decreasing on $(1,\infty)$.

## 7. Quick Verification
Direct substitution gives $\ln1-1+1=0$. The derivative changes from positive to negative at 1.

## 8. Common Mistakes
- Including zero in the domain because the nonlogarithmic terms are defined there.
- Saying the derivative exists at all real inputs.
- Calling the zero a minimum rather than the maximum.

## 9. Short In-Class Explanation
The logarithm restricts the domain to positive $x$. The derivative $(1-x)/x$ is positive up to 1 and negative afterward, so the maximum is $f(1)=0$ and this is the only zero.
