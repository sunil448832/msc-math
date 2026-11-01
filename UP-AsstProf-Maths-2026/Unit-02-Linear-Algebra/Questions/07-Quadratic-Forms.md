# Unit 2 · Topic 07 — Quadratic Forms
> Syllabus coverage: Quadratic forms, reduction and classification of quadratic forms (rank, index, signature, definiteness, canonical form, Sylvester's law of inertia)
> Cheatsheet: [../Cheatsheets/07-Quadratic-Forms.md](../Cheatsheets/07-Quadratic-Forms.md)

**Q1.** `[Concept]` ★ The symmetric matrix of the quadratic form $q(x,y)=x^2+4xy+2y^2$ is

(A) $`\begin{pmatrix}1&4\cr 0&2\end{pmatrix}`$

(B) $`\begin{pmatrix}1&4\cr 4&2\end{pmatrix}`$

(C) $`\begin{pmatrix}1&2\cr 2&2\end{pmatrix}`$

(D) $`\begin{pmatrix}1&2\cr 2&1\end{pmatrix}`$

**Q2.** `[Numerical]` ★★ For the real quadratic form $q=2xy+2yz+2zx$, the (rank, index, signature) is

(A) $(2,1,0)$

(B) $(3,2,1)$

(C) $(3,1,-1)$

(D) $(3,1,1)$

**Q3.** `[Numerical]` ★★★ The quadratic form $q=x^2+y^2+z^2+2k(xy+yz+zx)$ is positive definite if and only if

(A) $-1\lt k\lt 1$

(B) $-\tfrac12\lt k\lt 1$

(C) $0\lt k\lt 1$

(D) $-1\lt k\lt \tfrac12$

**Q4.** `[Multi-Statement]` ★★ Let $A$ be a real symmetric $n\times n$ matrix. Consider:

I. $A$ is positive definite iff all its eigenvalues are positive.

II. $A$ is positive definite iff all its leading principal minors are positive.

III. $A$ is positive semidefinite iff all its leading principal minors are non-negative.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** The form $x^2-4xy+y^2$ is indefinite.
**Reason (R):** The determinant of its $2\times2$ symmetric matrix is negative, so its two eigenvalues have opposite signs.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match the form on $\mathbb R^2$ with its nature.

| List-I | List-II |
|---|---|
| (a) $x^2+y^2$ | 1. indefinite |
| (b) $x^2-y^2$ | 2. negative definite |
| (c) $(x-y)^2$ | 3. positive definite |
| (d) $-x^2-2y^2$ | 4. positive semidefinite, not definite |

(A) a-3, b-1, c-2, d-4

(B) a-3, b-4, c-1, d-2

(C) a-4, b-1, c-3, d-2

(D) a-3, b-1, c-4, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Under a congruence $A\mapsto P^TAP$ ($P$ real invertible), which of the following is **NOT** necessarily preserved?

(A) rank

(B) index (number of positive squares)

(C) signature

(D) eigenvalues

**Q8.** `[Application]` ★★★ The number of congruence classes of real symmetric $3\times3$ matrices (equivalently, of real quadratic forms in 3 variables) is

(A) 4

(B) 7

(C) 9

(D) 10

**Q9.** `[Concept]` ★ Sylvester's law of inertia states that for a real quadratic form

(A) the number of positive and negative coefficients in any diagonal (canonical) form is the same

(B) every quadratic form is positive definite after a suitable change of variables

(C) the eigenvalues are invariant under every change of variables

(D) the canonical form is unique as a matrix, not just up to signs

**Q10.** `[Numerical]` ★ An orthogonal change of variables reduces $5x^2+8xy+5y^2$ to

(A) $9X^2+Y^2$

(B) $5X^2+5Y^2$

(C) $9X^2-Y^2$

(D) $13X^2-3Y^2$

**Q11.** `[Application]` ★★ The maximum value of $q=x^2+y^2+z^2+2xy+2yz+2zx$ on the unit sphere $x^2+y^2+z^2=1$ is

(A) 1

(B) 2

(C) 3

(D) 9

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | C | Numerical |
| 3 | B | Numerical |
| 4 | B | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | D | Match |
| 7 | D | NOT-true |
| 8 | D | Application |
| 9 | A | Concept |
| 10 | A | Numerical |
| 11 | C | Application |

## Solutions
**Q1 — (C).** Each cross term coefficient is split equally: $a_{12}=a_{21}=\tfrac42=2$. (B) doubles the cross term, and (A) is not symmetric.

**Q2 — (C).** The matrix $J-I$ has eigenvalues $2,-1,-1$. So the rank is 3, the index $p=1$, and the signature $p-q=1-2=-1$. Some books define signature as $p+q$ or report $(p,q)$; under the standard convention $s=p-q$, (C) is correct.

**Q3 — (B).** The matrix $(1-k)I+kJ$ has eigenvalues $1+2k$ (once) and $1-k$ (twice). Both are positive iff $-\tfrac12\lt k\lt 1$. (A) uses only the $2\times2$ leading minor $1-k^2\gt 0$.

**Q4 — (B).** III is false: $\mathop{\mathrm{diag}}\nolimits(0,-1)$ has leading minors $0,0$ but is negative semidefinite. For PSD you need **all** principal minors to be $\ge0$.

**Q5 — (A).** The matrix $`\begin{pmatrix}1&-2\cr -2&1\end{pmatrix}`$ has $\det=-3\lt 0$, so the eigenvalues $3$ and $-1$ have opposite signs. Example values: $q(1,1)=-2$ and $q(1,0)=1$.

**Q6 — (D).** $(x-y)^2\ge0$ and it vanishes on $x=y$, so it is positive semidefinite but not definite.

**Q7 — (D).** Congruence preserves rank, index and signature (Sylvester's law) but not eigenvalues. For example, $P=2I$ multiplies the eigenvalues by 4. Similarity, not congruence, preserves eigenvalues.

**Q8 — (D).** A class is determined by the pair $(p,q)$ with $p+q\le3$, and there are $\binom{5}{2}=10$ such pairs. In general there are $\frac{(n+1)(n+2)}2$ classes. (A) counts only the possible ranks.

**Q9 — (A).** The counts $p$ and $q$ of positive and negative squares are invariants, while the actual diagonal coefficients are not. That rules out (C) and (D).

**Q10 — (A).** The matrix $`\begin{pmatrix}5&4\cr 4&5\end{pmatrix}`$ has eigenvalues $9$ and $1$. Orthogonal reduction gives $\lambda_1X^2+\lambda_2Y^2$.

**Q11 — (C).** $q=(x+y+z)^2$ has matrix $J$ with eigenvalues $3,0,0$. The maximum of $x^TAx$ on $\Vert x\Vert =1$ is $\lambda_{\max}=3$, attained at $\frac1{\sqrt3}(1,1,1)$ (Rayleigh quotient). (D) forgets the normalization.
