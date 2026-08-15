# Navier–Stokes Positive Composition Frontier

A clean, standalone theorem laboratory extracted from one precise research frontier:

> **one-step Euler production may be arbitrarily efficient, but nontrivial repeated scale continuation must compose through the fixed Cartan network and eventually become visible to quadratic heat.**

This repository starts from the Navier–Stokes equation itself and keeps only structures forced by the PDE. It deliberately does **not** import the historical shell/packet/owner/traffic machinery of the earlier research repository.

Status: **structural research frontier; exact identities and falsification guards on smooth solutions; the final positive-composition theorem is open. No global-regularity claim is made.**

## 0. Starting equation

For a smooth mean-zero divergence-free velocity field,

\[
\partial_tu+(u\cdot\nabla)u+\nabla p=\nu\Delta u,
\qquad \nabla\cdot u=0.
\]

Set

\[
C=\operatorname{curl},\qquad C^*=C,\qquad C^2=-\Delta,
\]

\[
\omega=Cu,
\qquad
J_uv=\mathbb P(u\times v),
\qquad J_u^*=-J_u.
\]

Using

\[
(u\cdot\nabla)u=\nabla\frac{|u|^2}{2}-u\times\omega
\]

and applying the Leray projection gives the rotational form

\[
\boxed{u_t=J_uCu-\nu C^2u.}
\]

Define the energy and helicity

\[
E=\|u\|_2^2,
\qquad
H=\langle u,Cu\rangle,
\]

and the centered curl defect

\[
\lambda=H/E,
\qquad
r=(C-\lambda)u.
\]

Since \(J_uu=0\),

\[
\boxed{u_t=J_ur-\nu C^2u.}
\]

This is the primitive two-road grammar of the project:

\[
\boxed{\text{state-generated reversible Cartan/Euler rotation}}
\]

plus

\[
\boxed{\text{one-way diagonal quadratic heat}.}
\]

There is no third physical mechanism in the theorem chain below.

## 1. Fixed Cartan law

Choose a fixed orthonormal curl eigenbasis

\[
Ce_I=\lambda_Ie_I,
\qquad
u=\sum_I z_Ie_I,
\]

and let the fixed alternating Cartan tensor be

\[
f_{IJK}=\Omega(e_I,e_J,e_K).
\]

Then Euler is exactly

\[
\boxed{
\dot z_I^{NL}
=-\frac12\sum_{J,K}(\lambda_K-\lambda_J)f_{IJK}z_Jz_K,
}
\]

while viscosity adds only

\[
\boxed{-\nu\lambda_I^2z_I.}
\]

The rulebook is fixed. State dependence enters only through the amplitudes.

## 2. One-step productivity is not self-frustrating

Let

\[
\Lambda=|C|,
\qquad
K=\langle u,\Lambda u\rangle,
\qquad
F=F_E=J_uCu,
\qquad
\kappa=\langle\Lambda u,F\rangle.
\]

A fixed physical Fourier triad can realize all four sign pairs

\[
(\operatorname{sgn}\kappa,\operatorname{sgn}\kappa'_E)
=(+,+),(+,-),(-,+),(-,-).
\]

So no theorem of the form

\[
\text{productive now}\Longrightarrow\text{immediate sign reversal}
\]

can be primitive.

Euler invariance still fixes the normal acceleration. With

\[
F'=DF_E(u)[F],
\]

one has

\[
\boxed{\langle u,F'\rangle=-\|F\|_2^2,}
\qquad
\boxed{\langle Cu,F'\rangle=-\langle CF,F\rangle.}
\]

If

\[
P_{\operatorname{span}\{u,Cu\}}\Lambda u=a\,u+b\,Cu,
\qquad
g_K=P_T\Lambda u,
\]

then

\[
\boxed{
\kappa'_E
=\langle F,(\Lambda-a-bC)F\rangle
+\langle g_K,P_TF'\rangle.
}
\]

The irreducible freedom is tangent turning \(P_TF'\).

## 3. Continuation begins at the second interaction

A nested Euler path

\[
(J,K)\to M,
\qquad
(I,M)\to L
\]

carries the exact coefficient

\[
\boxed{
(\lambda_K-\lambda_J)(\lambda_M-\lambda_I)
 f_{MJK}f_{LIM}.
}
\]

The intermediate signed-curl scale therefore survives as a **gap**, not as a free label.

At the underlying bracket level, weighted Jacobi gives

\[
\boxed{A+B+C=0,}
\]

hence

\[
\boxed{|A|^2\le2(|B|^2+|C|^2),
\qquad
\max(|B|,|C|)\ge |A|/2.}
\]

But this is only a bracket-level compatibility law. Restoring the full signed-curl gaps can kill both cyclic full-Euler companions while one full continuation remains nonzero.

Therefore:

\[
\boxed{\text{Jacobi companion}\not\Rightarrow\text{comparable full-Euler companion}.}
\]

## 4. Fourier geometry prevents all carriers from hiding at zero scale

For a continuation diamond,

\[
m_1=j+k,
\qquad
m_2=k+i,
\qquad
m_3=i+j,
\qquad
\ell=i+j+k,
\]

one has

\[
\boxed{m_1+m_2+m_3=2\ell,}
\]

so

\[
\boxed{\max_r|m_r|\ge\frac23|\ell|.}
\]

Thus a high-frequency output cannot have all intermediate **locations** at negligible frequency. This does not yet prove nonzero work on the comparable-scale carrier.

Low-frequency sweeping is separately suppressed by the Galilean null, while every nonzero Fourier carrier is damped by

\[
\boxed{\nu|m|^2.}
\]

## 5. No fixed loss per step: the sharp continuous law

For a strict physical heterochiral UV triad, normalize the forward-child radius to \(M\), write donor and side ratios as \(D,S\) with

\[
0<D,S<1,
\qquad
D+S>1,
\]

and let \(R>0\) be the physical current. Define

\[
F_{\log}
=(D+S)R\log\frac1{\max(D,S)},
\]

and

\[
Q_\triangle
=M^2(1-D)(1+S)(D+S)R.
\]

Then on the entire strict physical triangle,

\[
\boxed{M^2F_{\log}\le Q_\triangle.}
\]

The constant \(1\) is sharp at a degenerate limit in which retained transfer tends to \(100\%\) while logarithmic scale progress tends to zero.

Hence the primitive statement is not a fixed loss such as \(10/13\). It is

\[
\boxed{
\text{near-perfect one-step retention}
\Longrightarrow
\text{vanishing one-step logarithmic displacement}.
}
\]

The obstruction is historical: \(Q_\triangle\) is positive for one oriented occurrence, but summing positive occurrence-wise curvature creates a representation-dependent gross traffic budget. The full Nijenhuis curvature is intrinsic but signed.

## 6. Exact escape action

Let

\[
Z=\|Cu\|_2^2,
\qquad
N^2=Z/E,
\]

and define the unique critical-uphill tangent

\[
s=(\Lambda-K/E)u.
\]

Then

\[
\|s\|_2^2=\frac{EZ-K^2}{E},
\qquad
\kappa=\langle s,F_E\rangle.
\]

With global \(L^2\)-normalizations

\[
\widehat s=s/\|s\|_2,
\qquad
\widehat\omega=\omega/\|\omega\|_2,
\]

the normalized escape action is exactly

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

Moreover,

\[
\boxed{
\frac d{dt}\log\frac KE
\le
\frac1{2\nu}\mathcal A_{\mathrm{escape}}(u).
}
\]

Therefore

\[
\boxed{
K/E\to\infty
\Longrightarrow
\int_0^T\mathcal A_{\mathrm{escape}}(u(t))\,dt=\infty.
}
\]

## 7. The one remaining theorem

The project is now concentrated on one statement:

\[
\boxed{
\int_0^T\mathcal A_{\mathrm{escape}}(u(t))\,dt<\infty
}
\]

for every finite smooth positive-energy Navier–Stokes interval in the stated setting.

The intended mechanism is a **representation-free positive composition theorem**:

> persistent nontrivial logarithmic continuation must force enough actual, non-cancelling Cartan/Nijenhuis carrier activity at heat-visible frequencies to produce a finite intrinsic historical budget.

What is forbidden as a proof device:

- summing \(Q_\triangle^+\) over an analyst-chosen triad decomposition;
- assuming one-step sign decay;
- promoting bracket-level Jacobi to a full-Euler companion lower bound;
- using the local \(10/13\) window as a global law;
- replacing the orientation problem by a scalar radial profile that loses phase.

The unresolved loophole is **coherent many-interaction cancellation/recycling**.

See [`THEOREM.md`](THEOREM.md) for the exact frontier and [`docs/`](docs/) for the derivation chain.

## Provenance

This repository is a fresh Git root distilled from the research state whose matching content was identified at

`bc37d3f755d5bb4aa739eeb4801c9f5a1e259507`

in `quemanhmcr/wang-ns-triad-diamond` (Draft PR #6 history).

No Git history was imported. See [`PROVENANCE.md`](PROVENANCE.md).
