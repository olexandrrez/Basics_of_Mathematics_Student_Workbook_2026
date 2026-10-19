# Problem 14: A Small Change in the Right-Hand Side

## 1. Original Problem
Compare the systems
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}$$
and
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}$$
Check the consistency of each system and explain why a small change in one number can change the type of the system.

## 2. What We Are Trying to Find
We must solve both 3-equation 2-variable systems, determine whether each system is consistent or inconsistent, and explain how the finite change from $3$ to $3.1$ in one constant affects consistency.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Overdetermined Systems**: A system with more equations than variables ($3$ equations for $2$ variables in $\mathbb{R}^2$) is generally inconsistent unless the additional equations pass through the exact same intersection point.
- **Geometric Meaning in the Plane**: Three linear equations represent three straight lines.
  - Consistent $\iff$ all three lines are **concurrent** (intersect at a single common point).
  - Inconsistent $\iff$ the third line misses the intersection point of the first two, forming a triangle with no point common to all three lines.

## 4. Step-by-Step Solution

### Step 1: Analyze System 1
$$\begin{cases} (1) \quad x + y = 2, \\ (2) \quad 2x - y = 1, \\ (3) \quad 3x = 3. \end{cases}$$
1. Solve the first two equations:
   Add Equation (1) and Equation (2):
   $$(x + y) + (2x - y) = 2 + 1 \implies 3x = 3 \implies x = 1.$$
2. Substitute $x = 1$ into Equation (1):
   $$1 + y = 2 \implies y = 1.$$
   The unique intersection of the first two lines is $(x, y) = (1, 1)$.
3. Test this point in the third equation:
   $$3x = 3(1) = 3.$$
   This matches the right-hand side ($3 = 3$, True).
All three equations are satisfied simultaneously by $(1, 1)$.
**Conclusion for System 1**: The system is **consistent** and has **exactly one unique solution**: $(x, y) = (1, 1)$.

### Step 2: Analyze System 2
$$\begin{cases} (1) \quad x + y = 2, \\ (2) \quad 2x - y = 1, \\ (3) \quad 3x = 3.1. \end{cases}$$
1. From the first two equations, adding them still yields:
   $$3x = 3 \implies x = 1, \quad y = 1.$$
   Any point satisfying the first two equations must be $(1, 1)$.
2. Substitute this candidate solution $(1, 1)$ into the third equation:
   $$3x = 3(1) = 3.$$
   However, Equation (3) requires:
   $$3x = 3.1 \implies 3 = 3.1,$$
   which is an impossible contradiction.
There is no point $(x, y)$ that satisfies all three equations.
**Conclusion for System 2**: The system is **inconsistent** and has **no solution**.

### Step 3: Explain Why a Small Change Alters the System Type
In System 1, the three lines are **concurrent**: the third line $x = 1$ passes precisely through the intersection point $(1, 1)$ of the first two lines.
Changing the constant from $3$ to $3.1$ shifts the third vertical line from $x = 1$ to $x = 3.1/3 = 31/30$.
The shift is $31/30 - 1 = 1/30$; this small finite change makes the third line miss $(1,1)$.
Since the first two lines meet only at $(1, 1)$, and the third line does not contain $(1, 1)$, there is no longer any point shared by all three lines.
With the first two equations fixed, any nonzero change to the third right-hand side moves the vertical line away from $x=1$, destroying the common intersection. This conclusion is specific to changing this right-hand side while keeping the first two equations fixed; arbitrary perturbations of an overdetermined system need not destroy consistency.

## 5. Why Each Step Is Valid
- Any solution to the entire system must satisfy the subset of the first two equations.
- Evaluating the unique candidate $(1, 1)$ in the third equation constitutes a complete, rigorous test for consistency.

## 6. Final Answer in Words
System 1 is consistent with unique solution $(1,1)$, while System 2 is inconsistent with no solution. When the first two equations stay fixed, any nonzero change to the third right-hand side shifts its vertical line away from their intersection at $(1,1)$ and destroys the common intersection. This conclusion concerns that specific change; arbitrary perturbations of an overdetermined system need not make it inconsistent.

## 7. Quick Verification
- Check augmented matrix of System 2:
  $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 3 & 0 & 3.1 \end{array}\right] \xrightarrow{R_3 - R_1 - R_2} \left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 0 & 0 & 3.1 - 3 \end{array}\right] = \left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 0 & 0 & 0.1 \end{array}\right].$$
  The row $[0 \; 0 \mid 0.1]$ is a contradiction, confirming inconsistency.

## 8. Common Mistakes
- Believing that an approximate solution ($x \approx 1$) makes the system "almost consistent". Linear systems are either strictly consistent or inconsistent.
- Overlooking that this is an overdetermined system (3 equations for 2 unknowns).

## 9. Short In-Class Explanation (3 Sentences)
The first two equations uniquely define $(1,1)$, which satisfies $3x=3$. Replacing the right-hand side by $3.1$ moves the third line from $x=1$ to $x=31/30$, a small finite shift of $1/30$, so the three lines no longer share a point. Any nonzero change to this third right-hand side has that effect while the first two equations stay fixed.
