# Unit 7 · Topic 04 — Laplace Transforms
> Syllabus coverage: Laplace transforms (existence, shifting theorems, derivatives/integrals of transforms, convolution, inverse transforms, initial/final value theorems, unit step and impulse, solution of ODEs and integral equations)
> Cheatsheet: [../Cheatsheets/04-Laplace-Transforms.md](../Cheatsheets/04-Laplace-Transforms.md)

**Q1.** `[Concept]` ★ $\mathcal{L}\lbrace \sqrt t\rbrace$ equals

(A) $\dfrac{\sqrt\pi}{2s^{3/2}}$

(B) $\dfrac{\sqrt\pi}{s^{1/2}}$

(C) $\dfrac{1}{2s^{3/2}}$

(D) $\dfrac{\sqrt\pi}{s^{3/2}}$

**Q2.** `[Numerical]` ★ $\mathcal{L}\lbrace e^{2t}\sin 3t\rbrace$ equals

(A) $\dfrac{3}{(s+2)^2+9}$

(B) $\dfrac{s-2}{(s-2)^2+9}$

(C) $\dfrac{3}{(s-2)^2+9}$

(D) $\dfrac{3}{(s-2)^2-9}$

**Q3.** `[Numerical]` ★★ $\mathcal{L}\lbrace t\sin t\rbrace$ equals

(A) $\dfrac{2s}{(s^2+1)^2}$

(B) $\dfrac{s^2-1}{(s^2+1)^2}$

(C) $\dfrac{-2s}{(s^2+1)^2}$

(D) $\dfrac{1}{(s^2+1)^2}$

**Q4.** `[Numerical]` ★★ $\mathcal L^{-1}\left\lbrace \dfrac{1}{s(s^2+1)}\right\rbrace$ equals

(A) $1+\cos t$

(B) $\sin t$

(C) $1-\cos t$

(D) $t-\sin t$

**Q5.** `[Numerical]` ★★★ The value of $\displaystyle\int_0^\infty \frac{e^{-t}\sin t}{t}\thinspace dt$ is

(A) $\dfrac{\pi}{2}$

(B) $\dfrac{\pi}{4}$

(C) $\dfrac{1}{2}$

(D) $\ln 2$

**Q6.** `[Concept]` ★★ $\mathcal L^{-1}\left\lbrace \dfrac{e^{-2s}}{s^2}\right\rbrace$ equals ($u$ = unit step)

(A) $t\thinspace u(t-2)$

(B) $(t-2)\thinspace u(t)$

(C) $(t+2)\thinspace u(t+2)$

(D) $(t-2)\thinspace u(t-2)$

**Q7.** `[Application]` ★★★ The solution of the integral equation $y(t)=t+\displaystyle\int_0^t \sin(t-u)\thinspace y(u)\thinspace du$ is

(A) $t+\dfrac{t^3}{6}$

(B) $\sinh t$

(C) $t+\dfrac{t^3}{3}$

(D) $t-\dfrac{t^3}{6}$

**Q8.** `[Multi-Statement]` ★★ Consider the statements:

I. Every piecewise continuous function of exponential order on $[0,\infty)$ has a Laplace transform for all sufficiently large $s$.

II. $\mathcal{L}\lbrace t^{-1/2}\rbrace$ exists, although $t^{-1/2}$ is not piecewise continuous on $[0,\infty)$.

III. $\mathcal{L}\lbrace e^{t^2}\rbrace$ exists for $s\gt 0$.

IV. If $f$ is piecewise continuous and of exponential order, then $\mathcal{L}\lbrace f\rbrace (s)\to0$ as $s\to\infty$.

Which are correct?

(A) I and II only

(B) I, II and IV only

(C) I and III only

(D) I, II, III and IV

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** By the final value theorem, $\displaystyle\lim_{t\to\infty}\sin t=\lim_{s\to0}\frac{s}{s^2+1}=0$.
**Reason (R):** The final value theorem $\lim_{t\to\infty}f(t)=\lim_{s\to0}sF(s)$ is valid only when all poles of $sF(s)$ lie in the open left half-plane.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[Match]` ★★ Match $F(s)$ (List-I) with $f(t)=\mathcal L^{-1}\lbrace F\rbrace$ (List-II).

| List-I | List-II |
|---|---|
| (a) $\dfrac{s}{s^2+a^2}$ | 1. $t\thinspace e^{at}$ |
| (b) $\dfrac{a}{s^2-a^2}$ | 2. $\delta(t)$ |
| (c) $\dfrac{1}{(s-a)^2}$ | 3. $\cos at$ |
| (d) $1$ | 4. $\sinh at$ |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-4, c-1, d-2

(C) a-4, b-3, c-1, d-2

(D) a-3, b-4, c-2, d-1

**Q11.** `[NOT-true / Counterexample]` ★ With $F=\mathcal{L}\lbrace f\rbrace$, $G=\mathcal{L}\lbrace g\rbrace$, which is NOT true in general?

(A) $\mathcal{L}\left\lbrace \int_0^t f(u)g(t-u)\thinspace du\right\rbrace =F(s)G(s)$

(B) $\mathcal{L}\lbrace f'(t)\rbrace =sF(s)-f(0)$

(C) $\mathcal{L}\lbrace f(t)g(t)\rbrace =F(s)G(s)$

(D) $\mathcal{L}\left\lbrace \dfrac{f(t)}{t}\right\rbrace =\displaystyle\int_s^\infty F(u)\thinspace du$ (when $\lim_{t\to0^+}f(t)/t$ exists)

**Q12.** `[Numerical]` ★★ If $F(s)=\dfrac{s+3}{s(s+1)(s+2)}$, then $\displaystyle\lim_{t\to\infty}f(t)$ equals

(A) $0$

(B) $3$

(C) $\dfrac{3}{2}$

(D) $\dfrac{1}{2}$

**Q13.** `[Numerical]` ★★ If $y'+y=u(t-1)$, $y(0)=0$, then $y(2)$ equals

(A) $1-e^{-2}$

(B) $0$

(C) $e^{-1}$

(D) $1-e^{-1}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | C | Numerical |
| 3 | A | Numerical |
| 4 | C | Numerical |
| 5 | B | Numerical |
| 6 | D | Concept |
| 7 | A | Application |
| 8 | B | Multi-Statement |
| 9 | D | Assertion-Reason |
| 10 | B | Match |
| 11 | C | NOT-true / Counterexample |
| 12 | C | Numerical |
| 13 | D | Numerical |

## Solutions
**Q1 — (A).** $\mathcal{L}\lbrace t^\nu\rbrace =\frac{\Gamma(\nu+1)}{s^{\nu+1}}$; $\Gamma(3/2)=\frac{\sqrt\pi}{2}$. (B) is $\mathcal{L}\lbrace t^{-1/2}\rbrace$.

**Q2 — (C).** First shifting: $\mathcal{L}\lbrace e^{at}f\rbrace =F(s-a)$ with $F=\frac{3}{s^2+9}$. (A) shifts the wrong way.

**Q3 — (A).** $\mathcal{L}\lbrace tf\rbrace =-F'(s)=-\frac{d}{ds}\frac1{s^2+1}=\frac{2s}{(s^2+1)^2}$. (B) is $\mathcal{L}\lbrace t\cos t\rbrace$; (C) forgets the minus sign.

**Q4 — (C).** $\frac{1}{s(s^2+1)}=\frac1s-\frac{s}{s^2+1}$ ⇒ $1-\cos t$ (or $\int_0^t\sin u\thinspace du$). (D) is $\mathcal L^{-1}\lbrace \frac{1}{s^2(s^2+1)}\rbrace$.

**Q5 — (B).** $\mathcal{L}\lbrace \frac{\sin t}{t}\rbrace =\int_s^\infty\frac{du}{u^2+1}=\tan^{-1}\frac1s$; at $s=1$: $\pi/4$. (A) is the value at $s=0$.

**Q6 — (D).** Second shifting: $\mathcal{L}\lbrace f(t-a)u(t-a)\rbrace =e^{-as}F(s)$ with $f=t$, $a=2$. (A) shifts the step but not the function.

**Q7 — (A).** $Y=\frac1{s^2}+\frac{Y}{s^2+1}$ ⇒ $Y\frac{s^2}{s^2+1}=\frac1{s^2}$ ⇒ $Y=\frac{s^2+1}{s^4}=\frac1{s^2}+\frac1{s^4}$ ⇒ $y=t+\frac{t^3}{6}$. (D) comes from a sign error.

**Q8 — (B).** I: standard existence theorem (sufficient). II: $\mathcal{L}\lbrace t^{-1/2}\rbrace =\sqrt{\pi/s}$, so the condition in I is not necessary. III: $e^{t^2-st}\to\infty$, no transform. IV: true for such $f$ (so e.g. $F(s)=1$ or $s$ is not the transform of an ordinary function).

**Q9 — (D).** $\lim_{t\to\infty}\sin t$ does not exist; $sF(s)=\frac{s}{s^2+1}$ has poles $\pm i$ on the imaginary axis, so the FVT does not apply. A is false, R is true.

**Q10 — (B).** $\cos at$; $\sinh at$; first shift of $\mathcal{L}\lbrace t\rbrace =1/s^2$ gives $te^{at}$; $\mathcal{L}\lbrace \delta\rbrace =1$.

**Q11 — (C).** The transform of a product is not the product of transforms (that is the convolution theorem, A). E.g. $f=g=1$: $\mathcal{L}\lbrace 1\rbrace =\frac1s\ne\frac1{s^2}$.

**Q12 — (C).** $sF=\frac{s+3}{(s+1)(s+2)}$ has poles $-1,-2$ (left half-plane), so FVT applies: $\frac{3}{2}$. (B) forgets the factor $(s+1)(s+2)=2$ at $s=0$; (A) wrongly assumes $f$ must decay (the pole of $F$ at $s=0$ gives a constant term $\frac32$ in $f$).

**Q13 — (D).** $(s+1)Y=\frac{e^{-s}}{s}$ ⇒ $Y=e^{-s}\left(\frac1s-\frac1{s+1}\right)$ ⇒ $y=\left(1-e^{-(t-1)}\right)u(t-1)$. At $t=2$: $1-e^{-1}$. (A) ignores the delay.
