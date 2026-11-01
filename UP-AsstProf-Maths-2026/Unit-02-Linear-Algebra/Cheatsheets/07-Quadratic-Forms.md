# Cheatsheet · Unit 2 · Topic 07 — Quadratic Forms

## 1. Basics
- A real quadratic form is $q(x)=x^TAx=\sum_{i,j}a_{ij}x_ix_j$ with $A=A^T$ (unique symmetric matrix).
- **Matrix from the form:** $a_{ii}$ is the coefficient of $x_i^2$, and $a_{ij}=a_{ji}=\tfrac12\times$ the coefficient of $x_ix_j$.
- Example: $`x^2+4xy+2y^2\leftrightarrow\begin{pmatrix}1&2\cr 2&2\end{pmatrix}`$, and $2xy+2yz+2zx\leftrightarrow J-I$.
- A change of variables $x=Py$ ($P$ invertible) sends $A\mapsto P^TAP$, which is **congruence**.
- **Hermitian forms** $x^\ast Ax$ ($A=A^\ast$) are always real-valued and follow the same theory with $P^\ast AP$.

## 2. Invariants (Sylvester's law of inertia)
Every real quadratic form can be reduced by congruence to
$$y_1^2+\dots+y_p^2-y_{p+1}^2-\dots-y_{p+q}^2,$$
and the numbers $p,q$ do not depend on the reduction.

| Invariant | Value |
|---|---|
| rank $r$ | $p+q=\operatorname{rank}A$ |
| index | $p$, the number of positive eigenvalues |
| signature | $s=p-q$ (some texts use $`(p,q)`$) |
| nullity | $n-r$, the number of zero eigenvalues |

- Two real symmetric matrices are congruent $\iff$ they have the same rank and signature.
- Number of congruence classes of $n\times n$ real symmetric matrices: $\dfrac{(n+1)(n+2)}2$ (pairs $p+q\le n$). For $n=2$ this is 6, for $n=3$ it is 10.
- Over $\mathbb C$ (with $P^TAP$), only the rank is an invariant, giving $n+1$ classes.
- Congruence does **not** preserve eigenvalues or the determinant (only the sign of $\det$).

## 3. Classification
| Nature | Eigenvalues | Canonical form | Test |
|---|---|---|---|
| Positive definite (PD) | all $\gt 0$ | $\sum_1^n y_i^2$ | all leading principal minors $\gt 0$ |
| Positive semidefinite (PSD) | all $\ge0$, some $=0$ | $\sum_1^r y_i^2$, $r\lt n$ | **all** principal minors $\ge0$ |
| Negative definite (ND) | all $\lt 0$ | $-\sum y_i^2$ | leading minors alternate: $D_1\lt 0,D_2\gt 0,D_3\lt 0,\dots$ |
| Negative semidefinite (NSD) | all $\le0$ | | $-A$ is PSD |
| Indefinite | both signs | $p,q\ge1$ | |

- **$2\times2$ shortcut** for $ax^2+2bxy+cy^2$ with $D=ac-b^2$: if $D\gt 0$ the form is PD when $a\gt 0$ and ND when $a\lt 0$; if $D\lt 0$ it is indefinite; if $D=0$ it is semidefinite.
- PD implies: every diagonal entry $\gt 0$, $\det\gt 0$, $\operatorname{tr}\gt 0$, $A^{-1}$ is PD, $A=B^TB$ (Cholesky), and $|a_{ij}|^2\lt a_{ii}a_{jj}$.
- $A^TA$ is always PSD, and PD iff $A$ has full column rank.
- The family $(1-k)I_n+kJ_n$ has eigenvalues $1+(n-1)k$ and $1-k$, so it is PD $\iff -\frac1{n-1}\lt k\lt 1$.

## 4. Reduction methods
1. **Orthogonal reduction (principal axes):** find the eigenvalues $\lambda_i$ and orthonormal eigenvectors forming $Q$. With $x=Qy$, $q=\sum\lambda_iy_i^2$.
2. **Lagrange (completing squares):** for example $x^2+4xy+y^2=(x+2y)^2-3y^2$, which gives $p=1,q=1$. If there are no square terms (like $2xy$), substitute $x=u+v$, $y=u-v$.
3. **Congruent row/column operations:** apply each elementary row operation together with the same column operation to $[A\thinspace |\thinspace I]$.

## 5. Extremal properties (Rayleigh)
- $\lambda_{\min}\le\dfrac{x^TAx}{x^Tx}\le\lambda_{\max}$. So the max (min) of $q$ on the unit sphere is $\lambda_{\max}$ ($\lambda_{\min}$).
- The conic $ax^2+2bxy+cy^2=1$ is an ellipse if PD, a hyperbola if indefinite, and a pair of parallel lines if semidefinite with rank 1.

## Exam traps
- Halve the cross-term coefficients when writing $A$.
- PSD needs **all** principal minors $\ge0$, not just the leading ones (counterexample $`\operatorname{diag}(0,-1)`$).
- Signature means $p-q$ (unless the question defines it otherwise), and index means $p$.
- Congruence preserves signs, not values, of the eigenvalues. Similarity preserves the values.
- The leading $2\times2$ minor alone is not enough for $3\times3$ forms: check $\det A$ too.
