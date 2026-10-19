# Problem 15: Recovering a Function from Its Derivative and a Condition

## 1. Original Problem
Given $F'(x)=2xe^{x^2}$ and $F(0)=3$, find the full family, determine the constant and verify.

## 2. What We Are Trying to Find
First find every antiderivative of the prescribed derivative, then use the initial value to select exactly one function.

## 3. Key Idea or Theorem Needed Before the Calculation
The factor $2x$ is the derivative of $x^2$, suggesting substitution. An initial condition determines the constant of integration.

## 4. Step-by-Step Solution
Set $u=x^2$, so $du=2x dx$. Then
$$F(x)=\int2xe^{x^2}dx=\int e^u du=e^u+C=e^{x^2}+C.$$
Apply $F(0)=3$:
$$1+C=3,$$
so $C=2$ and $F(x)=e^{x^2}+2$.

## 5. Why Each Step Is Valid
The substitution reverses the chain rule. Every antiderivative differs by a constant on this interval, and the condition fixes that constant uniquely.

## 6. Final Answer in Words
The family is $e^{x^2}+C$; the specified function is $F(x)=e^{x^2}+2$.

## 7. Quick Verification
$F'(x)=2xe^{x^2}$ and $F(0)=1+2=3$.

## 8. Common Mistakes
- Forgetting the constant and thus not obtaining the entire family.
- Setting $C=3$ without accounting for $e^0=1$.

## 9. Short In-Class Explanation
Substitute $u=x^2$ to integrate the derivative and get $e^{x^2}+C$. Plug in zero to solve $1+C=3$, yielding $C=2$; then check both conditions.
