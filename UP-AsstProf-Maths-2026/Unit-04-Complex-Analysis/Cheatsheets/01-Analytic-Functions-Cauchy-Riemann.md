# Cheatsheet · Unit 4 · Topic 01 — Analytic Functions and the Cauchy–Riemann Equations

## 1. Definitions
- $f$ is **differentiable at $z_0$** if $f'(z_0) = \lim_{h\to0}\frac{f(z_0+h)-f(z_0)}{h}$ exists, with $h\to0$ in $\mathbb{C}$ from every direction.
- $f$ is **analytic (holomorphic) at $z_0$** if it is differentiable on some *neighbourhood* of $z_0$. $f$ is **entire** if it is analytic on all of $\mathbb{C}$.
- Analyticity on an open set means differentiability at every point of it. A set with no interior (a point, a line) can carry differentiability but never analyticity.

## 2. Cauchy–Riemann equations
For $f = u + iv$ and $z = x + iy$:
$$u_x = v_y,\qquad u_y = -v_x,\qquad f'(z) = u_x + i v_x = v_y - i u_y.$$
- **Necessary:** if $f$ is differentiable at $z_0$, then CR holds at $z_0$.
- **Sufficient:** if $u$ and $v$ have *continuous* first partials near $z_0$ (or are merely Fréchet differentiable at $z_0$) and CR holds at $z_0$, then $f$ is differentiable at $z_0$.
- Complex form: $\dfrac{\partial f}{\partial \bar z} = \tfrac12(f_x + i f_y) = 0$.
- **Polar form** ($z = re^{i\theta}$): $u_r = \frac1r v_\theta$ and $v_r = -\frac1r u_\theta$. Then $f'(z) = e^{-i\theta}(u_r + i v_r)$.

| Function | Where CR holds | Differentiable | Analytic |
|---|---|---|---|
| $\bar z$ | nowhere | nowhere | nowhere |
| $\lvert z\rvert^2$ | $z=0$ | only at $0$ | nowhere |
| $x^2 + iy^2$ | line $y = x$ | on $y = x$ | nowhere |
| $\sqrt{\lvert xy\rvert}$ | at $0$ | **not** at $0$ (CR holds but $f$ is not differentiable) | nowhere |
| $e^{-1/z^4}$, $f(0)=0$ | at $0$ (partials exist) | not at $0$ (not even continuous) | — |

## 3. Harmonic functions
- $u$ is harmonic if $u\in C^2$ and $\Delta u = u_{xx} + u_{yy} = 0$. The real and imaginary parts of an analytic function are harmonic.
- $v$ is a **harmonic conjugate** of $u$ if $u + iv$ is analytic. A conjugate exists on any **simply connected** domain and is unique up to an additive constant. Counterexample: $\ln|z|$ on $\mathbb{C}\setminus\lbrace 0\rbrace$ has no single-valued conjugate.
- The conjugate of $v$ is $-u$; the relation is *not* symmetric.
- Products: $uv = \tfrac12\mathop{\mathrm{Im}}\nolimits(f^2)$ **is** harmonic, but $u^2$ is harmonic only if $u$ is constant. A product of two harmonic functions need not be harmonic.
- Level curves $u = c_1$ and $v = c_2$ cut orthogonally wherever $f' \ne 0$.
- Polar Laplacian: $u_{rr} + \frac1r u_r + \frac1{r^2}u_{\theta\theta} = 0$. Examples: $r^n\cos n\theta$ and $\ln r$ are harmonic.

**Finding $f$ from $u$ (Milne-Thomson):**
$$f'(z) = u_x(z,0) - i\thinspace u_y(z,0),\qquad f(z) = \int f'(z)\thinspace dz + iC.$$
Given $v$ instead: $f'(z) = v_y(z,0) + i\thinspace v_x(z,0)$.

**Rigidity:** $f$ analytic on a domain is constant if any of the following holds: $f' \equiv 0$; $\mathop{\mathrm{Re}}\nolimits f$ is constant; $\mathop{\mathrm{Im}}\nolimits f$ is constant; $|f|$ is constant; $\bar f$ is analytic; $f$ is real-valued; $f(D)$ lies on a line, circle or other curve (by the open mapping theorem). An example is $u = v^2$.

## 4. Elementary functions
| Function | Key facts |
|---|---|
| $e^z = e^x(\cos y + i\sin y)$ | entire, never $0$, period $2\pi i$, $\lvert e^z\rvert = e^x$ |
| $\sin z$, $\cos z$ | entire; zeros only at the real points $n\pi$ and $\frac\pi2 + n\pi$; **unbounded**: $\lvert\sin z\rvert^2 = \sin^2x + \sinh^2y$ |
| $\sin(iy) = i\sinh y$, $\cos(iy) = \cosh y$ | $\cos^2 z + \sin^2 z = 1$ still holds |
| $\sinh z = -i\sin(iz)$, $\cosh z = \cos(iz)$ | period $2\pi i$ |
| $\log z = \ln\lvert z\rvert + i\arg z$ | multivalued; values differ by $2\pi i k$ |
| $\mathop{\mathrm{Log}}\nolimits z$ (principal) | $\mathop{\mathrm{Arg}}\nolimits\in(-\pi,\pi]$; analytic on $\mathbb{C}\setminus(-\infty,0]$; derivative $1/z$ |
| $z^c = e^{c\log z}$ | single-valued iff $c\in\mathbb{Z}$; finitely many ($q$) values iff $c = p/q$ is rational in lowest terms; infinitely many otherwise |

Standard values: $\mathop{\mathrm{Log}}\nolimits(-1) = i\pi$; $\mathop{\mathrm{Log}}\nolimits i = i\pi/2$; $i^i = e^{-\pi/2 - 2k\pi}$ (all values real, principal value $e^{-\pi/2}$); $\log 1 = 2k\pi i$; $(1+i)^i = e^{-\pi/4}e^{\frac i2\ln2}$ (principal).

## 5. Branches and branch cuts
- A **branch** of a multivalued $F$ is a single-valued analytic choice on a domain. A **branch point** is a point that a loop around changes the value, e.g. $0$ and $\infty$ for $\log z$ and $z^{1/n}$.
- $\sqrt{z(z-1)}$ has branch points $0$ and $1$ only (not $\infty$), so a cut along $[0,1]$ suffices.
- $\mathop{\mathrm{Log}}\nolimits(z_1 z_2) = \mathop{\mathrm{Log}}\nolimits z_1 + \mathop{\mathrm{Log}}\nolimits z_2 \pmod{2\pi i}$ only. Equality can fail: $\mathop{\mathrm{Log}}\nolimits((-1+i)^2) - 2\mathop{\mathrm{Log}}\nolimits(-1+i) = -2\pi i$.
- The principal branch is discontinuous across the cut: $\mathop{\mathrm{Log}}\nolimits(-1 + i0^+) = i\pi$ but $\mathop{\mathrm{Log}}\nolimits(-1 - i0^+) \to -i\pi$.

## Exam traps
1. CR holding at a point does **not** give differentiability. You also need continuity of the partials (or differentiability of $`(u,v)`$).
2. Differentiable on a line or at a point does **not** mean analytic there, because analyticity needs an open set.
3. The conjugate of $v$ is $-u$, not $u$.
4. In polar CR, the factor $1/r$ goes with the $\theta$-derivative: $r u_r = v_\theta$.
5. $\sin z$ and $\cos z$ are unbounded, and $|\cos z|$ can exceed 1, e.g. $\cos i = \cosh 1 \approx 1.543$.
6. $i^i$ is real. $z^c$ for irrational or non-real $c$ has infinitely many values.
7. $\mathop{\mathrm{Log}}\nolimits$ is analytic off $(-\infty,0]$, and $0$ itself is always excluded.
8. Milne-Thomson needs the sign: $f' = u_x(z,0) - i u_y(z,0)$. Remember to add the constant $iC$.
