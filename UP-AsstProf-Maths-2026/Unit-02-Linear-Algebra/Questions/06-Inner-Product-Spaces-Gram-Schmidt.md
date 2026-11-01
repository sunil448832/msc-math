# Unit 2 · Topic 06 — Inner Product Spaces, Orthonormal Basis, Gram–Schmidt
> Syllabus coverage: Finite dimensional inner product spaces, Orthonormal basis, Gram-Schmidt orthogonalization process (also Cauchy–Schwarz, orthogonal projection)
> Cheatsheet: [../Cheatsheets/06-Inner-Product-Spaces-Gram-Schmidt.md](../Cheatsheets/06-Inner-Product-Spaces-Gram-Schmidt.md)

**Q1.** `[Concept]` ★ In an inner product space, equality $|\langle u,v\rangle|=\Vert u\Vert \thinspace \Vert v\Vert$ holds if and only if

(A) $u\perp v$

(B) $\Vert u\Vert =\Vert v\Vert$

(C) $u$ and $v$ are linearly dependent

(D) $u=v$

**Q2.** `[Numerical]` ★★ Applying Gram–Schmidt (standard inner product) to $v_1=(1,1,0)$, $v_2=(1,0,1)$ in that order, the second orthonormal vector is

(A) $\tfrac1{\sqrt2}(1,-1,0)$

(B) $\tfrac1{\sqrt6}(-1,1,2)$

(C) $\tfrac1{\sqrt3}(1,-1,1)$

(D) $\tfrac1{\sqrt6}(1,-1,2)$

**Q3.** `[Numerical]` ★★ The distance from the point $(1,2,3)$ to the line $\mathop{\mathrm{span}}\nolimits\lbrace (1,1,1)\rbrace$ in $\mathbb R^3$ (standard inner product) is

(A) $1$

(B) $\sqrt2$

(C) $\sqrt3$

(D) $2\sqrt3$

**Q4.** `[Numerical]` ★★★ In $C[0,1]$ with $\langle f,g\rangle=\int_0^1 f(x)g(x)\thinspace dx$, the polynomial $p(x)=a+bx$ closest to $x^2$ is

(A) $\tfrac12x+\tfrac1{12}$

(B) $x$

(C) $x-\tfrac13$

(D) $x-\tfrac16$

**Q5.** `[Multi-Statement]` ★★ Consider:

I. If $\langle u,v\rangle=0$, then $\Vert u+v\Vert ^2=\Vert u\Vert ^2+\Vert v\Vert ^2$.

II. The parallelogram law $\Vert u+v\Vert ^2+\Vert u-v\Vert ^2=2\Vert u\Vert ^2+2\Vert v\Vert ^2$ holds in every inner product space.

III. The norm $\Vert (x,y)\Vert _1=|x|+|y|$ on $\mathbb R^2$ is induced by some inner product.

Which is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★
**Assertion (A):** Every non-zero finite-dimensional inner product space has an orthonormal basis.
**Reason (R):** The Gram–Schmidt process converts any basis into an orthonormal basis.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Let $\lbrace e_1,\dots,e_k\rbrace$ be an orthonormal set in a real inner product space. Match the result with its statement.

| List-I | List-II |
|---|---|
| (a) Bessel's inequality | 1. $\langle x,y\rangle=\tfrac14\left(\Vert x+y\Vert ^2-\Vert x-y\Vert ^2\right)$ |
| (b) Parseval's identity ($\lbrace e_i\rbrace$ an orthonormal basis) | 2. $\sum_i\langle x,e_i\rangle^2\le\Vert x\Vert ^2$ |
| (c) Polarization identity | 3. $\Vert x+y\Vert \le\Vert x\Vert +\Vert y\Vert$ |
| (d) Triangle inequality | 4. $\sum_i\langle x,e_i\rangle^2=\Vert x\Vert ^2$ |

(A) a-2, b-4, c-1, d-3

(B) a-4, b-2, c-1, d-3

(C) a-2, b-4, c-3, d-1

(D) a-1, b-4, c-2, d-3

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** an inner product on $\mathbb R^2$ (for $x=(x_1,x_2)$, $`y=(y_1,y_2)`$)?

(A) $x_1y_1+2x_2y_2$

(B) $x_1y_1-x_2y_2$

(C) $2x_1y_1+x_1y_2+x_2y_1+x_2y_2$

(D) $3x_1y_1+5x_2y_2$

**Q9.** `[Application]` ★★ On $M_n(\mathbb{R})$ with $\langle A,B\rangle=\mathop{\mathrm{tr}}\nolimits(A^TB)$, the orthogonal complement of the subspace of symmetric matrices is

(A) $\lbrace 0\rbrace$

(B) the diagonal matrices

(C) the skew-symmetric matrices

(D) the trace-zero matrices

**Q10.** `[Numerical]` ★ If $x\perp y$ in a real inner product space with $\Vert x\Vert =3$ and $\Vert y\Vert =4$, then $\Vert x-y\Vert$ is

(A) 1

(B) 25

(C) 7

(D) 5

**Q11.** `[Application]` ★★ In $C[0,1]$ with $\langle f,g\rangle=\int_0^1fg\thinspace dx$, the angle between $f(x)=1$ and $g(x)=x$ is

(A) $\pi/6$

(B) $\pi/4$

(C) $\pi/3$

(D) $\pi/2$

**Q12.** `[Concept]` ★ A linear operator $P$ on a finite-dimensional inner product space is an orthogonal projection (onto its range) if and only if

(A) $P^2=P$

(B) $P^\ast =P$

(C) $P^2=P$ and $P^\ast =P$

(D) $P^\ast P=I$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | D | Numerical |
| 3 | B | Numerical |
| 4 | D | Numerical |
| 5 | B | Multi-Statement |
| 6 | A | Assertion-Reason |
| 7 | A | Match |
| 8 | B | NOT-true |
| 9 | C | Application |
| 10 | D | Numerical |
| 11 | A | Application |
| 12 | C | Concept |

## Solutions
**Q1 — (C).** This is the equality case of Cauchy–Schwarz. (A) gives $\langle u,v\rangle=0$, which is the opposite extreme.

**Q2 — (D).** $w_2=v_2-\frac{\langle v_2,v_1\rangle}{\Vert v_1\Vert ^2}v_1=(1,0,1)-\tfrac12(1,1,0)=(\tfrac12,-\tfrac12,1)\parallel(1,-1,2)$, with norm $\sqrt6$. (B) is a trap: it is a unit vector orthogonal to $v_1$, but it does **not** lie in $\mathop{\mathrm{span}}\nolimits\lbrace v_1,v_2\rbrace$, whose normal is $v_1\times v_2=(1,-1,-1)$ and $\langle(-1,1,2),(1,-1,-1)\rangle=-4\neq0$. (C) fails the same way, since $\langle(1,-1,1),(1,-1,-1)\rangle=1\ne0$. (A) is orthogonal to $v_1$, but $(1,-1,0)\notin\mathop{\mathrm{span}}\nolimits\lbrace v_1,v_2\rbrace$ either.

**Q3 — (B).** The projection is $\frac{6}{3}(1,1,1)=(2,2,2)$, and the residual $(-1,0,1)$ has norm $\sqrt2$.

**Q4 — (D).** Solve the normal equations $\langle x^2-a-bx,1\rangle=0$ and $\langle x^2-a-bx,x\rangle=0$, that is, $\tfrac13=a+\tfrac b2$ and $\tfrac14=\tfrac a2+\tfrac b3$. This gives $b=1$ and $a=-\tfrac16$.

**Q5 — (B).** I is Pythagoras. II follows by expanding. III is false: with $u=(1,0)$, $v=(0,1)$ we get $4+4\ne2+2$, so the parallelogram law fails, and a norm comes from an inner product iff the parallelogram law holds.

**Q6 — (A).** Gram–Schmidt applied to any basis, which exists in finite dimension, produces an orthonormal basis.

**Q7 — (A).** These are the standard statements.

**Q8 — (B).** $\langle(0,1),(0,1)\rangle=-1\lt 0$, so it is not positive definite. (C) has matrix $`\begin{pmatrix}2&1\cr 1&1\end{pmatrix}`$ with leading minors $2,1\gt 0$, so it is positive definite.

**Q9 — (C).** $M_n=\text{Sym}\oplus\text{Skew}$, and $\mathop{\mathrm{tr}}\nolimits(S^TK)=\mathop{\mathrm{tr}}\nolimits(SK)=0$ for $S$ symmetric and $K$ skew. The dimensions $n(n+1)/2+n(n-1)/2=n^2$ match.

**Q10 — (D).** By Pythagoras $\Vert x-y\Vert ^2=9+16=25$. (C) assumes the vectors are parallel.

**Q11 — (A).** $\langle1,x\rangle=\tfrac12$, $\Vert 1\Vert =1$, $\Vert x\Vert =1/\sqrt3$, so $\cos\theta=\frac{\sqrt3}2$ and $\theta=\pi/6$.

**Q12 — (C).** $P^2=P$ alone gives an *oblique* projection, for example $`\begin{pmatrix}1&1\cr 0&0\end{pmatrix}`$. Self-adjointness makes the kernel orthogonal to the range. (D) describes unitary operators.
