# Cheatsheet · Unit 3 · Topic 10 — Hilbert Spaces and Orthogonal Complement
> Questions: [../Questions/10-Hilbert-Spaces-Orthogonal-Complement.md](../Questions/10-Hilbert-Spaces-Orthogonal-Complement.md)

## 1. Inner product spaces
- **Axioms:** $\langle x,x\rangle\ge0$ with $=0\iff x=0$; $\langle x,y\rangle=\overline{\langle y,x\rangle}$; linear in the first slot. Then $\Vert x\Vert =\sqrt{\langle x,x\rangle}$.
- A **Hilbert space** is a complete inner product space.
- **Cauchy–Schwarz:** $|\langle x,y\rangle|\le\Vert x\Vert \Vert y\Vert$, with equality $\iff$ $x,y$ are linearly dependent.
- **Parallelogram law:** $\Vert x+y\Vert ^2+\Vert x-y\Vert ^2=2\Vert x\Vert ^2+2\Vert y\Vert ^2$.
  - **Jordan–von Neumann:** a norm comes from an inner product $\iff$ the parallelogram law holds.
  - Hence $\ell^p$, $L^p$ ($p\ne2$), $C[a,b]$ with sup norm, $\Vert \cdot\Vert _1$ and $\Vert \cdot\Vert _\infty$ on $\mathbb R^n$ are **not** inner product spaces.
- **Polarization:**
  - real: $\langle x,y\rangle=\frac14(\Vert x+y\Vert ^2-\Vert x-y\Vert ^2)$
  - complex: $\langle x,y\rangle=\frac14\sum_{k=0}^3 i^k\Vert x+i^ky\Vert ^2$
- **Pythagoras:** $x\perp y\Rightarrow\Vert x+y\Vert ^2=\Vert x\Vert ^2+\Vert y\Vert ^2$. Over $\mathbb R$ the converse also holds.
- **Continuity:** the inner product is jointly continuous, and $x_n\to x$, $y_n\to y$ imply $\langle x_n,y_n\rangle\to\langle x,y\rangle$.
- **Examples:**
  - Hilbert: $\mathbb C^n$, $\ell^2$, $L^2[a,b]$, Sobolev $H^1$.
  - Incomplete inner product spaces: $c_{00}$ with the $\ell^2$ inner product; $C[a,b]$ with $\int f\bar g$.

## 2. Orthogonal complement and projection
- $M^\perp=\lbrace x:\langle x,m\rangle=0\ \forall m\in M\rbrace$ is a **closed subspace for every subset $M$**.
- **Basic properties:**
  - $M\subseteq N\Rightarrow N^\perp\subseteq M^\perp$
  - $M^\perp=\overline M^\perp=(\mathop{\mathrm{span}}\nolimits M)^\perp$
  - $M\cap M^\perp\subseteq\lbrace 0\rbrace$
- **Double complement:** $M^{\perp\perp}=\overline{\mathop{\mathrm{span}}\nolimits M}$, which equals $M$ iff $M$ is a closed subspace.
- **Density test:** $M$ is dense $\iff$ $M^\perp=\lbrace 0\rbrace$ (for a subspace $M$).
- **Closest point theorem:** in a Hilbert space, every non-empty **closed convex** set $K$ has a **unique** point nearest to any $x$. This fails in general Banach spaces: in $(\mathbb R^2,\Vert \cdot\Vert _\infty)$ there are infinitely many nearest points.
- **Projection theorem:** if $M$ is a closed subspace, then $H=M\oplus M^\perp$ and $x=Px+(x-Px)$, where $Px$ is the best approximation and is characterised by $x-Px\perp M$.
- **Distance formulas:**
  - $d(x,M)^2=\Vert x\Vert ^2-\Vert Px\Vert ^2$.
  - For $M=\lbrace u\rbrace ^\perp$: $d(x,M)=\frac{|\langle x,u\rangle|}{\Vert u\Vert }$.
  - For a finite-dimensional $M$: solve the normal equations with the Gram matrix.
  - $d(t^2,\mathop{\mathrm{span}}\nolimits\lbrace 1,t\rbrace )$ in $L^2[0,1]$ is $\frac{1}{6\sqrt5}$, with projection $t-\frac16$.
- **Orthogonal projection $P$:** the following are equivalent for an idempotent $P$ ($P^2=P$):
  - $P$ is orthogonal ($\mathop{\mathrm{ran}}\nolimits P\perp\ker P$)
  - $P=P^\ast$
  - $\Vert P\Vert \le1$

  Also $\Vert P\Vert =1$ if $P\ne0$, $\langle Px,x\rangle=\Vert Px\Vert ^2$, and $\sigma(P)\subseteq\lbrace 0,1\rbrace$.
  - An oblique idempotent can have norm $\gt 1$: $(x,y)\mapsto(x+y,0)$ has norm $\sqrt2$.
- **Projection formula:** for an orthonormal basis $\lbrace u_1,\dots,u_k\rbrace$ of $M$, $Px=\sum\langle x,u_i\rangle u_i$.

## 3. Orthonormal sets and bases
- **Bessel's inequality:** $\sum|\langle x,e_\alpha\rangle|^2\le\Vert x\Vert ^2$ for every orthonormal set. Only countably many coefficients are non-zero, and $\langle x,e_n\rangle\to0$.
- **Equivalent conditions for a maximal (complete) orthonormal set $\lbrace e_\alpha\rbrace$:**
  - $\lbrace e_\alpha\rbrace$ is maximal (complete)
  - $\lbrace e_\alpha\rbrace ^\perp=\lbrace 0\rbrace$
  - $\overline{\mathop{\mathrm{span}}\nolimits}=H$
  - $x=\sum\langle x,e_\alpha\rangle e_\alpha$ for every $x$
  - **Parseval:** $\Vert x\Vert ^2=\sum|\langle x,e_\alpha\rangle|^2$ for every $x$
  - $\langle x,y\rangle=\sum\langle x,e_\alpha\rangle\overline{\langle y,e_\alpha\rangle}$
- **Riesz–Fischer:** if $\sum|c_n|^2\lt \infty$, then $\sum c_ne_n$ converges in $H$.
- Every Hilbert space has an orthonormal basis (Zorn), and all orthonormal bases have the same cardinality (the Hilbert dimension).
- $H$ is **separable** $\iff$ it has a **countable** orthonormal basis.
- Every infinite-dimensional separable Hilbert space is isometrically isomorphic to $\ell^2$.
- An orthonormal basis is **not** a Hamel basis in infinite dimensions.
- **Gram–Schmidt** turns an independent sequence into an orthonormal one. Applied to $1,x,x^2,\dots$ in $L^2[-1,1]$ it gives the normalised **Legendre** polynomials; the first two are $\frac1{\sqrt2}$ and $\sqrt{\frac32}\thinspace x$.
- **Standard orthonormal bases:**
  - $\lbrace e_n\rbrace$ in $\ell^2$
  - $`\left\lbrace \frac{1}{\sqrt{2\pi}}e^{inx}\right\rbrace _{n\in\mathbb Z}`$ in $`L^2[-\pi,\pi]`$, which gives Parseval for Fourier series: $`\frac1\pi\int_{-\pi}^{\pi}f^2=\frac{a_0^2}2+\sum(a_n^2+b_n^2)`$
- A weakly convergent orthonormal sequence: $e_n\rightharpoonup0$, but $\Vert e_n-e_m\Vert =\sqrt2$ for $n\neq m$, so the unit ball is not compact.

## 4. Riesz representation and adjoints
- **Riesz:** each $f\in H^\ast$ is $f(x)=\langle x,y_f\rangle$ for a unique $y_f$, and $\Vert f\Vert =\Vert y_f\Vert$. So $H^\ast \cong H$ (conjugate-linearly), and every Hilbert space is **reflexive**.
- **Norms via Riesz:**
  - On $\ell^2$, $f(x)=\sum a_nx_n$ has $\Vert f\Vert =\Vert a\Vert _2$.
  - On $L^2$, $f(x)=\int xg$ has $\Vert f\Vert =\Vert g\Vert _2$.
- **Adjoint** $T^\ast$: $\langle Tx,y\rangle=\langle x,T^\ast y\rangle$. Properties:
  - $\Vert T^\ast \Vert =\Vert T\Vert$ and $T^{\ast \ast }=T$
  - $(ST)^\ast =T^\ast S^\ast$ and $(\alpha T)^\ast =\bar\alpha T^\ast$
  - **C\*-identity:** $\Vert T^\ast T\Vert =\Vert T\Vert ^2$
  - $\ker T^\ast =(\mathop{\mathrm{ran}}\nolimits T)^\perp$ and $\overline{\mathop{\mathrm{ran}}\nolimits T}=(\ker T^\ast )^\perp$
- **Classes of operators:**

| Class | Definition | Spectrum / remarks |
|---|---|---|
| self-adjoint | $T=T^\ast$ | real spectrum; $\langle Tx,x\rangle\in\mathbb R$; $\Vert T\Vert =\sup_{\Vert x\Vert =1}\lvert\langle Tx,x\rangle\rvert$ |
| normal | $TT^\ast =T^\ast T$ | $\Vert Tx\Vert =\Vert T^\ast x\Vert$ |
| unitary | $T^\ast T=TT^\ast =I$ | onto isometry; spectrum $\subseteq$ unit circle |
| isometry | $T^\ast T=I$ | right shift $S$: $S^\ast S=I$, $SS^\ast \ne I$ |
| positive | $\langle Tx,x\rangle\ge0$ | self-adjoint (complex $H$) |

- **Shifts:** the adjoint of the right shift is the left shift. The right shift has no eigenvalues. Every $\lambda$ with $|\lambda|\lt 1$ is an eigenvalue of the left shift.
- **Matrix case:** the adjoint is the conjugate transpose. Hermitian $\leftrightarrow$ self-adjoint, unitary $\leftrightarrow$ unitary.

## Exam traps
- $M^\perp$ is closed even when $M$ is not, and $M^{\perp\perp}=\overline M$, not $M$.
- $H=M\oplus M^\perp$ requires $M$ **closed**: $c_{00}\oplus c_{00}^\perp=c_{00}\ne\ell^2$.
- Unique nearest points require a Hilbert-space norm (or uniform convexity) **and** a closed convex set.
- An orthonormal basis is not a Hamel basis, and a countable orthonormal basis exists only in **separable** $H$.
- Idempotent does not mean orthogonal projection: $\Vert P\Vert =1$ only for $P=P^\ast \ne0$.
- An isometry need not be unitary (the right shift).
- Bessel holds for any orthonormal set. Parseval only for a complete one.
- In the distance formula, take the **square root** of $\Vert x\Vert ^2-\Vert Px\Vert ^2$.
