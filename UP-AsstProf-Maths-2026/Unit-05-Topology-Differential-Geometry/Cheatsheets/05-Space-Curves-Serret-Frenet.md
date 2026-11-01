# Cheatsheet · Unit 5 · Topic 05 — Space Curves, Curvature, Torsion, Serret–Frenet
> Questions: [../Questions/05-Space-Curves-Serret-Frenet.md](../Questions/05-Space-Curves-Serret-Frenet.md)

## 1. Arc length and the Frenet frame
- **Arc length:** $s(t)=\int_{t_0}^t|\mathbf r'(u)|\thinspace du$. A curve is **unit speed** if $|\mathbf r'(s)|=1$. Every regular curve ($\mathbf r'\ne0$) can be reparametrised by arc length.
- Dashes below denote $d/ds$.

| Object | Definition (unit speed) |
|---|---|
| Unit tangent | $T=\mathbf r'$ |
| Curvature | $\kappa=\vert T'\vert =\vert \mathbf r''\vert \ge0$ |
| Radius of curvature | $\rho=1/\kappa$ |
| Principal normal | $N=T'/\kappa$ (needs $\kappa\ne0$) |
| Binormal | $B=T\times N$ |
| Torsion | $\tau=-B'\cdot N$, i.e. $B'=-\tau N$ |
| Radius of torsion | $\sigma=1/\tau$ |

Planes through $\mathbf r(s)$:
- **osculating** plane $\langle T,N\rangle$, normal $B$
- **normal** plane $\langle N,B\rangle$, normal $T$
- **rectifying** plane $\langle T,B\rangle$, normal $N$

## 2. Serret–Frenet formulae
$$
\begin{pmatrix}T\cr N\cr B\end{pmatrix}'=\begin{pmatrix}0&\kappa&0\cr -\kappa&0&\tau\cr 0&-\tau&0\end{pmatrix}\begin{pmatrix}T\cr N\cr B\end{pmatrix}
$$
- The coefficient matrix is skew-symmetric.
- **Darboux vector:** $\boldsymbol\omega=\tau T+\kappa B$, and $X'=\boldsymbol\omega\times X$ for $X=T,N,B$. Its length $|\boldsymbol\omega|=\sqrt{\kappa^2+\tau^2}$ is the "total curvature".
- $|T'|=\kappa$, $|B'|=|\tau|$, $|N'|=\sqrt{\kappa^2+\tau^2}$.
- $\mathbf r'''=-\kappa^2T+\kappa'N+\kappa\tau B$, so $\tau=\dfrac{[\mathbf r',\mathbf r'',\mathbf r''']}{\kappa^2}$ for unit speed.
- (Some books use $B'=+\tau N$, which flips the sign of $\tau$. The magnitude is unaffected.)

## 3. Formulas for an arbitrary parameter $t$
$$
\kappa=\frac{|\mathbf r'\times\mathbf r''|}{|\mathbf r'|^3},\qquad \tau=\frac{(\mathbf r'\times\mathbf r'')\cdot\mathbf r'''}{|\mathbf r'\times\mathbf r''|^2}=\frac{[\mathbf r'\ \mathbf r''\ \mathbf r''']}{|\mathbf r'\times\mathbf r''|^2}
$$
$$
T=\frac{\mathbf r'}{|\mathbf r'|},\quad B=\frac{\mathbf r'\times\mathbf r''}{|\mathbf r'\times\mathbf r''|},\quad N=B\times T
$$
- Plane curve $y=f(x)$: $\kappa=\dfrac{|f''|}{(1+f'^2)^{3/2}}$.
- Plane parametric curve: $\kappa=\dfrac{|x'y''-y'x''|}{(x'^2+y'^2)^{3/2}}$.

## 4. Standard curves
| Curve | $\kappa$ | $\tau$ |
|---|---|---|
| Straight line | $0$ | undefined / $0$ |
| Circle of radius $a$ | $1/a$ | $0$ |
| Helix $(a\cos t,a\sin t,bt)$ | $\dfrac{a}{a^2+b^2}$ | $\dfrac{b}{a^2+b^2}$ |
| Twisted cubic $(t,t^2,t^3)$ at $t=0$ | $2$ | $3$ |
| $(\cosh t,\sinh t,t)$ | $\dfrac1{2\cosh^2t}$ | $\dfrac1{2\cosh^2t}$ |
| $(t,t^2/2,t^3/3)$ | $\dfrac{\sqrt{1+4t^2+t^4}}{(1+t^2+t^4)^{3/2}}$ (so $1$ at $t=0$) | $\dfrac{2}{1+4t^2+t^4}$ (so $2$ at $t=0$) |

- **Helix:** the length of one turn is $2\pi\sqrt{a^2+b^2}$ and the pitch is $2\pi b$. The tangent makes angle $\alpha$ with the axis, where $\cos\alpha=b/\sqrt{a^2+b^2}$.
- **Inverse formulas:** given constant $\kappa,\tau$, the helix has $a=\dfrac{\kappa}{\kappa^2+\tau^2}$ and $b=\dfrac{\tau}{\kappa^2+\tau^2}$.
- A right-handed helix ($b\gt 0$) has $\tau\gt 0$.

## 5. Key theorems
- $\kappa\equiv0\iff$ the curve is a straight line (segment).
- For $\kappa\ne0$: $\tau\equiv0\iff$ the curve is planar ($B$ is constant).
- $\kappa$ constant $\gt 0$ and $\tau\equiv0$ $\iff$ the curve is an arc of a circle of radius $1/\kappa$.
- $\kappa,\tau$ both constant (non-zero) $\iff$ the curve is a circular helix.
- **Lancret:** generalized helix (the tangent makes a constant angle with a fixed direction $\mathbf u$) $\iff$ $\kappa/\tau$ is constant. The axis is along the Darboux vector, $\mathbf u\parallel\tau T+\kappa B$.
- **Fundamental theorem of curves:** given smooth $\kappa(s)\gt 0$ and $\tau(s)$, there is a unit-speed curve with these as its curvature and torsion. It is unique up to a rigid (proper Euclidean) motion.
- **Spherical curves** ($\tau\ne0$, $\kappa'\ne0$): the curve lies on a sphere of radius $R$ iff $\rho^2+(\rho'\sigma)^2=R^2$ is constant, with $\rho=1/\kappa$ and $\sigma=1/\tau$. Equivalently $\dfrac{\tau}{\kappa}=\Big(\dfrac{\kappa'}{\kappa^2\tau}\Big)'$.
- **Spherical indicatrices** (curvatures; $ds_T=\kappa\thinspace ds$, $ds_B=|\tau|\thinspace ds$):
  - tangent indicatrix: $\sqrt{\kappa^2+\tau^2}/\kappa$
  - binormal indicatrix: $\sqrt{\kappa^2+\tau^2}/|\tau|$
- **Bertrand curves:** two curves sharing principal normals. They exist iff $a\kappa+b\tau=1$ for constants $a\ne0$ and $b$.
- **Involute/evolute:** the involute of $\mathbf r$ is $\mathbf r+(c-s)T$, with curvature $\dfrac{\sqrt{\kappa^2+\tau^2}}{\kappa|c-s|}$.

## Exam traps
- Use $\kappa=|\mathbf r'\times\mathbf r''|/|\mathbf r'|^{3}$. Do not use $|\mathbf r''|$ unless the curve is unit speed.
- The torsion denominator is $|\mathbf r'\times\mathbf r''|^{2}$, not $|\mathbf r'|^{3}$ or $|\mathbf r'\times\mathbf r''|$.
- $B'=-\tau N$, with a minus sign. The middle formula $N'=-\kappa T+\tau B$ has two terms.
- The Darboux vector is $\tau T+\kappa B$, not $\kappa T+\tau B$.
- For the helix, $\kappa=a/(a^2+b^2)$, not $1/a$. The cylinder radius is $\kappa/(\kappa^2+\tau^2)$, not $1/\kappa$.
- $\kappa/\tau$ constant gives a generalized helix, not necessarily a circular one.
- A planar curve has $B$ **constant** (parallel to a fixed vector), not perpendicular to one.
