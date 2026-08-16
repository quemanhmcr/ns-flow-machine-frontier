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

## Dephasing spectral endgame

On finite periodic curl cutoffs, the helicity-pair amplifier
\[
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1}
\]
obeys the exact forced dephasing equation
\[
\partial_t\mathbb B=\nu\mathcal L_{dep}\mathbb B+\mathbb B_{F_E}.
\]
For `R=(mathbb B-I)_+` and `Theta=Tr R^2`, one has
\[
\boxed{\dot\Theta+\nu\mathcal I_\Theta=2\operatorname{Tr}(R\nabla_E\mathbb B),\qquad \mathcal I_\Theta\ge0,}
\]
where `nabla_E mathbb B=mathbb B_F+[A_u,mathbb B]`; the commutator term is isospectral and vanishes from the trace.  Jacobi reduces `nabla_E mathbb B` to quadratic curl curvature/Nijenhuis composition, so bare one-step regeneration is absent from the endgame.  The two remaining open gates are a curvature-memory absorption estimate and an infrared no-collapse lemma.  See `docs/08-dephasing-spectral-endgame.md`.

## Independent flow-machine branch

Further work on the Bogoliubov/dephasing route is now isolated in `quemanhmcr/ns-flow-machine-frontier`.  The first new result is the scalar finite-cutoff inequality
\[
\boxed{
\dot\Theta+\nu\frac{(\Theta+\Phi)^2}{\mathcal H_{IR}}
\le\frac{\mathcal H_{mem}}\nu,
}
\]
which separates the remaining problem into an infrared susceptibility gate and a fresh Cartan/Jacobi curvature-memory gate.  See `docs/09-critical-dephasing-flow-machine.md`.
