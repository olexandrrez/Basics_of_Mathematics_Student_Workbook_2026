# Problem 10: Complete Function Analysis

## 1. Original Problem
Analyze $f(x)=x/(x^2+1)$: domain, symmetry, zeros, limits, monotonicity, extrema, convexity, and sketch.

## 2. What We Are Trying to Find
We assemble the main features into a graph description: where it is defined, intercepts, end behavior, turning points and curvature.

## 3. Key Idea or Theorem Needed Before the Calculation
Use parity for symmetry, derivative signs for monotonicity, and the second derivative for concavity. Candidate inflection points must have an actual sign change of $f''$.

## 4. Step-by-Step Solution
The denominator is positive, so domain is $\mathbb R$. Since $f(-x)=-f(x)$ it is odd; its only zero is $x=0$. Its limits at both infinities are 0.

By the quotient rule,
$$f'=\frac{(x^2+1)-2x^2}{(x^2+1)^2}=\frac{1-x^2}{(x^2+1)^2}.$$
The denominator is positive. Thus $f'<0$ for $|x|>1$ and $f'>0$ for $|x|<1$. It decreases on $(-\infty,-1)$, increases on $(-1,1)$, then decreases on $(1,\infty)$. The minimum is $(-1,-1/2)$; the maximum is $(1,1/2)$.

Differentiating again,
$$f''=\frac{2x(x^2-3)}{(x^2+1)^3}.$$
Its sign changes at $-\sqrt3,0,\sqrt3$. It is negative on $(-\infty,-\sqrt3)$ and $(0,\sqrt3)$ and positive on $(-\sqrt3,0)$ and $(\sqrt3,\infty)$. Inflection points are $(-\sqrt3,-\sqrt3/4),(0,0),(\sqrt3,\sqrt3/4)$.

## 5. Why Each Step Is Valid
Positive denominators leave derivative signs controlled by the numerators. The derivative changes sign at $\pm1$, and the second derivative changes sign at all three listed roots.

## 6. Final Answer in Words
The curve is odd, crosses the origin, has minimum $(-1,-1/2)$ and maximum $(1,1/2)$, and approaches horizontal asymptote $y=0$ at both ends. Inflections are at $x=-\sqrt3,0,\sqrt3$ with the values stated above.

## 7. Quick Verification
Odd symmetry predicts the extrema and inflections occur in opposite pairs. Substitution gives $f(1)=1/2$ and $f(-1)=-1/2$.

## 8. Common Mistakes
- Assuming an odd function is symmetric about the $y$-axis; it is symmetric about the origin.
- Forgetting to square the denominator in the quotient rule.
- Giving inflection $x$-coordinates without their corresponding heights.

## 9. Short In-Class Explanation
The denominator never vanishes and the function is odd. The first derivative yields extrema at plus and minus one; the second changes sign at plus and minus root three and zero. The curve passes through the origin and approaches zero at both ends.

```text
y       ····················· y=0
↑                    ╭──• (1,1/2)
|                ╭───╯       ╲
|──────────────•──────────────╲────→ x
|           ╱ (0,0)            ╲
|   •──────╯
| (−1,−1/2)
```
