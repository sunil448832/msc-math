# Unit 2 · Topic 04 — Eigenvalues, Cayley–Hamilton Theorem, Diagonalization
> Syllabus coverage: eigen values and eigen vectors, Cayley-Hamilton Theorem, diagonalization (with minimal polynomial, trace/determinant, nilpotent/idempotent matrices)
> Cheatsheet: [../Cheatsheets/04-Eigenvalues-Cayley-Hamilton-Diagonalization.md](../Cheatsheets/04-Eigenvalues-Cayley-Hamilton-Diagonalization.md)

**Q1.** `[Concept]` ★ If $\lambda$ is an eigenvalue of an invertible $n\times n$ matrix $A$, then an eigenvalue of $\mathop{\mathrm{adj}}\nolimits A$ is

(A) $\lambda\det A$

(B) $\lambda^{n-1}$

(C) $\dfrac{1}{\lambda}$

(D) $\dfrac{\det A}{\lambda}$

**Q2.** `[Numerical]` ★★ A $3\times3$ matrix $A$ has eigenvalues $1,2,3$. Then $\det(A^2+I)$ equals

(A) 15

(B) 50

(C) 100

(D) 196

**Q3.** `[Numerical]` ★★ For $`A=\begin{pmatrix}1&2\cr 2&1\end{pmatrix}`$, the Cayley–Hamilton theorem gives $A^{-1}=$

(A) $\tfrac13(A-2I)$

(B) $\tfrac13(2I-A)$

(C) $A-2I$

(D) $\tfrac12(A-3I)$

**Q4.** `[Multi-Statement]` ★★ Consider the following for $A\in M_n(\mathbb{C})$:

I. Eigenvectors belonging to distinct eigenvalues are linearly independent.

II. $A$ is diagonalizable if and only if its minimal polynomial has no repeated roots.

III. If $A$ has a repeated eigenvalue, then $A$ is not diagonalizable.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★
**Assertion (A):** $`\begin{pmatrix}1&1\cr 0&1\end{pmatrix}`$ is not diagonalizable.
**Reason (R):** Its only eigenvalue $1$ has geometric multiplicity 1, which is less than its algebraic multiplicity 2.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match the matrix $A\in M_n(\mathbb{C})$ (List-I) with its minimal polynomial (List-II).

| List-I | List-II |
|---|---|
| (a) $A^k=0,\ A^{k-1}\ne0$ | 1. $x(x-1)$ |
| (b) $A^2=A,\ A\ne0,I$ | 2. $x^k$ |
| (c) $A^2=I,\ A\ne\pm I$ | 3. $x-c$ |
| (d) $A=cI$ | 4. $(x-1)(x+1)$ |

(A) a-2, b-1, c-4, d-3

(B) a-2, b-4, c-1, d-3

(C) a-1, b-2, c-4, d-3

(D) a-3, b-1, c-4, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Let $N\neq0$ be a nilpotent $n\times n$ complex matrix. Which of the following is **NOT** true?

(A) every eigenvalue of $N$ is $0$

(B) $\mathop{\mathrm{tr}}\nolimits N=0$

(C) $I+N$ is invertible

(D) $N$ is diagonalizable

**Q8.** `[Application]` ★★★ Let $T:M_3(\mathbb{R})\to M_3(\mathbb{R})$ be $T(X)=X^T$. The trace of $T$ (as a linear operator on the 9-dimensional space) is

(A) 0

(B) 3

(C) 6

(D) 9

**Q9.** `[Application]` ★★ Let $P$ be a $4\times4$ real matrix with $P^2=P$ and $\mathop{\mathrm{tr}}\nolimits P=2$. Then $\mathop{\mathrm{rank}}\nolimits P$ is

(A) 1

(B) 3

(C) 2

(D) cannot be determined

**Q10.** `[Numerical]` ★ The eigenvalues of $`\begin{pmatrix}4&1\cr 2&3\end{pmatrix}`$ are

(A) $1,6$

(B) $2,5$

(C) $3,4$

(D) $-2,-5$

**Q11.** `[Concept]` ★★ The characteristic polynomial of $A$ is $(x-1)^2(x-2)^3$. Which of the following **can** be the minimal polynomial of $A$?

(A) $(x-1)(x-2)^4$

(B) $(x-2)^3$

(C) $(x-1)^2(x-2)$

(D) $(x-1)^3(x-2)$

**Q12.** `[Numerical]` ★★★ Let $`A=\begin{pmatrix}1&0&0\cr 1&0&1\cr 0&1&0\end{pmatrix}`$. Using $A^n=A^{n-2}+A^2-I$ (for $n\ge3$), which follows from Cayley–Hamilton, $A^{50}$ equals

(A) $I$

(B) $`\begin{pmatrix}1&0&0\cr 50&1&0\cr 50&0&1\end{pmatrix}`$

(C) $`\begin{pmatrix}1&0&0\cr 25&0&1\cr 25&1&0\end{pmatrix}`$

(D) $`\begin{pmatrix}1&0&0\cr 25&1&0\cr 25&0&1\end{pmatrix}`$

**Q13.** `[Application]` ★★ Let $`A=\begin{pmatrix}0&1&0\cr 0&0&1\cr 1&0&0\end{pmatrix}`$. Then $A^{100}$ equals

(A) $I$

(B) $A$

(C) $A^2$

(D) $A^T$ with $A^T\ne A^2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Numerical |
| 3 | A | Numerical |
| 4 | B | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true |
| 8 | B | Application |
| 9 | C | Application |
| 10 | B | Numerical |
| 11 | C | Concept |
| 12 | D | Numerical |
| 13 | B | Application |

## Solutions
**Q1 — (D).** $\mathop{\mathrm{adj}}\nolimits A=(\det A)A^{-1}$ and $A^{-1}v=\lambda^{-1}v$, so $\mathop{\mathrm{adj}}\nolimits A\thinspace v=\dfrac{\det A}{\lambda}v$.

**Q2 — (C).** The eigenvalues of $A^2+I$ are $\lambda^2+1=2,5,10$, and their product is $100$. (A) adds instead of multiplying.

**Q3 — (A).** The characteristic polynomial is $\lambda^2-2\lambda-3$, so $A^2-2A-3I=0$. Then $A(A-2I)=3I$, giving $A^{-1}=\frac13(A-2I)$. (B) has the wrong sign.

**Q4 — (B).** I and II are standard. III is false: $I_n$ has a repeated eigenvalue and is diagonal. A repeated eigenvalue is only *necessary* for non-diagonalizability, not sufficient.

**Q5 — (A).** A matrix is diagonalizable iff GM $=$ AM for every eigenvalue. Here $A-I$ has rank 1, so GM $=1\lt 2$.

**Q6 — (A).** Nilpotent of index $k$ gives $x^k$. A non-trivial idempotent gives $x(x-1)$, a non-trivial involution gives $x^2-1$, and $cI$ gives $x-c$.

**Q7 — (D).** A diagonalizable nilpotent matrix is similar to $\mathop{\mathrm{diag}}\nolimits(0,\dots,0)=0$, so it is $0$. Since $N\ne0$, (D) fails. (C) holds because the eigenvalues of $I+N$ are all $1$, so $\det(I+N)=1$.

**Q8 — (B).** $T$ is $+1$ on symmetric matrices (dimension 6) and $-1$ on skew-symmetric matrices (dimension 3), so $\mathop{\mathrm{tr}}\nolimits T=6-3=3$. In general $\mathop{\mathrm{tr}}\nolimits T=n$ and $\det T=(-1)^{n(n-1)/2}$. (C) counts only the $+1$ eigenspace.

**Q9 — (C).** An idempotent is diagonalizable with eigenvalues 0 and 1, so $\mathop{\mathrm{rank}}\nolimits P=\mathop{\mathrm{tr}}\nolimits P=2$.

**Q10 — (B).** The trace is 7 and the determinant is 10, so $\lambda^2-7\lambda+10=0$ and $\lambda=2,5$.

**Q11 — (C).** The minimal polynomial divides the characteristic polynomial and has the same roots. (A) and (D) exceed the multiplicities, and (B) misses the root $1$.

**Q12 — (D).** The characteristic polynomial is $(\lambda-1)(\lambda^2-1)$, which gives $A^3=A^2+A-I$ and hence $A^n=A^{n-2}+A^2-I$. Then $A^{2m}=mA^2-(m-1)I$, and for $m=25$ this is $25A^2-24I$, the matrix in (D).

**Q13 — (B).** $A$ is a cyclic permutation matrix, so $A^3=I$. Since $100=3\cdot33+1$, $A^{100}=A$. (D) is a trap: for a permutation matrix $A^T=A^{-1}=A^2$, so (D) is impossible.
