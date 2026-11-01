# Cheatsheet · Unit 5 · Topic 06 — Surfaces: Fundamental Forms, Curvatures, Geodesics
> Questions: [../Questions/06-Surfaces-Fundamental-Forms-Curvatures-Geodesics.md](../Questions/06-Surfaces-Fundamental-Forms-Curvatures-Geodesics.md)

## 1. First fundamental form (the intrinsic metric)
For a surface patch $\mathbf r(u,v)$:
```math
I=E\thinspace du^2+2F\thinspace du\thinspace dv+G\thinspace dv^2,\qquad E=\mathbf r_u\negthinspace \cdot\negthinspace \mathbf r_u,\ F=\mathbf r_u\negthinspace \cdot\negthinspace \mathbf r_v,\ G=\mathbf r_v\negthinspace \cdot\negthinspace \mathbf r_v
```
- **Area element:** $dA=\sqrt{EG-F^2}\thinspace du\thinspace dv=|\mathbf r_u\times\mathbf r_v|\thinspace du\thinspace dv$. Here $EG-F^2\gt 0$ for a regular patch.
- **Arc length** of a curve $(u(t),v(t))$: $\int\sqrt{Eu'^2+2Fu'v'+Gv'^2}\thinspace dt$.
- **Angle** between the coordinate curves: $\cos\omega=F/\sqrt{EG}$. The parametrisation is **orthogonal** iff $F=0$.
- **Isometry:** a map preserving $I$. Locally, this means patches with the same $E,F,G$.

## 2. Second fundamental form
Unit normal $\mathbf n=\dfrac{\mathbf r_u\times\mathbf r_v}{|\mathbf r_u\times\mathbf r_v|}$.
```math
II=L\thinspace du^2+2M\thinspace du\thinspace dv+N\thinspace dv^2,\quad L=\mathbf r_{uu}\negthinspace \cdot\negthinspace \mathbf n=-\mathbf r_u\negthinspace \cdot\negthinspace \mathbf n_u,\ M=\mathbf r_{uv}\negthinspace \cdot\negthinspace \mathbf n,\ N=\mathbf r_{vv}\negthinspace \cdot\negthinspace \mathbf n
```
(Some books write $e,f,g$.)
- **Normal curvature** in a direction $du:dv$: $\kappa_n=\dfrac{II}{I}$.
- **Meusnier:** $\kappa_n=\kappa\cos\phi$, where $\phi$ is the angle between the principal normal of the curve and $\mathbf n$.

## 3. Principal curvatures, Gaussian and mean curvature
- **Shape (Weingarten) operator** $S=-d\mathbf n$. It is self-adjoint, its eigenvalues are the **principal curvatures** $\kappa_1,\kappa_2$ (the max and min of $\kappa_n$), and its eigenvectors are the **principal directions**. These are orthogonal at non-umbilic points.
- The principal curvatures solve $\det(II-\kappa I)=0$:
```math
(EG-F^2)\kappa^2-(EN-2FM+GL)\kappa+(LN-M^2)=0
```
```math
K=\kappa_1\kappa_2=\frac{LN-M^2}{EG-F^2},\qquad H=\frac{\kappa_1+\kappa_2}{2}=\frac{EN-2FM+GL}{2(EG-F^2)},\qquad \kappa_{1,2}=H\pm\sqrt{H^2-K}
```
- **Principal directions** satisfy
```math
\begin{vmatrix}dv^2&-du\thinspace dv&du^2\cr E&F&G\cr L&M&N\end{vmatrix}=0
```
- **Lines of curvature** are the curves tangent to principal directions. The coordinate curves are lines of curvature $\iff F=M=0$ (away from umbilics).
- **Rodrigues' formula:** along a line of curvature, $d\mathbf n=-\kappa\thinspace d\mathbf r$.
- **Euler's theorem:** $\kappa_n(\theta)=\kappa_1\cos^2\theta+\kappa_2\sin^2\theta$, where $\theta$ is measured from the $\kappa_1$-direction. Sum over two orthogonal directions: $\kappa_n(\theta)+\kappa_n(\theta+\tfrac\pi2)=2H$.
- **Asymptotic directions:** $\kappa_n=0$, i.e. $L\thinspace du^2+2M\thinspace du\thinspace dv+N\thinspace dv^2=0$. They exist iff $K\le0$, and are given by $\tan^2\theta=-\kappa_1/\kappa_2$.
- **Classification of points:**
  - elliptic ($K\gt 0$)
  - hyperbolic ($K\lt 0$, saddle)
  - parabolic ($K=0$, $H\ne0$)
  - planar ($\kappa_1=\kappa_2=0$)
  - **umbilic** ($\kappa_1=\kappa_2$)
- A connected surface in which every point is umbilic lies in a plane or a sphere.
- **Minimal surface:** $H\equiv0$, which implies $K\le0$. Examples: plane, catenoid, helicoid, Enneper, Scherk.

## 4. Useful formulas
**Monge patch** $z=f(x,y)$:
```math
K=\frac{f_{xx}f_{yy}-f_{xy}^2}{(1+f_x^2+f_y^2)^2},\qquad H=\frac{(1+f_y^2)f_{xx}-2f_xf_yf_{xy}+(1+f_x^2)f_{yy}}{2(1+f_x^2+f_y^2)^{3/2}}
```
At a critical point: $K=f_{xx}f_{yy}-f_{xy}^2$ (the Hessian determinant).

**Orthogonal parametrisation** ($F=0$), Brioschi formula:
```math
K=-\frac{1}{2\sqrt{EG}}\left[\Big(\frac{E_v}{\sqrt{EG}}\Big)_v+\Big(\frac{G_u}{\sqrt{EG}}\Big)_u\right]
```
- Geodesic polar coordinates $ds^2=dr^2+G\thinspace d\theta^2$: $K=-\dfrac{(\sqrt G)_{rr}}{\sqrt G}$.
- Isothermal coordinates $ds^2=\lambda(du^2+dv^2)$: $K=-\dfrac{1}{2\lambda}\Delta\ln\lambda$.

## 5. Standard surfaces
| Surface | Parametrisation | $E,F,G$ | $K$ | $H$ (sign depends on $\mathbf n$) |
|---|---|---|---|---|
| Plane | $(u,v,0)$ | $1,0,1$ | $0$ | $0$ |
| Sphere, radius $a$ | $(a\sin u\cos v,a\sin u\sin v,a\cos u)$ | $a^2,0,a^2\sin^2u$ | $1/a^2$ | $\pm1/a$ |
| Cylinder, radius $a$ | $(a\cos v,a\sin v,u)$ | $1,0,a^2$ | $0$ | $\pm1/(2a)$ |
| Cone | $(u\cos v,u\sin v,u)$ | $2,0,u^2$ | $0$ | $\ne0$ |
| Torus $(R\gt r)$ | $((R+r\cos u)\cos v,(R+r\cos u)\sin v,r\sin u)$ | $r^2,0,(R+r\cos u)^2$ | $\dfrac{\cos u}{r(R+r\cos u)}$ | – |
| Helicoid | $(u\cos v,u\sin v,cv)$ | $1,0,u^2+c^2$ | $-\dfrac{c^2}{(u^2+c^2)^2}$ | $0$ |
| Catenoid | $(\cosh u\cos v,\cosh u\sin v,u)$ | $\cosh^2u,0,\cosh^2u$ | $-\mathop{\mathrm{sech}}\nolimits^4u$ | $0$ |
| Pseudosphere | (tractrix of revolution) | – | $-1$ | – |

- **Torus:** the outer equator has $K=\dfrac{1}{r(R+r)}\gt 0$, the inner equator has $K=-\dfrac{1}{r(R-r)}\lt 0$, and the top and bottom circles have $K=0$. The total curvature is $\iint K\thinspace dA=0$.
- The catenoid and helicoid are **locally isometric**, and both are minimal.
- The cylinder and the cone are locally isometric to the plane ($K=0$, developable).

## 6. Theorema Egregium and isometries
- **Gauss:** $K$ depends only on $E,F,G$ and their derivatives, so it is intrinsic and invariant under local isometries. $H$ is **not** intrinsic: the plane and cylinder both have $K=0$, but $H$ differs.
- **Minding:** surfaces with the **same constant** $K$ are locally isometric.
- **Gauss–Bonnet** (compact surface): $\iint_S K\thinspace dA=2\pi\chi(S)$. For the sphere this is $4\pi$; for the torus it is $0$.

## 7. Geodesics
- **Definition:** a curve whose acceleration is normal to the surface. Equivalent conditions:
  - its geodesic curvature $\kappa_g=0$;
  - for $\kappa\ne0$, its principal normal is parallel to $\mathbf n$;
  - it satisfies the geodesic equations $\ddot u^k+\Gamma^k_{ij}\dot u^i\dot u^j=0$.
- Geodesics are locally length-minimising, and they have constant speed.
- **Curvature decomposition:** $\kappa^2=\kappa_n^2+\kappa_g^2$.
- A straight line on a surface is always a geodesic (and asymptotic).
- **Geodesic equations** for $F=0$:
```math
\frac{d}{ds}(E\dot u)=\tfrac12(E_u\dot u^2+G_u\dot v^2),\qquad \frac{d}{ds}(G\dot v)=\tfrac12(E_v\dot u^2+G_v\dot v^2)
```
- **Clairaut's relation:** on a surface of revolution, $\rho\sin\psi=$ const along a geodesic. Here $\rho$ is the distance from the axis and $\psi$ is the angle with the meridian. Consequences:
  - all meridians are geodesics;
  - a parallel is a geodesic iff $d\rho/ds=0$ there (i.e. $\rho$ is stationary along the meridian);
  - a geodesic never enters the region $\rho\lt c$, where $c=\rho\sin\psi$.

| Surface | Geodesics |
|---|---|
| Plane | straight lines |
| Sphere | great circles |
| Cylinder | rulings, parallels (circles), helices |
| Surface of revolution | all meridians; parallels where $\rho$ is extremal (e.g. the outer and inner equators of a torus) |

**Comparison of special curves on a surface**
| Curve | Condition |
|---|---|
| geodesic | $\kappa_g=0$ |
| asymptotic | $\kappa_n=0$ |
| line of curvature | tangent is a principal direction |

## Exam traps
- $H$ has a **2** in its denominator: $(EN-2FM+GL)/\big(2(EG-F^2)\big)$.
- In the Monge formula, remember $-f_{xy}^2$, and the power **2** of $1+|\nabla f|^2$ in $K$ (it is $3/2$ in $H$).
- The cylinder has $K=0$ but is **not** umbilic, and its $H\ne0$.
- Minimal surfaces have $K\le0$, not $K\ge0$.
- Clairaut uses $\rho\sin\psi$, with the angle measured from the **meridian**.
- Not every parallel of a surface of revolution is a geodesic (the parallels of a sphere other than the equator are not).
- Euler's formula is $\kappa_1\cos^2\theta+\kappa_2\sin^2\theta$, with $\theta$ measured from the $\kappa_1$-direction.
- On the torus, $K\gt 0$ on the outside, $K\lt 0$ on the inside, and $K=0$ on the top and bottom circles.
