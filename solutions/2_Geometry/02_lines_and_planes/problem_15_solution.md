# Problem 15: Complete Classification of a Line Relative to a Plane

## 1. Original Problem
Let
$$L:p+tv,\qquad \Pi:n\cdot x=d.$$
State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## 2. What We Are Trying to Find
We must formulate the general mathematical criteria that distinguish the three possible geometric relationships between a line $L$ and a plane $\Pi$ in $\mathbb{R}^3$ based on the dot products $v \cdot n$ and $n \cdot p$, and construct a concrete numerical example illustrating each case.

## 3. Key Idea or Theorem Needed Before the Calculation
- **General Equation of Line in Plane**: Substitute $x(t) = p + t v$ into $\Pi: n \cdot x = d$:
  $$n \cdot (p + t v) = d \iff (n \cdot p) + t(n \cdot v) = d \iff t(n \cdot v) = d - n \cdot p.$$
- **Classification Criteria**:
  1. **Case 1: Exactly One Intersection Point**
     $$n \cdot v \neq 0.$$
     The line is not parallel to the plane. The unique intersection parameter is $t = \frac{d - n \cdot p}{n \cdot v}$.
  2. **Case 2: Parallel with No Common Points (Disjoint)**
     $$n \cdot v = 0 \quad \text{and} \quad n \cdot p \neq d.$$
     The equation reduces to $0 \cdot t = d - n \cdot p \neq 0$, which is a contradiction.
  3. **Case 3: Line Contained in the Plane ($L \subset \Pi$)**
     $$n \cdot v = 0 \quad \text{and} \quad n \cdot p = d.$$
     The equation reduces to $0 \cdot t = 0$, which is satisfied for all $t \in \mathbb{R}$.

## 4. Step-by-Step Solution

### Step 1: Mathematical Classification
Substituting $L(t) = p + t v$ into $\Pi$ gives the scalar linear equation in $t$:
$$t(n \cdot v) = d - n \cdot p.$$
- If $n \cdot v \neq 0$: coefficient of $t$ is non-zero $\implies$ unique solution $\implies$ **One intersection point**.
- If $n \cdot v = 0$ and $n \cdot p \neq d$: equation is $0 = c \neq 0$ $\implies$ no solution $\implies$ **Parallel and disjoint**.
- If $n \cdot v = 0$ and $n \cdot p = d$: equation is $0 = 0$ $\implies$ all $t$ are solutions $\implies$ **Line lies in the plane**.

### Step 2: Numerical Example for Case 1 (One Intersection Point)
- Let the plane be $\Pi: z = 3$, so $n = (0, 0, 1)$ and $d = 3$.
- Let the line be $L: p + tv = (0, 0, 0) + t(1, 0, 1)$.
- Check condition:
  $$n \cdot v = (0, 0, 1) \cdot (1, 0, 1) = 0 + 0 + 1 = 1 \neq 0.$$
- Solve for intersection:
  $$t(1) = 3 - 0 \implies t = 3.$$
- Intersection point:
  $$X = (0, 0, 0) + 3(1, 0, 1) = (3, 0, 3).$$
The line pierces the plane at the single point $(3, 0, 3)$.

### Step 3: Numerical Example for Case 2 (Parallel, Disjoint)
- Let the plane be $\Pi: z = 3$, so $n = (0, 0, 1)$ and $d = 3$.
- Let the line be $L: p + tv = (0, 0, 1) + t(1, 1, 0)$.
- Check condition:
  $$n \cdot v = (0, 0, 1) \cdot (1, 1, 0) = 0 + 0 + 0 = 0.$$
  $$n \cdot p = (0, 0, 1) \cdot (0, 0, 1) = 1 \neq 3 = d.$$
- The equation is $0 \cdot t = 3 - 1 = 2 \implies 0 = 2$ (impossible).
The line lies entirely in the plane $z = 1$, which is parallel to $z = 3$ and never meets it.

### Step 4: Numerical Example for Case 3 (Line Contained in the Plane)
- Let the plane be $\Pi: z = 3$, so $n = (0, 0, 1)$ and $d = 3$.
- Let the line be $L: p + tv = (0, 0, 3) + t(1, 1, 0)$.
- Check condition:
  $$n \cdot v = (0, 0, 1) \cdot (1, 1, 0) = 0.$$
  $$n \cdot p = (0, 0, 1) \cdot (0, 0, 3) = 3 = d.$$
- The equation is $0 \cdot t = 3 - 3 = 0 \implies 0 = 0$ (satisfied for every $t$).
Every point on the line has $z = 3$, so the entire line lies in the plane.

## 5. Why Each Step Is Valid
- Substituting parametric forms reduces 3D geometric intersection to a standard 1D linear equation $a t = b$.
- The three cases correspond to $a \neq 0$, $a = 0$ with $b \neq 0$, and $a = 0$ with $b = 0$.

## 6. Final Answer in Words
The three cases are classified by the equation $t(n \cdot v) = d - n \cdot p$:
1. $n \cdot v \neq 0$: exactly one intersection point.
2. $n \cdot v = 0$ and $n \cdot p \neq d$: parallel with no intersection.
3. $n \cdot v = 0$ and $n \cdot p = d$: line is contained entirely in the plane.
The simple plane $z = 3$ illustrates all three cases: line $(0,0,0)+t(1,0,1)$ hits at $(3,0,3)$; line $(0,0,1)+t(1,1,0)$ stays at $z=1$ and never meets it; line $(0,0,3)+t(1,1,0)$ lies completely inside the plane.

## 7. Quick Verification
- Case 1: Point $(3, 0, 3)$ satisfies $z = 3$.
- Case 2: For any $t$, $z(t) = 1 \neq 3$.
- Case 3: For any $t$, $z(t) = 3$, which always satisfies $z = 3$.

## 8. Common Mistakes
- Omitting the condition $n \cdot p \neq d$ for parallelism, failing to distinguish disjoint parallel lines from lines contained in the plane.
- Choosing complicated numerical examples where arithmetic errors obscure the geometric clarity.

## 9. Short In-Class Explanation (3 Sentences)
Substituting the line into the plane gives the linear equation $t(n \cdot v) = d - n \cdot p$. If $n \cdot v \neq 0$, there is a unique solution for $t$, giving exactly one intersection point. If $n \cdot v = 0$, the line is parallel to the plane: it has no solution if the base point lies off the plane ($n \cdot p \neq d$), and infinitely many solutions if the base point lies in the plane ($n \cdot p = d$).
