# The Remaining Positive-Composition Theorem

## Setting

Let \(u\) be a smooth mean-zero divergence-free Navier–Stokes velocity field on a periodic domain or on \(\mathbb R^3\) with sufficient decay:

\[
u_t=J_uCu-\nu C^2u,
\qquad
J_uv=\mathbb P(u\times v),
\qquad
C=\operatorname{curl}.
\]

Define

\[
E=\|u\|_2^2,
\quad
Z=\|Cu\|_2^2,
\quad
\Lambda=|C|,
\quad
K=\langle u,\Lambda u\rangle,
\quad
N^2=Z/E,
\]

\[
F_E=J_uCu,
\qquad
\kappa=\langle\Lambda u,F_E\rangle,
\qquad
s=(\Lambda-K/E)u.
\]

Then

\[
\|s\|_2^2=\frac{EZ-K^2}{E}
\]

and the exact normalized critical-uphill action is

\[
\boxed{
\mathcal A_{\mathrm{escape}}(u)
=
\frac{\kappa^2}{N^2(EZ-K^2)}
=
\left|
\left\langle
\widehat\omega,
\widehat s\times u
\right\rangle
\right|^2.
}
\]

## Already proved direction

The completed-square estimate gives

\[
\frac d{dt}\log\frac KE
\le \frac{1}{2\nu}\mathcal A_{\mathrm{escape}}(u),
\]

hence

\[
\boxed{
K/E\to\infty
\Longrightarrow
\int_0^T\mathcal A_{\mathrm{escape}}(u(t))\,dt=\infty.
}
\]

## Open theorem

Prove, using only intrinsic Navier–Stokes structure, that on every finite smooth positive-energy interval

\[
\boxed{
\int_0^T
\frac{\kappa(t)^2}
{N(t)^2\,[E(t)Z(t)-K(t)^2]}
\,dt<\infty.
}
\]

Equivalently,

\[
\boxed{
\int_0^T
\left|
\left\langle
\widehat\omega,
\widehat{(\Lambda-K/E)u}\times u
\right\rangle
\right|^2dt<\infty.
}
\]

This would close the **critical-escape gap represented by \(K/E\)**. It is not asserted here to be, by itself, a complete proof of global regularity.

## Required mechanism

The theorem must be obtained through a representation-free positive composition principle. The currently exact ingredients are:

1. fixed Cartan Euler tensor plus diagonal heat;
2. no one-step sign monotone;
3. invariant-constrained Euler acceleration with tangent turning left free;
4. actual two-step signed-curl gaps;
5. bracket-level weighted Jacobi compatibility;
6. Fourier comparable-carrier location geometry;
7. Galilean nullity at low carrier frequency;
8. quadratic heat \(\nu|m|^2\) on every nonzero carrier;
9. sharp occurrence-wise law \(M^2F_{\log}\le Q_\triangle\).

The missing implication is schematically

\[
\boxed{
\text{persistent nontrivial log continuation}
\Longrightarrow
\text{intrinsic non-cancelling heat-visible historical cost}.
}
\]

The cost must be defined from the full PDE state/current, not from a positive-part sum over a chosen triad representation.

---

## Current minimal frontier: heat-depth positive composition

The earlier `K/E` and Krylov/Ritz statements remain valid stronger diagnostics, but the current sufficient target is smaller.  Since

\[
K'=2\kappa-2\nu M_3,
\qquad M_3=\langle u,\Lambda^3u\rangle,
\]

\[
\boxed{
(\log K)'=\frac1{2\nu}\left[
\mathcal A_K-\frac{(\kappa-2\nu M_3)^2}{KM_3}
\right],
\qquad
\mathcal A_K:=\frac{\kappa^2}{KM_3}.
}
\]

Thus `int_0^T A_K dt < infinity` is sufficient to bound the critical norm `K`.

Let

\[
H_s=e^{-s\Lambda^2},\quad U_s=H_su,\quad
\tau_s=H_s(u\otimes u)-U_s\otimes U_s\succeq0,
\]

and

\[
D_s=E-\|U_s\|_2^2,\quad
R_s=Z-\|\Lambda U_s\|_2^2,\quad
W_s=\int\tau_s:\nabla U_s\,dx.
\]

With `c0=(2 sqrt(2 pi))^(-1)`, Balakrishnan gives the common-depth identities

\[
\boxed{
K=c_0\int s^{-3/2}D_s\,ds,\qquad
M_3=c_0\int s^{-3/2}R_s\,ds,\qquad
\kappa=-c_0\int s^{-3/2}W_s\,ds,
}
\]

where all heat-depth integrals are over `(0,infinity)`.  At each depth,

\[
\boxed{\partial_tD_s=-2W_s-2\nu R_s.}
\]

Set `A_s=nabla U_s` and

\[
\mathscr B_s=\int\operatorname{tr}(A_s^T\tau_sA_s)\,dx\ge0.
\]

Then

\[
\boxed{|W_s|^2\le D_s\mathscr B_s.}
\]

The stress obeys the exact Loewner/Germano laws

\[
\boxed{
\partial_s\tau_s=\Delta\tau_s+2A_sA_s^T,
\qquad
\tau_{s+t}(u)=H_t\tau_s(u)+\tau_t(H_su).
}
\]

If `V_s=||tau_s||_2^2` and `G_s=||nabla tau_s||_2^2`, then

\[
\mathscr B_s=\frac14V_s'+\frac12G_s.
\]

Hence the intrinsic positive composition cost

\[
\boxed{
\mathfrak C(u):=\int s^{-3/2}\mathscr B_s\,ds
=\frac38\int s^{-5/2}V_s\,ds
+\frac12\int s^{-3/2}G_s\,ds
}
\]

satisfies, after assembling the full current before Cauchy,

\[
\boxed{\mathcal A_K\le c_0\,\mathfrak C(u)/M_3.}
\]

The Germano cocycle is genuinely positive across heat depth:

\[
\boxed{
\|\tau_{s+t}(u)\|_2^2\ge
\|H_t\tau_s(u)\|_2^2+\|\tau_t(H_su)\|_2^2.
}
\]

### Remaining theorem

It is now sufficient to prove

\[
\boxed{
\int_0^T\frac{\mathfrak C(u(t))}{M_3(t)}\,dt<\infty.
}
\]

Heat-depth composition is already positive.  The unresolved step is cutoff-independent control of how the **actual Cartan/Jacobi Euler current** regenerates covariance toward `s=0` in physical time.  Ordinary energy dissipation alone cannot supply this critical bound by scaling.  No global-regularity claim is made until this estimate is proved.

### Intrinsic torsion sharpening

For `J=sgn C`, let `N_J(a,b)=[Ja,Jb]-J[Ja,b]-J[a,Jb]+[a,b]`.  The full helicity-Nijenhuis torsion gives the exact identity

\[
\boxed{\langle u,N_J(u,\Lambda u)\rangle=2\kappa}
\]

and therefore the representation-free sufficient majorant

\[
\boxed{
\mathcal A_K\le
\mathcal T_J(u):=
\frac{\|\Lambda^{-1/2}N_J(u,\Lambda u)\|_2^2}{4M_3}.
}
\]

Thus `int_0^T T_J dt < infinity` would also close the minimal critical-action gap.  This historical torsion estimate is open.  The candidate mechanism uses the curl-Nijenhuis heat defect of `S_u=[J_u,C]` together with a backward-tent conjugate identity that removes inherited residual transport before any absolute values are taken; see `docs/07-torsion-conjugate-frontier.md`.

### Finite-cutoff spectral-flow reduction

A sharper **open endgame reduction**, presently justified on finite periodic curl cutoffs, uses
\[
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1},\qquad
\Theta=\operatorname{Tr}(\mathbb B-I)_+^2.
\]
It satisfies
\[
\boxed{
\partial_t\mathbb B=\nu\mathcal L_{dep}\mathbb B+\mathbb B_{F_E},\qquad
\dot\Theta+\nu\mathcal I_\Theta=2\operatorname{Tr}((\mathbb B-I)_+\nabla_E\mathbb B),
}
\]
with `mathcal I_Theta >= 0` and `nabla_E mathbb B=mathbb B_F+[A_u,mathbb B]`.  The isospectral commutator does not contribute to the spectral entropy, while Jacobi/Bianchi identities force the remaining secular source to start at genuine curl-curvature/Nijenhuis order.  Closing a curvature-memory absorption estimate plus an infrared no-collapse lemma would turn this reduction into a bound on persistent supercritical occupation.  Neither estimate is proved; see `docs/08-dephasing-spectral-endgame.md`.
