# Cheatsheet · Unit 8 · Topic 01 — Generalised Coordinates, Lagrange's Equations, Hamilton's Principle
> Questions: [../Questions/01-Generalised-Coordinates-Lagrange-Hamilton-Principle.md](../Questions/01-Generalised-Coordinates-Lagrange-Hamilton-Principle.md)

## 1. Constraints and degrees of freedom
| Type | Definition | Example |
|---|---|---|
| Holonomic | can be written as $f(\vec r_1,\dots,\vec r_N,t)=0$ | rigid body, pendulum $x^2+y^2=\ell^2$ |
| Non-holonomic | not expressible as such (inequalities, non-integrable velocity relations) | disc rolling on a plane, gas in a box ($r\le a$) |
| Scleronomic | no explicit $t$ | fixed wire |
| Rheonomic | explicit $t$ | bead on a rotating wire or a moving support |
| Bilateral / unilateral | equality / inequality | rod vs. string (can slacken) |
| Conservative / dissipative | constraint forces do no work / do work | smooth vs. rough surface |

- **Degrees of freedom** $= 3N - k$ for $N$ particles with $k$ independent holonomic constraints.
- Standard counts: free particle 3; particle on a surface 2; simple pendulum 1; spherical pendulum 2; double pendulum (plane) 2; rigid dumbbell in space 5, in a plane 3; **free rigid body 6**; rigid body with one point fixed 3; rigid body with an axis fixed 1.
- Rolling without slipping: a **sphere/disc on a plane** is non-holonomic; a **cylinder rolling on a line** is holonomic ($x = a\theta$ integrates).

## 2. Generalised coordinates and generalised forces
- $\vec r_i = \vec r_i(q_1,\dots,q_n,t)$. Virtual displacement: $\delta\vec r_i = \sum_j \dfrac{\partial\vec r_i}{\partial q_j}\delta q_j$ (with $\delta t = 0$).
- **Generalised force:** $Q_j = \sum_i \vec F_i\cdot\dfrac{\partial\vec r_i}{\partial q_j}$. Conservative case: $Q_j = -\partial V/\partial q_j$. Its dimension is [work]/[$q_j$]; for an angle, $Q_\theta$ is a **torque**.
- Identities used to derive Lagrange's equations: $\dfrac{\partial\dot{\vec r}_i}{\partial\dot q_j} = \dfrac{\partial\vec r_i}{\partial q_j}$ ("cancellation of dots") and $\dfrac{d}{dt}\dfrac{\partial\vec r_i}{\partial q_j} = \dfrac{\partial\dot{\vec r}_i}{\partial q_j}$.
- $T = T_2 + T_1 + T_0$ (homogeneous of degree 2, 1, 0 in $\dot q$). For scleronomic constraints $T = T_2$.

## 3. Principles
- **Virtual work (statics):** $\sum \vec F^{(a)}_i\cdot\delta\vec r_i = 0$.
- **D'Alembert:** $\sum(\vec F^{(a)}_i - \dot{\vec p}_i)\cdot\delta\vec r_i = 0$, valid for workless constraints.
- **Lagrange's equations:** $\dfrac{d}{dt}\dfrac{\partial T}{\partial\dot q_j} - \dfrac{\partial T}{\partial q_j} = Q_j$. With $L = T - V$:
$$\frac{d}{dt}\frac{\partial L}{\partial\dot q_j} - \frac{\partial L}{\partial q_j} = 0 .$$
- **Velocity-dependent potential** $U(q,\dot q,t)$ with $Q_j = -\dfrac{\partial U}{\partial q_j} + \dfrac{d}{dt}\dfrac{\partial U}{\partial\dot q_j}$. Charged particle: $U = e\phi - e\vec v\cdot\vec A$, so $L = \tfrac12 mv^2 - e\phi + e\vec v\cdot\vec A$ and $\vec p = m\vec v + e\vec A$.
- **Dissipation (Rayleigh):** $\mathcal F = \tfrac12\sum k_j\dot q_j^2$, giving $\dfrac{d}{dt}\dfrac{\partial L}{\partial\dot q_j} - \dfrac{\partial L}{\partial q_j} + \dfrac{\partial\mathcal F}{\partial\dot q_j} = 0$.
- **Hamilton's principle:** among all paths with fixed end points $q(t_1), q(t_2)$, the actual motion makes the action $S = \int_{t_1}^{t_2}L\,dt$ **stationary** (not necessarily a minimum). This holds for holonomic systems with $L$ derivable from a (generalised) potential.
- **Euler–Lagrange** for $\int F(x,y,y')dx$: $\dfrac{\partial F}{\partial y} - \dfrac{d}{dx}\dfrac{\partial F}{\partial y'} = 0$.
  - If $F$ has no $y$: $\partial F/\partial y' = $ const.
  - If $F$ has no $x$ (Beltrami): $F - y'\,\partial F/\partial y' = $ const.
- Classic extremals: shortest path in a plane gives a **straight line**; geodesic on a sphere is a **great circle**; brachistochrone is a **cycloid**; minimum surface of revolution is a **catenary**; isoperimetric problem gives a **circle**.

## 4. Non-uniqueness of $L$
- $L' = L + \dfrac{dF(q,t)}{dt}$ and $L' = \lambda L$ ($\lambda\ne 0$) give the same equations of motion.
- Lagrange's equations are **form-invariant** under point transformations $Q = Q(q,t)$.

## 5. Cyclic coordinates and conservation laws
- **Generalised momentum** $p_j = \partial L/\partial\dot q_j$. If $q_j$ is **cyclic** (absent from $L$) then $p_j$ is conserved.
- Noether's correspondence:

| Symmetry of $L$ | Conserved quantity |
|---|---|
| Translation along $\hat n$ | $\vec P\cdot\hat n$ (linear momentum) |
| Rotation about $\hat n$ | $\vec L\cdot\hat n$ (angular momentum) |
| No explicit $t$ | Jacobi integral $h$ |
| $V(x - y)$ only (relative coordinate) | total momentum $p_x + p_y$ |

- **Jacobi integral (energy function):** $h = \sum\dot q_j\,\partial L/\partial\dot q_j - L$, with $\dfrac{dh}{dt} = -\dfrac{\partial L}{\partial t}$.
  - $h = T_2 - T_0 + V$ in general.
  - $h = T + V = E$ **only if** $T$ is homogeneous quadratic (scleronomic) **and** $V$ does not depend on velocity.
- **Central force:** $L = \tfrac12 m(\dot r^2 + r^2\dot\theta^2) - V(r)$. Here $\theta$ is cyclic, so $p_\theta = mr^2\dot\theta = $ const (Kepler's 2nd law, areal velocity $h/2$).

## 6. Standard worked systems
| System | Lagrangian / result |
|---|---|
| Atwood machine | $(m_1+m_2)\ddot x = (m_1-m_2)g$ |
| Simple pendulum | $\ddot\theta + (g/\ell)\sin\theta = 0$ |
| Spherical pendulum | $L = \tfrac12 m\ell^2(\dot\theta^2 + \sin^2\theta\,\dot\phi^2) + mg\ell\cos\theta$; $\phi$ is cyclic |
| Bead on a hoop rotating at $\omega$ | $\ddot\theta = \sin\theta(\omega^2\cos\theta - g/a)$; equilibrium $\cos\theta_0 = g/(a\omega^2)$ exists iff $\omega^2 > g/a$; small-oscillation frequency $\omega\sin\theta_0$ |
| Caldirola–Kanai | $L = e^{\gamma t}(\tfrac12 m\dot q^2 - \tfrac12 kq^2)$ gives $m\ddot q + \gamma m\dot q + kq = 0$ |
| Bead on a rotating straight wire | $\ddot r = \omega^2 r$, so $r = Ae^{\omega t} + Be^{-\omega t}$ |

## Exam traps
- A rheonomic constraint can still be **holonomic** (rotating wire, moving pendulum support).
- $h \ne E$ for rotating or driven systems. Even then, $h$ is conserved whenever $\partial L/\partial t = 0$.
- A generalised momentum need not be $m\dot q$ (charged particle; $p_\theta$ is an angular momentum).
- Hamilton's principle says the action is **stationary**, not minimum.
- A rolling disc on a plane is non-holonomic, but rolling on a straight line is holonomic.
- Count degrees of freedom **after** removing only independent holonomic constraints; non-holonomic constraints do not reduce the number of generalised coordinates.
