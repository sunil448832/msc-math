# Cheatsheet · Unit 8 · Topic 05 — Fluid Kinematics: Continuity, Velocity Potential, Stream Lines, Vorticity
> Questions: [../Questions/05-Fluid-Kinematics-Continuity-Potential-Vorticity.md](../Questions/05-Fluid-Kinematics-Continuity-Potential-Vorticity.md)

## 1. Descriptions of fluid motion
| | Lagrangian | Eulerian |
|---|---|---|
| Variables | initial label $(a,b,c)$ and $t$; follows a particle | fixed point $(x,y,z)$ and $t$; field description |
| Velocity | $\partial\vec r/\partial t$ at fixed $(a,b,c)$ | $\vec q(\vec r,t)$ |

- **Material (substantial) derivative:** $\dfrac{D}{Dt} = \dfrac{\partial}{\partial t} + \vec q\cdot\nabla$.
- **Acceleration:** $\dfrac{D\vec q}{Dt} = \dfrac{\partial\vec q}{\partial t} + (\vec q\cdot\nabla)\vec q = \dfrac{\partial\vec q}{\partial t} + \nabla\left(\tfrac12q^2\right) - \vec q\times\vec\omega$.
- **Steady flow:** $\partial/\partial t = 0$ at every fixed point. The acceleration can still be non-zero because of the convective term.
- **Uniform flow:** $\vec q$ is independent of position.

## 2. Lines in a flow
- **Streamline** (tangent to $\vec q$ at a fixed instant): $\dfrac{dx}{u} = \dfrac{dy}{v} = \dfrac{dz}{w}$, with $t$ frozen.
- **Pathline:** $\dfrac{d\vec r}{dt} = \vec q(\vec r,t)$, the trajectory of one particle.
- **Streakline:** the locus of particles that passed through a fixed point.
- In **steady** flow these three coincide. In unsteady flow they generally differ (e.g. $u = x/(1+t)$, $v = 1$).
- Streamlines cannot cross except at stagnation points ($\vec q = 0$) or singular points.
- **Stream tube:** the surface formed by streamlines through a closed curve. No fluid crosses its wall.

## 3. Equation of continuity (conservation of mass)
| Form | Equation |
|---|---|
| Vector (Euler) | $\dfrac{\partial\rho}{\partial t} + \nabla\cdot(\rho\vec q) = 0 \iff \dfrac{D\rho}{Dt} + \rho\nabla\cdot\vec q = 0$ |
| Cartesian | $\rho_t + (\rho u)_x + (\rho v)_y + (\rho w)_z = 0$ |
| Cylindrical $(r,\theta,z)$ | $\rho_t + \dfrac1r\dfrac{\partial(r\rho q_r)}{\partial r} + \dfrac1r\dfrac{\partial(\rho q_\theta)}{\partial\theta} + \dfrac{\partial(\rho q_z)}{\partial z} = 0$ |
| Spherical $(r,\theta,\phi)$ | $\rho_t + \dfrac{1}{r^2}\dfrac{\partial(r^2\rho q_r)}{\partial r} + \dfrac{1}{r\sin\theta}\dfrac{\partial(\sin\theta\,\rho q_\theta)}{\partial\theta} + \dfrac{1}{r\sin\theta}\dfrac{\partial(\rho q_\phi)}{\partial\phi} = 0$ |
| Lagrangian | $\rho J = \rho_0$, with $J = \dfrac{\partial(x,y,z)}{\partial(a,b,c)}$ |
| Incompressible | $D\rho/Dt = 0 \iff \nabla\cdot\vec q = 0$ |
| Steady | $\nabla\cdot(\rho\vec q) = 0$ |

- Purely radial incompressible flow: in 3-D $q_r \propto 1/r^2$; in 2-D $q_r \propto 1/r$.
- **Possible motion test** for an incompressible fluid: check $\nabla\cdot\vec q = 0$. Also check the boundary condition $\dfrac{DF}{Dt} = 0$ on a moving surface $F(\vec r,t) = 0$, i.e. $\dfrac{\partial F}{\partial t} + \vec q\cdot\nabla F = 0$.

## 4. Velocity potential and irrotational flow
- **Vorticity** $\vec\omega = \nabla\times\vec q$, equal to twice the local angular velocity. In 2-D, $\zeta = v_x - u_y$.
- **Irrotational:** $\nabla\times\vec q = 0$. On a simply connected domain this gives $\vec q = -\nabla\phi$, the convention used in most Indian texts (Raisinghania, Shanti Swarup); many Western texts use $+\nabla\phi$.
- Incompressible and irrotational gives **Laplace's equation** $\nabla^2\phi = 0$.
- Irrotational does **not** imply incompressible: $\vec q = (x,y)$ is irrotational with divergence 2. Incompressible does not imply irrotational either: rigid rotation.
- **Circulation:** $\Gamma = \oint_C\vec q\cdot d\vec r = \iint_S\vec\omega\cdot d\vec S$ (Stokes). Irrotational flow in a simply connected region gives $\Gamma = 0$.
- A multiply connected region allows a **cyclic** (many-valued) potential. Example: the line vortex $\phi = -\tfrac{\Gamma}{2\pi}\theta$ has $\Gamma \ne 0$ although $\nabla\times\vec q = 0$ for $r > 0$.
- **Equipotentials** $\phi = $ const are orthogonal to the streamlines.
- **Classic 3-D example:** $u = -\dfrac{2xyz}{(x^2+y^2)^2}$, $v = \dfrac{(x^2-y^2)z}{(x^2+y^2)^2}$, $w = \dfrac{y}{x^2+y^2}$. It is a possible incompressible motion and it is irrotational, with $\phi = \pm\dfrac{yz}{x^2+y^2}$.

## 5. Stream function (2-D incompressible)
- Convention 1: $u = -\partial\psi/\partial y$, $v = \partial\psi/\partial x$ (Milne-Thomson / Indian texts, paired with $\vec q = -\nabla\phi$). Convention 2: $u = \partial\psi/\partial y$, $v = -\partial\psi/\partial x$.
- In either convention: continuity holds automatically; speed $= |\nabla\psi|$; $\psi = $ const are the streamlines; $\zeta = \pm\nabla^2\psi$.
- **Flux** between two streamlines $= \psi_2 - \psi_1$.
- Irrotational flow gives $\nabla^2\psi = 0$, and $\phi$, $\psi$ are harmonic conjugates. With $w = \phi + i\psi$: $\phi_x = \psi_y$ and $\phi_y = -\psi_x$ (Cauchy–Riemann).
- **Stokes stream function** (axisymmetric 3-D): $q_r = -\dfrac{1}{r^2\sin\theta}\dfrac{\partial\psi}{\partial\theta}$, $q_\theta = \dfrac{1}{r\sin\theta}\dfrac{\partial\psi}{\partial r}$ (sign convention varies).

## 6. Vortex kinematics
- **Vortex line:** tangent to $\vec\omega$, $\dfrac{dx}{\omega_x} = \dfrac{dy}{\omega_y} = \dfrac{dz}{\omega_z}$. A vortex tube is formed from vortex lines.
- **Strength** of a vortex tube $= \iint\vec\omega\cdot d\vec S$, which is the same along the tube because $\nabla\cdot\vec\omega = 0$. Vortex tubes cannot end inside the fluid.
- **Forced vortex** (rigid rotation $q_\theta = \Omega r$) has vorticity $2\Omega$. **Free vortex** ($q_\theta = k/r$) is irrotational for $r > 0$ and has $\Gamma = 2\pi k$.

## 7. Quick examples
| Flow | Streamlines | Div | Curl |
|---|---|---|---|
| $(x, -y)$ | $xy = c$ | 0 | 0 |
| $(x, y)$ | radial lines | 2 | 0 |
| $(-\Omega y, \Omega x)$ | circles | 0 | $2\Omega$ |
| $(-y, x)/r^2$ | circles | 0 | 0 for $r \ne 0$ |
| $(y, 0)$ (shear) | lines $y = c$ | 0 | $-1$ |

## Exam traps
- Vorticity is **twice** the angular velocity.
- A steady flow can still have non-zero acceleration.
- For a streamline you integrate with $t$ frozen; for a pathline you integrate in $t$. They differ for unsteady flow.
- Check sign conventions for $\phi$ and $\psi$. Magnitudes (speed, flux, $|\zeta|$) do not depend on the convention.
- A non-zero circulation round a singular point is compatible with irrotational flow away from that point.
- Radial flux: 3-D gives $1/r^2$, 2-D gives $1/r$.
- In the incompressible condition use $\nabla\cdot\vec q = 0$, not $\nabla\times\vec q = 0$.
