# Unit 2 · Topic 01 — Linear Transformations, Rank–Nullity, Matrix Representation
> Syllabus coverage: Linear transformations, Algebra of linear transformations, kernel, range, Rank-Nullity Theorem, Matrix representation of a linear transformation, change of bases
> Cheatsheet: [../Cheatsheets/01-Linear-Transformations-Rank-Nullity-Matrix-Rep.md](../Cheatsheets/01-Linear-Transformations-Rank-Nullity-Matrix-Rep.md)

**Q1.** `[Concept]` ★ Let $T:\mathbb R^7\to\mathbb R^4$ be a linear transformation that is onto. Then $\dim\ker T$ equals

(A) 0

(B) 7

(C) 4

(D) 3

**Q2.** `[Numerical]` ★ Let $T:\mathbb R^3\to\mathbb R^3$, $T(x,y,z)=(x+y,\ y+z,\ x-z)$. The nullity of $T$ is

(A) 0

(B) 1

(C) 2

(D) 3

**Q3.** `[Numerical]` ★★ Let $P_4$ be the space of real polynomials of degree $\le 4$ and $D=\dfrac{d}{dx}$. The nullity of $D^2:P_4\to P_4$ is

(A) 1

(B) 2

(C) 3

(D) 4

**Q4.** `[Multi-Statement]` ★★ Consider the statements:

I. There exists an injective linear map $\mathbb R^3\to\mathbb R^2$.

II. There exists a surjective linear map $\mathbb R^3\to\mathbb R^2$.

III. If $V$ is finite-dimensional and $T:V\to V$ is linear and one-one, then $T$ is onto.

Which of the above is/are correct?

(A) II and III only

(B) I and II only

(C) III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** There is no linear map $T:\mathbb R^5\to\mathbb R^5$ with $\ker T=\operatorname{range}T$.
**Reason (R):** If $\ker T=\operatorname{range}T$, then by the Rank–Nullity Theorem $5=2\operatorname{rank}T$, which is impossible.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match the subspace of $M_3(\mathbb{R})$ (List-I) with its dimension (List-II).

| List-I | List-II |
|---|---|
| (a) $M_3(\mathbb{R})$ | 1. 3 |
| (b) symmetric matrices | 2. 6 |
| (c) skew-symmetric matrices | 3. 8 |
| (d) trace-zero matrices | 4. 9 |

(A) a-4, b-2, c-1, d-3

(B) a-4, b-1, c-2, d-3

(C) a-3, b-2, c-1, d-4

(D) a-4, b-2, c-3, d-1

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following maps is **NOT** linear over the indicated field?

(A) $z\mapsto \bar z$ on $\mathbb{C}$, regarded as a vector space over $\mathbb{R}$

(B) $f\mapsto \int_0^1 f(t)\thinspace dt$ on $C[0,1]$ over $\mathbb{R}$

(C) $A\mapsto \operatorname{tr}A$ on $M_n(\mathbb{C})$ over $\mathbb{C}$

(D) $z\mapsto \bar z$ on $\mathbb{C}$, regarded as a vector space over $\mathbb{C}$

**Q8.** `[Application]` ★★★ Let $V$ be a real vector space of dimension 6 and $T:V\to V$ a linear map with $T^2=0$. The maximum possible rank of $T$ is

(A) 2

(B) 5

(C) 4

(D) 3

**Q9.** `[Numerical]` ★★ A linear operator $T$ on $\mathbb R^2$ has matrix $`\begin{pmatrix}1&2\cr 0&3\end{pmatrix}`$ with respect to the standard basis. Its matrix with respect to the ordered basis $\mathcal{B}=\lbrace (1,0),(1,1)\rbrace$ is

(A) $`\begin{pmatrix}1&2\cr 0&3\end{pmatrix}`$

(B) $`\begin{pmatrix}1&0\cr 0&3\end{pmatrix}`$

(C) $`\begin{pmatrix}3&0\cr 0&1\end{pmatrix}`$

(D) $`\begin{pmatrix}1&3\cr 0&3\end{pmatrix}`$

**Q10.** `[Concept]` ★ The dimension of the real vector space $L(\mathbb R^3,\mathbb R^4)$ of all linear maps from $\mathbb R^3$ to $\mathbb R^4$ is

(A) 7

(B) 4

(C) 12

(D) 81

**Q11.** `[Application]` ★★★ Let $U$ and $W$ be subspaces of $\mathbb R^7$ with $\dim U=4$ and $\dim W=5$. The smallest possible value of $\dim(U\cap W)$ is

(A) 0

(B) 1

(C) 2

(D) 4

**Q12.** `[NOT-true / Counterexample]` ★ Two similar $n\times n$ matrices $A$ and $B=P^{-1}AP$ need **NOT** have the same

(A) trace

(B) rank

(C) eigenvectors

(D) characteristic polynomial

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | B | Numerical |
| 4 | A | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true |
| 8 | D | Application |
| 9 | B | Numerical |
| 10 | C | Concept |
| 11 | C | Application |
| 12 | C | NOT-true |

## Solutions
**Q1 — (D).** Onto means rank $=4$. Rank–Nullity: nullity $=7-4=3$. (C) mixes up rank and nullity.

**Q2 — (B).** The matrix $`\begin{pmatrix}1&1&0\cr 0&1&1\cr 1&0&-1\end{pmatrix}`$ has determinant $0$ and two independent rows, so rank $2$ and nullity $3-2=1$. The kernel is spanned by $(1,-1,1)$.

**Q3 — (B).** $D^2$ sends $1,x\mapsto 0$ and $x^2,x^3,x^4\mapsto 2,6x,12x^2$, so its kernel is $P_1$, of dimension 2. (A) is the nullity of $D$ itself.

**Q4 — (A).** I is false: an injective map needs $\dim(\text{domain})\le\dim(\text{codomain})$. II is true (take the projection $`(x,y,z)\mapsto(x,y)`$). III is true: injective means nullity $0$, so rank $=\dim V$. III fails for infinite-dimensional $V$ (for example the right shift on sequences).

**Q5 — (A).** If $\ker T=\operatorname{range}T$ then rank $=$ nullity $=r$ and $2r=5$, which is impossible. R gives exactly this argument. In even dimension such maps exist, e.g. $`\begin{pmatrix}0&1\cr 0&0\end{pmatrix}`$ on $\mathbb R^2$.

**Q6 — (A).** For $n=3$: $n^2=9$, $n(n+1)/2=6$, $n(n-1)/2=3$, $n^2-1=8$.

**Q7 — (D).** Over $\mathbb{C}$, $\overline{iz}=-i\bar z\ne i\bar z$, so conjugation is not $\mathbb{C}$-linear. It is additive and commutes with real scalars, so (A) is linear. Linearity depends on the field of scalars.

**Q8 — (D).** $T^2=0$ gives $\operatorname{range}T\subseteq\ker T$, so $r\le 6-r$ and $r\le3$. The bound is attained by three Jordan blocks $`\begin{pmatrix}0&1\cr 0&0\end{pmatrix}`$.

**Q9 — (B).** Take $`P=\begin{pmatrix}1&1\cr 0&1\end{pmatrix}`$ (new basis vectors as columns). Then $`P^{-1}AP=\begin{pmatrix}1&0\cr 0&3\end{pmatrix}`$. This works because $(1,0)$ and $(1,1)$ are eigenvectors for $1$ and $3$. The order of the basis fixes the order on the diagonal, which rules out (C).

**Q10 — (C).** $\dim L(V,W)=\dim V\cdot\dim W=3\cdot4=12$, since these maps correspond to $4\times3$ matrices.

**Q11 — (C).** $\dim(U\cap W)=\dim U+\dim W-\dim(U+W)\ge 4+5-7=2$, and equality is possible.

**Q12 — (C).** Similar matrices share trace, determinant, rank, characteristic and minimal polynomials, and eigenvalues. Eigenvectors change: if $Av=\lambda v$ then $B(P^{-1}v)=\lambda P^{-1}v$.
