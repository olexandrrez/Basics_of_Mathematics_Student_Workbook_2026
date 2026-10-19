# Problem 4: A Function with Two Vertical Asymptotes

## 1. Original Problem
For $f(x)=1/(x^2-1)$, determine domain, asymptotes, sign, and monotonicity on the domain intervals. Explain why the intervals are separate.

## 2. What We Are Trying to Find
We map where the denominator is zero, determine sign and limits, then use the derivative to study each interval independently.

## 3. Key Idea or Theorem Needed Before the Calculation
A rational function is undefined at denominator zeros unless a factor cancels. Derivative signs determine monotonicity only on intervals where the function is defined.

## 4. Step-by-Step Solution
Factor $x^2-1=(x-1)(x+1)$. Thus the domain is $\mathbb R\setminus\{-1,1\}$. These two points are vertical asymptotes because the numerator stays 1. Since $f(x)\to0$ at both infinities, $y=0$ is horizontal asymptote.

The denominator is positive when $|x|>1$ and negative when $|x|<1$. Hence $f>0$ on the two outer intervals and $f<0$ between the poles. Differentiate:
$$f'(x)=-\frac{2x}{(x^2-1)^2}.$$
The denominator is positive on the domain; the sign is opposite to $x$. So $f$ increases on $(-\infty,-1)$ and $(-1,0)$; it decreases on $(0,1)$ and $(1,\infty)$. At zero, $f(0)=-1$ is a local maximum on the middle interval.

## 5. Why Each Step Is Valid
The poles split the real line into disconnected domain intervals, so behavior cannot be continued through them. The squared denominator in $f'$ has positive sign wherever defined.

## 6. Final Answer in Words
Domain excludes $\pm1$; vertical asymptotes are $x=\pm1$, horizontal asymptote is $y=0$. The function is positive outside $[-1,1]$, negative inside, and changes monotonicity at zero.

## 7. Quick Verification
$f(0)=-1$ confirms the middle branch is below the axis; for $x=2$, $f(2)=1/3>0$, consistent with the outer sign.

## 8. Common Mistakes
- Treating $x=\pm1$ as part of the domain.
- Inferring sign only from the numerator and ignoring denominator factors.
- Merging monotonicity intervals across a vertical asymptote.

## 9. Short In-Class Explanation
The denominator vanishes at plus or minus one and splits the domain. Its sign is positive outside and negative between the poles. The derivative has sign opposite to $x$, so the middle branch turns at zero.
