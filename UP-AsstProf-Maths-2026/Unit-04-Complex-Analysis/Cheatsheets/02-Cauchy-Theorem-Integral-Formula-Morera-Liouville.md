# Cheatsheet · Unit 4 · Topic 02 — Cauchy's Theorem, Integral Formula, Morera and Liouville

## 1. Contour integrals
- $\int_\gamma f\thinspace dz = \int_a^b f(\gamma(t))\gamma'(t)\thinspace dt$.
- **ML-inequality:** $\left|\int_\gamma f\thinspace dz\right| \le M\cdot L(\gamma)$, where $M = \max_\gamma|f|$ and $L(\gamma)$ is the length of $\gamma$.
- **Basic integral:** $\oint_{|z-a|=r}(z-a)^n\thinspace dz = 2\pi i$ if $n = -1$, and $0$ for every other integer $n$.
- **Fundamental theorem:** if $F' = f$ on $D$, then $\int_\gamma f = F(\text{end}) - F(\text{start})$, and closed-curve integrals vanish. So $1/z^2$, $1/z^3, \dots$ have zero integral around $0$, while $1/z$ does not.
- On $|z| = r$ we have $\bar z = r^2/z$. Hence $\oint_{|z|=1}\bar z\thinspace dz = 2\pi i$ and $\oint_{|z|=r}\bar z\thinspace dz = 2\pi i r^2$.

## 2. Cauchy's theorem
| Version | Hypotheses | Conclusion |
|---|---|---|
| Cauchy–Goursat | $`f`$ analytic on and inside a simple closed contour $`\gamma`$ ($`f'`$ continuity **not** needed) | $`\oint_\gamma f = 0`$ |
| Simply connected | $`f`$ analytic on a simply connected domain $`D`$ | $`\oint_\gamma f = 0`$ for every closed $`\gamma\subset D`$; $`f`$ has a primitive |
| Homology form | $`f`$ analytic on $`D`$, $`\gamma`$ a cycle with $`n(\gamma,a) = 0`$ for all $`a\notin D`$ | $`\oint_\gamma f = 0`$ |
| Deformation | $\gamma_1$ and $\gamma_2$ homotopic in $D$ | $\oint_{\gamma_1} f = \oint_{\gamma_2} f$ |

Multiply connected regions: $\oint_{\text{outer}} = \sum\oint_{\text{inner}}$ when all curves are oriented positively.

## 3. Cauchy's integral formula (CIF)
For $`f`$ analytic inside and on a positively oriented simple closed $`\gamma`$, and $`a`$ inside $`\gamma`$:
$$f(a) = \frac{1}{2\pi i}\oint_\gamma\frac{f(z)}{z-a}\thinspace dz,\qquad f^{(n)}(a) = \frac{n!}{2\pi i}\oint_\gamma\frac{f(z)}{(z-a)^{n+1}}\thinspace dz.$$
- Consequences: an analytic function is $C^\infty$, and $f'$ is analytic.
- **Gauss mean value:** $f(a) = \frac{1}{2\pi}\int_0^{2\pi}f(a + re^{i\theta})\thinspace d\theta$.
- If $a$ is outside $\gamma$, the integral is $0$.
- With several points inside, use partial fractions or a separate small circle around each point.

## 4. Cauchy's estimates
If $`f`$ is analytic on $`|z - a| \le R`$ and $`|f| \le M`$ on $`|z - a| = R`$, then
$$|f^{(n)}(a)| \le \frac{n!\thinspace M}{R^{n}}.$$

## 5. Liouville and consequences
- **Liouville:** a bounded entire function is constant.
- **Generalised Liouville:** if $`f`$ is entire and $`|f(z)| \le A + B|z|^{k}`$, then $`f`$ is a polynomial of degree $`\le \lfloor k\rfloor`$.
- An entire $`f`$ is constant if any of these holds:
  - $\mathop{\mathrm{Re}}\nolimits f \le c$ (use $e^{f}$);
  - $\mathop{\mathrm{Re}}\nolimits f \ge c$ (use $e^{-f}$);
  - its range misses a disc (use $`1/(f - a)`$);
  - $|f| \ge \varepsilon \gt  0$ everywhere (use $1/f$);
  - $`f`$ is doubly periodic.
- **Fundamental theorem of algebra:** if a polynomial $p$ of degree $\ge 1$ had no zero, $1/p$ would be bounded and entire, hence constant. So every polynomial of degree $n$ has exactly $n$ roots counted with multiplicity.
- **Picard's little theorem (beyond syllabus, but useful):** a non-constant entire function omits at most one complex value. For example, $e^z$ omits $0$.

## 6. Morera's theorem
If $`f`$ is **continuous** on a domain $`D`$ and $`\oint_{\partial T}f = 0`$ for every triangle (or rectangle) $`T\subset D`$, then $`f`$ is analytic on $`D`$.
Uses: uniform limits of analytic functions are analytic; Schwarz reflection; functions defined by integrals with analytic parameter dependence.

## 7. Maximum and minimum modulus
- **Maximum modulus:** if $`f`$ is analytic and non-constant on a domain $`D`$, then $`|f|`$ has no local maximum in $`D`$. On a bounded $`D`$ with $`f`$ continuous on $`\bar D`$, $`\max_{\bar D}|f|`$ is attained on $`\partial D`$.
- **Minimum modulus:** the same for the minimum, provided $f$ has no zeros in $D$.
- The same principles hold for $\mathop{\mathrm{Re}}\nolimits f$ (harmonic functions satisfy max and min principles).
- **Schwarz lemma:** if $f:\mathbb{D}\to\mathbb{D}$ is analytic with $f(0) = 0$, then $|f(z)| \le |z|$ and $|f'(0)| \le 1$. Equality in either holds iff $f(z) = e^{i\theta}z$.
- Standard maximum: on $[0,2\pi]^2$, $\max|\sin z| = \cosh 2\pi$, using $|\sin z|^2 = \sin^2 x + \sinh^2 y$.

## Exam traps
1. Cauchy's theorem needs analyticity on a **simply connected** region containing the curve. An annulus around a pole does not qualify.
2. A zero integral does **not** imply analyticity inside: $\oint_{|z|=1}z^{-2}dz = 0$ despite the pole.
3. $\bar z$ and $|z|^2$ are not analytic, so do not apply Cauchy's theorem to them. Rewrite $\bar z = r^2/z$ on the circle instead.
4. Morera needs **continuity** of $`f`$ as a hypothesis.
5. Liouville needs $`f`$ to be **entire**. $1/(1 + z^2)$ is bounded on $\mathbb{R}$ but not entire.
6. The minimum modulus principle needs **no zeros**.
7. CIF for derivatives has the factor $n!/(2\pi i)$ and the power $(z - a)^{n+1}$. Get the off-by-one right.
8. $|f| \le A + B|z|^{3/2}$ gives degree $\le 1$, not $\le 2$.
