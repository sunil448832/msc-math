# Cheatsheet · Unit 4 · Topic 03 — Zeros, Taylor and Laurent Series, Singularities

## 1. Power series and radius of convergence
For $\sum a_n(z-a)^n$:
- **Cauchy–Hadamard:** $\dfrac1R = \limsup |a_n|^{1/n}$.
- **Ratio form:** $R = \lim\left|\dfrac{a_n}{a_{n+1}}\right|$, when this limit exists.
- The series converges absolutely for $|z - a| \lt  R$ and uniformly on compact subsets, and it diverges for $|z - a| \gt  R$.
- On $|z - a| = R$ anything can happen:

| Series | $R$ | Behaviour on $\lvert z\rvert = 1$ |
|---|---|---|
| $\sum z^n$ | 1 | diverges everywhere |
| $\sum z^n/n$ | 1 | diverges only at $z = 1$ |
| $\sum z^n/n^2$ | 1 | converges everywhere |

- Term-by-term differentiation and integration do not change $R$.
- Standard values:

| Series | $R$ |
|---|---|
| $\sum \frac{n!}{n^n}z^n$ | $e$ |
| $\sum n^n z^n$ | $0$ |
| $\sum \frac{z^n}{n!}$ | $\infty$ |
| $\sum z^{n!}$, $\sum z^{2^n}$ | $1$ (lacunary; the unit circle is a natural boundary) |
| $\sum \frac{(n!)^2}{(2n)!}z^n$ | $4$ |

## 2. Taylor's theorem
If $f$ is analytic on $|z - a| \lt  \rho$, then $f(z) = \sum \frac{f^{(n)}(a)}{n!}(z - a)^n$ there. **The radius of the Taylor series equals the distance from $a$ to the nearest singularity**, which may be non-real. For example, $\frac{1}{1+x^2}$ about $0$ has $R = 1$ because of $\pm i$.

Standard expansions:
| Function | Expansion |
|---|---|
| $e^z$ | $\sum \frac{z^n}{n!}$ |
| $\sin z$ | $z - \frac{z^3}{3!} + \frac{z^5}{5!} - \cdots$ |
| $\cos z$ | $1 - \frac{z^2}{2!} + \frac{z^4}{4!} - \cdots$ |
| $\frac{1}{1-z}$ ($\lvert z\rvert\lt 1$) | $\sum z^n$ |
| $\operatorname{Log}(1+z)$ ($\lvert z\rvert\lt 1$) | $z - \frac{z^2}{2} + \frac{z^3}{3} - \cdots$ |
| $\tan z$ ($R = \pi/2$) | $z + \frac{z^3}{3} + \frac{2z^5}{15} + \cdots$ |
| $\frac{z}{e^z-1}$ ($R = 2\pi$) | $1 - \frac z2 + \frac{z^2}{12} - \cdots$ |

Multiplying by $\frac{1}{1-z}$ produces partial sums of coefficients: $\frac{e^z}{1-z} = \sum\left(\sum_{k\le n}\frac1{k!}\right)z^n$.

## 3. Zeros
- $a$ is a **zero of order $m$** if $f(a) = \cdots = f^{(m-1)}(a) = 0 \ne f^{(m)}(a)$. Equivalently $f = (z - a)^m g$ with $g$ analytic and $g(a) \ne 0$.
- **Isolated zeros:** a non-constant analytic $f$ on a domain has isolated zeros.
- **Identity theorem:** if $f$ and $g$ are analytic on a domain $D$ and $f = g$ on a set with a **limit point in $D$**, then $f \equiv g$.
  - The limit point must lie in $D$: $\sin\frac{1}{1-z}$ on the unit disc has zeros accumulating at $1 \notin D$.
  - $f(1/n) = (-1)^n/n$ is impossible, $f(1/n) = \frac{1}{n+1}$ is possible, and $f(1/n) = e^{-n}$ is impossible.
- The order of a zero of $fg$ is the sum of the orders. $(z - a)^m$ has a zero of order $m$.

## 4. Laurent series
If $f$ is analytic on the annulus $r \lt  |z - a| \lt  R$, then
$$f(z) = \sum_{n=-\infty}^{\infty}a_n(z - a)^n,\qquad a_n = \frac{1}{2\pi i}\oint\frac{f(\zeta)}{(\zeta - a)^{n+1}}\thinspace d\zeta.$$
The expansion is **unique for each annulus**, but different annuli give different series. The **principal part** is $\sum_{n\lt 0}a_n(z - a)^n$.
- **Method:** use partial fractions, then expand $\frac{1}{z-b}$ as $-\frac1b\sum(z/b)^n$ when $|z| \lt  |b|$, or as $\frac1z\sum(b/z)^n$ when $|z| \gt  |b|$.
- **Example:** for $\frac{1}{(z-1)(z-2)}$:

| Region | Expansion |
|---|---|
| $\lvert z\rvert \lt  1$ | $\sum(1 - 2^{-n-1})z^n$ |
| $1 \lt  \lvert z\rvert \lt  2$ | $-\sum_{n\ge0}z^{-n-1} - \sum_{n\ge0}\frac{z^n}{2^{n+1}}$ |
| $\lvert z\rvert \gt  2$ | $\sum_{n\ge0}(2^n - 1)z^{-n-1}$ |

## 5. Isolated singularities
| Type | Laurent principal part | Limit behaviour | Test |
|---|---|---|---|
| Removable | none | $\lim f$ exists (finite) | $f$ is bounded near $a$ (Riemann) |
| Pole of order $m$ | finite, ending at $a_{-m}$ | $\lvert f\rvert \to \infty$ | $(z-a)^m f \to c \ne 0$; $a$ is a zero of order $m$ of $1/f$ |
| Essential | infinitely many terms | no limit, finite or infinite | Casorati–Weierstrass |

- **Casorati–Weierstrass:** near an essential singularity, the image of every punctured neighbourhood is dense in $\mathbb{C}$.
- **Great Picard:** near an essential singularity, $f$ takes every complex value, with at most one exception, infinitely often.
- If $f$ has a pole at $a$, then $e^{f}$ has an **essential** singularity at $a$. If $a$ is a zero of order $m$ of $g$, then it is a pole of order $m$ of $1/g$.
- A **non-isolated** singularity is a limit of singularities: $\frac{1}{\sin(1/z)}$ and $\tan(1/z)$ at $0$, and $\operatorname{Log} z$ at $0$ (a branch point).
- **At $\infty$:** classify $f(1/w)$ at $w = 0$.
  - Polynomials of degree $n$ have a pole of order $n$ at $\infty$.
  - $e^z$, $\sin z$ and other transcendental entire functions have an essential singularity at $\infty$.
  - Meromorphic on $\hat{\mathbb{C}}$ $\iff$ rational.

## 6. Argument principle and Rouché's theorem
- **Argument principle:** if $f$ is meromorphic inside and on $\gamma$, with no zeros or poles on $\gamma$, then
$$\frac{1}{2\pi i}\oint_\gamma\frac{f'}{f}\thinspace dz = Z - P,$$
  counted with multiplicity. Equivalently, it is the winding number of $f(\gamma)$ about $0$.
- **Rouché's theorem:** if $f$ and $g$ are analytic inside and on $\gamma$ and $|g| \lt  |f|$ on $\gamma$, then $f$ and $f + g$ have the **same number of zeros** inside $\gamma$. The symmetric form only needs $|f + g| \lt  |f| + |g|$ on $\gamma$.
- **Recipe for an annulus $r \lt  |z| \lt  R$:** count the zeros in $|z| \lt  R$, subtract those in $|z| \le r$, and check that there are no zeros on $|z| = r$.
- **Example:** $z^5 + 15z + 1$ has 1 zero in $|z| \lt  1$ (15z dominates) and 5 in $|z| \lt  2$ ($z^5$ dominates), so 4 in the annulus.
- **Hurwitz:** if $f_n \to f$ uniformly on compact sets, $f_n$ are non-vanishing, and $f$ is not identically zero, then $f$ is non-vanishing.

## Exam traps
1. A Taylor radius can be cut short by a **complex** singularity even when the function is smooth on $\mathbb{R}$.
2. Laurent coefficients depend on the annulus. In $1 \lt  |z| \lt  2$, $\frac{1}{(z-1)(z-2)}$ has a $z^{-1}$ coefficient of $-1$, even though $f$ is analytic at $0$.
3. The identity theorem needs the limit point **inside** the domain.
4. A function bounded near an isolated singularity has a removable singularity there.
5. A pole of $f$ becomes an **essential** singularity of $e^f$.
6. $\frac{1}{\sin(1/z)}$ has a non-isolated singularity at $0$, so it cannot be classified as a pole or essential singularity.
7. In the argument principle, poles count **negatively**.
8. Before using Rouché, check the strict inequality on the *whole* contour: $|z^5| = 32 \gt  31 \ge |15z + 1|$.
