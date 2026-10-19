# Problem 5: The Same Substitution in a Different Context

## 1. Original Problem
Compute $\int xe^{x^2}dx$ and compare its structure with the preceding substitution problem.

## 2. What We Are Trying to Find
We seek a substitution that removes the nested exponent and transforms the remaining differential into a constant multiple of $du$.

## 3. Key Idea or Theorem Needed Before the Calculation
As in the previous exercise, look for an inner function whose derivative is proportional to a factor in the integrand. The outer function can differ; the substitution pattern is the same.

## 4. Step-by-Step Solution
The inner function is $u=x^2$, with $du=2x\,dx$, so $x\,dx=du/2$. Then
$$\int xe^{x^2}dx=\frac12\int e^u du=\frac12e^u+C=\frac12e^{x^2}+C.$$

## 5. Why Each Step Is Valid
The factor $1/2$ compensates for the missing factor 2 in $du$. Substitution undoes the chain-rule derivative of $e^{x^2}$.

## 6. Final Answer in Words
The antiderivative is $e^{x^2}/2+C$.

## 7. Quick Verification
Differentiating gives $\frac12e^{x^2}(2x)=xe^{x^2}$.

## 8. Common Mistakes
- Omitting the factor $1/2$ because $du$ is $2x\,dx$.
- Assuming the same substitution only works for powers; it also works for exponentials.

## 9. Short In-Class Explanation
The inner expression $x^2$ has derivative $2x$. Convert $x dx$ to $du/2$, integrate the exponential, and substitute back. The result differentiates to the original integrand.
