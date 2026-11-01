# Cheatsheet · Unit 2 · Topic 05 — Hermitian, Skew-Hermitian, Unitary (and Orthogonal, Normal) Matrices

## 1. Definitions ($A^\ast =\bar A^T$)
| Class | Definition | Real analogue | Eigenvalues | Diagonal entries |
|---|---|---|---|---|
| Hermitian | $A^\ast =A$ | symmetric | real | real |
| Skew-Hermitian | $A^\ast =-A$ | skew-symmetric | $0$ or purely imaginary | $0$ or purely imaginary |
| Unitary | $U^\ast U=I$ | orthogonal ($Q^TQ=I$) | $\lvert\lambda\rvert=1$ | $\lvert u_{ii}\rvert\le1$ |
| Normal | $AA^\ast =A^\ast A$ | — | anywhere | — |
| Positive definite | Hermitian with $x^\ast Ax\gt 0$ for $x\ne0$ | — | $\gt 0$ | $\gt 0$ |
| Orthogonal projection | $P^2=P=P^\ast$ | — | $0,1$ | in $[0,1]$ |

## 2. Algebraic facts
- $A$ is Hermitian $\iff iA$ is skew-Hermitian.
- **Cartesian decomposition:** $A=H+S$ uniquely, with $H=\frac{A+A^\ast }2$ and $S=\frac{A-A^\ast }2$. Equivalently $A=H_1+iH_2$ with $H_1,H_2$ Hermitian.
- $A^\ast A$ and $AA^\ast$ are always Hermitian and positive semidefinite.
- For Hermitian $A,B$: $AB$ is Hermitian $\iff AB=BA$, and $AB+BA$ and $i(AB-BA)$ are Hermitian.
- $\det$ of a Hermitian matrix is real. $\det$ of a unitary matrix has modulus 1. $\det$ of a real orthogonal matrix is $\pm1$.
- A skew-Hermitian $S$ of order $n$ has $\det S$ real if $n$ is even and purely imaginary (or $0$) if $n$ is odd.
- A real skew-symmetric matrix of **odd** order has $\det=0$. Its rank is always even.
- Products and inverses of unitary matrices are unitary, so the unitary matrices form the group $U(n)$. Sums of unitary matrices need not be unitary.
- $U$ is unitary $\iff$ its columns (equivalently rows) are orthonormal $\iff \Vert Ux\Vert =\Vert x\Vert$ for all $x$ $\iff \langle Ux,Uy\rangle=\langle x,y\rangle$.
- **Cayley transform:** for skew-Hermitian $S$, $I+S$ is invertible and $(I-S)(I+S)^{-1}$ is unitary (orthogonal if $S$ is real).

## 3. Spectral theorems
- **Normal:** $A$ is normal $\iff A=UDU^\ast$ with $U$ unitary and $D$ diagonal (unitarily diagonalizable).
- **Hermitian:** unitarily diagonalizable with real $D$. Eigenvectors for distinct eigenvalues are orthogonal.
- **Real symmetric:** $A=QDQ^T$ with $Q$ real orthogonal.
- Normal $+$ real spectrum $\iff$ Hermitian. Normal $+$ spectrum on the unit circle $\iff$ unitary. Normal $+$ imaginary spectrum $\iff$ skew-Hermitian.
- **Schur:** every $A$ is unitarily similar to an upper triangular matrix, and $A$ is normal iff that triangular matrix is diagonal.
- Hermitian $A$ with $A^k=I$ ($k$ odd) forces $A=I$. Hermitian (or normal) nilpotent forces $0$.

## 4. Orthogonal matrices
- $2\times2$, $\det=1$: rotation $`\begin{pmatrix}\cos\theta&-\sin\theta\cr \sin\theta&\cos\theta\end{pmatrix}`$ with eigenvalues $e^{\pm i\theta}$.
- $2\times2$, $\det=-1$: reflection $`\begin{pmatrix}\cos\theta&\sin\theta\cr \sin\theta&-\cos\theta\end{pmatrix}`$, which is symmetric with eigenvalues $\pm1$.
- $3\times3$ with $\det=1$: always has eigenvalue $1$ (a rotation axis), and $\mathop{\mathrm{tr}}\nolimits=1+2\cos\theta$.
- Any $n\times n$ orthogonal $Q$ with $\det Q=-1$ has eigenvalue $-1$. If $n$ is odd and $\det Q=1$, then $1$ is an eigenvalue.
- The real eigenvalues of an orthogonal matrix are $\pm1$.

## 5. Quick checks
- **Normality test for $2\times2$ real matrices:** $`\begin{pmatrix}a&b\cr c&d\end{pmatrix}`$ is normal iff $b=c$, or ($b=-c$ and $a=d$).
- **Unitary test:** check that every column has norm 1 and that $\langle c_i,c_j\rangle=\sum_k (c_i)_k\overline{(c_j)_k}=0$ for $i\ne j$.

## Exam traps
- Hermitian does **not** mean positive eigenvalues; it only means real ones.
- A unitary matrix need not be Hermitian; the two coincide only when $U^2=I$.
- When computing $\det$ of a Hermitian $2\times2$ matrix, use $|b|^2$, not $b^2$.
- A complex symmetric matrix ($A^T=A$) need **not** be Hermitian or normal. For example $`\begin{pmatrix}1&i\cr i&-1\end{pmatrix}`$ is symmetric and nilpotent, not normal.
- A triangular matrix that is normal must be diagonal.
