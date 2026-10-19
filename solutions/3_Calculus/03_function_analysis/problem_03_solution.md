# Problem 3: A Rational Function

## 1. Original Problem
Analyze domain, zeros, asymptotes, monotonicity and sketch $f(x)=(x+1)/(x-2)$.

## 2. What We Are Trying to Find
We identify where the function is defined, where it crosses the axis, its end behavior near excluded points and infinity, and its intervals of increase or decrease.

## 3. Key Idea or Theorem Needed Before the Calculation
For rational functions, denominator zeros may create vertical asymptotes. Division can expose a horizontal or oblique asymptote. The derivative sign gives monotonicity on each connected domain interval.

## 4. Step-by-Step Solution
The denominator excludes $x=2$. The numerator vanishes at $x=-1$, so the zero is $(-1,0)$. Divide to obtain
$$f(x)=1+\frac3{x-2}.$$
As $x\to2^-$, the fraction tends to $-\infty$; as $x\to2^+$ it tends to $+\infty$, so $x=2$ is vertical asymptote. At either infinity the fraction tends to zero, giving horizontal asymptote $y=1$.

Differentiate: $f'=-3/(x-2)^2<0$. The function decreases on $(-\infty,2)$ and also on $(2,\infty)$.

## 5. Why Each Step Is Valid
The denominator is squared in $f'$, so its sign cannot change the negative numerator. The excluded point separates the domain, so decreasing behavior must be stated on two intervals.

## 6. Final Answer in Words
Domain $\mathbb R\setminus\{2\}$, zero $x=-1$, vertical asymptote $x=2$, horizontal asymptote $y=1$, decreasing on each side of the vertical asymptote.

## 7. Quick Verification
At $x=0$, $f(0)=-1/2$; the left branch crosses zero at $-1$. For large $|x|$, the fraction $3/(x-2)$ is small, confirming approach to 1.

## 8. Common Mistakes
- Calling $y=2$ the vertical asymptote; the excluded input gives a vertical line $x=2$.
- Claiming the function decreases across $x=2$, where it is undefined.

## 9. Short In-Class Explanation
Rewrite the function as $1+3/(x-2)$. This reveals both asymptotes; the derivative is always negative on each side, and the zero is at $x=-1$.

```text
y       y=1 ···························
↑                 ╲                 ╱
|                  ╲               ╱
|                   ╲             ╱
|      • (−1,0)      ╲           ╱
+--------------------│--------------------→ x
                     x=2
```
