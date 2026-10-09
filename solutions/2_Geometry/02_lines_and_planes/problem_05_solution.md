# Problem 05: Relative Position of Two Lines

## 1. Original Problem
Analyze the position of
$$L_1:(x,y,z)=(1,1,0)+t(1,2,1),$$
$$L_2:(x,y,z)=(2,0,1)+s(0,1,-1).$$
If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## 2. What We Are Trying to Find
We must determine the geometric relationship between two lines in 3D space: whether they are parallel, intersecting at a single point, coincident, or skew (non-parallel and non-intersecting).

## 3. Key Idea or Theorem Needed Before the Calculation
- **Classification of Two Lines in Space**:
  1. **Parallel / Coincident**: Direction vectors are proportional ($v_1 = c v_2$).
  2. **Intersecting**: Direction vectors are non-proportional, and equating coordinates yields a consistent solution $(t, s)$.
  3. **Skew**: Direction vectors are non-proportional, and equating coordinates leads to a mathematical contradiction (they lie in parallel planes and never meet).

## 4. Step-by-Step Solution

### Step 1: Compare Direction Vectors for Parallelism
- Direction vector of $L_1$: $v_1 = (1, 2, 1)$.
- Direction vector of $L_2$: $v_2 = (0, 1, -1)$.
Check if $v_1 = c v_2$:
The first component requires $1 = c(0) = 0$, which is impossible.
Because $v_1$ and $v_2$ are not scalar multiples of each other, the lines are **not parallel**.

### Step 2: Test for an Intersection Point
Equate the coordinate equations for $L_1$ and $L_2$:
$$\begin{cases} 1 + t = 2 + 0s \\ 1 + 2t = 0 + s \\ 0 + t = 1 - s \end{cases}$$
1. From the $x$-equation:
   $$1 + t = 2 \implies t = 1.$$
2. Substitute $t = 1$ into the $y$-equation:
   $$s = 1 + 2(1) = 1 + 2 = 3.$$
3. Now test the pair $(t, s) = (1, 3)$ in the third ($z$) equation:
   - Left-hand side: $z = 0 + t = 0 + 1 = 1$.
   - Right-hand side: $z = 1 - s = 1 - 3 = -2$.
   $$\text{LHS} = 1 \neq -2 = \text{RHS}.$$
The third equation yields $1 = -2$, which is an impossible contradiction!

### Step 3: Conclude the Classification
1. The direction vectors are not parallel ($v_1 \nparallel v_2$).
2. The coordinate system for intersection is inconsistent (no common point exists).
Therefore, the lines are **skew** (in Polish: *skośne*).

## 5. Why Each Step Is Valid
- Non-proportionality of vectors is necessary and sufficient to rule out parallelism.
- Equating parametric equations tests whether the intersection set $L_1 \cap L_2$ is non-empty; inconsistency rigorously proves $L_1 \cap L_2 = \emptyset$.
- Non-parallel lines with empty intersection in $\mathbb{R}^3$ are skew by definition.

## 6. Final Answer in Words
The lines $L_1$ and $L_2$ are skew. They are not parallel because their direction vectors $(1, 2, 1)$ and $(0, 1, -1)$ are not proportional, and they do not intersect because solving the first two coordinates gives $t = 1$ and $s = 3$, which contradicts the third coordinate ($1 \neq -2$).

## 7. Quick Verification
- Check with the coplanarity determinant:
  $P_1 = (1, 1, 0)$, $P_2 = (2, 0, 1) \implies \overrightarrow{P_1 P_2} = (1, -1, 1)$.
  Compute the scalar triple product:
  $$\det\begin{pmatrix} 1 & -1 & 1 \\ 1 & 2 & 1 \\ 0 & 1 & -1 \end{pmatrix}$$
  Expand along row 3:
  $$-1 \det\begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix} + (-1) \det\begin{pmatrix} 1 & -1 \\ 1 & 2 \end{pmatrix} = -1(0) - 1(2 - (-1)) = -3 \neq 0.$$
  Because the scalar triple product is non-zero ($-3 \neq 0$), the displacement vector does not lie in the plane of the directions. This proves that the lines are skew.

## 8. Common Mistakes
- Concluding the lines intersect at $t=1, s=3$ without checking the third equation.
- Assuming non-intersecting lines in space must be parallel (forgetting that skew lines exist in 3D).

## 9. Short In-Class Explanation (3 Sentences)
The direction vectors $(1, 2, 1)$ and $(0, 1, -1)$ are not proportional, which means the lines are not parallel. Setting the $x$ and $y$ coordinates equal gives $t = 1$ and $s = 3$, but substituting these into the $z$ equation yields $1 = -2$, an impossible contradiction. Because the lines are non-parallel and have no common point, they are skew lines in space.
