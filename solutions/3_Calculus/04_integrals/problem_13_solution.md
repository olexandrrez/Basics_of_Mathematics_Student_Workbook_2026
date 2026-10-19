# Problem 13: An Integral Depending on the Upper Limit

## 1. Original Problem
For $F(x)=\int_0^x(t^2+1)dt$, determine $F$, calculate $F'$, and explain the integrand's role as a local rate.

## 2. What We Are Trying to Find
We evaluate accumulated area up to a variable endpoint and differentiate it to relate accumulation to the original function.

## 3. Key Idea or Theorem Needed Before the Calculation
The Fundamental Theorem of Calculus states that if $F(x)=\int_a^x f(t)dt$ and $f$ is continuous, then $F'(x)=f(x)$.

## 4. Step-by-Step Solution
Integrate with respect to dummy variable $t$ and evaluate:
$$F(x)=\left[\frac{t^3}{3}+t\right]_0^x=\frac{x^3}{3}+x.$$
Then
$$F'(x)=x^2+1.$$
This matches the integrand with $t$ replaced by the upper endpoint $x$.

## 5. Why Each Step Is Valid
The integrand is continuous everywhere, so the Fundamental Theorem applies. A small endpoint increase adds a thin area strip whose height is approximately $x^2+1$ and width is the endpoint change.

## 6. Final Answer in Words
$F(x)=x^3/3+x$ and $F'(x)=x^2+1$. The integrand gives the instantaneous rate of area accumulation.

## 7. Quick Verification
Differentiate the explicit formula for $F$ to recover $x^2+1$.

## 8. Common Mistakes
- Treating $t$ as the variable of the final function rather than a dummy variable.
- Forgetting to evaluate at the lower limit zero.

## 9. Short In-Class Explanation
Integrate $t^2+1$ from zero to $x$ to get $x^3/3+x$. Differentiating gives $x^2+1$, the height at the moving endpoint, which is the local accumulation rate.
