# 01 — From Navier–Stokes to the Two Physical Roads

Start with

\[
\partial_tu+(u\cdot\nabla)u+\nabla p=\nu\Delta u,
\qquad \nabla\cdot u=0.
\]

For \(\omega=\operatorname{curl}u\),

\[
(u\cdot\nabla)u
=\nabla\frac{|u|^2}{2}-u\times\omega.
\]

The Leray projector removes the exact gradient, so with

\[
C=\operatorname{curl},
\qquad
J_uv=\mathbb P(u\times v),
\]

we obtain

\[
\boxed{u_t=J_uCu-\nu C^2u.}
\]

Because \(J_u\) is skew-adjoint, the Euler road is reversible at the quadratic-energy level. Since \(C^2=-\Delta\) on divergence-free fields, the viscous road is positive quadratic heat.

Center the signed curl using

\[
\lambda=H/E,
\qquad
H=\langle u,Cu\rangle,
\qquad
E=\|u\|_2^2,
\]

and

\[
r=(C-\lambda)u.
\]

Since \(J_uu=0\),

\[
\boxed{u_t=J_ur-\nu C^2u.}
\]

This is the ontology boundary of the repository. Any later coordinate system is only a reading of these same two roads.
