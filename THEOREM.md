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
