# Cheatsheet · Unit 3 · Topic 09 — Normed Linear Spaces, Banach Spaces, OMT, CGT, Hahn–Banach
> Questions: [../Questions/09-Normed-Banach-Spaces-OMT-CGT-Hahn-Banach.md](../Questions/09-Normed-Banach-Spaces-OMT-CGT-Hahn-Banach.md)

## 1. Norms
- **Norm axioms:**
  - $\Vert x\Vert \ge0$, with $\Vert x\Vert =0\iff x=0$
  - $\Vert \alpha x\Vert =|\alpha|\Vert x\Vert$
  - $\Vert x+y\Vert \le\Vert x\Vert +\Vert y\Vert$
- A **Banach space** is a complete normed space.
- **Equivalent norms:** $a\Vert x\Vert \le\Vert x\Vert '\le b\Vert x\Vert$. On a **finite-dimensional** space all norms are equivalent. Consequences:
  - every finite-dimensional normed space is complete
  - every finite-dimensional subspace is closed
  - every linear map from a finite-dimensional space is continuous
  - closed and bounded sets are compact
- **In $\mathbb R^n$:** $\Vert x\Vert _\infty\le\Vert x\Vert _2\le\Vert x\Vert _1\le\sqrt n\Vert x\Vert _2\le n\Vert x\Vert _\infty$. Also $\Vert x\Vert _2\le\sqrt n\Vert x\Vert _\infty$.
- **Riesz lemma:** if $M$ is a proper closed subspace, then for every $\theta\lt 1$ there is $\Vert x\Vert =1$ with $d(x,M)\ge\theta$. So the closed unit ball is compact $\iff\dim X\lt \infty$.
- **Quotient:** $X/M$ with $M$ closed is normed. If $X$ is Banach, so is $X/M$.
- **Series test:** $X$ is Banach $\iff$ every absolutely convergent series converges.

## 2. Standard spaces
| Space | Norm | Banach? | Separable? | Dual | Reflexive? |
|---|---|---|---|---|---|
| $\mathbb R^n,\mathbb C^n$ | any | ✔ | ✔ | itself | ✔ |
| $c_{00}$ | $\sup$ | ✘ | ✔ | $\ell^1$ | ✘ |
| $c_0$ | $\sup$ | ✔ | ✔ | $\ell^1$ | ✘ |
| $\ell^1$ | $\sum\lvert x_n\rvert$ | ✔ | ✔ | $\ell^\infty$ | ✘ |
| $\ell^p$, $1\lt p\lt \infty$ | $(\sum\lvert x_n\rvert^p)^{1/p}$ | ✔ | ✔ | $\ell^q$ | ✔ |
| $\ell^\infty$, $L^\infty$ | $\sup$ | ✔ | ✘ | $ba$ (strictly bigger than $\ell^1$) | ✘ |
| $C[a,b]$ | $\sup$ | ✔ | ✔ (Weierstrass) | $NBV[a,b]$ / regular Borel measures | ✘ |
| $C[a,b]$ | $\int\lvert f\rvert$ | ✘ | ✔ | | |
| polynomials $\mathcal P[a,b]$ | $\sup$ | ✘ | ✔ | | |
| $L^p$, $1\le p\lt \infty$ | $\Vert \cdot\Vert _p$ | ✔ | ✔ | $L^q$ | ✔ iff $1\lt p\lt \infty$ |

Here $\frac1p+\frac1q=1$.

- **Inclusions:** $\ell^1\subset\ell^p\subset\ell^q\subset c_0\subset\ell^\infty$ for $1\lt p\lt q$.
- An infinite-dimensional Banach space has Hamel dimension $\ge\mathfrak c$, and **never a countable Hamel basis** (by Baire). So $\mathbb R[x]$ and $c_{00}$ admit no complete norm.

## 3. Bounded linear operators
- **Equivalent for linear $T$:** continuous $\iff$ continuous at $0$ $\iff$ bounded ($\Vert Tx\Vert \le M\Vert x\Vert$) $\iff$ uniformly continuous.
- **Operator norm:**
  $$\Vert T\Vert =\sup_{\Vert x\Vert \le1}\Vert Tx\Vert =\sup_{x\ne0}\frac{\Vert Tx\Vert }{\Vert x\Vert }.$$
  $B(X,Y)$ is Banach **if $Y$ is Banach**, so $X^\ast$ is **always** Banach. Also $\Vert ST\Vert \le\Vert S\Vert \Vert T\Vert$.
- **Matrix norms:**
  - $\Vert A\Vert _{1\to1}$ is the max **column** sum.
  - $\Vert A\Vert _{\infty\to\infty}$ is the max **row** sum.
  - $`\Vert A\Vert _{2\to2}`$ is the largest singular value $`=\sqrt{\lambda_{\max}(A^TA)}`$.
- **Functionals on $C[0,1]$ (sup norm):**
  - $\varphi(x)=\int_0^1x(t)g(t)\thinspace dt$ has $\Vert \varphi\Vert =\int_0^1|g|$.
  - $\varphi(x)=\sum c_ix(t_i)$ (distinct $t_i$) has $\Vert \varphi\Vert =\sum|c_i|$.
  - Combinations simply add: $\Vert \int x-x(\tfrac12)\Vert =2$.
- **Functionals on $\ell^p$:** $\varphi(x)=\sum a_nx_n$ has $\Vert \varphi\Vert =\Vert a\Vert _q$.
- **Unbounded operators:** differentiation on $(C^1,\Vert \cdot\Vert _\infty)$ or on polynomials ($\Vert D t^n\Vert =n$). Every infinite-dimensional normed space carries unbounded linear functionals (built from a Hamel basis).

## 4. The four big theorems
| Theorem | Hypotheses | Conclusion |
|---|---|---|
| **Hahn–Banach** (normed form) | $X$ normed (no completeness), $M$ subspace, $f\in M^\ast$ | there is $F\in X^\ast$ with $F\vert _M=f$ and $\Vert F\Vert =\Vert f\Vert$ |
| **Uniform Boundedness** (Banach–Steinhaus) | $X$ **Banach**, $Y$ normed, $\sup_\alpha\Vert T_\alpha x\Vert \lt \infty$ for each $x$ | $\sup_\alpha\Vert T_\alpha\Vert \lt \infty$ |
| **Open Mapping** | $X,Y$ **Banach**, $T\in B(X,Y)$ **onto** | $T$ is open |
| **Bounded Inverse** | $X,Y$ Banach, $T\in B(X,Y)$ bijective | $T^{-1}$ is bounded |
| **Closed Graph** | $X,Y$ **Banach**, $T$ linear, graph closed | $T$ is bounded |

- **Hahn–Banach, real/sublinear form:** if $f\le p$ on $M$ with $p$ sublinear, then $f$ extends to $F$ with $F\le p$ on $X$.
- **Corollaries of Hahn–Banach:**
  - For $x_0\ne0$ there is $f$ with $\Vert f\Vert =1$ and $f(x_0)=\Vert x_0\Vert$.
  - $X^\ast$ separates points.
  - $\Vert x\Vert =\max_{\Vert f\Vert \le1}|f(x)|$.
  - The canonical map $J:X\to X^{\ast \ast }$ is an isometry.
  - If $M$ is closed and $x_0\notin M$, there is $f$ with $f|_M=0$ and $f(x_0)=d(x_0,M)$ (with $\Vert f\Vert =1$).
  - If $X^\ast$ is separable, then $X$ is separable.
  - Geometric form: separating hyperplanes for convex sets.
- **Uniqueness of the extension** is not guaranteed. It holds when $X^\ast$ is strictly convex, e.g. in Hilbert spaces.
- **Consequences of the uniform boundedness principle:**
  - weakly convergent sequences are bounded
  - a pointwise limit of bounded operators on a Banach space is bounded
  - there is a continuous function whose Fourier series diverges at a point
- **Consequences of the open mapping theorem / bounded inverse theorem:** if $\Vert \cdot\Vert _1\le c\Vert \cdot\Vert _2$ and both norms are complete, then they are equivalent. So $\Vert \cdot\Vert _1$ on $C[0,1]$ cannot be complete.
- **Closed graph, sequential form:** $x_n\to x$ and $Tx_n\to y$ imply $y=Tx$.

## 5. Dual, bidual, reflexivity
- $X$ is **reflexive** if $J(X)=X^{\ast \ast }$.
  - Reflexive $\Rightarrow$ Banach.
  - Closed subspaces of reflexive spaces are reflexive.
  - $X$ is reflexive $\iff$ $X^\ast$ is reflexive (for Banach $X$).
- **Reflexive:** finite-dimensional spaces, Hilbert spaces, $\ell^p$ and $L^p$ for $1\lt p\lt \infty$.
- **Not reflexive:** $c_0,\ell^1,\ell^\infty,L^1,L^\infty,C[a,b]$.
- If $X$ is separable and $X^\ast$ is not, then $X$ is not reflexive. Example: $\ell^1$.
- **Weak convergence:** $x_n\rightharpoonup x$ means $f(x_n)\to f(x)$ for all $f\in X^\ast$. Norm convergence implies weak convergence. In $\ell^p$ ($1\lt p\lt \infty$), $e_n\rightharpoonup0$ but $\Vert e_n\Vert =1$. In finite dimensions, weak and norm convergence coincide.

## Exam traps
- The closed graph theorem, open mapping theorem and uniform boundedness principle need **completeness**. Hahn–Banach does **not**.
- An operator norm on $\ell^1$ is a column sum, not a row sum.
- $(\ell^\infty)^\ast \ne\ell^1$. $\ell^1$ is the dual of $c_0$.
- $X^\ast$ is Banach even when $X$ is not.
- A Hahn–Banach extension exists but need not be unique.
- "Closed graph" is not the same as "closed map".
- An open linear map must be onto.
- Every Banach space is a normed space, but a normed space need not be Banach. Examples of incomplete normed spaces: $c_{00}$ and polynomials.
