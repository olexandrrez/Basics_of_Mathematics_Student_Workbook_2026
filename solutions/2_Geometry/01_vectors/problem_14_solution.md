# Problem 14: Closest Point on a Line

## 1. Original Problem
Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## 2. What We Are Trying to Find
We must find the point $Q$ on the line $L$ passing through the origin with direction $v = (1, 2)$ that is closest to $P = (4, 1)$ using vector projection, calculate the perpendicular distance $d(P, L) = \|\overrightarrow{QP}\|$, and verify that the error vector $\overrightarrow{QP}$ is orthogonal to $v$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Closest Point as Orthogonal Projection**: The point on a line through the origin closest to an external point $P$ is the orthogonal projection of the position vector $u = \overrightarrow{OP}$ onto the direction vector $v$:
  $$Q = \operatorname{proj}_v u = \left(\frac{u \cdot v}{v \cdot v}\right) v.$$
- **Distance Formula**: The shortest distance is the length of the perpendicular error vector:
  $$d(P, L) = \|u - Q\| = \|\overrightarrow{QP}\|.$$
- **Orthogonality**: By geometric construction, the shortest distance occurs along a segment perpendicular to the line: $\overrightarrow{QP} \cdot v = 0$.

## 4. Step-by-Step Solution

### Step 1: Compute the Projection to Find Closest Point $Q$
Let $u = \overrightarrow{OP} = (4, 1)$ and $v = (1, 2)$.
1. Compute dot products:
   $$u \cdot v = (4)(1) + (1)(2) = 4 + 2 = 6.$$
   $$v \cdot v = 1^2 + 2^2 = 1 + 4 = 5.$$
2. Compute the projection:
   $$Q = \operatorname{proj}_v u = \left(\frac{u \cdot v}{v \cdot v}\right) v = \frac{6}{5} (1, 2) = \left(\frac{6}{5}, \frac{12}{5}\right) = (1.2, 2.4).$$
The closest point on the line is $Q = (6/5, 12/5)$.

### Step 2: Compute the Displacement Vector $\overrightarrow{QP}$
The vector from $Q$ to $P$ is:
$$\overrightarrow{QP} = P - Q = (4, 1) - \left(\frac{6}{5}, \frac{12}{5}\right) = \left(\frac{20 - 6}{5}, \frac{5 - 12}{5}\right) = \left(\frac{14}{5}, -\frac{7}{5}\right) = (2.8, -1.4).$$

### Step 3: Compute the Distance from $P$ to the Line
The distance is the length of $\overrightarrow{QP}$:
$$d(P, L) = \|\overrightarrow{QP}\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196 + 49}{25}} = \sqrt{\frac{245}{25}} = \sqrt{\frac{49 \cdot 5}{25}} = \frac{7\sqrt{5}}{5} = \frac{7}{\sqrt{5}} \approx 3.130.$$

### Step 4: Verify Orthogonality of $\overrightarrow{QP}$ to $v$
Compute the dot product of $\overrightarrow{QP} = (14/5, -7/5)$ and $v = (1, 2)$:
$$\overrightarrow{QP} \cdot v = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0.$$
Because the dot product is $0$, the vector $\overrightarrow{QP}$ is strictly perpendicular to the direction vector $v$ of the line.

## 5. Why Each Step Is Valid
- In Euclidean geometry, the shortest distance from a point to a line is along the unique perpendicular line segment dropped from the point.
- The projection formula uniquely isolates this perpendicular point by minimizing the quadratic distance function $f(t) = \|u - t v\|^2$.

## 6. Final Answer in Words
The point on the line closest to $P$ is $Q = (6/5, 12/5) = (1.2, 2.4)$. The distance from $P$ to the line is $\frac{7\sqrt{5}}{5}$ (or $7/\sqrt{5} \approx 3.13$). Computing the dot product $\overrightarrow{QP} \cdot v = \frac{14}{5} - \frac{14}{5} = 0$ confirms that the connecting segment is strictly perpendicular to the line.

## 7. Quick Verification
- Check using the standard 2D point-to-line distance formula:
  Line equation through origin with direction $(1, 2)$: slope is $2/1 = 2 \implies y = 2x \implies 2x - y = 0$.
  Distance from $(4, 1)$ to line $2x - y = 0$:
  $$d = \frac{|2(4) - 1|}{\sqrt{2^2 + (-1)^2}} = \frac{|8 - 1|}{\sqrt{5}} = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}.$$
  Exact match with the projection result.

## 8. Common Mistakes
- Dividing by $\|v\| = \sqrt{5}$ rather than $\|v\|^2 = 5$ in the projection formula.
- Forgetting that the point on the line must have coordinates $(1.2, 2.4)$ and reporting only the distance.

## 9. Short In-Class Explanation (3 Sentences)
We find the closest point $Q$ by projecting the position vector of $P$ onto the direction vector $v$, which gives $Q = \frac{6}{5}(1, 2) = (1.2, 2.4)$. The shortest distance is the length of the connecting vector $(14/5, -7/5)$, which evaluates to $\frac{7\sqrt{5}}{5}$. Taking the dot product of this connecting vector with $v$ gives $14/5 - 14/5 = 0$, confirming that it is perpendicular to the line.
