# Unit 2 · Topic 03 — Systems of Linear Equations
> Syllabus coverage: system of linear equations (rank conditions, consistency, rank properties)
> Cheatsheet: [../Cheatsheets/03-Systems-of-Linear-Equations.md](../Cheatsheets/03-Systems-of-Linear-Equations.md)

**Q1.** `[Concept]` ★ A system $AX=B$ of $m$ equations in $n$ unknowns is consistent if and only if

(A) $\operatorname{rank}A=n$

(B) $\det A\neq0$

(C) $\operatorname{rank}A=m$

(D) $\operatorname{rank}A=\operatorname{rank}[A\,|\,B]$

**Q2.** `[Numerical]` ★★ The system
$$x+y+z=6,\quad x+2y+3z=10,\quad x+2y+\lambda z=\mu$$
has **no** solution when

(A) $\lambda=3,\ \mu=10$

(B) $\lambda=3,\ \mu\ne10$

(C) $\lambda\ne3,\ \mu=10$

(D) $\lambda\ne3,\ \mu\ne10$

**Q3.** `[Numerical]` ★ Let $A$ be a $4\times6$ real matrix of rank 3. The number of linearly independent solutions of $AX=0$ is

(A) 1

(B) 2

(C) 3

(D) 6

**Q4.** `[Multi-Statement]` ★★ For real matrices of compatible sizes, consider:

I. $\operatorname{rank}(A^TA)=\operatorname{rank}A$.

II. $\operatorname{rank}(A+B)\le\operatorname{rank}A+\operatorname{rank}B$.

III. $\operatorname{rank}(AB)=\min(\operatorname{rank}A,\operatorname{rank}B)$.

Which is/are correct?

(A) I and II only

(B) I only

(C) II and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** A homogeneous system of 3 equations in 5 unknowns always has a non-trivial solution.
**Reason (R):** For the coefficient matrix $A$, $\operatorname{rank}A\le3<5$, so the solution space has dimension $5-\operatorname{rank}A\ge2$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ For a system $AX=B$ with $A$ of order $n\times n$, match the condition with the conclusion.

| List-I | List-II |
|---|---|
| (a) $\operatorname{rank}A=\operatorname{rank}[A\,|\,B]=n$ | 1. no solution |
| (b) $\operatorname{rank}A=\operatorname{rank}[A\,|\,B]<n$ | 2. only the trivial solution of $AX=0$ |
| (c) $\operatorname{rank}A<\operatorname{rank}[A\,|\,B]$ | 3. infinitely many solutions (over $\mathbb{R}$) |
| (d) $\det A\neq0$, $B=0$ | 4. unique solution |

(A) a-4, b-3, c-1, d-2

(B) a-4, b-1, c-3, d-2

(C) a-2, b-3, c-1, d-4

(D) a-3, b-4, c-1, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true for every real matrix $A$ (square where needed)?

(A) $\operatorname{rank}A=\operatorname{rank}A^T$

(B) $\operatorname{rank}(AA^T)=\operatorname{rank}A$

(C) $\operatorname{rank}(A^2)=\operatorname{rank}A$

(D) $\operatorname{rank}(PAQ)=\operatorname{rank}A$ for invertible $P,Q$

**Q8.** `[Application]` ★★★ Let $A,B$ be $5\times5$ real matrices with $\operatorname{rank}A=4$ and $\operatorname{rank}B=3$. The minimum possible value of $\operatorname{rank}(AB)$ is

(A) 1

(B) 2

(C) 3

(D) 0

**Q9.** `[Numerical]` ★★ The rank of the $4\times4$ matrix $A=(a_{ij})$ with $a_{ij}=i+j$ is

(A) 1

(B) 4

(C) 3

(D) 2

**Q10.** `[Application]` ★★ The system
$$kx+y+z=1,\quad x+ky+z=1,\quad x+y+kz=1$$
is **inconsistent** for

(A) $k=1$

(B) $k=-2$

(C) $k=2$

(D) $k=0$

**Q11.** `[Concept]` ★ If $X_1$ and $X_2$ are solutions of $AX=B$ with $B\neq0$, which of the following is also a solution of $AX=B$?

(A) $X_1+X_2$

(B) $X_1-X_2$

(C) $2X_1-X_2$

(D) $\tfrac12X_1$

**Q12.** `[Application]` ★★★ Let $A$ be a $3\times3$ real matrix with $\operatorname{rank}A=2$. Then $\operatorname{rank}(\operatorname{adj}A)$ is

(A) 0

(B) 3

(C) 2

(D) 1

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | A | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | C | NOT-true |
| 8 | B | Application |
| 9 | D | Numerical |
| 10 | B | Application |
| 11 | C | Concept |
| 12 | D | Application |

## Solutions
**Q1 — (D).** This is the Rouché–Capelli (Kronecker–Capelli) theorem. (A) and (B) are conditions for uniqueness or invertibility, not for consistency.

**Q2 — (B).** Subtracting equation 2 from equation 3 gives $(\lambda-3)z=\mu-10$. If $\lambda=3$ and $\mu\ne10$, then $\operatorname{rank}A=2<\operatorname{rank}[A|B]=3$, so there is no solution. $\lambda=3,\mu=10$ gives infinitely many solutions, and $\lambda\ne3$ gives a unique one.

**Q3 — (C).** The solution space has dimension $n-\operatorname{rank}A=6-3=3$. Here $n$ is the number of unknowns (columns), not the number of equations.

**Q4 — (A).** I: $A^TAx=0\Rightarrow\|Ax\|^2=0$, so the null spaces agree. II is subadditivity. III is false: only $\operatorname{rank}(AB)\le\min$ holds. For example $A=\begin{pmatrix}1&0\\0&0\end{pmatrix}$, $B=\begin{pmatrix}0&0\\0&1\end{pmatrix}$ gives $AB=0$.

**Q5 — (A).** R is precisely the reason. More unknowns than equations forces a non-zero null space.

**Q6 — (A).** These are the standard consistency cases. A homogeneous system with $\det A\ne0$ has only $X=0$.

**Q7 — (C).** For the nilpotent $A=\begin{pmatrix}0&1\\0&0\end{pmatrix}$, $\operatorname{rank}A=1$ but $A^2=0$. (B) holds over $\mathbb{R}$ (it fails over $\mathbb{C}$ without conjugation).

**Q8 — (B).** Sylvester's inequality gives $\operatorname{rank}(AB)\ge\operatorname{rank}A+\operatorname{rank}B-n=4+3-5=2$. The bound is attained when the 1-dimensional $\ker A$ lies inside the 3-dimensional range of $B$. (C) is the *maximum*.

**Q9 — (D).** Row $i$ equals $i\cdot(1,1,1,1)+(1,2,3,4)$, so every row lies in the span of two fixed vectors and the rank is 2. This holds for every $n\ge2$.

**Q10 — (B).** $\det=(k-1)^2(k+2)$. At $k=-2$, adding the three equations gives $0=3$, so the system is inconsistent (rank 2 against rank 3). At $k=1$ all three equations reduce to $x+y+z=1$, giving infinitely many solutions. Other values of $k$ give a unique solution.

**Q11 — (C).** $A(2X_1-X_2)=2B-B=B$. In general, $\sum c_iX_i$ is a solution iff $\sum c_i=1$ (an affine combination). (B) solves the homogeneous system instead.

**Q12 — (D).** $\operatorname{rank}(\operatorname{adj}A)=n$, $1$ or $0$ according as $\operatorname{rank}A=n$, $n-1$ or $\le n-2$. Here $A\operatorname{adj}A=0$ puts the columns of adj $A$ in the 1-dimensional $\ker A$, and adj $A\ne0$ because some $2\times2$ minor is non-zero.
