# Cheatsheet · Unit 2 · Topic 04 — Eigenvalues, Cayley–Hamilton Theorem, Diagonalization

## 1. Eigenvalues and eigenvectors
- $\lambda$ is an eigenvalue of $A$ $\iff$ $Av=\lambda v$ for some $v\ne0$ $\iff$ $\det(A-\lambda I)=0$.
- **Characteristic polynomial:** $\chi_A(x)=\det(xI-A)=x^n-(\operatorname{tr}A)x^{n-1}+\dots+(-1)^n\det A$.
- For $2\times2$ matrices: $\chi=x^2-(\operatorname{tr})x+\det$. For $3\times3$: $\chi=x^3-(\operatorname{tr})x^2+(\text{sum of principal }2\times2\text{ minors})x-\det$.
- $\sum\lambda_i=\operatorname{tr}A$ and $\prod\lambda_i=\det A$. $A$ is singular $\iff 0$ is an eigenvalue.
- **Algebraic multiplicity** (AM) is the multiplicity as a root of $\chi$. **Geometric multiplicity** (GM) is $\dim\ker(A-\lambda I)=n-\operatorname{rank}(A-\lambda I)$. Always $1\le\text{GM}\le\text{AM}$.

| Matrix | Eigenvalues | Eigenvector |
|---|---|---|
| $A^k$ | $\lambda^k$ | same $v$ |
| $p(A)$ | $p(\lambda)$ | same $v$ |
| $A^{-1}$ | $1/\lambda$ | same $v$ |
| $\operatorname{adj}A$ | $\det A/\lambda$ | same $v$ (for invertible $A$) |
| $A+cI$ | $\lambda+c$ | same $v$ |
| $A^T$ | $\lambda$ | different in general |
| $P^{-1}AP$ | $\lambda$ | $P^{-1}v$ |
| $AB$ vs $BA$ | same non-zero eigenvalues; $\chi_{AB}=\chi_{BA}$ for square matrices | |

- Triangular or diagonal matrices have their diagonal entries as eigenvalues.
- $J_n$ (all ones) has eigenvalues $n$ (once) and $0$ ($n-1$ times).
- $aI+bJ_n$ has eigenvalues $a+nb$ (once) and $a$ ($n-1$ times).
- A rank-one matrix $uv^T$ has eigenvalues $v^Tu$ and $0$ ($n-1$ times).
- An $n$-cycle permutation matrix has the $n$-th roots of unity as eigenvalues.
- Eigenvectors for distinct eigenvalues are linearly independent.

## 2. Cayley–Hamilton theorem
Every square matrix satisfies its own characteristic equation: $\chi_A(A)=0$.
- **Inverse:** if $\chi_A(x)=x^n+c_{n-1}x^{n-1}+\dots+c_0$ with $c_0\ne0$, then $A^{-1}=-\frac1{c_0}(A^{n-1}+c_{n-1}A^{n-2}+\dots+c_1I)$.
- **Powers:** reduce $A^m$ modulo $\chi_A$, so $A^m=r(A)$ with $\deg r<n$. Find $r$ by evaluating at the eigenvalues, using derivatives at repeated roots.
- **Classic:** $A=\begin{pmatrix}1&0&0\\1&0&1\\0&1&0\end{pmatrix}$ satisfies $A^n=A^{n-2}+A^2-I$, so $A^{2m}=mA^2-(m-1)I$.

## 3. Minimal polynomial $m_A$
- $m_A$ is the monic polynomial of least degree with $m_A(A)=0$. It divides every $p$ with $p(A)=0$, in particular $\chi_A$.
- $m_A$ and $\chi_A$ have the **same roots**, possibly with different multiplicities.
- The multiplicity of $\lambda$ in $m_A$ equals the size of the largest Jordan block for $\lambda$.
- Similar matrices have the same $m_A$.
- **Diagonalizability test:** $A$ is diagonalizable over $F$ $\iff$ $m_A$ splits into **distinct** linear factors over $F$.
- **Block diagonal:** $m_{A\oplus B}=\operatorname{lcm}(m_A,m_B)$.

## 4. Diagonalization
$A$ ($n\times n$) is diagonalizable $\iff$ it has $n$ independent eigenvectors $\iff$ GM $=$ AM for every eigenvalue (and $\chi$ splits) $\iff$ $m_A$ has distinct roots.
- Sufficient condition: $n$ **distinct** eigenvalues. This is not necessary, e.g. $I$.
- Then $P^{-1}AP=D$, where the columns of $P$ are the eigenvectors in the order of the diagonal of $D$. This gives $A^k=PD^kP^{-1}$.
- **Simultaneous diagonalization:** two diagonalizable matrices are simultaneously diagonalizable iff $AB=BA$.
- Real symmetric matrices are always orthogonally diagonalizable (spectral theorem, Topic 05).
- Rotation by $\theta\notin\pi\mathbb Z$ is not diagonalizable over $\mathbb R$ but is diagonalizable over $\mathbb C$.

## 5. Special matrices
| Type | Minimal polynomial | Eigenvalues | Key facts |
|---|---|---|---|
| Nilpotent ($N^k=0$) | $x^k$, $k\le n$ | all $0$ | $\operatorname{tr}=0$, $\det=0$, $I+N$ invertible, diagonalizable only if $N=0$, $N^n=0$ |
| Idempotent ($P^2=P$) | divides $x(x-1)$ | $0,1$ | diagonalizable, $\operatorname{rank}=\operatorname{tr}$, $I-P$ idempotent, $V=\ker P\oplus\operatorname{range}P$ |
| Involution ($A^2=I$) | divides $x^2-1$ | $\pm1$ | diagonalizable (char $\ne2$) |
| $A^k=I$ over $\mathbb C$ | divides $x^k-1$ | $k$-th roots of unity | diagonalizable |
| Transpose map on $M_n$ | $x^2-1$ | $+1$ (mult. $n(n+1)/2$), $-1$ (mult. $n(n-1)/2$) | $\operatorname{tr}=n$ |

- A real $n\times n$ matrix with $A^2=-I$ exists iff $n$ is even, since $\det(A)^2=(-1)^n$.

## Exam traps
- A repeated eigenvalue does **not** imply non-diagonalizable. Check GM.
- A non-zero nilpotent matrix is **never** diagonalizable, yet it has all eigenvalues equal (to $0$).
- The minimal polynomial must contain every eigenvalue. Dropping a root is a common distractor.
- Eigenvalues of $A+B$ or $AB$ are **not** sums or products of eigenvalues in general (unless $A,B$ commute, and even then only after pairing).
- $\det(p(A))=\prod p(\lambda_i)$: multiply, don't add.
