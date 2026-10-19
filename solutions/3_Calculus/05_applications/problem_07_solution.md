# Problem 7: Exponential Growth

## 1. Original Problem
For $N(t)=N_0e^{kt}$ with $k>0$, verify $N'=kN$, find doubling time, and explain its independence from $N_0$.

## 2. What We Are Trying to Find
We check the model's proportional-growth law and solve for the elapsed time needed to multiply the initial population by two.

## 3. Key Idea or Theorem Needed Before the Calculation
Differentiate exponentials by the chain rule. To solve a doubling equation, divide by $N_0$ and use natural logarithms.

## 4. Step-by-Step Solution
Differentiate:
$$N'(t)=N_0ke^{kt}=kN(t).$$
Let $T$ be the doubling time. Then $N(T)=2N_0$, so
$$N_0e^{kT}=2N_0.$$
For $N_0>0$, divide by $N_0$: $e^{kT}=2$. Taking logs yields $kT=\ln2$, hence $T=\ln2/k$.

## 5. Why Each Step Is Valid
The initial size is a multiplicative scale factor and cancels from the ratio condition. The logarithm is inverse to the exponential.

## 6. Final Answer in Words
The model satisfies $N'=kN$ and the doubling time is $\ln2/k$, independent of initial population.

## 7. Quick Verification
At $T=\ln2/k$, $e^{kT}=e^{\ln2}=2$, so $N(T)=2N_0$.

## 8. Common Mistakes
- Using $2/k$ instead of $\ln2/k$.
- Claiming the doubling time depends on $N_0$.

## 9. Short In-Class Explanation
Differentiate the model to get $N'=kN$. Set its value at time $T$ equal to twice its initial value; solving the exponential equation gives $T=\ln2/k$.
