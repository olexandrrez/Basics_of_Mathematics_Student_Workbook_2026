# Problem 13: Closest Point on a Plane

## 1. Original Problem
Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## 2. What We Are Trying to Find
We must determine the coordinates of point $Q$ on the plane $x + 2y + 2z = 4$ that minimizes the Euclidean distance to $P = (3, 0, 0)$, compute this minimum distance $d(P, \Pi)$, and verify that the segment vector $\overrightarrow{QP}$ is parallel to the normal vector of the plane.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Closest Point as Orthogonal Projection**: The point on a plane closest to an external point $P$ is the orthogonal projection $Q$ obtained by dropping a perpendicular along the plane's normal vector $n = (A, B, C)$.
- **Parametric Normal Line**: $X(t) = P + t n$.
- **Distance Formula**:
  $$d(P, \Pi) = \frac{|A x_0 + B y_0 + C z_0 + D|}{\sqrt{A^2 + B^2 + C^2}}.$$

## 4. Step-by-Step Solution

### Step 1: Identify Plane Normal and Normal Line
For the plane $\Pi: x + 2y + 2z = 4$:
- Normal vector: $n = (1, 2, 2)$.
- Normal length:
  $$\|n\| = \sqrt{1^2 + 2^2 + 2^2} = \sqrt{1 + 4 + 4} = \sqrt{9} = 3.$$
Construct the normal line through $P = (3, 0, 0)$:
$$\begin{pmatrix} x(t) \\ y(t) \\ z(t) \end{pmatrix} = \begin{pmatrix} 3 \\ 0 \\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\ 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 3 + t \\ 2t \\ 2t \end{pmatrix}.$$

### Step 2: Find the Intersection Parameter $t$
Substitute the coordinates into the plane equation $x + 2y + 2z = 4$:
$$(3 + t) + 2(2t) + 2(2t) = 4.$$
Expand and collect like terms:
$$3 + t + 4t + 4t = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}.$$

### Step 3: Compute the Coordinates of Closest Point $Q$
Substitute $t = 1/9$ into the normal line:
$$x = 3 + \frac{1}{9} = \frac{28}{9},$$
$$y = 2\left(\frac{1}{9}\right) = \frac{2}{9},$$
$$z = 2\left(\frac{1}{9}\right) = \frac{2}{9}.$$
The closest point on the plane is:
$$Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right).$$

### Step 4: Compute the Distance
The distance is the length of $\overrightarrow{QP} = P - Q$:
$$P - Q = (3, 0, 0) - \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right) = \left(-\frac{1}{9}, -\frac{2}{9}, -\frac{2}{9}\right) = -\frac{1}{9}(1, 2, 2).$$
The distance is:
$$d(P, \Pi) = \|P - Q\| = \left|-\frac{1}{9}\right| \|(1, 2, 2)\| = \frac{1}{9} (3) = \frac{1}{3}.$$

Check with the direct distance formula:
$$d(P, \Pi) = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|3 - 4|}{3} = \frac{|-1|}{3} = \frac{1}{3}.$$
Both methods yield exactly $1/3$.

### Step 5: Check That the Segment Is Perpendicular to the Plane
The displacement vector between the two points is:
$$\overrightarrow{QP} = \left(-\frac{1}{9}, -\frac{2}{9}, -\frac{2}{9}\right) = -\frac{1}{9}(1, 2, 2) = -\frac{1}{9} n.$$
Because $\overrightarrow{QP}$ is a direct scalar multiple of the normal vector $n = (1, 2, 2)$, the segment joining $P$ and $Q$ is strictly parallel to $n$ and therefore strictly perpendicular to the plane.

## 5. Why Each Step Is Valid
- The shortest distance from a point to a flat surface in Euclidean space is along the unique orthogonal line.
- The point $Q$ satisfies the plane equation $28/9 + 2(2/9) + 2(2/9) = (28 + 4 + 4)/9 = 36/9 = 4$.

## 6. Final Answer in Words
The closest point on the plane is $Q = (28/9, 2/9, 2/9)$, and the distance is $1/3$. The segment connecting $P$ and $Q$ is represented by the vector $-1/9(1, 2, 2)$, which is a scalar multiple of the plane's normal vector $n = (1, 2, 2)$, verifying that the connecting segment is perpendicular to the plane.

## 7. Quick Verification
- Check that $Q$ lies on the plane:
  $$\frac{28}{9} + 2\left(\frac{2}{9}\right) + 2\left(\frac{2}{9}\right) = \frac{28 + 4 + 4}{9} = \frac{36}{9} = 4. \quad (\text{Matches})$$
- Distance squared check:
  $(-1/9)^2 + (-2/9)^2 + (-2/9)^2 = (1 + 4 + 4)/81 = 9/81 = 1/9 \implies d = 1/3$.

## 8. Common Mistakes
- Inverting the fraction when solving $9t = 1$, writing $t = 9$ instead of $t = 1/9$.
- Forgetting to verify that $Q$ satisfies the plane equation.

## 9. Short In-Class Explanation (3 Sentences)
We construct a line through $P(3, 0, 0)$ along the plane's normal vector $(1, 2, 2)$ and find that it intersects the plane at $t = 1/9$, giving the closest point $(28/9, 2/9, 2/9)$. The distance from $P$ to this point is the length of the displacement vector, which evaluates to $1/3$. The connecting vector is $-\frac{1}{9}(1, 2, 2)$, which is directly proportional to the normal vector, confirming that the segment is perpendicular to the plane.
