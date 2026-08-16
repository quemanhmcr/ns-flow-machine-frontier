# Research status

## Closed structural chain

Critical dynamics is reduced to fixed Cartan Euler current plus diagonal quadratic heat.  One-step sign monotonicity, a global `10/13` law, a full-Euler companion theorem from Jacobi alone, and a monotone radial Herglotz-phase shortcut are ruled out.  The sharp physical triangle law remains

\[
M^2F_{\log}\le Q_\triangle.
\]

## Current frontier

The minimal critical action is

\[
\boxed{
\mathcal A_K=\frac{\kappa^2}{KM_3},\qquad
(\log K)'=\frac1{2\nu}\left[\mathcal A_K-
\frac{(\kappa-2\nu M_3)^2}{KM_3}\right].
}
\]

For `H_s=e^{-s Lambda^2}`, the covariance stress

\[
\tau_s=H_s(u\otimes u)-H_su\otimes H_su\succeq0
\]

obeys the exact Germano cocycle and Loewner heat law.  They produce an intrinsic positive cost `mathfrak C(u)` satisfying

\[
\boxed{\mathcal A_K\le (2\sqrt{2\pi})^{-1}\,\mathfrak C(u)/M_3.}
\]

## Remaining theorem

It is sufficient to prove

\[
\boxed{\int_0^T\mathfrak C(u(t))/M_3(t)\,dt<\infty.}
\]

Scale composition is already positive; the sole current seam is cutoff-independent control of **physical-time covariance regeneration toward zero heat depth** by the actual Cartan/Jacobi current.  Energy dissipation alone is insufficient by scaling.  No global-regularity claim is made until this estimate is proved.

## Sharpened torsion/conjugate route

A new exact full-state sharpening is

\[
\boxed{2\kappa=\langle u,N_J(u,\Lambda u)\rangle,\qquad
\mathcal A_K\le \mathcal T_J:=
\frac{\|\Lambda^{-1/2}N_J(u,\Lambda u)\|_2^2}{4M_3}.}
\]

The Cartan strain `S_u=[J_u,C]` satisfies `F_E=S_u u`; its heat incompatibility is expressed by the curl-Nijenhuis tensor `N_C`.  On backward heat tents, an adjoint/conjugate equation removes the inherited residual term `DF_E(U_s) R_s` exactly, leaving only fresh two-step regeneration and Euler/heat curvature.  Thus `int T_J dt < infinity` is a new sufficient **candidate route**, not a proved estimate.  See `docs/07-torsion-conjugate-frontier.md`.
