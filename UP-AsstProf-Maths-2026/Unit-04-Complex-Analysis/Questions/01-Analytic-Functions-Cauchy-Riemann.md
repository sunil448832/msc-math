# Unit 4 · Topic 01 — Analytic Functions and the Cauchy–Riemann Equations
> Syllabus coverage: Analytic functions, Cauchy-Riemann equations (Cartesian and polar), harmonic functions and conjugates, Milne-Thomson method, elementary functions, branches of $\log$ and powers
> Cheatsheet: [../Cheatsheets/01-Analytic-Functions-Cauchy-Riemann.md](../Cheatsheets/01-Analytic-Functions-Cauchy-Riemann.md)

**Q1.** `[Concept]` ★ For $f(re^{i\theta}) = u(r,\theta) + i\thinspace v(r,\theta)$ with $r\gt 0$, the Cauchy–Riemann equations in polar form are

(A) $u_\theta = \dfrac{1}{r}v_r,\quad v_\theta = -\dfrac{1}{r}u_r$

(B) $u_r = r\thinspace v_\theta,\quad v_r = -r\thinspace u_\theta$

(C) $u_r = -\dfrac{1}{r}v_\theta,\quad v_r = \dfrac{1}{r}u_\theta$

(D) $u_r = \dfrac{1}{r}v_\theta,\quad v_r = -\dfrac{1}{r}u_\theta$

**Q2.** `[Numerical]` ★ The real values of $a$ for which $u(x,y) = e^{ax}\cos 2y$ is harmonic on $\mathbb R^2$ are

(A) $a = 2$ only

(B) $a = \pm 2$

(C) $a = 4$ only

(D) $a = \pm 4$

**Q3.** `[Concept]` ★ If $v$ is a harmonic conjugate of $u$ on a domain, then a harmonic conjugate of $v$ is

(A) $u$

(B) $-u$

(C) $-v$

(D) $u^2 - v^2$

**Q4.** `[Numerical]` ★★ (Milne-Thomson) An entire function $f = u + iv$ has $u(x,y) = e^{x}(x\cos y - y\sin y)$ and $f(0) = 0$. Then $f(z)$ is

(A) $z e^{-z}$

(B) $(z+1)e^{z}$

(C) $z e^{z}$

(D) $z^2 e^{z}$

**Q5.** `[Numerical]` ★★ The function $f(z) = x^3 + i(1-y)^3$ is complex-differentiable

(A) nowhere

(B) everywhere, but analytic nowhere

(C) at every point of the imaginary axis

(D) only at $z = i$

**Q6.** `[Multi-Statement]` ★★ Consider the statements:

I. $f(z) = |z|^2$ is differentiable at $z = 0$ but analytic nowhere.

II. $f(z) = \bar z$ is differentiable at no point of $\mathbb{C}$.

III. $f(z) = x^2 + i y^2$ is analytic on the line $y = x$.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★ 
**Assertion (A):** $f(z) = \sqrt{|xy|}$ satisfies the Cauchy–Riemann equations at $z = 0$, yet it is not differentiable at $z = 0$.
**Reason (R):** The Cauchy–Riemann equations at a point are necessary but not sufficient for complex differentiability there.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match the principal values (principal branch of $\log$, $\mathop{\mathrm{Arg}}\nolimits\in(-\pi,\pi]$):

| List-I | List-II |
|---|---|
| (a) $\mathop{\mathrm{Log}}\nolimits(i)$ | 1. $i\sinh 1$ |
| (b) $i^{\thinspace i}$ | 2. $e^{-\pi/2}$ |
| (c) $\sin(i)$ | 3. $i\pi/2$ |
| (d) $\cos(i)$ | 4. $\cosh 1$ |

(A) a-3, b-2, c-1, d-4

(B) a-3, b-2, c-4, d-1

(C) a-2, b-3, c-1, d-4

(D) a-3, b-4, c-1, d-2

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) $|\sin z|$ is bounded on $\mathbb{C}$.

(B) $e^{z}$ is periodic with period $2\pi i$.

(C) The zeros of $\sin z$ in $\mathbb{C}$ are exactly $z = n\pi$, $n\in\mathbb{Z}$.

(D) $e^{z} \neq 0$ for every $z\in\mathbb{C}$.

**Q10.** `[Concept]` ★ The principal branch $\mathop{\mathrm{Log}}\nolimits z = \ln|z| + i\mathop{\mathrm{Arg}}\nolimits z$ is analytic on

(A) $\mathbb{C}\setminus\lbrace 0\rbrace$

(B) $\mathbb{C}\setminus[0,\infty)$

(C) $\mathbb{C}\setminus(-\infty,0]$

(D) the right half-plane only

**Q11.** `[Numerical]` ★★ The principal value of $(1+i)^{i}$ is

(A) $\sqrt2\thinspace  e^{-\pi/4}$

(B) $e^{\pi/4}\left[\cos\left(\tfrac12\ln 2\right) + i\sin\left(\tfrac12\ln 2\right)\right]$

(C) $e^{-\pi/4}\left[\cos(\ln 2) + i\sin(\ln 2)\right]$

(D) $e^{-\pi/4}\left[\cos\left(\tfrac12\ln 2\right) + i\sin\left(\tfrac12\ln 2\right)\right]$

**Q12.** `[Application]` ★★★ Let $f = u + iv$ be analytic on a domain $D$ with $u = v^2$ throughout $D$. Then

(A) $f$ must be constant on $D$

(B) $f$ must be a polynomial of degree exactly 2

(C) $f(D)$ lies on the parabola $u = v^2$, but $f$ need not be constant

(D) no such $f$ exists

**Q13.** `[Application]` ★★★ With $\mathop{\mathrm{Log}}\nolimits$ the principal branch and $z = -1 + i$, the value of $\mathop{\mathrm{Log}}\nolimits(z^2) - 2\mathop{\mathrm{Log}}\nolimits z$ is

(A) $0$

(B) $2\pi i$

(C) $-2\pi i$

(D) $\pi i$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | B | Concept |
| 4 | C | Numerical |
| 5 | D | Numerical |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | A | Match |
| 9 | A | NOT-true / Counterexample |
| 10 | C | Concept |
| 11 | D | Numerical |
| 12 | A | Application |
| 13 | C | Application |

## Solutions
**Q1 — (D).** From $x = r\cos\theta$, $y = r\sin\theta$: $u_r = \frac1r v_\theta$ and $v_r = -\frac1r u_\theta$, i.e. $r u_r = v_\theta$. In (B) the factor $r$ is on the wrong side, and (C) has the signs swapped.

**Q2 — (B).** $u_{xx} + u_{yy} = (a^2 - 4)e^{ax}\cos 2y = 0 \Rightarrow a^2 = 4$, so $a = \pm 2$. Option (A) forgets the negative root, since $e^{-2x}\cos 2y = \mathop{\mathrm{Re}}\nolimits e^{-2z}$ is harmonic too.

**Q3 — (B).** If $f = u + iv$ is analytic, then so is $-if = v - iu$, which has real part $v$ and imaginary part $-u$. So the conjugate of $v$ is $-u$, not $u$.

**Q4 — (C).** By Milne-Thomson, $f'(z) = u_x(z,0) - i\thinspace u_y(z,0)$. Here $u_x = e^x(x\cos y - y\sin y + \cos y)$ gives $u_x(z,0) = (z+1)e^z$, and $u_y(z,0) = 0$. So $f' = (z+1)e^z$ and $f = ze^z + C$, with $C = 0$ because $f(0) = 0$. Option (B) is $f'$, not $f$.

**Q5 — (D).** $u_x = 3x^2$ and $v_y = -3(1-y)^2$, so $u_x = v_y$ forces $x = 0$ and $y = 1$. Also $u_y = 0 = -v_x$. The partial derivatives are continuous, so $f$ is differentiable exactly at $z = i$. A single point is not open, so $f$ is analytic nowhere.

**Q6 — (B).** I: the difference quotient $\frac{|h|^2}{h} = \bar h \to 0$, so $f$ is differentiable at $0$; CR fails everywhere else, so it is analytic nowhere. II: $u_x = 1 \ne v_y = -1$ everywhere. III: CR holds only on $y = x$, and a line contains no open set, so $f$ is differentiable on the line but analytic nowhere. Statement III is the trap.

**Q7 — (A).** $u = \sqrt{|xy|}$ and $v = 0$. Since $u(x,0) = u(0,y) = 0$, all four partials at $0$ vanish and CR holds. Along $y = x$, the difference quotient $\frac{|x|}{x(1+i)}$ has no limit. R is the general principle that this example illustrates.

**Q8 — (A).** $\mathop{\mathrm{Log}}\nolimits i = i\pi/2$. $i^i = e^{i\mathop{\mathrm{Log}}\nolimits i} = e^{-\pi/2}$, which is real. $\sin(iy) = i\sinh y$ and $\cos(iy) = \cosh y$.

**Q9 — (A).** $|\sin(iy)| = \sinh|y| \to \infty$, so $\sin z$ is unbounded (as it must be, being a non-constant entire function, by Liouville). (B), (C) and (D) are true: $\sin z = 0 \iff e^{2iz} = 1 \iff z = n\pi$.

**Q10 — (C).** $\mathop{\mathrm{Arg}}\nolimits$ jumps by $2\pi$ across the negative real axis, and $0$ is excluded, so the cut is $(-\infty,0]$. On $\mathbb{C}\setminus(-\infty,0]$ we have $(\mathop{\mathrm{Log}}\nolimits z)' = 1/z$.

**Q11 — (D).** $\mathop{\mathrm{Log}}\nolimits(1+i) = \tfrac12\ln 2 + i\pi/4$. Then $i\mathop{\mathrm{Log}}\nolimits(1+i) = -\pi/4 + \tfrac{i}{2}\ln 2$, and exponentiating gives (D) (numerically $0.4288 + 0.1549i$). Option (C) uses $\ln|1+i| = \ln 2$, which is wrong.

**Q12 — (A).** $u_x = 2v v_x$ and $u_y = 2v v_y$. With CR ($u_x = v_y$, $u_y = -v_x$) this becomes $v_y = 2v v_x$ and $-v_x = 2v v_y$, so $v_y(1 + 4v^2) = 0$. Hence $v_y = 0$, and then $v_x = 0$. So $v$ is constant, $u = v^2$ is constant, and $f$ is constant (the open mapping theorem gives the same conclusion). Constants such as $f = 1 + i$ do exist, so (D) is false.

**Q13 — (C).** $z^2 = -2i$, so $\mathop{\mathrm{Log}}\nolimits(z^2) = \ln 2 - i\pi/2$. Also $\mathop{\mathrm{Log}}\nolimits z = \tfrac12\ln 2 + 3\pi i/4$, so $2\mathop{\mathrm{Log}}\nolimits z = \ln 2 + 3\pi i/2$. The difference is $-2\pi i$. Because $\mathop{\mathrm{Log}}\nolimits(z^2) \ne 2\mathop{\mathrm{Log}}\nolimits z$ in general, (A) is wrong; (B) has the wrong sign.
