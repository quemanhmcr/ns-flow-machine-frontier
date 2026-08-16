# 07 — Torsion + conjugate frontier

Only exact identities are recorded here. The historical estimate remains open.

Let `J=sgn C`, `C=J Lambda`, and let `[.,.]` be the divergence-free Lie bracket, so
\[
CJ_uv=-[u,v].
\]

## 1. Helicity torsion isolates productive critical current

Define
\[
N_J(a,b)=[Ja,Jb]-J[Ja,b]-J[a,Jb]+[a,b].
\]
Cartan alternation gives
\[
\boxed{\langle u,N_J(u,\Lambda u)\rangle=2\kappa.}
\]
Hence, after the full torsion is assembled,
\[
\boxed{\mathcal A_K\le \mathcal T_J(u):=
\frac{\|\Lambda^{-1/2}N_J(u,\Lambda u)\|_2^2}{4M_3}.}
\]
In fact
\[
\mathcal T_J=\mathcal A_K+
\frac{\|P_{(\Lambda^{1/2}u)^\perp}\Lambda^{-1/2}N_J(u,\Lambda u)\|_2^2}{4M_3}.
\]
Thus `N_J(u,Lambda u)=0` forces `A_K=0`. With `P_++P_-=I`,
\[
P_+N_J(a,b)=4P_+[P_-a,P_-b],\qquad
P_-N_J(a,b)=4P_-[P_+a,P_+b].
\]
The homochiral output channel is removed before absolute values.

## 2. Curl torsion is the heat defect of Cartan strain

Set
\[
S_u=[J_u,C]=J_uC-CJ_u.
\]
Then
\[
\boxed{S_u^*=S_u,\qquad F_E(u)=S_uu,\qquad DF_E(u)[h]=S_uh+S_hu.}
\]
Define
\[
N_C(u,v)=[Cu,Cv]-C[Cu,v]-C[u,Cv]+C^2[u,v].
\]
Directly,
\[
N_C(u,v)=C(CS_u-S_{Cu})v.
\]
Therefore, on the nonzero curl spectral subspace,
\[
\boxed{(\partial_s+C^2)S_{H_su}
=N_C(H_su,\cdot)+C^{-1}N_C(CH_su,\cdot).}
\]
Equivalently, without `C^{-1}`,
\[
C(\partial_s+C^2)S_{H_su}=CN_C(H_su,\cdot)+N_C(CH_su,\cdot).
\]
For the vector-field commutator,
\[
\boxed{[F_E,-C^2](u)=S_uC^2u+C^{-1}N_C(u,Cu)}
\]
on the same nonzero spectral subspace.

## 3. Conjugate removal of inherited residual

Let
\[
U_s=H_su,\quad \mathcal R_s=H_sF_E(u)-F_E(U_s),\quad
\mathcal N_s=H_sDF_E(u)[F_E(u)]-DF_E(U_s)[F_E(U_s)],
\]
and `mathscr D=partial_t-nu partial_s`, `mathcal K=[F_E,-C^2]`. Then
\[
\boxed{\mathscr D\mathcal R_s
=\mathcal N_s-DF_E(U_s)\mathcal R_s-\nu H_s\mathcal K(u).}
\]
On a backward heat tent `0<s<nu(T_*-t)`, solve
\[
\mathscr D\phi-DF_E(U_s)^*\phi=a,\qquad \phi(t_0,s)=0.
\]
Since `mathscr D` is tangent to the sloping edge and `R_0=0`,
\[
\boxed{\iint\langle a,\mathcal R\rangle
=-\iint\langle\phi,\mathcal N-\nu H_s\mathcal K\rangle.}
\]
Thus inherited `DF_E(U_s) R_s` is removed at the identity level. Also
\[
\boxed{DF_E(u)+DF_E(u)^*=S_u,}
\]
so the conjugate dynamics still sees the true signed-curl Cartan strain.

## 4. Open route

A sharper sufficient target is
\[
\boxed{\int_0^T\mathcal T_J(u(t))\,dt<\infty.}
\]
It would imply `int A_K dt < infinity`; it is **not proved**. The next task is to remove all linear residual terms by the conjugate identity, then group the remaining fresh source at full cyclic Cartan/Jacobi level before any modulus. No occurrence-wise positive traffic sum is allowed.
