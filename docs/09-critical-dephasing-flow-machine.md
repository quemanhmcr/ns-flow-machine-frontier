# 09 — Critical dephasing flow machine

This note belongs to the independent `ns-flow-machine-frontier` branch.  It records only finite periodic cutoff identities that have been algebraically audited.  The continuum memory estimate remains open.

## 1. Forced dephasing normal form

Let
\[
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1},\qquad A_u=\operatorname{ad}_u,
\]
and, in a Fourier-helicity cutoff basis, let `X_j e_k=k_j e_k`.  Put
\[
L:=-\mathcal L_{dep}=\sum_{j=1}^3[X_j,[X_j,\cdot]]\ge0.
\]
Mean-zero velocity implies that `mathbb B_u` has no zero-carrier matrix component.  Quadratic heat acts exactly by dephasing,
\[
\boxed{\partial_t\mathbb B=-\nu L\mathbb B+\mathbb B_{F_E}.}
\]
Thus inherited pair amplification is only dephased; new amplification enters only through the actual quadratic Cartan current `F_E`.

## 2. Supercritical entropy

Set
\[
R=(\mathbb B-I)_+,\qquad
\Theta=\operatorname{Tr}R^2,\qquad
\Phi=\operatorname{Tr}R.
\]
At threshold-regular times,
\[
\boxed{\dot\Theta+\nu\mathcal I_\Theta=2\operatorname{Tr}(R\mathbb B_{F_E}),}
\]
where spectral differentiation gives `mathcal I_Theta>=0` and, more concretely,
\[
\boxed{\mathcal I_\Theta\ge2D_R,\qquad
D_R:=\sum_j\|[X_j,R]\|_{HS}^2.}
\]
Also, because `R(B-I)=R^2` on the supercritical spectral subspace,
\[
\boxed{\operatorname{Tr}(R\mathbb B)=\Theta+\Phi.}
\]

## 3. Infrared susceptibility: a cutoff-safe Nash inequality

Since `mathbb B` has no zero carrier, define
\[
\mathcal H_{IR}(u):=
\langle\mathbb B,L^{-1}\mathbb B\rangle_{HS}.
\]
Writing `Q=L^{-1}mathbb B` and integrating by parts in the operator Dirichlet form,
\[
\Theta+\Phi
=\langle R,LQ\rangle_{HS}
=\sum_j\langle[X_j,R],[X_j,Q]\rangle_{HS}.
\]
Hence
\[
(\Theta+\Phi)^2\le D_R\,\mathcal H_{IR}.
\]
Together with `mathcal I_Theta>=2D_R`, this yields
\[
\boxed{
\mathcal I_\Theta\ge
\frac{2(\Theta+\Phi)^2}{\mathcal H_{IR}}.
}
\]
Unlike a torus spectral-gap estimate, this uses the exact inverse carrier Laplacian and therefore identifies the true infrared susceptibility rather than hiding it in a cutoff-dependent constant.

## 4. Fresh-memory absorption

The Euler current has zero spatial mean, so `mathbb B_{F_E}` also lies in the carrier-mean-zero range of `L`.  Define
\[
\mathcal H_{mem}(u):=
\langle\mathbb B_{F_E},L^{-1}\mathbb B_{F_E}\rangle_{HS}.
\]
Then
\[
2|\operatorname{Tr}(R\mathbb B_{F_E})|
\le2\sqrt{D_R\mathcal H_{mem}}
\le\sqrt{2\mathcal I_\Theta\mathcal H_{mem}}.
\]
Young's inequality with the physical viscosity gives the exact absorption
\[
\boxed{
2\operatorname{Tr}(R\mathbb B_{F_E})
\le \frac\nu2\mathcal I_\Theta+
\frac1\nu\mathcal H_{mem}.
}
\]
Consequently
\[
\boxed{
\dot\Theta+
\nu\frac{(\Theta+\Phi)^2}{\mathcal H_{IR}}
\le
\frac{\mathcal H_{mem}}{\nu}.
}
\]
This is the current scalar flow-machine inequality.  It unifies the two previous open gates: infrared collapse is isolated in `mathcal H_IR`, while genuine physical-time regeneration is isolated in `mathcal H_mem`.

## 5. Structural meaning and guards

`mathcal H_IR` and `mathcal H_mem` are full-state carrier-resolvent quadratic forms.  They are not sums of positive triad occurrences.  No norm of the raw first-order connection `A_u` is introduced.

The estimate is not yet a proof.  In particular, replacing `mathcal H_mem` by a generic Sobolev bound for `F_E` would lose the Cartan/Jacobi advantage and is not an accepted closure.  The next task is to rewrite the secular part of `mathbb B_{F_E}` through the Bianchi-Riccati/Nijenhuis identities before estimating it.  The infrared task is to show that large `mathcal H_IR` forces a rigid low-carrier/affine model that is paid by quadratic heat (Kelvin-type accumulated wave-number growth or an equivalent intrinsic mechanism).

## 6. Isolated-triad calibration

For one heterochiral Cartan block with signed curl eigenvalues `(-a,b,c)`, `a,b,c>0`, the unique positive singular value `s` of the pair amplifier obeys
\[
\boxed{
\frac d{dt}s^2\Big|_{Euler}
=\frac{\kappa_\triangle}{\nu^2abc}.
}
\]
Thus a single triad is not isospectral: it can regenerate pair gain.  The inverse product `1/(abc)` shows explicitly that the spectral source is already resolvent weighted.  This rules out the tempting but false claim that only multi-triad diamonds can move the amplifier spectrum; Jacobi is needed to control coherent continuation, not to create the first spectral derivative.
