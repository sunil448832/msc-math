# Cheatsheet · Unit 7 · Topic 03 — Fredholm Equations, Separable Kernels, Eigenvalues
> Questions: [../Questions/03-Fredholm-Separable-Kernels-Eigenvalues.md](../Questions/03-Fredholm-Separable-Kernels-Eigenvalues.md)

## 1. Setting
$$y(x)=f(x)+\lambda\int_a^b K(x,t)\thinspace y(t)\thinspace dt\qquad(\ast)$$
- **Characteristic value** (eigenvalue in many Indian texts): $\lambda$ for which the homogeneous equation $y=\lambda\int Ky$ has a nonzero solution (an **eigenfunction**). Operator eigenvalue $\mu=1/\lambda$.
- $\lambda=0$ is never a characteristic value.
- **Transposed (adjoint) kernel:** $K^T(x,t)=K(t,x)$; $K$ and $K^T$ have the same characteristic values (with same multiplicities).

## 2. Degenerate (separable) kernels — method
$K(x,t)=\sum_{i=1}^n a_i(x)b_i(t)$, $\lbrace a_i\rbrace ,\lbrace b_i\rbrace$ linearly independent.
1. Put $c_i=\int_a^b b_i(t)y(t)dt$ ⇒ $y=f+\lambda\sum c_ia_i(x)$.
2. Multiply by $b_j$ and integrate: $c_j=f_j+\lambda\sum_i\alpha_{ji}c_i$, where
$$\alpha_{ji}=\int_a^b b_j(t)a_i(t)dt,\qquad f_j=\int_a^b b_j(t)f(t)dt.$$
3. Linear system $(I-\lambda A)c=F$.
- **Characteristic values:** roots of $D(\lambda)=\det(I-\lambda A)=0$ — a polynomial of degree $\le n$ ⇒ **at most $n$** characteristic values (possibly none).
- Eigenfunctions: $y=\sum c_ia_i(x)$ with $c$ in the null space of $I-\lambda A$.
- **Rank-one kernel** $a(x)b(t)$: $\lambda=1/\int_a^b a\thinspace b\thinspace dt$ (none if $\int ab=0$); solution of $(\ast)$:
$$y=f+\frac{\lambda\thinspace a(x)\int_a^b b f\thinspace dt}{1-\lambda\int_a^b ab\thinspace dt}.$$

### Standard results
| Kernel (interval) | Characteristic value(s) | Eigenfunction(s) |
|---|---|---|
| $1$ on $[0,1]$ | $1$ | $1$ |
| $x$ on $[0,1]$ | $2$ | $x$ |
| $xt$ on $[0,1]$ | $3$ | $x$ |
| $x^2t^2$ on $[0,1]$ | $5$ | $x^2$ |
| $e^{x+t}$ on $[0,1]$ | $\frac{2}{e^2-1}$ | $e^x$ |
| $e^xe^{-t}$ on $[0,1]$ | $1$ | $e^x$ |
| $x+t$ on $[0,1]$ | $-6\pm4\sqrt3$ | $\lambda(c_1x+c_2)$ |
| $\cos(x+t)$ on $[0,2\pi]$ | $\pm1/\pi$ | $\cos x$, $\sin x$ |
| $\cos(x-t)$ on $[0,2\pi]$ | $1/\pi$ (double) | $\cos x,\sin x$ |
| $\sin x\sin t$ on $[0,\pi]$ | $2/\pi$ | $\sin x$ |
| $\sin x\cos t$ on $[0,\pi]$ | none | — |
| $\sin(x+t)$ on $[0,\pi]$ | $\pm 2/\pi$ | $\sin x\pm\cos x$ |

## 3. Fredholm alternative (continuous / $L^2$ kernel)
1. If $\lambda$ is **not** a characteristic value: $(\ast)$ has a **unique** solution for every $f$; the homogeneous equation has only $y\equiv0$.
2. If $\lambda$ **is** a characteristic value: homogeneous equations for $K$ and $K^T$ have the same finite number $r$ of independent solutions; $(\ast)$ is solvable **iff** $\int_a^b f(x)\thinspace z(x)dx=0$ for every solution $z$ of $z=\lambda\int K(t,x)z(t)dt$; then the solution is $y_p+\sum c_k\phi_k$ (infinitely many).
- Characteristic values have no finite accumulation point; each has finite multiplicity.

## 4. Neumann series & resolvent (Fredholm)
$K_1=K$, $K_n(x,t)=\int_a^bK(x,s)K_{n-1}(s,t)ds$, $R=\sum_{n\ge1}\lambda^{n-1}K_n$, $y=f+\lambda\int Rf$.
- Converges for $|\lambda|\lt \dfrac{1}{M(b-a)}$, $M=\max|K|$; better $|\lambda|\lt 1/\Vert K\Vert _{L^2}$; exactly up to the smallest $|\lambda_1|$.
- $xt$ on $[0,1]$: $K_n=xt/3^{n-1}$, $R=\dfrac{3xt}{3-\lambda}$, radius $3$.
- Fredholm's theory: $R=D(x,t;\lambda)/D(\lambda)$, ratio of two entire functions; zeros of $D(\lambda)$ = characteristic values.

## 5. Symmetric kernels (Hilbert–Schmidt)
For real continuous $K(x,t)=K(t,x)\not\equiv0$:
- characteristic values are **real**; eigenfunctions for distinct ones are **orthogonal**;
- at least **one** characteristic value exists (non-symmetric kernels may have none);
- if non-degenerate, infinitely many, $|\lambda_n|\to\infty$; degenerate ⇒ finitely many;
- **bilinear formula** $K(x,t)\sim\sum\frac{\phi_n(x)\phi_n(t)}{\lambda_n}$ (orthonormal $\phi_n$); $\sum\frac{1}{\lambda_n^2}=\iint K^2$; trace $\sum\frac1{\lambda_n}=\int K(x,x)dx$ (for continuous positive-definite, Mercer);
- **Hilbert–Schmidt:** every $g=\int K h$ has a convergent eigenfunction expansion; solution of $(\ast)$:
$$y=f+\lambda\sum_n\frac{f_n}{\lambda_n-\lambda}\phi_n(x),\quad f_n=\int f\phi_n.$$
- Green's function $t(1-x)/x(1-t)$ on $[0,1]$: $\lambda_n=n^2\pi^2$, $\phi_n=\sin n\pi x$.

## 6. Exam traps
- Characteristic value $\lambda$ vs operator eigenvalue $1/\lambda$ — check which the options mean.
- Degenerate kernel ⇒ **at most** $n$ characteristic values, possibly zero.
- Real symmetric nonzero kernel always has one; non-symmetric need not ($\sin x\cos t$ on $[0,\pi]$).
- At a characteristic value the equation is not "never solvable": check orthogonality of $f$ to the **transposed** eigenfunctions.
- Fredholm Neumann series converges only for small $|\lambda|$; Volterra for all.
- Don't drop the $\lambda c\int ab$ feedback term when solving separable equations.
- For $\cos(x+t)$ on a full period the values are $\pm1/\pi$; for $\cos(x-t)$ it's a double $1/\pi$.
