# Cheatsheet · Unit 2 · Topic 06 — Inner Product Spaces, Orthonormal Basis, Gram–Schmidt

## 1. Inner product axioms (over $F=\mathbb R$ or $\mathbb C$)
1. $\langle u,u\rangle\gt 0$ for $u\ne0$ (positive definite).
2. Linear in the first slot: $\langle au+bv,w\rangle=a\langle u,w\rangle+b\langle v,w\rangle$.
3. $\langle u,v\rangle=\overline{\langle v,u\rangle}$ (conjugate symmetry). Hence it is conjugate-linear in the second slot.

- On $\mathbb R^n$ **every** inner product has the form $\langle x,y\rangle=x^TAy$ with $A$ symmetric positive definite. Test $A$ with leading minors $\gt 0$.
- Standard examples:
  - $\mathbb C^n$: $\langle x,y\rangle=\sum x_i\bar y_i$.
  - $C[a,b]$: $\int_a^b f\bar g$.
  - $M_n$: $\langle A,B\rangle=\operatorname{tr}(B^\ast A)$ (Frobenius).

## 2. Key inequalities and identities
| Name | Statement |
|---|---|
| Cauchy–Schwarz | $\lvert\langle u,v\rangle\rvert\le\Vert u\Vert \Vert v\Vert$, with equality iff $u,v$ are linearly dependent |
| Triangle inequality | $\Vert u+v\Vert \le\Vert u\Vert +\Vert v\Vert$ |
| Pythagoras | $u\perp v\Rightarrow\Vert u+v\Vert ^2=\Vert u\Vert ^2+\Vert v\Vert ^2$ (the converse holds over $\mathbb R$, not over $\mathbb C$) |
| Parallelogram law | $\Vert u+v\Vert ^2+\Vert u-v\Vert ^2=2\Vert u\Vert ^2+2\Vert v\Vert ^2$ |
| Polarization ($\mathbb R$) | $\langle u,v\rangle=\frac14(\Vert u+v\Vert ^2-\Vert u-v\Vert ^2)$ |
| Polarization ($\mathbb C$) | $\langle u,v\rangle=\frac14\sum_{k=0}^3 i^k\Vert u+i^kv\Vert ^2$ |
| Bessel | orthonormal $\lbrace e_i\rbrace$: $\sum\lvert\langle x,e_i\rangle\rvert^2\le\Vert x\Vert ^2$ |
| Parseval | orthonormal **basis**: equality, and $x=\sum\langle x,e_i\rangle e_i$ |

- **Jordan–von Neumann:** a norm comes from an inner product $\iff$ it satisfies the parallelogram law. So $\Vert \cdot\Vert _1$ and $\Vert \cdot\Vert _\infty$ on $\mathbb R^n$ ($n\ge2$) are **not** inner-product norms.
- Angle: $\cos\theta=\dfrac{\langle u,v\rangle}{\Vert u\Vert \Vert v\Vert }$ (real case).

## 3. Orthogonality
- An orthogonal set of non-zero vectors is linearly independent.
- $W^\perp$ is always a subspace. In finite dimension: $V=W\oplus W^\perp$, $\dim W^\perp=n-\dim W$, and $(W^\perp)^\perp=W$.
- $(W_1+W_2)^\perp=W_1^\perp\cap W_2^\perp$.
- For a real matrix: $(\text{row space})^\perp=\text{null space}$ and $(\text{col space})^\perp=\ker A^T$.
- In $M_n(\mathbb R)$ with the trace inner product, $\text{Sym}^\perp=\text{Skew}$ and the complement of the scalar matrices is the trace-zero matrices.

## 4. Gram–Schmidt process
Given independent $v_1,\dots,v_k$:
$$w_1=v_1,\qquad w_j=v_j-\sum_{i\lt j}\frac{\langle v_j,w_i\rangle}{\Vert w_i\Vert ^2}w_i,\qquad e_j=\frac{w_j}{\Vert w_j\Vert }.$$
- $\operatorname{span}\lbrace e_1..e_j\rbrace =\operatorname{span}\lbrace v_1..v_j\rbrace$ for each $j$. If the $v$'s are dependent, some $w_j=0$.
- Matrix form: $A=QR$ with $Q$ having orthonormal columns and $R$ upper triangular with positive diagonal.
- Applied to $1,x,x^2,\dots$:
  - On $[-1,1]$ it gives the Legendre polynomials (up to scaling): $1,\ x,\ x^2-\tfrac13$.
  - On $[0,1]$ it gives $1,\ \sqrt3(2x-1),\ \sqrt5(6x^2-6x+1)$.

## 5. Orthogonal projection and best approximation
- With an orthonormal basis $\lbrace e_i\rbrace$ of $W$: $P_Wx=\sum\langle x,e_i\rangle e_i$, and in general $P_W=A(A^TA)^{-1}A^T$ (columns of $A$ a basis of $W$).
- Onto a line: $\operatorname{proj}_u x=\frac{\langle x,u\rangle}{\langle u,u\rangle}u$.
- **Best approximation:** $\Vert x-P_Wx\Vert \le\Vert x-w\Vert$ for all $w\in W$. The residual $x-P_Wx\in W^\perp$, which gives the normal equations.
- $P$ is an orthogonal projection $\iff P^2=P=P^\ast$. Its eigenvalues are 0 and 1, $\operatorname{tr}P=\operatorname{rank}P$, and $\Vert Px\Vert \le\Vert x\Vert$.
- Distance from $x$ to the hyperplane $a\cdot x=0$ is $|a\cdot x|/\Vert a\Vert$.
- $L^2[0,1]$ best linear approximation to $x^2$ is $x-\tfrac16$.

## 6. Orthonormal bases and matrices
- If $\lbrace e_i\rbrace$ is an orthonormal basis, then $[T]_{ij}=\langle Te_j,e_i\rangle$, and the matrix of $T^\ast$ is the conjugate transpose.
- The change of basis between two orthonormal bases is unitary (orthogonal).
- **Riesz representation** (finite dimension): every $f\in V^\ast$ is $f(x)=\langle x,y\rangle$ for a unique $y$.

## Exam traps
- Check positive definiteness, not just symmetry, when deciding whether a formula is an inner product: $x_1y_1-x_2y_2$ fails.
- Gram–Schmidt depends on the **order** of the vectors and on the inner product.
- $P^2=P$ alone is not an orthogonal projection.
- Pythagoras' converse fails over $\mathbb C$: $\Vert u+v\Vert ^2=\Vert u\Vert ^2+\Vert v\Vert ^2$ only gives $\operatorname{Re}\langle u,v\rangle=0$.
- The $\ell^1$ and $\ell^\infty$ norms are not inner-product norms.
