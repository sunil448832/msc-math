# Cheatsheet · Unit 4 · Topic 04 — Calculus of Residues and Contour Integration

## 1. Residue
If $f$ has an isolated singularity at $a$, then $`\mathop{\mathrm{Res}}\nolimits_a f = a_{-1}`$, the coefficient of $(z-a)^{-1}$ in the Laurent series on $0 \lt  |z-a| \lt  r$.

**Residue theorem:** if $f$ is analytic inside and on a simple closed $\gamma$ (positively oriented) except at $a_1,\dots,a_n$ inside $\gamma$, then
$$\oint_\gamma f\thinspace dz = 2\pi i\sum_k\mathop{\mathrm{Res}}\nolimits_{a_k}f.$$

## 2. Computing residues
| Situation | Formula |
|---|---|
| Simple pole | $\lim_{z\to a}(z-a)f(z)$ |
| $f = p/q$, $p(a) \ne 0$, $q$ has a simple zero at $a$ | $\dfrac{p(a)}{q'(a)}$ |
| Pole of order $m$ | $\dfrac{1}{(m-1)!}\lim_{z\to a}\dfrac{d^{m-1}}{dz^{m-1}}\big[(z-a)^m f\big]$ |
| Removable singularity | $0$ |
| Essential singularity | read $a_{-1}$ from the Laurent series |
| $f$ even about $a$, i.e. $f(a+h) = f(a-h)$ | $0$ |
| $\frac{g'}{g}$ at a zero of order $m$ / pole of order $m$ | $m$ / $-m$ |

Useful values:
| Function | Residue |
|---|---|
| $\frac{e^z}{z^n}$ at $0$ | $\frac{1}{(n-1)!}$ |
| $e^{1/z}$ at $0$ | $1$ |
| $z\cos\frac1z$ at $0$ | $-\frac12$ |
| $\sin\frac1z$ at $0$ | $1$ |
| $\cot z$ at $n\pi$ | $1$ |
| $\frac{1}{z^4+1}$ at a root $a$ | $-\frac a4$ |
| $\frac{\cot z}{z}$ at $0$ | $0$ |
| $\frac{1}{z^2\sin z}$ at $0$ | $\frac16$ |

## 3. Residue at infinity
$$\mathop{\mathrm{Res}}\nolimits_{\infty}f = -\mathop{\mathrm{Res}}\nolimits_{w=0}\frac{1}{w^2}f\negthinspace \left(\frac1w\right) = -(\text{coefficient of } 1/z \text{ in the expansion for large } |z|).$$
- The sum of all residues, including $\infty$, is $0$. So if all singularities lie inside $\gamma$, then $\oint_\gamma f = -2\pi i\mathop{\mathrm{Res}}\nolimits_\infty f$.
- **Shortcut for rationals:** if $f = P/Q$ with $\deg Q = \deg P + 1$ and leading coefficients $p$ and $q$, then $`\mathop{\mathrm{Res}}\nolimits_\infty = -p/q`$. If $\deg Q \ge \deg P + 2$, then $`\mathop{\mathrm{Res}}\nolimits_\infty = 0`$.
- **Trap:** $f$ can be analytic at $\infty$ with $\mathop{\mathrm{Res}}\nolimits_\infty \ne 0$, e.g. $1/z$. Conversely, $z$ has a pole at $\infty$ but residue $0$ there.

## 4. Standard real integrals
**(i) Trigonometric $\int_0^{2\pi}R(\cos\theta,\sin\theta)\thinspace d\theta$.** Substitute $z = e^{i\theta}$, $\cos\theta = \frac{z+z^{-1}}{2}$, $\sin\theta = \frac{z-z^{-1}}{2i}$, $d\theta = \frac{dz}{iz}$, and sum the residues inside $|z| = 1$.
$$\int_0^{2\pi}\frac{d\theta}{a+b\cos\theta} = \frac{2\pi}{\sqrt{a^2-b^2}}\ (a\gt |b|),\qquad \int_0^{2\pi}\frac{d\theta}{(a+b\cos\theta)^2} = \frac{2\pi a}{(a^2-b^2)^{3/2}}.$$

**(ii) Rational $\int_{-\infty}^{\infty}\frac{P}{Q}\thinspace dx$.** This needs $`\deg Q \ge \deg P + 2`$ and no real zeros of $Q$. The value is $2\pi i\sum_{\mathop{\mathrm{Im}}\nolimits a \gt  0}\mathop{\mathrm{Res}}\nolimits$.
- $\int_{\mathbb{R}}\frac{dx}{1+x^2} = \pi$
- $\int_{\mathbb{R}}\frac{dx}{(1+x^2)^2} = \frac\pi2$
- $\int_0^\infty\frac{dx}{1+x^4} = \frac{\pi}{2\sqrt2}$
- $\int_0^\infty\frac{dx}{1+x^n} = \frac{\pi/n}{\sin(\pi/n)}$

**(iii) Fourier type $\int_{\mathbb{R}}\frac{P}{Q}e^{imx}\thinspace dx$ with $m \gt  0$.** This needs only $\deg Q \ge \deg P + 1$, by Jordan's lemma. Close the contour in the **upper** half-plane, where $|e^{imz}| = e^{-my} \le 1$.
- $\int_{\mathbb{R}}\frac{\cos mx}{x^2+a^2}\thinspace dx = \frac{\pi}{a}e^{-ma}$
- $\int_{\mathbb{R}}\frac{x\sin mx}{x^2+a^2}\thinspace dx = \pi e^{-ma}$

**(iv) Indented contours (pole on the real axis).** For simple poles $b_j$ on $\mathbb{R}$:
$$\mathrm{P.V.}\int_{\mathbb{R}}f = 2\pi i\sum_{\text{UHP}}\mathop{\mathrm{Res}}\nolimits + \pi i\sum_{\mathbb{R}}\mathop{\mathrm{Res}}\nolimits.$$
A small semicircle around a simple pole contributes $-\pi i\mathop{\mathrm{Res}}\nolimits$ when traversed clockwise above the pole.
- $\int_0^\infty\frac{\sin x}{x}\thinspace dx = \frac\pi2$
- $\mathrm{P.V.}\int_{\mathbb{R}}\frac{e^{ix}}{x}\thinspace dx = i\pi$
- $\int_0^\infty\frac{\sin^2x}{x^2}\thinspace dx = \frac\pi2$

**(v) Branch cuts, keyhole and other contours.**
- $\int_0^\infty\frac{x^{a-1}}{1+x}\thinspace dx = \frac{\pi}{\sin a\pi}$ for $0 \lt  a \lt  1$.
- $\int_0^\infty\frac{\ln x}{1+x^2}\thinspace dx = 0$, by the substitution $x \mapsto 1/x$.
- $\int_0^\infty\frac{\ln x}{(1+x^2)^2}\thinspace dx = -\frac\pi4$.
- Fresnel: $\int_0^\infty\cos x^2\thinspace dx = \int_0^\infty\sin x^2\thinspace dx = \frac12\sqrt{\frac\pi2}$.
- Gaussian: $\int_{\mathbb{R}}e^{-x^2}\cos 2bx\thinspace dx = \sqrt\pi\thinspace e^{-b^2}$.

## 5. Estimation lemmas
- **ML:** if $|zf(z)| \to 0$ on $C_R$, then $\int_{C_R}f \to 0$. This is the rational case, which needs a degree gap $\ge 2$.
- **Jordan's lemma:** if $\max_{C_R}|f| \to 0$ and $m \gt  0$, then $\int_{C_R}e^{imz}f\thinspace dz \to 0$. It rests on $\int_0^\pi e^{-R\sin\theta}d\theta \lt  \pi/R$.
- **Small-circle lemma:** if $f$ has a simple pole at $a$ and $C_\varepsilon$ is an arc of angle $\alpha$ around $a$, then $\int_{C_\varepsilon}f \to i\alpha\mathop{\mathrm{Res}}\nolimits_a f$.

## Exam traps
1. Count only the poles **inside** the contour. For $|z - i| = 1$, the pole $-i$ is outside.
2. For $e^{imx}$ with $m \gt  0$, close upward. For $m \lt  0$, close downward and add a minus sign for the orientation.
3. Real parts: $\int\frac{\cos x}{x^2+1} = \mathop{\mathrm{Re}}\nolimits\frac{\pi}{e}$. Do not use $\cos z$ directly on the large arc, because it blows up.
4. $\int_0^\infty$ is half of $\int_{\mathbb{R}}$ only for **even** integrands.
5. A pole on the axis contributes $\pi i\mathop{\mathrm{Res}}\nolimits$, not $2\pi i\mathop{\mathrm{Res}}\nolimits$, to the principal value.
6. When all poles are inside, the residue at $\infty$ is the fastest method.
7. Jordan's lemma is needed when the degree gap is only 1. ML fails there, e.g. for $\frac{e^{iz}}{z}$.
8. An even function has zero residue at $0$ even when the singularity is a pole of even order.
