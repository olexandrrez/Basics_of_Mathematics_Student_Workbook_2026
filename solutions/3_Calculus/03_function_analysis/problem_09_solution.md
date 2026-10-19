# Problem 9: An Oblique Asymptote

## 1. Original Problem
Analyze the asymptotes of $f(x)=(x^2+1)/(x-1)$, perform polynomial division, and explain why the remainder vanishes for large $|x|$.

## 2. What We Are Trying to Find
We identify vertical behavior where the denominator vanishes and compare the rational function with a line at large positive and negative inputs.

## 3. Key Idea or Theorem Needed Before the Calculation
Polynomial division writes a rational function as a polynomial quotient plus a proper fraction. If the remainder fraction tends to zero, the quotient line is an oblique asymptote.

## 4. Step-by-Step Solution
Division gives
$$\frac{x^2+1}{x-1}=x+1+\frac2{x-1}.$$
At $x=1$, the denominator vanishes and the numerator equals 2, so $x=1$ is a vertical asymptote. As $x\to\pm\infty$, $2/(x-1)\to0$. Hence the difference between $f(x)$ and $x+1$ tends to zero, so $y=x+1$ is an oblique asymptote.

## 5. Why Each Step Is Valid
An asymptote line is characterized by the vertical difference between the graph and line tending to zero. Here that difference is exactly $2/(x-1)$.

## 6. Final Answer in Words
Vertical asymptote: $x=1$. Oblique asymptote: $y=x+1$.

## 7. Quick Verification
For $x=101$, the difference from $y=x+1$ is $2/100=0.02$; it becomes smaller as $|x|$ grows.

## 8. Common Mistakes
- Calling $x+1$ the exact function instead of an asymptotic approximation.
- Looking only at degree and missing the vertical asymptote.

## 9. Short In-Class Explanation
Division separates the function into the line $x+1$ and remainder $2/(x-1)$. The remainder tends to zero, so the line is oblique asymptote; $x=1$ is the vertical asymptote.
