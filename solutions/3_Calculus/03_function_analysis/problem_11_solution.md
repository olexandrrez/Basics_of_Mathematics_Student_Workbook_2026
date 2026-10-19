# Problem 11: A Parameter and the Number of Extrema

## 1. Original Problem
For $f_a(x)=x^3-3ax$, determine the number and character of critical points for each real $a$.

## 2. What We Are Trying to Find
The parameter affects the roots of the derivative, so we separate cases according to its sign and classify each root by sign changes.

## 3. Key Idea or Theorem Needed Before the Calculation
Critical points solve $f_a'=0$. A stationary point need not be an extremum: inspect the derivative on both sides.

## 4. Step-by-Step Solution
Differentiate with respect to $x$:
$$f_a'(x)=3x^2-3a=3(x^2-a).$$
If $a<0$, then $x^2-a>0$ everywhere, so there are no critical points and $f_a$ increases on all of $\mathbb R$.

If $a=0$, then $f_a'=3x^2$, zero only at zero and positive on both sides. The graph has a horizontal tangent at the origin but remains increasing; there is no extremum.

If $a>0$, roots are $x=\pm\sqrt a$. The derivative is positive outside and negative between them. Thus $-\sqrt a$ is a local maximum and $\sqrt a$ a local minimum. Values are $2a^{3/2}$ and $-2a^{3/2}$ respectively.

## 5. Why Each Step Is Valid
The sign of $x^2-a$ determines the derivative. The three parameter cases correspond to no real roots, one double root, or two distinct roots.

## 6. Final Answer in Words
For $a<0$ there are no critical points; for $a=0$ there is one stationary non-extremum; for $a>0$ there are two extrema, a maximum at $-\sqrt a$ and minimum at $\sqrt a$.

## 7. Quick Verification
For $a>0$, substituting $x=-\sqrt a$ gives $-a^{3/2}+3a^{3/2}=2a^{3/2}$; the positive root gives its negative.

## 8. Common Mistakes
- Counting a stationary point at $a=0$ as an extremum automatically.
- Forgetting the parameter changes the number of real roots of the derivative.

## 9. Short In-Class Explanation
The derivative is $3(x^2-a)$. Negative $a$ gives no zeros; zero gives one double root without a sign change; positive $a$ gives two roots with maximum then minimum.
