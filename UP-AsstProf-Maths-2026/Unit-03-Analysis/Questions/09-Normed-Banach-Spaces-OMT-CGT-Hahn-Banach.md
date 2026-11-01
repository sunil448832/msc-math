# Unit 3 · Topic 09 — Normed Linear Spaces, Banach Spaces, OMT, CGT, Hahn–Banach
> Syllabus coverage: Normed linear spaces, Banach spaces, open mapping theorem, closed graph theorem, Hahn-Banach theorem (also: bounded operators and operator norm, equivalence of norms, uniform boundedness principle, dual spaces)
> Cheatsheet: [../Cheatsheets/09-Normed-Banach-Spaces-OMT-CGT-Hahn-Banach.md](../Cheatsheets/09-Normed-Banach-Spaces-OMT-CGT-Hahn-Banach.md)

**Q1.** `[Concept]` ★ On a finite-dimensional real vector space,

(A) only the Euclidean norm makes it complete

(B) the $\ell^1$ and $\ell^\infty$ norms give different topologies

(C) any two norms are equivalent

(D) a linear functional may be discontinuous for some norm

**Q2.** `[Numerical]` ★ The smallest constant $c$ such that $\Vert x\Vert _1\le c\thinspace \Vert x\Vert _2$ for all $x\in\mathbb R^4$ is

(A) $1$

(B) $\sqrt2$

(C) $2$

(D) $4$

**Q3.** `[Numerical]` ★★ The operator norm of $`A=\begin{pmatrix}1&2\cr 3&4\end{pmatrix}`$ acting on $(\mathbb R^2,\Vert \cdot\Vert _1)$ is

(A) $5$

(B) $6$

(C) $7$

(D) $10$

**Q4.** `[Numerical]` ★★★ On $C[0,1]$ with the sup norm, let $\varphi(x)=\displaystyle\int_0^1x(t)\thinspace dt-x\negthinspace \left(\tfrac12\right)$. Then $\Vert \varphi\Vert$ equals

(A) $0$

(B) $1$

(C) $\tfrac32$

(D) $2$

**Q5.** `[Multi-Statement]` ★★ Consider the following statements.

I. A bounded linear surjection between Banach spaces is an open map.

II. A bounded linear bijection between Banach spaces has a bounded inverse.

III. A linear map between normed spaces whose graph is closed is bounded.

Which is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q6.** `[Assertion-Reason]` ★
**Assertion (A):** Every finite-dimensional subspace of a normed linear space is closed.
**Reason (R):** Every finite-dimensional normed linear space is complete.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each space with its dual space (up to isometric isomorphism).

| List-I | List-II |
|---|---|
| (a) $c_0$ | 1. $\ell^{3/2}$ |
| (b) $\ell^1$ | 2. $\ell^\infty$ |
| (c) $\ell^3$ | 3. $\ell^1$ |
| (d) $C[a,b]$ (sup norm) | 4. $NBV[a,b]$ (regular Borel measures on $[a,b]$) |

(A) a-2, b-3, c-1, d-4

(B) a-3, b-2, c-1, d-4

(C) a-3, b-2, c-4, d-1

(D) a-3, b-1, c-2, d-4

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) $\ell^\infty$ is not separable.

(B) $c_0$ is separable.

(C) $\ell^1$ is reflexive.

(D) $\ell^p$ is reflexive for $1\lt p\lt \infty$.

**Q9.** `[Concept]` ★★ For a normed space $X$ (not necessarily complete), its dual $X^\ast$ with the operator norm

(A) is always a Banach space

(B) is a Banach space if and only if $X$ is a Banach space

(C) may be $\lbrace 0\rbrace$ even when $X\ne\lbrace 0\rbrace$

(D) is always isometrically isomorphic to $X$

**Q10.** `[Application]` ★★★ Let $D:(C^1[0,1],\Vert \cdot\Vert _\infty)\to(C[0,1],\Vert \cdot\Vert _\infty)$, $Df=f'$. Which of the following is true?

(A) $D$ is bounded, by the closed graph theorem.

(B) $D$ has a closed graph but is unbounded. This does not contradict the closed graph theorem, because $(C^1[0,1],\Vert \cdot\Vert _\infty)$ is not complete.

(C) The graph of $D$ is not closed.

(D) $D$ is bounded with $\Vert D\Vert =1$.

**Q11.** `[Application]` ★★ The space $\mathbb R[x]$ of all real polynomials

(A) is a Banach space under the sup norm on $[0,1]$

(B) admits no norm under which it is a Banach space

(C) is a Banach space under every norm, since all norms on it are equivalent

(D) is a Banach space under the norm $\Vert \sum a_kx^k\Vert =\sum|a_k|$

**Q12.** `[Concept]` ★ The closed unit ball of a normed space $X$ is compact if and only if

(A) $X$ is complete

(B) $X$ is reflexive

(C) $X$ is separable

(D) $X$ is finite-dimensional

**Q13.** `[Multi-Statement]` ★★★ Let $X$ be a normed space. Consider the following statements.

I. If $f(x)=0$ for every $f\in X^\ast$, then $x=0$.

II. $\Vert x\Vert =\sup\lbrace |f(x)|: f\in X^\ast ,\ \Vert f\Vert \le1\rbrace$ for every $x\in X$, and the supremum is attained.

III. A norm-preserving (Hahn–Banach) extension of a bounded linear functional from a subspace to $X$ is always unique.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q14.** `[Concept]` ★★ Let $X$ be a Banach space, $Y$ a normed space, and $\lbrace T_\alpha\rbrace$ a family of bounded linear operators $X\to Y$ with $\sup_\alpha\Vert T_\alpha x\Vert \lt \infty$ for every $x\in X$. Then necessarily

(A) $\sup_\alpha\Vert T_\alpha\Vert \lt \infty$

(B) $\lbrace T_\alpha\rbrace$ has a norm-convergent subsequence

(C) $T_\alpha x\to0$ for every $x$

(D) each $T_\alpha$ is compact

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | C | Numerical |
| 3 | B | Numerical |
| 4 | D | Numerical |
| 5 | D | Multi-Statement |
| 6 | A | Assertion-Reason |
| 7 | B | Match |
| 8 | C | NOT-true / Counterexample |
| 9 | A | Concept |
| 10 | B | Application |
| 11 | B | Application |
| 12 | D | Concept |
| 13 | B | Multi-Statement |
| 14 | A | Concept |

## Solutions
**Q1 — (C).** All norms on a finite-dimensional space are equivalent. So every norm makes the space complete, all norms give the same topology, and every linear map is continuous.

**Q2 — (C).** By Cauchy–Schwarz, $\sum|x_i|\le\sqrt n\left(\sum x_i^2\right)^{1/2}$, with equality at $x=(1,1,1,1)$. So $c=\sqrt4=2$. Option (D) confuses $\sqrt n$ with $n$.

**Q3 — (B).** $\Vert A\Vert _{1\to1}$ is the maximum absolute **column** sum: $\max(1+3,2+4)=6$. The maximum row sum, $7$, is $\Vert A\Vert _{\infty\to\infty}$, which is the trap.

**Q4 — (D).** $|\varphi(x)|\le\Vert x\Vert +\Vert x\Vert =2\Vert x\Vert$. Take $x$ equal to $1$ except for a narrow continuous dip to $-1$ at $t=\frac12$ (width $\to0$). Then $\varphi(x)\to1-(-1)=2$. So $\Vert \varphi\Vert =2$. It is not attained, since that would need $x=1$ a.e. and $x(\frac12)=-1$.

**Q5 — (D).** I is the open mapping theorem and II is the bounded inverse theorem. III needs completeness of the spaces: see Q10, where a closed-graph unbounded operator is defined on an incomplete space.

**Q6 — (A).** A finite-dimensional subspace $M$ is complete with the induced norm (R). A complete subspace of a metric space is closed. So R is exactly why A holds.

**Q7 — (B).** $c_0^\ast =\ell^1$ and $(\ell^1)^\ast =\ell^\infty$. For $\ell^3$ the conjugate exponent is $q$ with $\frac13+\frac1q=1$, so $(\ell^3)^\ast =\ell^{3/2}$. $C[a,b]^\ast$ is $NBV[a,b]$ by the Riesz representation theorem. A common error is $(\ell^\infty)^\ast =\ell^1$; that is false, since $\ell^1$ is only the dual of $c_0$.

**Q8 — (C).** If $X$ is reflexive and separable, then $X^\ast$ is separable. But $\ell^1$ is separable and $(\ell^1)^\ast =\ell^\infty$ is not, so $\ell^1$ is not reflexive. (Equivalently, $(\ell^\infty)^\ast \supsetneq\ell^1$.) (A), (B) and (D) are standard.

**Q9 — (A).** $B(X,Y)$ is complete whenever $Y$ is, and $X^\ast =B(X,\mathbb R)$ with $\mathbb R$ complete. (C) is ruled out by Hahn–Banach. (B) is wrong: $c_{00}$ is incomplete but $c_{00}^\ast \cong\ell^1$ is Banach.

**Q10 — (B).** Suppose $f_n\to f$ and $f_n'\to g$ uniformly. Then $f\in C^1$ and $f'=g$, so the graph is closed. But $\Vert t^n\Vert _\infty=1$ while $\Vert (t^n)'\Vert _\infty=n$, so $D$ is unbounded. The closed graph theorem needs **both** spaces complete, and the domain here is not.

**Q11 — (B).** $\mathbb R[x]$ has the countably infinite Hamel basis $\lbrace 1,x,x^2,\dots\rbrace$. By Baire, an infinite-dimensional Banach space cannot have a countable Hamel basis: it would be a countable union of the closed, nowhere dense finite-dimensional subspaces. (A) and (D) describe incomplete normed spaces. (C) is false because "all norms equivalent" holds only in finite dimensions.

**Q12 — (D).** This is Riesz's lemma: in infinite dimensions, there is a sequence of unit vectors with $\Vert x_n-x_m\Vert \ge\frac12$ for $n\neq m$. $\ell^2$ is complete, separable and reflexive, yet its unit ball is not compact.

**Q13 — (B).** I and II are corollaries of Hahn–Banach: for $x\ne0$ there is $f$ with $\Vert f\Vert =1$ and $f(x)=\Vert x\Vert$, so the supremum is attained. III is false. In $(\mathbb R^2,\Vert \cdot\Vert _1)$, $f(x,0)=x$ on the $x$-axis has the norm-one extensions $x+cy$ for every $|c|\le1$. (Uniqueness holds, for instance, in Hilbert spaces.)

**Q14 — (A).** This is the uniform boundedness principle (Banach–Steinhaus). Completeness of $X$ is essential. On $c_{00}$ (finitely supported sequences, sup norm), $T_nx=nx_n$ is pointwise bounded, since $x_n$ is eventually $0$, but $\Vert T_n\Vert =n$. Nothing forces (B), (C) or (D).
