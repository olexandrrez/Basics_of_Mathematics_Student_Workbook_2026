# Problem 10: Definite Integral and Checking the Result

## 1. Original Problem
Estimate the range of $\int_0^2(x^2+1)dx$ using $1\le x^2+1\le5$, then compute exactly and explain the check.

## 2. What We Are Trying to Find
We first bound the accumulated area using lower and upper rectangles, then evaluate exactly and check consistency.

## 3. Key Idea or Theorem Needed Before the Calculation
If $m\le f(x)\le M$ on an interval of length $L$, then $mL\le\int f\le ML$.

## 4. Step-by-Step Solution
The integrand lies between 1 and 5 on $[0,2]$, whose length is 2. Therefore
$$2\le I\le10.$$
An antiderivative is $x^3/3+x$. Thus
$$I=\left[\frac{x^3}{3}+x\right]_0^2=\frac83+2=\frac{14}{3}\approx4.667.$$

## 5. Why Each Step Is Valid
Integrating the pointwise inequalities preserves order because the interval is the same and the integrands are continuous. The exact value lies within the predicted range.

## 6. Final Answer in Words
The integral equals $14/3$, which is between 2 and 10.

## 7. Quick Verification
The integrand increases from 1 to 5, so an average height around 2.33 is plausible; multiplying by width 2 gives 4.67.

## 8. Common Mistakes
- Multiplying the bounds by the wrong interval length.
- Forgetting to subtract the antiderivative value at the lower endpoint.

## 9. Short In-Class Explanation
The integrand is between 1 and 5 over width 2, so the integral must be between 2 and 10. Exact integration gives $14/3$, consistent with that estimate.
