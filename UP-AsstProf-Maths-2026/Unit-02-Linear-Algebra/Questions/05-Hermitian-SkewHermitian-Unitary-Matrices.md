# Unit 2 · Topic 05 — Hermitian, Skew-Hermitian and Unitary Matrices
> Syllabus coverage: Hermitian, Skew-Hermitian and Unitary matrices (also orthogonal and normal matrices, location of eigenvalues)
> Cheatsheet: [../Cheatsheets/05-Hermitian-SkewHermitian-Unitary-Matrices.md](../Cheatsheets/05-Hermitian-SkewHermitian-Unitary-Matrices.md)

**Q1.** `[Concept]` ★ The eigenvalues of a Hermitian matrix are

(A) purely imaginary

(B) real

(C) of modulus 1

(D) always positive

**Q2.** `[Match]` ★★ Match the class of matrices (List-I) with the location of its eigenvalues (List-II).

| List-I | List-II |
|---|---|
| (a) Hermitian | 1. on the unit circle $\lvert z\rvert=1$ |
| (b) Skew-Hermitian | 2. in $\{0,1\}$ |
| (c) Unitary | 3. on the real axis |
| (d) Hermitian idempotent | 4. on the imaginary axis |

(A) a-3, b-1, c-4, d-2

(B) a-4, b-3, c-1, d-2

(C) a-3, b-4, c-2, d-1

(D) a-3, b-4, c-1, d-2

**Q3.** `[Numerical]` ★★ The eigenvalues of $A=\begin{pmatrix}2&1+i\\1-i&3\end{pmatrix}$ are

(A) $2,3$

(B) $1,4$

(C) $\tfrac{5\pm i\sqrt7}{2}$

(D) $0,5$

**Q4.** `[Multi-Statement]` ★★ Consider:

I. If $A$ is Hermitian, then $iA$ is skew-Hermitian.

II. Every $A\in M_n(\mathbb{C})$ can be written uniquely as $H+S$ with $H$ Hermitian and $S$ skew-Hermitian.

III. The product of two Hermitian matrices is Hermitian.

Which is/are correct?

(A) I only

(B) II and III only

(C) I and II only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** The determinant of a unitary matrix has modulus 1.
**Reason (R):** If $U$ is unitary, then $|\det U|^2=\det U\cdot\overline{\det U}=\det(UU^*)=1$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[NOT-true / Counterexample]` ★★ Let $U$ be an $n\times n$ unitary matrix. Which of the following is **NOT** necessarily true?

(A) the columns of $U$ form an orthonormal basis of $\mathbb{C}^n$

(B) $\|Ux\|=\|x\|$ for all $x\in\mathbb{C}^n$

(C) $U^{-1}=U^*$

(D) $U$ is Hermitian

**Q7.** `[Numerical]` ★★ The matrix $\dfrac1{\sqrt2}\begin{pmatrix}1&1\\ i&a\end{pmatrix}$ is unitary for

(A) $a=i$

(B) $a=-i$

(C) $a=1$

(D) $a=-1$

**Q8.** `[Application]` ★★★ Let $A$ be an $n\times n$ Hermitian matrix with $A^5=I$. Then

(A) $A$ can be any matrix whose eigenvalues are fifth roots of unity

(B) $A$ need not be diagonalizable

(C) $A=\pm I$

(D) $A=I$

**Q9.** `[Concept]` ★ If $A$ is a real skew-symmetric matrix of order 5, then $\det A$ is

(A) 1

(B) $-1$

(C) 0

(D) positive

**Q10.** `[Application]` ★★ If $S$ is a real skew-symmetric matrix, then the matrix $(I-S)(I+S)^{-1}$

(A) may fail to exist, since $I+S$ can be singular

(B) is always defined and symmetric

(C) is always defined and orthogonal

(D) is always defined and skew-symmetric

**Q11.** `[Concept]` ★★ Every $3\times3$ real orthogonal matrix $Q$ with $\det Q=1$

(A) has $1$ as an eigenvalue

(B) has $-1$ as an eigenvalue

(C) is symmetric

(D) has only real eigenvalues

**Q12.** `[NOT-true / Counterexample]` ★★ Which of the following matrices is **NOT** normal?

(A) $\begin{pmatrix}1&1\\0&1\end{pmatrix}$

(B) $\begin{pmatrix}1&-1\\1&1\end{pmatrix}$

(C) $\begin{pmatrix}0&1\\-1&0\end{pmatrix}$

(D) $\begin{pmatrix}2&i\\ i&2\end{pmatrix}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | D | Match |
| 3 | B | Numerical |
| 4 | C | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | D | NOT-true |
| 7 | B | Numerical |
| 8 | D | Application |
| 9 | C | Concept |
| 10 | C | Application |
| 11 | A | Concept |
| 12 | A | NOT-true |

## Solutions
**Q1 — (B).** From $Av=\lambda v$: $\lambda\|v\|^2=v^*Av=\overline{v^*Av}$, so $\lambda$ is real. Positivity needs positive definiteness, so (D) is wrong.

**Q2 — (D).** Hermitian matrices have real eigenvalues, skew-Hermitian ones have purely imaginary (or zero) eigenvalues, and unitary ones have $|\lambda|=1$. A Hermitian idempotent is an orthogonal projection, with eigenvalues $0,1$.

**Q3 — (B).** The trace is $5$ and the determinant is $6-(1+i)(1-i)=6-2=4$. Then $\lambda^2-5\lambda+4=0$ gives $\lambda=1,4$, which are real as expected. (C) uses $(1+i)^2$ instead of $|1+i|^2$.

**Q4 — (C).** I: $(iA)^*=-iA^*=-iA$. II: take $H=\frac{A+A^*}2$ and $S=\frac{A-A^*}2$. III is false: $(AB)^*=BA$, so $AB$ is Hermitian iff $AB=BA$.

**Q5 — (A).** R is the proof. It uses $\det U^*=\overline{\det U}$ and $UU^*=I$.

**Q6 — (D).** For example $\begin{pmatrix}0&-1\\1&0\end{pmatrix}$ is unitary but not Hermitian. A unitary matrix is Hermitian iff $U^2=I$.

**Q7 — (B).** The columns must be orthogonal: $\langle c_2,c_1\rangle=1\cdot\bar1+a\cdot\bar i=1-ia=0$, so $a=1/i=-i$, and $|a|=1$ makes the columns unit vectors. With $a=i$ the inner product is $2$.

**Q8 — (D).** A Hermitian matrix is unitarily diagonalizable with real eigenvalues. A real $\lambda$ with $\lambda^5=1$ is $1$, so $A=U\,I\,U^*=I$. (C) would need $\lambda^5=1$ for $\lambda=-1$, which fails, and (A) ignores that the eigenvalues are real.

**Q9 — (C).** $\det A=\det A^T=\det(-A)=(-1)^5\det A$, so $\det A=0$.

**Q10 — (C).** The eigenvalues of $S$ are purely imaginary, so $-1$ is never an eigenvalue and $I+S$ is invertible. The Cayley transform of a skew-symmetric (skew-Hermitian) matrix is orthogonal (unitary).

**Q11 — (A).** The eigenvalues are $1$ or conjugate pairs $e^{\pm i\theta}$ (or $\pm1$), and their product is $1$. With 3 eigenvalues, a real one must exist, and the product condition forces $1$ to occur. This is Euler's rotation theorem: $Q$ is a rotation about an axis. A rotation by $90^\circ$ about the $z$-axis refutes (B), (C) and (D).

**Q12 — (A).** For $A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$, $AA^T=\begin{pmatrix}2&1\\1&1\end{pmatrix}\ne A^TA=\begin{pmatrix}1&1\\1&2\end{pmatrix}$. (B) is a scaled rotation, (C) is skew-symmetric, and (D) $=2I+iJ$ with $J$ real symmetric, so $A^*=2I-iJ$ commutes with $A$.
