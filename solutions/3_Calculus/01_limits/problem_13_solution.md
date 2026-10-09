# Problem 13: Fundamental Trigonometric Limit

## 1. Original Problem
Using
$$\lim_{x\to0}\frac{\sin x}{x}=1,$$
compute
$$\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.$$
In each case, show how you reduce the expression to the fundamental limit.

## 2. What We Are Trying to Find
We must evaluate two trigonometric limits as $x \to 0$:
1. $L_1 = \lim_{x \to 0} \frac{\sin 5x}{x}$
2. $L_2 = \lim_{x \to 0} \frac{\sin 2x}{\sin 3x}$

Both expressions present the indeterminate form $\frac{0}{0}$. We must systematically transform each quotient using algebraic scaling so that each sine term matches its exact interior argument in the denominator, allowing direct application of $\lim_{u \to 0} \frac{\sin u}{u} = 1$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Fundamental Trigonometric Limit**:
  $$\lim_{u \to 0} \frac{\sin u}{u} = 1.$$
- **Substitution Principle**:
  If $g(x) \to 0$ as $x \to 0$ and $g(x) \neq 0$ for $x \neq 0$, then:
  $$\lim_{x \to 0} \frac{\sin(g(x))}{g(x)} = 1.$$
- **Argument-Balancing Technique**:
  To apply the theorem to $\sin(k x)$, the denominator must contain exactly $k x$. We achieve this by multiplying and dividing by the appropriate constant factor $k$:
  $$\frac{\sin(k x)}{x} = k \cdot \frac{\sin(k x)}{k x}.$$

## 4. Step-by-Step Solution

### Part 1: Computing $\lim_{x\to0}\frac{\sin5x}{x}$

#### Step 1: Identify the required argument
The numerator has argument $5x$. To apply the fundamental limit, the denominator must also be $5x$.

#### Step 2: Multiply numerator and denominator by $5$
For $x \neq 0$:
$$\frac{\sin 5x}{x} = \frac{5 \sin 5x}{5x} = 5 \cdot \frac{\sin 5x}{5x}.$$

#### Step 3: Perform the substitution and evaluate
Let $u = 5x$. As $x \to 0$, $u \to 0$.
$$\lim_{x \to 0} \frac{\sin 5x}{5x} = \lim_{u \to 0} \frac{\sin u}{u} = 1.$$
Using the constant multiple rule for limits:
$$\lim_{x \to 0} \frac{\sin 5x}{x} = 5 \cdot \lim_{x \to 0} \frac{\sin 5x}{5x} = 5 \cdot 1 = 5.$$

---

### Part 2: Computing $\lim_{x\to0}\frac{\sin2x}{\sin3x}$

#### Step 1: Deconstruct the quotient
Both numerator and denominator approach $0$ as $x \to 0$.
We need to introduce $2x$ beneath $\sin 2x$ and $3x$ beneath $\sin 3x$.

#### Step 2: Divide both numerator and denominator by $x$
For $x \neq 0$:
$$\frac{\sin 2x}{\sin 3x} = \frac{\frac{\sin 2x}{x}}{\frac{\sin 3x}{x}}.$$

#### Step 3: Balance the constants in both parts
- For the numerator: multiply and divide by $2$:
  $$\frac{\sin 2x}{x} = 2 \cdot \frac{\sin 2x}{2x}.$$
- For the denominator: multiply and divide by $3$:
  $$\frac{\sin 3x}{x} = 3 \cdot \frac{\sin 3x}{3x}.$$

Substitute these back into the complex fraction:
$$\frac{\sin 2x}{\sin 3x} = \frac{2 \cdot \frac{\sin 2x}{2x}}{3 \cdot \frac{\sin 3x}{3x}} = \frac{2}{3} \cdot \frac{\frac{\sin 2x}{2x}}{\frac{\sin 3x}{3x}}.$$

#### Step 4: Take the limit
As $x \to 0$:
- $\lim_{x \to 0} \frac{\sin 2x}{2x} = 1$ (by setting $u = 2x$).
- $\lim_{x \to 0} \frac{\sin 3x}{3x} = 1$ (by setting $v = 3x$).

Applying the quotient rule for limits:
$$\lim_{x \to 0} \frac{\sin 2x}{\sin 3x} = \frac{2}{3} \cdot \frac{1}{1} = \frac{2}{3}.$$

## 5. Why Each Step Is Valid
1. **Multiplication by $1$**: Multiplying by $\frac{k}{k} = 1$ is an identity transformation that preserves numerical values.
2. **Limit of scaled arguments**: Since $u = kx$ is a linear continuous function with $u(0) = 0$, $\lim_{x \to 0} f(kx) = \lim_{u \to 0} f(u)$.
3. **Quotient rule**: Both numerator and denominator limits exist and the denominator limit is non-zero ($3 \cdot 1 = 3 \neq 0$).

## 6. Final Answer in Words
The first limit is $5$, and the second limit is $\frac{2}{3}$. In both problems, we reduce the expression to the fundamental limit $\frac{\sin u}{u} \to 1$ by multiplying and dividing by constants so that each sine argument is matched exactly by the variable expression in its denominator.

## 7. Quick Verification
- Numerical test for $\frac{\sin 5x}{x}$ with $x = 0.001$ radians:
  $$\sin(0.005) \approx 0.0049999583 \implies \frac{0.0049999583}{0.001} = 4.99996 \approx 5.$$
- Numerical test for $\frac{\sin 2x}{\sin 3x}$ with $x = 0.001$ radians:
  $$\sin(0.002) \approx 0.0019999987, \quad \sin(0.003) \approx 0.0029999955$$
  $$\frac{0.0019999987}{0.0029999955} \approx 0.666667 = \frac{2}{3}.$$
Both numerical tests confirm the exact fractional values.

## 8. Common Mistakes
- **Pulling constants out of the sine function**: Writing $\sin(5x) = 5\sin(x)$. The sine function is non-linear; $\sin(kx) \neq k\sin(x)$!
- **Canceling the sine symbols**: Writing $\frac{\sin 2x}{\sin 3x} = \frac{2x}{3x} = \frac{2}{3}$ without justifying via the fundamental limit. While the answer happens to match, treating $\sin$ as an algebraic variable that can be canceled is mathematically invalid.
- **Using degree mode on calculators**: Evaluating trigonometric limits requires angles in radians; the limit $\lim \frac{\sin x}{x} = 1$ is false in degrees!

## 9. Short In-Class Explanation (3 Sentences)
To use the fundamental limit $\lim_{u\to0}\frac{\sin u}{u}=1$, the denominator must match the argument inside the sine function. For $\frac{\sin 5x}{x}$, we multiply and divide by $5$ to form $5\frac{\sin 5x}{5x}$, which evaluates to $5 \times 1 = 5$. For $\frac{\sin 2x}{\sin 3x}$, we divide both parts by $x$ and introduce the constants $2$ and $3$, giving $\frac{2}{3} \frac{(\sin 2x)/(2x)}{(\sin 3x)/(3x)} = \frac{2}{3}$.
