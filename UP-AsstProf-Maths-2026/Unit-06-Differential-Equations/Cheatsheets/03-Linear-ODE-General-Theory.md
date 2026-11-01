# Cheatsheet · Unit 6 · Topic 03 — General Theory of Linear ODEs
> Questions: [../Questions/03-Linear-ODE-General-Theory.md](../Questions/03-Linear-ODE-General-Theory.md)

$$L[y]=y^{(n)}+p_1(x)y^{(n-1)}+\dots+p_n(x)y=r(x),\qquad p_i,r\ \text{continuous on } I.$$

## 1. Existence, uniqueness and structure
- For any $x_0\in I$ and any data $y(x_0),\dots,y^{(n-1)}(x_0)$, there is a **unique solution on all of $I$**.
- The solutions of $L[y]=0$ form a vector space of **dimension exactly $n$**.
- If $y\not\equiv0$ is a solution, its zeros are isolated, and $y(x_0)=y'(x_0)=\dots=y^{(n-1)}(x_0)=0$ forces $y\equiv0$.
- **Non-homogeneous equation:** the general solution is $y=y_c+y_p$, where $y_c=\sum c_iy_i$. The difference of two solutions of $L[y]=r$ solves $L[y]=0$.
- **Superposition:** if $L[y_1]=r_1$ and $L[y_2]=r_2$, then $L[y_1+y_2]=r_1+r_2$.

## 2. Wronskian and Abel's formula
$$W(y_1,\dots,y_n)=\det\big[y_j^{(i-1)}\big],\qquad \boxed{W(x)=W(x_0)\,e^{-\int_{x_0}^x p_1(t)\,dt}}\ \text{(Abel–Liouville)}.$$
- For **solutions**, $W\equiv0$ or $W$ is never $0$ on $I$, and $W\ne0$ iff the solutions are LI.
- For **arbitrary functions**: $W(x_0)\ne0$ at some point implies LI. The converse fails: $x^2$ and $x|x|$, or $x^3$ and $|x|^3$, have $W\equiv0$ but are LI on $[-1,1]$.
- **Consequences:** two solutions with a common zero, or a common critical point, are LD. Also, $x$ and $x^2$ cannot both solve a second-order equation with continuous $p,q$ on an interval containing $0$.
- For the normalised equation $y''+py'+qy=0$, $W$ is constant iff $p\equiv0$.
- Useful values: $W(e^{ax},e^{bx})=(b-a)e^{(a+b)x}$, $W(\cos kx,\sin kx)=k$, $W(e^{ax},xe^{ax})=e^{2ax}$, $W(1,x,\dots,x^{n-1})=\prod_{k=0}^{n-1}k!$.

## 3. Constant coefficients $a_0y^{(n)}+\dots+a_ny=0$
| Root of auxiliary equation | Contribution |
|---|---|
| real $m$, multiplicity $k$ | $(c_1+c_2x+\dots+c_kx^{k-1})e^{mx}$ |
| $\alpha\pm i\beta$, multiplicity $k$ | $e^{\alpha x}\big[(\dots)\cos\beta x+(\dots)\sin\beta x\big]$, with polynomial coefficients of degree $k-1$ |

## 4. Particular integral
**Undetermined coefficients.** For $r=e^{ax}P_m(x)(\cos bx\text{ or }\sin bx)$, try $x^s e^{ax}[Q_m\cos bx+R_m\sin bx]$, where $s$ is the multiplicity of $a+ib$ as a root ($0$ if it is not a root).

**Operator shortcuts** ($D=d/dx$):
- $\frac{1}{f(D)}e^{ax}=\frac{e^{ax}}{f(a)}$ if $f(a)\ne0$. If $f$ has $a$ as a root of multiplicity $k$, so that $f(D)=(D-a)^k g(D)$ with $g(a)\ne0$, then $\frac{1}{f(D)}e^{ax}=\frac{x^k}{k!\,g(a)}e^{ax}$. In particular, for a simple root, $\frac{1}{f(D)}e^{ax}=\frac{x\,e^{ax}}{f'(a)}$.
- $\frac{1}{f(D^2)}\sin ax=\frac{\sin ax}{f(-a^2)}$ if $f(-a^2)\ne0$. In the resonant case, $\frac{1}{D^2+a^2}\sin ax=-\frac{x\cos ax}{2a}$ and $\frac{1}{D^2+a^2}\cos ax=\frac{x\sin ax}{2a}$.
- For a polynomial $r$, expand $[f(D)]^{-1}$ in ascending powers of $D$.
- **Exponential shift:** $\frac{1}{f(D)}e^{ax}V=e^{ax}\frac{1}{f(D+a)}V$.

**Variation of parameters** (for $y''+py'+qy=r$, any continuous $r$):
$$y_p=-y_1\int\frac{y_2r}{W}dx+y_2\int\frac{y_1r}{W}dx .$$
For example, $y''+y=\sec x$ gives $y_p=x\sin x+\cos x\ln|\cos x|$, and $y''+y=\tan x$ gives $y_p=-\cos x\ln|\sec x+\tan x|$.

**Green's function / Cauchy kernel (IVP):** $y_p(x)=\int_{x_0}^x\frac{y_1(t)y_2(x)-y_1(x)y_2(t)}{W(t)}r(t)\,dt$.

## 5. Reduction of order
If $y_1$ solves $y''+py'+qy=0$, then
$$y_2=y_1\int\frac{e^{-\int p\,dx}}{y_1^2}\,dx .$$
| Equation | $y_1$ | $y_2$ |
|---|---|---|
| $x^2y''-xy'+y=0$ | $x$ | $x\ln x$ |
| $(1-x^2)y''-2xy'+2y=0$ | $x$ | $\frac{x}{2}\ln\frac{1+x}{1-x}-1$ |
| $y''-2ay'+a^2y=0$ | $e^{ax}$ | $xe^{ax}$ |
| $x y''-(x+1)y'+y=0$ | $e^x$ | $x+1$ |

**Normal form:** $y=v\,e^{-\frac12\int p}$ removes the first-derivative term, giving $v''+\big(q-\frac{p^2}{4}-\frac{p'}{2}\big)v=0$.

## 6. Cauchy–Euler equation $x^2y''+axy'+by=0$
Substitute $x=e^t$ and $\theta=\frac{d}{dt}$. Then $xD=\theta$, $x^2D^2=\theta(\theta-1)$ and $x^3D^3=\theta(\theta-1)(\theta-2)$. The indicial equation is $m(m-1)+am+b=0$.
| Roots | Solution |
|---|---|
| distinct real $m_1,m_2$ | $c_1x^{m_1}+c_2x^{m_2}$ |
| double root $m$ | $(c_1+c_2\ln x)x^m$ |
| $\alpha\pm i\beta$ | $x^{\alpha}[c_1\cos(\beta\ln x)+c_2\sin(\beta\ln x)]$ |

For the **Legendre-type** equation $(ax+b)^2y''+\dots$, put $ax+b=e^t$.

## 7. Exact linear ODE
$P_0y''+P_1y'+P_2y=r$ is exact iff $P_0''-P_1'+P_2=0$. Its first integral is $P_0y'+(P_1-P_0')y=\int r$.

## Exam traps
- Before using Abel's formula, divide by the leading coefficient: $xy''+2y'+\dots$ has $p=2/x$, not $2$.
- The test "$W\equiv0$ implies LD" is valid **only for solutions** of a linear ODE with continuous coefficients.
- With resonance, the trial solution must be multiplied by $x^s$. Count the multiplicity carefully: $(D-1)^2$ needs $x^2e^x$.
- A linear combination of non-homogeneous solutions is a solution only if the coefficients sum to $1$.
- For Cauchy–Euler, a double root gives $\ln x$, not $x$.
- The order-$n$ solution space has dimension exactly $n$. Three solutions of a second-order equation are always LD.
