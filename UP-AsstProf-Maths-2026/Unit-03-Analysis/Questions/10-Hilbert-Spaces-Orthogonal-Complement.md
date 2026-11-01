# Unit 3 · Topic 10 — Hilbert Spaces and Orthogonal Complement
> Syllabus coverage: Hilbert spaces, Orthogonal complement of a subspace in a Hilbert space (also: parallelogram law, projection theorem, Riesz representation theorem, orthonormal bases, Bessel's inequality and Parseval's identity, adjoint operators)
> Cheatsheet: [../Cheatsheets/10-Hilbert-Spaces-Orthogonal-Complement.md](../Cheatsheets/10-Hilbert-Spaces-Orthogonal-Complement.md)

**Q1.** `[Concept]` ★ A norm on a vector space is induced by an inner product if and only if it satisfies

(A) the triangle inequality

(B) the Cauchy–Schwarz inequality

(C) the parallelogram law $\|x+y\|^2+\|x-y\|^2=2\|x\|^2+2\|y\|^2$

(D) completeness

**Q2.** `[Numerical]` ★ In an inner product space, $\|x\|=3$, $\|y\|=4$ and $\|x+y\|=5$. Then $\|x-y\|$ equals

(A) $1$

(B) $\sqrt7$

(C) $5$

(D) $7$

**Q3.** `[Numerical]` ★★ In $L^2[0,1]$ (real), the distance from $f(t)=t^2$ to the subspace $\operatorname{span}\{1,t\}$ is

(A) $\dfrac{1}{6\sqrt5}$

(B) $\dfrac{1}{180}$

(C) $\dfrac{1}{\sqrt{12}}$

(D) $\dfrac{1}{6}$

**Q4.** `[Multi-Statement]` ★★ Let $H$ be a Hilbert space and $M\subseteq H$ a linear subspace. Consider the following statements.

I. $M^\perp$ is always a closed subspace of $H$.

II. $(M^\perp)^\perp=M$ for every subspace $M$.

III. If $M$ is closed, then $H=M\oplus M^\perp$.

Which is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and III only

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** For $p\ne2$, $\ell^p$ is a Banach space but not a Hilbert space.
**Reason (R):** For $p\ne2$, the $\ell^p$ norm does not satisfy the parallelogram law.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Here $\{e_n\}$ is an orthonormal set in a Hilbert space $H$. Match each result with its statement.

| List-I | List-II |
|---|---|
| (a) Bessel's inequality | 1. Every $f\in H^*$ is $f(x)=\langle x,y\rangle$ for a unique $y$, with $\|f\|=\|y\|$ |
| (b) Parseval's identity | 2. A non-empty closed convex set has a unique element of minimum distance from any point |
| (c) Riesz representation theorem | 3. $\sum|\langle x,e_n\rangle|^2\le\|x\|^2$ |
| (d) Projection (best approximation) theorem | 4. $\sum|\langle x,e_n\rangle|^2=\|x\|^2$ for all $x$, if and only if $\{e_n\}$ is complete |

(A) a-3, b-4, c-1, d-2

(B) a-4, b-3, c-1, d-2

(C) a-3, b-4, c-2, d-1

(D) a-3, b-1, c-4, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) Every infinite-dimensional separable Hilbert space is isometrically isomorphic to $\ell^2$.

(B) Every orthonormal set in a separable Hilbert space is countable.

(C) Every Hilbert space is reflexive.

(D) Every infinite-dimensional Hilbert space has a countable orthonormal basis.

**Q8.** `[Numerical]` ★★★ On $\ell^2$, let $f(x)=\displaystyle\sum_{n=1}^\infty\frac{x_n}{2^{\,n-1}}=x_1+\frac{x_2}{2}+\frac{x_3}{4}+\cdots$. Then $\|f\|$ equals

(A) $2$

(B) $\dfrac{2}{\sqrt3}$

(C) $\dfrac43$

(D) $1$

**Q9.** `[Concept]` ★★ Let $S$ be the right shift on $\ell^2$, $S(x_1,x_2,\dots)=(0,x_1,x_2,\dots)$. Then

(A) $S^*=S$

(B) $S^*S=I$ but $SS^*\ne I$

(C) $SS^*=I$ but $S^*S\ne I$

(D) $S^*S=SS^*=I$

**Q10.** `[Application]` ★★★ The number of points on the $x$-axis nearest to $(0,1)$ is $m$ in $(\mathbb R^2,\|\cdot\|_2)$ and $k$ in $(\mathbb R^2,\|\cdot\|_\infty)$. Then

(A) $m=1,\ k=1$

(B) $m=1,\ k=2$

(C) $m=1$ and $k$ is infinite

(D) $m=2$ and $k$ is infinite

**Q11.** `[Concept]` ★ In an inner product space, equality $|\langle x,y\rangle|=\|x\|\,\|y\|$ holds if and only if

(A) $x\perp y$

(B) $x$ and $y$ are linearly dependent

(C) $\|x\|=\|y\|$

(D) $x=y$

**Q12.** `[Application]` ★★ In $\ell^2$, let $M=\{x\in\ell^2: x_1=x_2\}$. Then $M^\perp$ is

(A) $\{0\}$

(B) $\operatorname{span}\{(1,1,0,0,\dots)\}$

(C) $\{x: x_1=-x_2\}$

(D) $\operatorname{span}\{(1,-1,0,0,\dots)\}$

**Q13.** `[Numerical]` ★★★ Let $P:\mathbb R^2\to\mathbb R^2$, $P(x,y)=(x+y,0)$, with the Euclidean norm. Then $P^2=P$ and $\|P\|$ equals

(A) $1$

(B) $\sqrt2$

(C) $2$

(D) $\tfrac12$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | C | Numerical |
| 3 | A | Numerical |
| 4 | D | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true / Counterexample |
| 8 | B | Numerical |
| 9 | B | Concept |
| 10 | C | Application |
| 11 | B | Concept |
| 12 | D | Application |
| 13 | B | Numerical |

## Solutions
**Q1 — (C).** This is the Jordan–von Neumann theorem. If the parallelogram law holds, the polarization identity defines an inner product. Every norm satisfies (A), and (D) concerns completeness, not the inner product.

**Q2 — (C).** By the parallelogram law, $\|x-y\|^2=2(9+16)-25=25$, so $\|x-y\|=5$. (Here $x\perp y$.)

**Q3 — (A).** The best approximation is the orthogonal projection $t-\frac16$. The squared distance is $\int_0^1\left(t^2-t+\frac16\right)^2dt=\frac1{180}$, so the distance is $\frac1{\sqrt{180}}=\frac1{6\sqrt5}$. Option (B) forgets the square root.

**Q4 — (D).** $M^\perp=\bigcap_{y\in M}\ker\langle\cdot,y\rangle$ is closed for **any** subset $M$. In general $(M^\perp)^\perp=\overline M$, which differs from $M$ for a non-closed subspace, e.g. $c_{00}\subset\ell^2$, where $(c_{00}^\perp)^\perp=\ell^2$. So II fails. III is the projection theorem.

**Q5 — (A).** $\ell^p$ is complete for all $p\ge1$. With $x=e_1$ and $y=e_2$: $\|x\pm y\|_p^2=2^{2/p}$, so the left side of the parallelogram law is $2\cdot2^{2/p}$, while the right side is $4$. These are equal only when $p=2$. So no inner product induces the norm, and R explains A.

**Q6 — (A).** Bessel (3) holds for every orthonormal set. Parseval (4) characterises complete orthonormal sets. Riesz representation is (1). The projection or best-approximation theorem in a Hilbert space is (2).

**Q7 — (D).** A non-separable Hilbert space, such as $\ell^2(\mathbb R)$, has an uncountable orthonormal basis. (A) holds by Riesz–Fischer and Parseval. (B) holds because distinct orthonormal vectors are $\sqrt2$ apart. (C) follows from the Riesz representation theorem.

**Q8 — (B).** By Riesz, $f=\langle\cdot,y\rangle$ with $y=(1,\frac12,\frac14,\dots)$. So $\|f\|=\|y\|_2=\left(\sum_{n\ge0}4^{-n}\right)^{1/2}=\sqrt{4/3}=\frac{2}{\sqrt3}$. Option (A) is $\|y\|_1$, the norm of $f$ on $\ell^\infty$, not on $\ell^2$.

**Q9 — (B).** $S^*$ is the left shift $(x_1,x_2,\dots)\mapsto(x_2,x_3,\dots)$. Then $S^*Sx=x$, but $SS^*x=(0,x_2,x_3,\dots)\ne x$. $S$ is an isometry that is not unitary, and it is not self-adjoint.

**Q10 — (C).** In the Euclidean norm, closed convex sets in a Hilbert space have unique nearest points, so the unique point is $(0,0)$ and $m=1$. In the sup norm, $\|(0,1)-(t,0)\|_\infty=\max(|t|,1)=1$ for every $|t|\le1$, so there are infinitely many nearest points. Uniqueness needs the Hilbert (uniformly convex) structure.

**Q11 — (B).** The Cauchy–Schwarz inequality is an equality exactly when one vector is a scalar multiple of the other. (A) gives $\langle x,y\rangle=0$, which is the opposite extreme.

**Q12 — (D).** $M=\{x: \langle x,u\rangle=0\}$ for $u=(1,-1,0,\dots)$, i.e. $M=\{u\}^\perp$, which is closed. So $M^\perp=\{u\}^{\perp\perp}=\operatorname{span}\{u\}$. Option (B) is the common sign slip.

**Q13 — (B).** The matrix is $\begin{pmatrix}1&1\\0&0\end{pmatrix}$, and $A^TA=\begin{pmatrix}1&1\\1&1\end{pmatrix}$ has largest eigenvalue $2$, so $\|P\|=\sqrt2$. $P$ is idempotent but not self-adjoint, i.e. an oblique projection. Only **orthogonal** projections ($P^2=P=P^*$, $P\neq0$) have norm exactly $1$. That makes (A) the trap.
