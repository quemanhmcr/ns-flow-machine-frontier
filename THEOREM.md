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

## Latest exact reduction: Krylov–Ritz impedance

Normalize `q=u/sqrt(E)` and let `mu` be the spectral measure of `Lambda=|C|` seen from `q`.  On

\[
\mathcal K_n=\operatorname{span}\{q,\Lambda q,\ldots,\Lambda^{n-1}q\},
\]

let `R_n` be the top Ritz value, `v_n=p_n(Lambda)q` its normalized Ritz vector, and

\[
(\Lambda-R_n)v_n=\rho_n e_{n+1}.
\]

If `P_n` is the degree-`n` orthonormal polynomial of `mu`, Ritz orthogonality gives

\[
\boxed{(r-R_n)p_n(r)=\rho_nP_n(r).}
\]

With `f=F_E/sqrt(E)`, define

\[
Q_n(r)=\frac{P_n(r)^2}{r-R_n},
\qquad
b_n=\operatorname{Re}\langle Q_n(\Lambda)q,f\rangle,
\qquad
\beta_n=\langle e_{n+1},\Lambda e_{n+1}\rangle.
\]

Then the Euler boundary speed has the compulsory extra opening `a_n=rho_n b_n`, and the full NS frontier law is

\[
\boxed{R_n'=2\rho_n^2\,[b_n-\nu(R_n+\beta_n)].}
\]

Thus Euler progress and heat use the same quadratic opening.  The canonical frontier polynomial satisfies

\[
\boxed{
\int Q_n\,d\mu=0,\qquad
\int rQ_n\,d\mu=1,\qquad
\int r^2Q_n\,d\mu=R_n+\beta_n.
}
\]

At the critical frontier `n=1`, with

\[
m=K/E,\qquad \sigma^2=Z/E-m^2,
\]

one has

\[
\boxed{
Q_1(r)=\frac{r-m}{\sigma^2},\qquad
b_1=\frac{\operatorname{Cov}_\mu(r,g)}{\operatorname{Var}_\mu(r)},\qquad
m'=2\sigma^2[b_1-\nu(m+\beta)].
}
\]

Here `g` is the actual Euler radial fitness: `Re<h(Lambda)q,f>=int h(r)g(r)dmu`.  Therefore it is sufficient to prove the weaker intrinsic frontier estimate

\[
\boxed{
\int_0^T\frac{\sigma^2}{m}\,[b_1-\nu(m+\beta)]_+\,dt<\infty.
}
\]

This bounds `log(K/E)`.  In the fixed curl basis, `b_n` retains the Cartan/Waleffe cubic symbol and every physical triad contribution is divisible by a same-helicity quadratic-heat difference `r_k^2-r_j^2`; for `n=1` this is the Loewner heat commutator `(Lambda_L+Lambda_R)^(-1)[Lambda^2,J_q]`.  The unresolved step is cutoff-independent control of the coherent super-heat impedance without a gross positive triad budget.
