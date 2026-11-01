# Unit 9 · Topic 07 — Linear Systems: Gauss Elimination, LU, Jacobi and Gauss–Seidel
> Syllabus coverage: Solution of systems of linear algebraic equations using Gauss elimination and Gauss-Seidel methods
> Cheatsheet: [../Cheatsheets/07-Linear-Systems-Gauss-Elimination-Gauss-Seidel.md](../Cheatsheets/07-Linear-Systems-Gauss-Elimination-Gauss-Seidel.md)

**Q1.** `[Concept]` ★ For a dense $n\times n$ system, the number of multiplications/divisions in Gauss elimination (with back substitution) is asymptotically

(A) $n^3/3$

(B) $n^3/2$

(C) $n^3$

(D) $n^2$

**Q2.** `[Concept]` ★ The Gauss–Seidel method converges for every initial vector whenever the coefficient matrix $A$ is

(A) symmetric with nonzero diagonal entries

(B) nonsingular

(C) symmetric positive definite

(D) of positive determinant

**Q3.** `[Numerical]` ★ In the Doolittle factorisation $A=LU$ ($L$ unit lower triangular) of $A=\begin{pmatrix}2&3\\4&7\end{pmatrix}$, the entry $u_{22}$ is

(A) $-1$

(B) $2$

(C) $3$

(D) $1$

**Q4.** `[Numerical]` ★★ Gauss elimination without pivoting is applied to
$$x+y+z=6,\quad x+2y+3z=14,\quad x+4y+9z=36.$$
The third pivot $u_{33}$ in the resulting upper triangular system is

(A) $1$

(B) $2$

(C) $3$

(D) $6$

**Q5.** `[Numerical]` ★★ For the system
$$10x+y+z=12,\quad x+10y+z=12,\quad x+y+10z=12,$$
the first Gauss–Seidel iterate from $(0,0,0)$ is

(A) $(1.2,\ 1.2,\ 1.2)$

(B) $(1.2,\ 0.96,\ 0.984)$

(C) $(1.2,\ 1.08,\ 1.08)$

(D) $(1.2,\ 1.08,\ 0.972)$

**Q6.** `[Numerical]` ★★★ For $A=\begin{pmatrix}2&-1\\-1&2\end{pmatrix}$, the spectral radius of the Gauss–Seidel iteration matrix is

(A) $1/2$

(B) $1/8$

(C) $1/\sqrt2$

(D) $1/4$

**Q7.** `[Multi-Statement]` ★★ Consider the following statements.

I. If $A$ is strictly diagonally dominant, both the Jacobi and the Gauss–Seidel methods converge for every starting vector.

II. The iteration $x^{(k+1)}=Bx^{(k)}+c$ converges for every $x^{(0)}$ if and only if $\rho(B)<1$.

III. For every matrix $A$, convergence of the Jacobi method implies convergence of the Gauss–Seidel method.

Which are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** Gauss elimination without row interchanges breaks down on $y=1,\ x+y=2$ (written in this order), although the system has a unique solution.
**Reason (R):** Gauss elimination without pivoting runs to completion only when the leading principal minors $\Delta_1,\dots,\Delta_{n-1}$ of $A$ are nonzero.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match the process with its asymptotic number of multiplications for an $n\times n$ dense system.

| List-I | List-II |
|---|---|
| A. Gauss elimination (forward phase) | 1. $n^2$ |
| B. Gauss–Jordan elimination | 2. $n^3/3$ |
| C. Back substitution | 3. $n^3/2$ |
| D. One Gauss–Seidel sweep | 4. $n^2/2$ |

(A) A-2, B-3, C-4, D-1

(B) A-3, B-2, C-4, D-1

(C) A-2, B-3, C-1, D-4

(D) A-2, B-1, C-4, D-3

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) If all leading principal minors of $A$ are nonzero, $A$ has a unique factorisation $A=LU$ with $L$ unit lower triangular.

(B) Every symmetric positive definite matrix has a Cholesky factorisation $A=LL^{T}$.

(C) Every nonsingular matrix has an $LU$ factorisation without row interchanges.

(D) In the Doolittle factorisation, $\det A$ equals the product of the diagonal entries of $U$.

**Q11.** `[Application]` ★★ Consider the system $x+2y=3,\ 2x+y=3$. Which of the following is correct about the Jacobi method?

(A) It converges with the equations in the given order.

(B) It diverges in both orders.

(C) It diverges in the given order, but converges after the two equations are interchanged.

(D) It converges in both orders.

**Q12.** `[Application]` ★★★ Let $A=\begin{pmatrix}1&2&-2\\1&1&1\\2&2&1\end{pmatrix}$. For $Ax=b$ with an arbitrary starting vector,

(A) both Jacobi and Gauss–Seidel converge

(B) Jacobi converges but Gauss–Seidel diverges

(C) Gauss–Seidel converges but Jacobi diverges

(D) both diverge

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | C | Concept |
| 3 | D | Numerical |
| 4 | B | Numerical |
| 5 | D | Numerical |
| 6 | D | Numerical |
| 7 | B | Multi-Statement |
| 8 | A | Assertion-Reason |
| 9 | A | Match |
| 10 | C | NOT-true / Counterexample |
| 11 | C | Application |
| 12 | B | Application |

## Solutions
**Q1 — (A).** Forward elimination costs $\sum_k (n-k)^2\approx n^3/3$, while back substitution costs only $n^2/2$. $n^3/2$ is the cost of Gauss–Jordan.

**Q2 — (C).** Gauss–Seidel converges for SPD matrices (Ostrowski–Reich theorem). Symmetry or nonsingularity alone is not enough.

**Q3 — (D).** $l_{21}=4/2=2$, so $u_{22}=7-2\cdot3=1$. As a check, $\det A=2\cdot1=2$.

**Q4 — (B).** $R_2-R_1$ gives $(0,1,2\mid8)$ and $R_3-R_1$ gives $(0,3,8\mid30)$. Then $R_3-3R_2$ gives $(0,0,2\mid6)$, so $u_{33}=2$ and $z=3$, with solution $(1,2,3)$. Distractor (C) is $z$. As a check, $\det A=1\cdot1\cdot2=2$, which is the Vandermonde value.

**Q5 — (D).** $x=12/10=1.2$, then $y=(12-1.2)/10=1.08$, then $z=(12-1.2-1.08)/10=0.972$. (A) is the Jacobi iterate, which does not use the new values.

**Q6 — (D).** The Jacobi matrix $\begin{pmatrix}0&1/2\\1/2&0\end{pmatrix}$ has $\rho_J=1/2$. For this tridiagonal (consistently ordered) matrix $\rho_{GS}=\rho_J^2=1/4$. Directly, $B_{GS}=-(D+L)^{-1}U=\begin{pmatrix}0&1/2\\0&1/4\end{pmatrix}$. (A) is $\rho_J$.

**Q7 — (B).** I is the standard sufficient condition. II is the fundamental theorem of stationary iterations. III is false: there are matrices for which Jacobi converges and GS diverges (Q12), and also the reverse.

**Q8 — (A).** In the given order $a_{11}=0$, so the first pivot vanishes ($\Delta_1=0$) and the elimination cannot start, although $\det A=-1\ne0$. R is exactly the condition for no-pivot elimination ($u_{kk}=\Delta_k/\Delta_{k-1}$), so it explains A. Partial pivoting (swapping rows) fixes the problem.

**Q9 — (A).** Gauss elimination costs $n^3/3$, Gauss–Jordan $n^3/2$, back substitution $n^2/2$, and one sweep of an iterative method on a dense matrix about $n^2$.

**Q10 — (C).** $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ is nonsingular, but $a_{11}=l_{11}u_{11}=u_{11}=0$ would force $l_{21}u_{11}=1$, which is impossible. Only $PA=LU$ is guaranteed. A, B and D are standard facts.

**Q11 — (C).** In the given order $B_J=\begin{pmatrix}0&-2\\-2&0\end{pmatrix}$ with $\rho=2>1$, so Jacobi diverges. After interchanging, $A=\begin{pmatrix}2&1\\1&2\end{pmatrix}$ is diagonally dominant and $\rho=1/2$, so it converges (solution $x=y=1$).

**Q12 — (B).** $B_J$ is nilpotent ($B_J^3=0$), so $\rho_J=0$ and Jacobi converges (in at most 3 steps). $B_{GS}$ has eigenvalues $0,2,2$, so $\rho_{GS}=2$ and Gauss–Seidel diverges. This is the classic counterexample to "GS is always better".
