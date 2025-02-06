
# Relativistic quantum mechanics

## Klein-Gordon equation
- Consider _plane waves_:
$$\phi \sim \exp(-iEt+i\boldsymbol{p}\cdot \boldsymbol{x})=\exp(-ip_{\mu}x^{\mu})$$
- The _relativistic dispersion relation_ $p_{\mu}p^{\mu}=m^{2}$ must be regained
- One then gets the _Klein-Gordon equation_
$$(\partial_{\mu}\partial^{\mu}+m^{2})\phi=0$$
- It is _Lorentz invariant_

- There is a corresponding _conserved quantity_
	- $|\phi|^{2}$ is no longer _conserved in time_
$$j^{\mu}=i(\phi\partial^{\mu}\phi^{*}-\phi^{*}\partial^{\mu}\phi) \qquad \partial_{\mu}j^{\mu}=0$$
- The Klein-Gordon equation has both _positive_ and _negative energy solutions_
## Dirac equation
- Motivated by only wanting _positive energy_ solutions

- An equation _linear_ in both _space and time derivatives_
- The _Dirac equation_:
$$(i\gamma^{\mu}\partial_{\mu}-m)\psi=0$$
- This can give the _Klein-Gordon equation_ for some condition on $\gamma^{\mu}$

- Acting with $(i\gamma^{\mu}\partial_{\mu}+m)$ on the left, and _symmetrising_:
$$(-\gamma^{\mu}\gamma^{\nu}\partial_{\mu}\partial_{\nu}-m^{2})\psi=\left( -\frac{1}{2}\{\gamma^{\mu},\gamma^{\nu}\}\partial_{\mu}\partial_{\nu}-m^{2} \right)=0$$
- This gives the _Klein-Gordon equation_ if:
$$\{\gamma^{\mu},\gamma^{\nu}\}=2\eta^{\mu \nu}$$
- The _smallest_ matrices that can satisfy this are $4 \times 4$

### Representations

### Dirac spinors

## Electrodynamics
- Maxwell's equations:
$$\begin{align}
\nabla\cdot \boldsymbol{E}&=\rho \\ \nabla\times \boldsymbol{E}&=- \dot{\boldsymbol{B}} \\ \nabla\cdot \boldsymbol{B}&=0 \\ \nabla\times \boldsymbol{B}&= \boldsymbol{J}+ \dot{\boldsymbol{E}}
\end{align}$$
- This can be accounted for by the _potentials_ $V$ and $\boldsymbol{A}$
$$\boldsymbol{E}=-\nabla V- \dot{\boldsymbol{A}} \qquad \boldsymbol{B}=\nabla\times \boldsymbol{A}$$
- Introduce the _4-potential_ and _4-current_:
$$A^{\mu}=(V,\boldsymbol{A}) \qquad j^{\mu}=(\rho,\boldsymbol{j})$$
- The _field tensor_:
$$F_{\mu \nu}\equiv\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}$$
- Maxwell's equations are then:
$$\displaylines{ \partial_{\mu}F^{\mu \nu}=0 \\ \partial_{\lambda}F_{\mu \nu}+\partial_{\mu}F_{\nu\lambda}+\partial_{\nu}F_{\lambda \mu}=0}$$
- This also encodes the _gauge invariance_ of electromagnetism:
$$A_{\mu}\to A_{\mu}+\partial_{\mu}\chi$$
- One can commit to _gauge fixing_, e.g. the _Lorenz gauge_
$$\partial_{\mu}A^{\mu}=0$$
- This gives _plane wave solutions_, with some _polarisation vector_ $\epsilon^{\mu}$
$$A^{\mu}=\epsilon^{\mu}\exp(ip_{\mu}x^{\mu}) \implies p^{2}=0 \qquad \epsilon \cdot p=0$$
- The _residual_ gauge invariance means one can have a _choice_ out of _two polarisations_
	- _Shift_ $\epsilon^{\mu}$ by some amount perpendicular to $p^{\mu}$

### Minimal coupling
- When _coupling_ to other Lagrangians, use _minimal coupling_:
$$\partial_{\mu}\to D_{\mu}=\partial_{\mu}+ieA_{\mu}$$
- Coupling to either the _Klein Gordon_ or _Dirac_ fields:
$$\displaylines{[(\partial_{\mu}+ieA_{\mu})(\partial^{\mu}+ieA^{\mu})+m^{2}]\phi=0 \\ [i\gamma^{\mu}(\partial_{\mu}+ieA_{\mu})-m]\psi=0}$$
- In the Klein-Gordon case, a _negative energy solution_ $\phi$ with charge $e$ is _equivalent_ to the solution $\phi^{*}$ with _opposite charge and momentum_

