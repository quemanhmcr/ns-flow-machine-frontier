# 08 — Dephasing spectral endgame

This note records the current finite-cutoff periodic reduction.  The continuum historical estimate remains open.

Let `A_u=ad_u=[u,.]`, `J=sgn C`, and
\[
A_u^\perp=\tfrac12(A_u-JA_uJ).
\]
On the nonzero curl spectral subspace define the helicity-pair amplifier
\[
\boxed{\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1}.}
\]
It is self-adjoint in `g(a,b)=<Lambda^{-1}a,b>` and `J mathbb B J=-mathbb B`.  After the natural heat-clock normalization, critical growth requires occupied spectrum above the fixed threshold `1`.

## 1. Quadratic heat becomes operator dephasing

In a Fourier-helicity cutoff basis, a matrix element of `mathbb B_u` joins carriers `k,l` through the velocity carrier `k-l`. Hence
\[
(\mathbb B_{H_su})_{kl}=e^{-s|k-l|^2}(\mathbb B_u)_{kl}.
\]
With `X_j e_k=k_j e_k`, define
\[
\mathcal L_{dep}B=-\sum_{j=1}^3[X_j,[X_j,B]].
\]
Linearity of `u -> mathbb B_u` gives the exact forced dephasing equation
\[
\boxed{\partial_t\mathbb B=\nu\mathcal L_{dep}\mathbb B+\mathbb B_{F_E(u)}.}
\]
## 2. Supercritical spectral entropy

Set
\[
R=(\mathbb B-I)_+,\qquad
\Theta(\mathbb B)=\operatorname{Tr}R^2,
\qquad
\Phi(\mathbb B)=\operatorname{Tr}R.
\]
At times without threshold eigenvalue `1`, spectral differentiation gives
\[
\boxed{\dot\Theta+\nu\mathcal I_\Theta
=2\operatorname{Tr}(R\mathbb B_{F_E}).}
\]
If `mathbb B e_a=beta_a e_a`, then
\[
\mathcal I_\Theta=
\sum_{j,a,b}(\beta_a-\beta_b)
(\theta'(\beta_a)-\theta'(\beta_b))
|\langle e_a,X_je_b\rangle|^2\ge0,
\]
where `theta(x)=(x-1)_+^2`.  In particular
\[
\boxed{\mathcal I_\Theta\ge2\sum_j\|[X_j,R]\|_{HS}^2.}
\]
## 3. Isospectral Euler motion is quotiented exactly

Because `R` is a spectral function of `mathbb B`,
\[
\operatorname{Tr}(R[A,\mathbb B])=0.
\]
Define the secular/covariant Euler derivative
\[
\boxed{\nabla_E\mathbb B:=\mathbb B_{F_E}+[A,\mathbb B].}
\]
Then the entropy law is exactly
\[
\boxed{\dot\Theta+\nu\mathcal I_\Theta
=2\operatorname{Tr}(R\nabla_E\mathbb B).}
\]
## 4. The remaining source starts at curvature order

Let
\[
\mathcal K=[A,C],\qquad \mathcal N=N_C(u,\cdot).
\]
Jacobi and `CF_E=-[u,Cu]` give the Euler-curl Bianchi-Riccati identity
\[
\boxed{
C(\mathcal K_{F_E}+[A,\mathcal K])
=-\mathcal K^2-[A,\mathcal N]+[A_{Cu},\mathcal K]-\mathcal N_{F_E}.
}
\]
By the Sylvester relation between `A^perp` and `mathcal K^perp`, `nabla_E mathbb B` contains no bare one-step transport: only quadratic curl curvature and full Nijenhuis/Jacobi composition remain before modulus.

A single heat-resolvent corrector cancels the linear Euler source but leaves a nonnegative Hessian term `D^2 Theta[mathbb B_F,mathbb B_F]`.  Therefore the endgame cannot be a one-corrector monotone entropy; it must control a curvature-memory/quadratic-variation term.

## 5. Two open gates

The first target is a representation-free curvature-memory inequality of the form
\[
\boxed{
2\int_{t_0}^T\operatorname{Tr}(R\nabla_E\mathbb B)\,dt
\le \mathcal M(t_0)+(1-\delta)\nu\int_{t_0}^T\mathcal I_\Theta\,dt,
\qquad \delta>0,
}
\]
with finite intrinsic storage `mathcal M` and no occurrence-wise positive traffic sum.

The second target is a no-collapse implication: persistent supercritical occupation with small dephasing production must converge to a rigid infrared model.  The zero carrier is removed by Galilean nullity; the first nontrivial affine branch must be paid by accumulated Kelvin/viscous wave-number growth or another intrinsic heat-visible rigidity mechanism.

Both gates are open; no global-regularity claim is made.
