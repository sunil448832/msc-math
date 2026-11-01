# Cheatsheet · Unit 8 · Topic 03 — Rigid Body Dynamics and Euler's Equations
> Questions: [../Questions/03-Rigid-Body-Euler-Equations.md](../Questions/03-Rigid-Body-Euler-Equations.md)

## 1. Moments and products of inertia
- **Moments of inertia:**
  - $I_{xx} = A = \int(y^2+z^2)\thinspace dm$
  - $I_{yy} = B = \int(z^2+x^2)\thinspace dm$
  - $I_{zz} = C = \int(x^2+y^2)\thinspace dm$
- **Products of inertia:** $D = \int yz\thinspace dm$, $E = \int zx\thinspace dm$, $F = \int xy\thinspace dm$. They can be of either sign.
- **Inertia tensor:** $`\mathbf I = \begin{pmatrix}A & -F & -E\cr  -F & B & -D\cr  -E & -D & C\end{pmatrix}`$, which is real, symmetric and positive semi-definite.
- **Moment about a line** with direction cosines $(l,m,n)$ through $O$:
$$I = Al^2 + Bm^2 + Cn^2 - 2Dmn - 2Enl - 2Flm .$$
- **Momental ellipsoid:** $Ax^2 + By^2 + Cz^2 - 2Dyz - 2Ezx - 2Fxy = 1$. The moment about a line through $O$ is $1/r^2$, where $r$ is the radius vector of the ellipsoid along that line.
- **Parallel axis theorem:** $I = I_G + Md^2$, where the axis through **G** is parallel to the given one. For products: $F_O = F_G + M\bar x\bar y$.
- **Perpendicular axis theorem** (lamina in the $xy$-plane only): $I_z = I_x + I_y$.
- **Triangle inequality:** $A + B \ge C$ and cyclically.

### Standard moments of inertia (mass $M$)
| Body | Axis | $I$ |
|---|---|---|
| Rod of length $2a$ | ⟂ through centre | $Ma^2/3$ |
| Rod of length $\ell$ | ⟂ through end | $M\ell^2/3$ |
| Rectangle $2a\times 2b$ | through centre, parallel to side $2a$ | $Mb^2/3$ |
| Ring of radius $a$ | axis / diameter | $Ma^2$ / $Ma^2/2$ |
| Disc of radius $a$ | axis / diameter | $Ma^2/2$ / $Ma^2/4$ |
| Solid cylinder (radius $a$, length $\ell$) | axis / ⟂ through centre | $Ma^2/2$ / $M(a^2/4 + \ell^2/12)$ |
| Solid sphere | diameter | $2Ma^2/5$ |
| Spherical shell | diameter | $2Ma^2/3$ |
| Solid cube of edge $a$ | any line through centre | $Ma^2/6$ |
| Solid cube of edge $a$ | an edge | $2Ma^2/3$ |
| Ellipsoid with semi-axes $a,b,c$ | $x$-axis | $M(b^2+c^2)/5$ |
| Elliptic disc with semi-axes $a,b$ | major axis ($x$) | $Mb^2/4$ |

## 2. Principal axes
- These are the eigenvectors of $\mathbf I$, and the principal moments are its eigenvalues, the roots of $\det(\mathbf I - \lambda\mathbf 1) = 0$. Principal axes exist at **every** point.
- Along a principal axis all products of inertia vanish and $\vec L \parallel \vec\omega$.
- **Symmetry rules:**
  - an axis of symmetry is principal;
  - a normal to a plane of symmetry is principal at every point of that plane;
  - isotropic bodies (sphere, cube) about their centre have every axis principal.
- **Lamina in the $xy$-plane:** the principal axes in the plane are at angle $\theta$ with $\tan 2\theta = \dfrac{2F}{B - A}$, where $F = \int xy\thinspace dm$ and $A = \int y^2\thinspace dm$, $B = \int x^2\thinspace dm$. Check the sign convention used in your textbook.
- **Equimomental bodies** have the same mass, centre of mass and principal moments and axes. Example: a uniform triangle is equimomental with masses $M/3$ at the midpoints of its sides.

## 3. Angular momentum and kinetic energy
- $\vec L = \mathbf I\vec\omega$. In principal axes $\vec L = (A\omega_1, B\omega_2, C\omega_3)$.
- $T = \tfrac12\vec\omega\cdot\vec L = \tfrac12(A\omega_1^2 + B\omega_2^2 + C\omega_3^2)$.
- For general motion, $T = \tfrac12 Mv_G^2 + \tfrac12\vec\omega\cdot\mathbf I_G\vec\omega$ (König's theorem).

## 4. Euler's dynamical equations
For body-fixed principal axes, with the origin at a fixed point or at **G**, $\left(\dfrac{d\vec L}{dt}\right)_{\text{body}} + \vec\omega\times\vec L = \vec N$:
$$A\dot\omega_1 - (B - C)\thinspace \omega_2\omega_3 = N_1,\quad B\dot\omega_2 - (C - A)\thinspace \omega_3\omega_1 = N_2,\quad C\dot\omega_3 - (A - B)\thinspace \omega_1\omega_2 = N_3 .$$
(The indices are cyclic: $1\to2\to3$ together with $A\to B\to C$.)

### Torque-free motion ($\vec N = 0$)
- **Integrals:** $2T = A\omega_1^2 + B\omega_2^2 + C\omega_3^2$ and $L^2 = A^2\omega_1^2 + B^2\omega_2^2 + C^2\omega_3^2$ are constant, and $\vec L$ is fixed in space.
- **Symmetric body $A = B$:**
  - $\omega_3 = n$ is constant;
  - $\omega_1 + i\omega_2 = \omega_\perp e^{i\Omega t}$ with $\Omega = \dfrac{(C - A)n}{A}$;
  - so $\vec\omega$ precesses about the symmetry axis (relative to the body) with period $2\pi/|\Omega|$;
  - for Earth $(C - A)/A \approx 1/305$, giving the Euler period of about 305 days (observed as the Chandler wobble, about 430 days).
- **Poinsot construction:** the inertia ellipsoid rolls without slipping on the **invariable plane** (normal to $\vec L$). The curve traced on the ellipsoid is the polhode; the curve traced on the plane is the herpolhode.
- **Stability:** rotation about the axis of **largest or smallest** moment is stable, and about the **intermediate** axis it is unstable (tennis-racket theorem). The reason is that $\ddot\omega_2 \propto (C - A)(A - B)\thinspace \omega_2$.

### Euler angles $(\phi, \theta, \psi)$
- $\omega_1 = \dot\phi\sin\theta\sin\psi + \dot\theta\cos\psi$
- $\omega_2 = \dot\phi\sin\theta\cos\psi - \dot\theta\sin\psi$
- $\omega_3 = \dot\phi\cos\theta + \dot\psi$
- **Heavy symmetric top:** $L = \tfrac12 A(\dot\theta^2 + \dot\phi^2\sin^2\theta) + \tfrac12 C(\dot\psi + \dot\phi\cos\theta)^2 - Mgl\cos\theta$. Here $\phi$ and $\psi$ are cyclic, so $p_\phi$ and $p_\psi$ are conserved.
- **Sleeping top** is stable if $C^2\omega_3^2 \gt  4AMgl$.

## Exam traps
- In Euler's equations, the coefficient of $\omega_2\omega_3$ is $(B - C)$ with a **minus** sign on the left.
- $\vec L \parallel \vec\omega$ only along principal axes.
- The parallel-axis theorem uses the axis through **G**, never an arbitrary parallel axis.
- The perpendicular-axis theorem holds **only for laminae**.
- About a cube's centre **every** axis has moment $Ma^2/6$, including the diagonals.
- The intermediate-axis rotation is the unstable one, not the axis with the smallest moment.
- The disc has $Ma^2/2$ about its axis but $Ma^2/4$ about a diameter. The shell has $2/3$ and the solid sphere $2/5$.
