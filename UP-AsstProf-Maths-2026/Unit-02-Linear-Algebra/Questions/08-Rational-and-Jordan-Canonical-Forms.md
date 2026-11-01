# Unit 2 · Topic 08 — Rational and Jordan Canonical Forms
> Syllabus coverage: Rational and Jordan canonical forms (similarity classes, Jordan blocks from rank data, invariant factors)
> Cheatsheet: [../Cheatsheets/08-Rational-and-Jordan-Canonical-Forms.md](../Cheatsheets/08-Rational-and-Jordan-Canonical-Forms.md)

**Q1.** `[Concept]` ★ The number of Jordan blocks for an eigenvalue $\lambda$ in the Jordan form of $A$ equals

(A) the algebraic multiplicity of $\lambda$

(B) the geometric multiplicity of $\lambda$

(C) the multiplicity of $\lambda$ as a root of the minimal polynomial

(D) $\mathop{\mathrm{rank}}\nolimits(A-\lambda I)$

**Q2.** `[Numerical]` ★★ The number of similarity classes of $4\times4$ nilpotent complex matrices is

(A) 4

(B) 8

(C) 7

(D) 5

**Q3.** `[Numerical]` ★★ A complex matrix has characteristic polynomial $(x-2)^3(x-3)^2$. The number of possible Jordan canonical forms (up to the order of blocks) is

(A) 5

(B) 12

(C) 8

(D) 6

**Q4.** `[Numerical]` ★★ A $4\times4$ complex matrix has characteristic polynomial $(x-1)^4$ and minimal polynomial $(x-1)^2$. The number of possible Jordan forms is

(A) 2

(B) 1

(C) 3

(D) 4

**Q5.** `[Application]` ★★★ Let $N$ be a $6\times6$ nilpotent matrix with $\mathop{\mathrm{rank}}\nolimits N=3$, $\mathop{\mathrm{rank}}\nolimits N^2=1$ and $N^3=0$. The sizes of the Jordan blocks of $N$ are

(A) $3,3$

(B) $2,2,2$

(C) $3,2,1$

(D) $4,1,1$

**Q6.** `[Multi-Statement]` ★★ For $A,B\in M_n(\mathbb{C})$ consider:

I. $A$ and $B$ are similar iff they have the same Jordan canonical form (up to the order of blocks).

II. If $A$ and $B$ have the same characteristic and minimal polynomials, then they are similar.

III. $A$ is similar to $A^T$.

Which is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** Every complex square matrix is similar to an upper triangular matrix.
**Reason (R):** Over $\mathbb{C}$ the characteristic polynomial splits into linear factors, so a Jordan form exists.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Let $J_4(\lambda)$ be the $4\times4$ Jordan block with eigenvalue $\lambda$. Match:

| List-I | List-II |
|---|---|
| (a) $\mathop{\mathrm{rank}}\nolimits J_4(0)$ | 1. 1 |
| (b) minimal polynomial of $J_4(2)$ | 2. 2 |
| (c) $\dim$ of the eigenspace of $J_4(2)$ | 3. 3 |
| (d) nullity of $J_4(0)^2$ | 4. $(x-2)^4$ |

(A) a-3, b-4, c-1, d-2

(B) a-3, b-4, c-2, d-1

(C) a-1, b-4, c-3, d-2

(D) a-4, b-3, c-1, d-2

**Q9.** `[NOT-true / Counterexample]` ★★ Let $C(f)$ be the companion matrix of a monic polynomial $f$ of degree $n$. Which of the following is **NOT** always true?

(A) the characteristic polynomial of $C(f)$ is $f$

(B) the minimal polynomial of $C(f)$ is $f$

(C) $C(f)$ is diagonalizable over $\mathbb{C}$

(D) every eigenvalue of $C(f)$ has geometric multiplicity 1

**Q10.** `[Numerical]` ★★ A matrix over $\mathbb{Q}$ has elementary divisors $(x-1),\ (x-1)^2,\ (x-2)$. Its invariant factors (which give the rational canonical form) are

(A) $(x-1),\ (x-1)^2,\ (x-2)$

(B) $(x-1),\ (x-1)^2(x-2)$

(C) $(x-1)(x-2),\ (x-1)^2$

(D) $(x-1)^3(x-2)$

**Q11.** `[Application]` ★★★ The number of similarity classes of $3\times3$ complex matrices $A$ satisfying $A^3=I$ is

(A) 3

(B) 6

(C) 9

(D) 10

**Q12.** `[Concept]` ★ The Jordan canonical form of a non-zero $2\times2$ nilpotent matrix is

(A) $`\begin{pmatrix}0&0\cr 0&0\end{pmatrix}`$

(B) $`\begin{pmatrix}0&1\cr 0&0\end{pmatrix}`$

(C) $`\begin{pmatrix}1&1\cr 0&0\end{pmatrix}`$

(D) $`\begin{pmatrix}0&1\cr 1&0\end{pmatrix}`$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | D | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | C | Application |
| 6 | C | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | A | Match |
| 9 | C | NOT-true |
| 10 | B | Numerical |
| 11 | D | Application |
| 12 | B | Concept |

## Solutions
**Q1 — (B).** Each Jordan block contributes exactly one eigenvector, so the number of blocks is $\dim\ker(A-\lambda I)$. (A) gives the *total size* of the blocks, and (C) gives the size of the *largest* block.

**Q2 — (D).** Nilpotent classes correspond to partitions of 4: $4,\ 3{+}1,\ 2{+}2,\ 2{+}1{+}1,\ 1{+}1{+}1{+}1$. So $p(4)=5$.

**Q3 — (D).** Choose the blocks for each eigenvalue independently: $p(3)\cdot p(2)=3\cdot2=6$. (A) adds instead of multiplying.

**Q4 — (A).** The largest block must have size exactly 2, so the partitions of 4 with largest part 2 are $2{+}2$ and $2{+}1{+}1$. This also shows that the characteristic and minimal polynomials do not determine the class when $n\ge4$.

**Q5 — (C).** The number of blocks of size $\ge k$ is $\mathop{\mathrm{rank}}\nolimits N^{k-1}-\mathop{\mathrm{rank}}\nolimits N^k$. That gives $6-3=3$ blocks of size $\ge1$, $3-1=2$ of size $\ge2$, $1-0=1$ of size $\ge3$, and none of size $\ge4$. So the sizes are $3,2,1$. Check: (A) gives rank sequence $4,2,0$ and (B) gives $3,0$.

**Q6 — (C).** II fails for $n\ge4$: $J_2(0)\oplus J_2(0)$ and $J_2(0)\oplus J_1(0)\oplus J_1(0)$ both have $\chi=x^4$ and $m=x^2$ but different ranks (2 and 1). II does hold for $n\le3$. III is true because $J_k(\lambda)^T$ is similar to $J_k(\lambda)$ via the reversal permutation.

**Q7 — (A).** The Jordan form is upper triangular and exists exactly because $\chi_A$ splits over $\mathbb{C}$. (Schur's theorem gives this unitarily as well.)

**Q8 — (A).** $\mathop{\mathrm{rank}}\nolimits J_4(0)=3$. The minimal polynomial of $J_4(2)$ is $(x-2)^4$. A single block has a 1-dimensional eigenspace. $J_4(0)^2$ has rank 2, so its nullity is 2.

**Q9 — (C).** $`C(x^2)=\begin{pmatrix}0&0\cr 1&0\end{pmatrix}`$ is non-zero nilpotent, so it is not diagonalizable. $C(f)$ is diagonalizable over $\mathbb C$ iff $f$ has distinct roots. (A), (B) and (D) always hold: $C(f)$ is cyclic, so each eigenvalue has a single Jordan block.

**Q10 — (B).** Group the highest powers first: $d_2=(x-1)^2(x-2)$ (the minimal polynomial), then $d_1=(x-1)$. Each divides the next, $d_1\mid d_2$, and the product is the characteristic polynomial $(x-1)^3(x-2)$. (C) fails the divisibility $d_1\mid d_2$.

**Q11 — (D).** $x^3-1$ has distinct roots $1,\omega,\omega^2$, so $A$ is diagonalizable. Its class is determined by the multiset of 3 eigenvalues chosen from 3 values, and there are $\binom{3+3-1}{3}=10$ such multisets. (A) counts only scalar matrices.

**Q12 — (B).** $N\ne0$ and $N^2=0$ give a single block $J_2(0)$. (D) is not nilpotent, since its square is $I$.
