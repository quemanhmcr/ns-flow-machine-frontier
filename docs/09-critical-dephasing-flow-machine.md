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

## 7. Quotient the isospectral orbit before paying memory

The raw memory `mathcal H_mem` still overpays Euler motion that only rotates the eigenspaces of `mathbb B`.  Since `R=f(mathbb B)`, for every skew-adjoint cutoff operator `Omega`,
\[
\operatorname{Tr}\bigl(R[\Omega,\mathbb B]\bigr)=0.
\]
Let `Pi_0` denote projection onto the kernel of `L` (zero carrier).  Define the extended gauge-minimal secular memory
\[
\boxed{
\mathcal H_{sec}:=
\inf_{\substack{\Omega^*=-\Omega\\
\Pi_0(\mathbb B_{F_E}+[\Omega,\mathbb B])=0}}
\left\langle S_\Omega,L^{-1}S_\Omega\right\rangle_{HS},
\qquad
S_\Omega:=\mathbb B_{F_E}+[\Omega,\mathbb B].
}
\]
If the constraint set is empty, the cost is `+infinity`; that failure is itself a dephasing-invisible infrared obstruction.

For every admissible `Omega`, the entropy source is unchanged and the carrier Dirichlet integration by parts gives
\[
2\operatorname{Tr}(R\mathbb B_{F_E})
=2\operatorname{Tr}(RS_\Omega)
\le\frac\nu2\mathcal I_\Theta+
\frac1\nu\langle S_\Omega,L^{-1}S_\Omega\rangle.
\]
Taking the infimum sharpens the flow-machine inequality to
\[
\boxed{
\dot\Theta+
\nu\frac{(\Theta+\Phi)^2}{\mathcal H_{IR}}
\le\frac{\mathcal H_{sec}}\nu.
}
\]
Thus only eigenvalue-changing Euler regeneration is charged.

At an interior minimizer, set `V=L^{-1}S_{Omega_*}`.  Variation in skew `delta Omega` yields
\[
0=\langle V,[\delta\Omega,\mathbb B]\rangle_{HS},
\]
hence the weighted Coulomb/horizontal condition
\[
\boxed{[\mathbb B,V]=0.}
\]
So the optimal dephasing potential is in the spectral commutant of `mathbb B`.  This is the operator-level quotient required before any positive curvature-memory estimate.  The admissible physical Cartan competitor is the `g`-skew helicity-preserving part `Omega=A_u^parallel`.  The helicity-mixing part is `g`-self-adjoint and is not an isospectral Hodge generator; it is entropy-invisible only by parity.  The resulting covariant source is audited in Section 12.

## 8. Dephasing Hodge decomposition on the spectral orbit

The minimization defining `mathcal H_sec` is a weighted horizontal/vertical decomposition.  At a minimizer, let
\[
V=L^{-1}(\mathbb B_{F_E}+[\Omega_*,\mathbb B]).
\]
Then
\[
\boxed{
\mathbb B_{F_E}=LV-[\Omega_*,\mathbb B],
\qquad [\mathbb B,V]=0.
}
\]
The first term is the secular direction seen by dephasing; the second is a pure isospectral tangent.  The normal equation for the gauge is
\[
\boxed{
[\mathbb B,L^{-1}[\Omega_*,\mathbb B]]
=-[\mathbb B,L^{-1}\mathbb B_{F_E}].
}
\]
It is linear in `Omega_*` for fixed `mathbb B` and is unique modulo the stabilizer of `mathbb B` once the zero-carrier constraint and an orthogonality convention are fixed.  The Pythagorean identity for the weighted quadratic functional shows that every other admissible gauge pays `mathcal H_sec` plus a nonnegative vertical excess.

The admissible physical choice is `Omega=A_u^parallel`; Section 12 records the parity correction and the resulting covariant source.  The remaining task is to compare the optimal Hodge gauge to that corrected physical Cartan gauge without taking occurrence-wise absolute values.

## 9. Pair-Gram Loewner law

Because `J mathbb B J=-mathbb B`, write in helicity blocks
\[
\mathbb B=\begin{pmatrix}0&T\\T^*&0\end{pmatrix}.
\]
Let `X_{j,+/-}` be the translation generators on the two helicity sectors,
\[
\delta_jT=X_{j,+}T-TX_{j,-},\qquad
L_TT=\sum_j\delta_j^2T,
\]
and set `Q=T^*T`.  The dephasing equation gives
\[
T_t=-\nu L_TT+T_F.
\]
A direct product calculation yields
\[
\boxed{
Q_t=-\nu L_-Q-2\nu\Gamma_T+T_F^*T+T^*T_F,
\qquad
\Gamma_T:=\sum_j(\delta_jT)^*(\delta_jT)\succeq0,
}
\]
where `L_-Q=sum_j[X_{j,-},[X_{j,-},Q]]`.  Thus viscosity produces a genuine Loewner-negative pair-decoherence square, not merely trace-convex damping.

For the threshold occupation `Upsilon=Tr(Q-I)_+` and `P=1_{Q>1}`, at threshold-regular times,
\[
\boxed{
\dot\Upsilon+\nu\operatorname{Tr}(P L_-Q)
+2\nu\operatorname{Tr}(P\Gamma_T)
=2\Re\operatorname{Tr}(P T^*T_F).
}
\]
Both heat terms on the left are nonnegative.  This identity is presently a diagnostic rather than the chosen smooth entropy: the sharp projector `P` has a threshold singularity, while `Theta` has the firmly-nonexpansive soft-threshold gradient needed for the clean `H^{-1}` absorption above.

## 10. Spectral resistor network and odd soft-threshold normal form

Work at a threshold-regular time and first assume the spectrum of `mathbb B` is simple,
\[
\mathbb B e_a=\beta_a e_a.
\]
Set
\[
c_{ab}:=\sum_{j=1}^3|\langle e_a,X_je_b\rangle|^2,
\qquad
(\Delta_c z)_a:=2\sum_b c_{ab}(z_a-z_b).
\]
If `V=L^{-1}S_*` is the optimal dephasing potential from Section 8 and `V e_a=v_a e_a`, then the Hodge equation is the Kirchhoff law
\[
\boxed{
y_a:=\langle e_a,\mathbb B_{F_E}e_a\rangle=(\Delta_c v)_a,
\qquad
\mathcal H_{sec}=\sum_{a,b}c_{ab}(v_a-v_b)^2.
}
\]
The heat part has the same graph Laplacian:
\[
\boxed{
\dot\beta_a=-\nu(\Delta_c\beta)_a+(\Delta_c v)_a.
}
\]
Thus the eigenvalue motion is a time-dependent resistor-network diffusion forced by the secular Euler voltage.

Because `J mathbb B J=-mathbb B` and `[J,X_j]=0`, the spectral graph has the involution `beta -> -beta`.  The source `mathbb B_F` is odd under the same involution.  By parity orthogonality the minimizing potential can be chosen odd.  Hence it is natural to replace the one-sided threshold gradient by the odd soft-threshold
\[
\boxed{
G:=\operatorname{sgn}(\mathbb B)(|\mathbb B|-I)_+.
}
\]
On the `J`-odd manifold,
\[
\boxed{
\Theta=\tfrac12\|G\|_{HS}^2,
\qquad
\Phi=\tfrac12\operatorname{Tr}|G|.
}
\]
Let
\[
\mathcal E_c(f,g):=\sum_{a,b}c_{ab}(f_a-f_b)(g_a-g_b).
\]
Then the exact entropy law becomes
\[
\boxed{
\dot\Theta+\nu\mathcal E_c(G,\beta)=\mathcal E_c(G,v).
}
\]
The scalar soft-threshold map is firmly nonexpansive, so
\[
\mathcal E_c(G,\beta)\ge \mathcal E_c(G,G).
\]
Moreover `mathbb B` has no zero-carrier component.  Carrier integration by parts gives
\[
2(\Theta+\Phi)=\langle G,\mathbb B\rangle_{HS},
\]
and therefore
\[
\boxed{
\mathcal E_c(G,G)\ge
\frac{4(\Theta+\Phi)^2}{\mathcal H_{IR}}.
}
\]
This is the parity-sharpened noncommutative Nash inequality.

The network law also admits an exact passivity completion.  Put
\[
E_G:=\mathcal E_c(G,G),\qquad
E_{th}:=\mathcal E_c(G,\beta-G)\ge0,
\qquad
J_G:=\mathcal E_c(G,v).
\]
Then
\[
\boxed{
\dot\Theta+\nu E_G+\nu E_{th}=J_G.
}
\]
Equivalently, with
\[
\mathcal A_G:=\frac{J_G^2}{E_G}
\]
when `E_G>0`,
\[
\boxed{
\dot\Theta+\nu E_{th}
=\frac1{4\nu}\left[
\mathcal A_G-
\frac{(J_G-2\nu E_G)^2}{E_G}
\right].
}
\]
Thus the flow machine produces a second minimal-action/reflection identity, now on the dephasing spectral graph.  Only the rank-one projection of the secular voltage onto the odd threshold gradient can grow `Theta`; all Dirichlet-orthogonal secular memory is nonproductive.

Finally use the intrinsic heat clock
\[
d\sigma=\nu m\,dt,\qquad m=M_3/K,
\]
and the normalized conductances `bar c_ab=c_ab/m`, voltage `w=v/nu`.  Then
\[
\boxed{
\partial_\sigma\beta=-\Delta_{\bar c}(\beta-w),
}
\]
so the supercritical spectral problem is dimensionless.  Infrared collapse is precisely degeneration of the normalized conductances `|k-l|^2/m`; efficient regeneration requires the normalized secular voltage to align with the odd soft-threshold gradient.  These are now the two explicit rigidity defects to be classified.

For degenerate eigenvalues the same statement must be written with spectral blocks and a matrix-valued commutant potential; the simple-spectrum formula above is the audited finite-cutoff normal form, not yet a continuum theorem.

## 11. Equality rigidity: no continuum supercritical dephasing soliton

The odd soft-threshold admits the complementary clipping decomposition
\[
G=\operatorname{soft}_1(\mathbb B),\qquad
H=\mathbb B-G=\operatorname{clip}_{[-1,1]}(\mathbb B).
\]
The threshold defect from Section 10 is
\[
\boxed{
E_{th}=\sum_j\langle[X_j,G],[X_j,H]\rangle_{HS}\ge0.
}
\]
In a spectral basis its summands are
\[
\sum_{a,b}c_{ab}
\bigl(g(\beta_a)-g(\beta_b)\bigr)
\bigl(h(\beta_a)-h(\beta_b)\bigr),
\]
where `g=soft_1` and `h=clip_[-1,1]`; every scalar factor is nonnegative.

Assume there is no eigenvalue at `+/-1`.  If `E_th=0`, every dephasing edge joining a positive supercritical eigenvalue to its complement, or a negative supercritical eigenvalue to its complement, has zero conductance.  Therefore
\[
\boxed{
[X_j,P_+]=[X_j,P_-]=0,
\qquad
P_+=1_{\{\mathbb B>1\}},\quad
P_-=1_{\{\mathbb B<-1\}}.
}
\]
Thus exact zero threshold leakage forces the supercritical spectral subspaces to be decoherence-free for all carrier-coordinate generators.

This yields an exact continuum equality rigidity.  Suppose the carrier Hilbert space is `L^2(R^3_k;C^m)`, `X_j` is multiplication by `k_j`, and `mathbb B` is compact.  Then `P_+` and `P_-` have finite rank.  A finite-rank projection commuting with all coordinate multipliers on the atomless carrier measure must vanish.  Hence
\[
\boxed{E_{th}=0\quad\Longrightarrow\quad P_+=P_-=0}
\]
under these continuum assumptions.  In particular there is no nonzero exact supercritical dephasing soliton with zero threshold leakage.

The near-equality interpretation is equally important.  If the active spectrum is separated from the threshold by a margin `delta>0`, then small `E_th` forces the corresponding spectral projector to almost commute with the `X_j`.  For a rank-one projector this commutator norm is exactly a Fourier-carrier variance.  Thus a near-lossless supercritical mode must become a narrow carrier packet.  This identifies the infrared/affine WKB-Kelvin branch as the quantitative near-equality model, rather than an independently postulated case split.

The periodic lattice has atoms, so the exact finite-rank argument above does not apply verbatim there.  The expected blow-up-scale use is through rescaling, where the carrier lattice spacing tends to zero and the continuum rigidity is the candidate limiting no-soliton statement.  Turning this into a compactness theorem remains open.

## 11. Midpoint-transform audit: what the flow machine does and does not buy

After conjugating the `g`-self-adjoint amplifier to the standard Hilbert representation, it is exactly the critical Reynolds operator from the midpoint transform
\[
T(u)=\mathcal Q_c(u)=\tfrac12\Lambda^{-1/2}[J_u,J]\Lambda^{-1/2},
\qquad
\widehat{\mathbb B_u}=\nu^{-1}T(u).
\]
The audited continuum identities are
\[
T^*T=\Lambda/64,
\qquad
\langle T(u),T(v)\rangle_{HS}=\tfrac1{64}\langle u,\Lambda v\rangle,
\qquad
LT(u)=T(C^2u).
\]
Consequently the infrared susceptibility is not a new unknown:
\[
\boxed{
\mathcal H_{IR}
=\langle\mathbb B,L^{-1}\mathbb B\rangle_{HS}
=\frac1{64\nu^2}\langle u,\Lambda^{-1}u\rangle.
}
\]
On a periodic mean-zero domain with lowest absolute-curl frequency `lambda_1>0`,
\[
\mathcal H_{IR}\le \frac{E}{64\nu^2\lambda_1},
\]
so the infrared denominator in the Nash estimate is energy-controlled.  The corresponding raw source memory is
\[
\boxed{
\mathcal H_{mem}
=\frac1{64\nu^2}\|\Lambda^{-1/2}F_E\|_2^2,
}
\]
which is exactly the old critical Hilbert currency and has no known finite energy budget.

For the odd soft threshold `G`, define its physical preimage
\[
\psi_G:=64\Lambda^{-1}T^*G.
\]
Since the closed range of `T` reduces `L`,
\[
\boxed{
J_G=\operatorname{Tr}(G\mathbb B_{F_E})
=\frac1{64\nu}\langle\Lambda\psi_G,F_E\rangle,
}
\]
and
\[
\boxed{
K(\psi_G)\le128\Theta,
\qquad
M_3(\psi_G)\le64E_G.
}
\]
Thus the second minimal action obeys only the generic estimate
\[
\boxed{
\mathcal A_G=\frac{J_G^2}{E_G}
\le\frac1{64\nu^2}\|\Lambda^{-1/2}F_E\|_2^2.
}
\]
This is not a closure: after Cauchy the flow machine collapses back to the previously open critical Hilbert action.  Any genuine gain must therefore come from the **isospectral Hodge quotient** `mathcal H_sec`, not from the threshold transform followed by a pointwise norm bound.

There is also an exact clipping decomposition.  If
\[
H=\operatorname{clip}_{[-1,1]}(\mathbb B),
\qquad
\eta_H:=64\Lambda^{-1}T^*H,
\]
then
\[
\boxed{\psi_G+\eta_H=u/\nu}
\]
and hence
\[
\boxed{
J_G=\frac{\kappa}{64\nu^2}
-\frac1{64\nu}\langle\Lambda\eta_H,F_E\rangle.
}
\]
Thus the soft-threshold source is an exact spectral partition of the original critical Euler current, not a new independent current.

## 12. Parity guard on the Bianchi--Riccati source

In the physical Hodge comparison the admissible isospectral generator is the `g`-skew helicity-preserving part `A^parallel`, not the full `A=ad_u`; `A^perp` is `g`-self-adjoint.  Because `G` and `mathbb B_{F_E}` are helicity-odd, the even term `[A^perp,mathbb B]` is invisible in the entropy pairing.  The distinguished physical covariant source is therefore
\[
\boxed{
S_{phys}=\mathbb B_{F_E}+[A^\parallel,\mathbb B],
\qquad
J_G=\operatorname{Tr}(G S_{phys}).
}
\]
This corrects the earlier shorthand that treated the full `A` as an admissible skew Hodge competitor.

The positive Riccati square does not directly feed the odd secular source.  With
\[
\mathcal K=\mathcal K^\parallel+\mathcal K^\perp,
\]
parity gives
\[
\boxed{
(-\mathcal K^2)^\perp
=-\{\mathcal K^\parallel,\mathcal K^\perp\},
\qquad
[-(\mathcal K^\perp)^2]^\perp=0.
}
\]
Hence the positive square `-(mathcal K^perp)^2` found in the Bochner audit is not the term that can pay `J_G`; the surviving one-triad spectral regeneration is the signed cross-Riccati interaction between within-helicity curl shear and helicity mixing.

For an isolated heterochiral block with signed curl values `(-a,b,c)` and positive pair singular value `s>1`, the already audited law
\[
(s^2)'_E=\frac{\kappa_\triangle}{\nu^2abc}
\]
gives
\[
\boxed{
J_G=\dot\Theta_E
=\frac{s-1}{s}\frac{\kappa_\triangle}{\nu^2abc}.
}
\]
Thus the secular source is genuinely nonzero on one triad.  It vanishes at `b=c`; the driver is the same-helicity signed-curl shear `(b-c)`.  Fourier triangle geometry gives `|b-c|<=a`, so occurrence-wise the driver gap is paid by the quadratic heat of its carrier.  Promoting that fact to a full-state estimate without positive occurrence traffic is now the precise remaining structural question.

## 13. Isolated-triad Hodge calibration and the next non-gross target

The Hodge quotient is genuinely smaller than the raw critical Hilbert source already on one productive heterochiral triad.  Take signed curl values `(-a,b,c)`, `a,b,c>0`, and write the modal amplitudes as `(x,y,z)`.  In the standard critical Hilbert representation the pair block is a two-component star with positive singular value
\[
s^2=\frac{b|y|^2+c|z|^2}{abc\nu^2}.
\]
For `s>1`, the odd soft threshold is `(s-1)/s` times that block.  Optimizing the weighted dephasing memory over the single within-positive-helicity rotation removes the orientation derivative and leaves
\[
\boxed{
\mathcal H_{sec}^{\triangle}
=\mathcal A_G^{\triangle}
=\frac{\kappa_\triangle^2}
{2\nu^2abc\,(b^3|y|^2+c^3|z|^2)}.
}
\]
Thus in the one-secular-direction model the Hodge Cauchy inequality is an equality: the quotient retains exactly the eigenvalue-changing source and discards the orthogonal pair rotation.

There is also a direct driver-heat estimate.  Using
\[
\frac{\mathcal H_{sec}^{\triangle}}{a^2|x|^2s^2}
=
\frac{2(b-c)^2|y|^2|z|^2}
{(b^3|y|^2+c^3|z|^2)(b|y|^2+c|z|^2)},
\]
and
\[
(b^3|y|^2+c^3|z|^2)(b|y|^2+c|z|^2)
\ge bc(b^2+c^2)|y|^2|z|^2,
\]
one obtains, on a periodic domain with `a,b,c>=lambda_1>0`,
\[
\mathcal H_{sec}^{\triangle}
\le \frac{2}{\lambda_1^2}a^2|x|^2s^2
\le \boxed{\frac{4}{\lambda_1^2}Z_\triangle(1+\Theta_\triangle)}.
\]
The first inequality uses `(b-c)^2<=b^2+c^2`; the second uses `s=1+sqrt(Theta_triangle)` on the supercritical branch.  Hence the secular spectral source on one triad is paid by the quadratic heat of the same-helicity driver, after the Hodge quotient removes orientation motion.

This is only a calibration, not a many-mode theorem.  Summing the displayed triad bound occurrence by occurrence would recreate the forbidden gross-traffic budget.  The next live test of the flow machine is therefore the representation-free operator analogue
\[
\boxed{
\mathcal H_{sec}(u)
\stackrel{?}{\lesssim}
\lambda_1^{-2} Z(u)\,[1+\Theta(\mathbb B_u)]
}
\]
(or a sharper current-level version) obtained **after** full Cartan/Hodge assembly.  A proof of such an estimate must use the cross-Riccati same-helicity driver as a full operator, not a positive triad sum.  Failure of this operator lift would mean that the flow machine remains a useful reformulation but does not yet supply the missing positive-composition mechanism.

## 14. Standalone sector absorption is falsified by an actual Galerkin driver family

A scale-correct self-absorption candidate is

\[
\mathfrak S(u):=
\frac{\mathcal H_{sec}(u)\,\mathcal H_{IR}(u)}{(\Theta(u)+\Phi(u))^2}.
\]

With the odd soft threshold conventions above, dephasing plus optimal Hodge Cauchy would close
instantaneously if `mathfrak S<=4 nu^2`.  This is **false** even before any continuum limit.

Take the full Fourier ball `|k|<=2` and an actual reality-paired heterochiral triad with wavevectors
`(1,0,0)`, `(0,1,0)`, `(-1,-1,0)` and helicities `(-,+,+)`.  Hold the two pair-support amplitudes fixed,
keep a fixed nonzero phase, and increase only the remaining driver amplitude.  The full retained
critical Reynolds operator, its Euler source, the dephasing Hodge minimizer and the Kirchhoff normal
equation are all evaluated on the whole Fourier ball, not on a compressed three-mode matrix.
For driver amplitudes `0.25,0.5,1,2,4` the computed sector ratios are respectively

\[
0.2075,\quad0.5302,\quad1.2737,\quad3.2645,\quad8.7131,
\]

while the relative Kirchhoff residual stays below `2.4e-15`.  Larger drivers remain above the
absorption threshold in the same audit.

Thus the Hodge quotient removes isospectral rotation but does **not** remove the independent physical
driver reservoir.  The isolated-triad formula already explains the mechanism: secular spectral
production is a minimal action whose numerator contains the same-helicity driver current.  Repeated
regeneration cannot be paid by spectral dephasing alone; the driver stock/inflow history must enter.

There is a second guard.  A material-stress estimate of the form

\[
|\operatorname{Tr}(G\,\mathbb B_F)|^2
\lesssim Z\,E_G(1+\Theta)
\]

has the wrong continuum Navier--Stokes scaling: under `u_lambda(x)=lambda u(lambda x)`, the left side
scales like `lambda^4` whereas `Z E_G` scales like `lambda^3`.  Material pullback remains a useful
interpretation of the source, but an `L_t^2 L_x^2` strain budget cannot by itself be the critical
endgame.

**Verdict.**  The flow/dephasing machinery survives as a canonical *demand meter*: `H_sec` is the
minimal eigenvalue-changing regeneration cost after all isospectral recycling is quotiented.  It is
not a closed entropy mechanism.  Any endgame must couple this demand to a representation-free
historical accounting of the actual driver energy/current; otherwise the family above is an explicit
finite-dimensional obstruction.
