# Problem 4: Substitution as Reversing the Chain Rule

## 1. Original Problem
Compute $\int2x(x^2+1)^4dx$, identify $u$, show its derivative occurs, and verify.

## 2. What We Are Trying to Find
We recognize a composite power and test whether the derivative of the inside is present as a factor.

## 3. Key Idea or Theorem Needed Before the Calculation
Substitution reverses the chain rule. If $u=g(x)$ and $du=g'(x)dx$, then an integral containing $g'(x)F(g(x))$ becomes $\int F(u)du$.

## 4. Step-by-Step Solution
Choose $u=x^2+1$, so $du=2x\,dx$, exactly the factor outside the fourth power. Then
$$\int2x(x^2+1)^4dx=\int u^4du=\frac{u^5}{5}+C.$$
Substitute back:
$$F(x)=\frac{(x^2+1)^5}{5}+C.$$

## 5. Why Each Step Is Valid
The change of variable replaces the entire inner expression and its differential together. This is exactly the reverse of differentiating $(x^2+1)^5/5$ by the chain rule.

## 6. Final Answer in Words
$\int2x(x^2+1)^4dx=(x^2+1)^5/5+C$.

## 7. Quick Verification
$F'(x)=\frac15\cdot5(x^2+1)^4\cdot2x=2x(x^2+1)^4$.

## 8. Common Mistakes
- Using $du=2x$ but forgetting the differential $dx$.
- Substituting for the inside but leaving an unmatched $x$ factor.

## 9. Short In-Class Explanation
The inside is $x^2+1$ and its derivative $2x$ is already present. Substitute $u=x^2+1$ and integrate $u^4$ to get $u^5/5+C$; differentiation checks it.
