# Problem 3: Recognizing Basic Antiderivatives

## 1. Original Problem
Compute $\int(2e^x+3\cos x-4\sin x)dx$ and verify the complete result.

## 2. What We Are Trying to Find
We match each integrand term with a familiar derivative and combine the resulting antiderivatives.

## 3. Key Idea or Theorem Needed Before the Calculation
Use $(e^x)'=e^x$, $(\sin x)'=\cos x$, and $(\cos x)'=-\sin x$. Linearity allows termwise integration.

## 4. Step-by-Step Solution
The first term gives $2e^x$; the second gives $3\sin x$. For the last term, since the derivative of cosine is negative sine, $4\cos x$ differentiates to $-4\sin x$. Therefore
$$F(x)=2e^x+3\sin x+4\cos x+C.$$

## 5. Why Each Step Is Valid
Each term has been chosen so its derivative equals the corresponding term of the integrand. The arbitrary constant accounts for all antiderivatives.

## 6. Final Answer in Words
The integral is $2e^x+3\sin x+4\cos x+C$.

## 7. Quick Verification
Differentiating gives $2e^x+3\cos x-4\sin x$, as required.

## 8. Common Mistakes
- Writing $-4\cos x$ for the last antiderivative, which gives the wrong sign after differentiation.
- Omitting $C$.

## 9. Short In-Class Explanation
Integrate each term using the known derivatives of exponential, sine, and cosine. The last term becomes positive $4\cos x$ because cosine differentiates to negative sine. Differentiate the sum to verify.
