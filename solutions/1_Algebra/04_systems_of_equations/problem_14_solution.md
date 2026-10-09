# Problem 14: A Small Change in the Right-Hand Side

## 1. Original Problem
Compare the systems
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}$$
and
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}$$
Check the consistency of each system and explain why a small change in one number can change the type of the system.

## 2. What We Are Trying to Find
We must solve both 3-equation 2-variable systems, determine whether each system is consistent or inconsistent, and explain why an infinitesimal change from $3.0$ to $3.1$ in a single constant fundamentally alters the mathematical nature of the system from having a unique solution to having no solution.

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
Changing the constant from $3$ to $3.1$ shifts the third vertical line from $x = 1$ to $x = 1.0333\dots$.
Even though the shift is tiny ($0.1$), the third line no longer passes through the point $(1, 1)$.
Since the first two lines meet only at $(1, 1)$, and the third line does not contain $(1, 1)$, there is no longer any point shared by all three lines.
In linear algebra, consistency in overdetermined systems is an exact equality condition (a point lies on a line or it doesn't); a perturbation of any size destroys concurrency.

## 5. Why Each Step Is Valid
- Any solution to the entire system must satisfy the subset of the first two equations.
- Evaluating the unique candidate $(1, 1)$ in the third equation constitutes a complete, rigorous test for consistency.

## 6. Final Answer in Words
System 1 is consistent with unique solution $(1, 1)$, while System 2 is inconsistent with no solution. A small change in the constant shifts the third line away from the intersection point of the first two lines; because three lines must meet at the exact same point to have a solution, moving the third line by even a fraction creates an empty intersection.

## 7. Quick Verification
- Check augmented matrix of System 2:
  $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 3 & 0 & 3.1 \end{array}\right] \xrightarrow{R_3 - R_1 - R_2} \left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 0 & 0 & 3.1 - 3 \end{array}\right] = \left[\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 0 & 0 & 0.1 \end{array}\right].$$
  The row $[0 \; 0 \mid 0.1]$ is a contradiction, confirming inconsistency.

## 8. Common Mistakes
- Believing that an approximate solution ($x \approx 1$) makes the system "almost consistent". Linear systems are either strictly consistent or inconsistent.
- Overlooking that this is an overdetermined system (3 equations for 2 unknowns).

## 9. Short In-Class Explanation (3 Sentences)
The first two equations uniquely define the point $(1, 1)$, which satisfies the third equation $3x = 3$ in the first system, giving a unique solution. In the second system, the third equation requires $3x = 3.1$, which contradicts the value $3x = 3$ demanded by the first two equations. Geometrically, this slight change shifts the third line so that the three lines no longer intersect at a single common point.
