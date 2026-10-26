# Problem 13: A Logarithm and an Asymptote

## 1. Original Problem
Analyze $f(x)=\ln x/x$ for $x>0$, including its maximum and behavior at the domain ends.

## 2. What We Are Trying to Find
We identify the domain, zero, endpoint limits, asymptotes, monotonicity and maximum needed for a correct graph.

## 3. Key Idea or Theorem Needed Before the Calculation
Use the quotient rule for the derivative. For limits, logarithm grows more slowly than a positive power of $x$ as $x\to\infty$; as $x\to0^+$, $\ln x\to-\infty$.

## 4. Step-by-Step Solution
The domain is $x>0$. The numerator vanishes at $x=1$, so the zero is $(1,0)$. At the left endpoint, $\ln x/x\to-\infty$ as $x\to0^+$, so $x=0$ is a vertical asymptote. At infinity, $\ln x/x\to0^+$, giving horizontal asymptote $y=0$ on the right.

Differentiate:
$$f'(x)=\frac{(1/x)x-\ln x}{x^2}=\frac{1-\ln x}{x^2}.$$
Since the denominator is positive, $f'>0$ for $x<e$ and $f'<0$ for $x>e$. The unique maximum is $f(e)=1/e$.

To determine curvature, differentiate $f'=(1-\ln x)x^{-2}$ using the product rule:
$$f''=-\frac1x x^{-2}+(1-\ln x)(-2x^{-3})=\frac{2\ln x-3}{x^3}.$$
For $x>0$, the denominator $x^3$ is positive. Therefore $f''<0$ when $x<e^{3/2}$ and $f''>0$ when $x>e^{3/2}$. Concavity changes at $x=e^{3/2}$, so the inflection point is
$$\left(e^{3/2},\frac{\ln(e^{3/2})}{e^{3/2}}\right)=\left(e^{3/2},\frac{3}{2e^{3/2}}\right).$$
This change in curvature is another feature that determines how the graph bends as it approaches the horizontal asymptote.

## 5. Why Each Step Is Valid
The derivative sign change is positive to negative, so the critical point is a maximum. The boundary limits and monotonicity describe the entire graph on the domain.

## 6. Final Answer in Words
The function rises from $-\infty$ near zero, crosses at 1, peaks at $(e,1/e)$, then decreases toward the horizontal asymptote $y=0$ from above. It is concave down until $x=e^{3/2}$, inflects at $(e^{3/2},3/(2e^{3/2}))$, and is concave up afterward.

## 7. Quick Verification
At $x=e$, $1-\ln e=0$ and $f(e)=1/e$. For $x>e$, derivative is negative while values tend to zero.

## 8. Common Mistakes
- Treating $x=0$ as part of the domain.
- Calling $y=0$ a two-sided horizontal asymptote despite the domain only extending to positive inputs.
- Stopping after finding the maximum and omitting curvature information needed for the requested full sketch.

## 9. Short In-Class Explanation
The domain is positive reals, and the function crosses at one. Its derivative changes from positive to negative at $e$, where the maximum is $1/e$. It diverges downward near zero and approaches zero at infinity.
