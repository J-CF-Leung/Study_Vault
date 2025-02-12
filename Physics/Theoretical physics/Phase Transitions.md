- For many-body systems, one can have both _microscopic_ and _macroscopic_ descriptions
	- The Hamiltonian gives a _microscopic description_ (classical or quantum)
	- The _macroscopic_ description uses _state variables_ $P,V,T\dots$
	- Connected by _statistical mechanics_ and the _partition function_ $Z$
$$Z=\exp(-\beta F)=\mathrm{Tr}(e^{-\beta H})$$

- A _non-interacting system_ has separable partition functions, giving rise to an _ideal gas_

- With interactions, one gets _phase transitions_, corresponding to _singularities_ in $Z$
- This occurs in many different systems, where the transition can be characterised by _symmetry breaking_, and a corresponding _order parameter_
- Symmetry breaking also gives rise to _collective excitations_
	- Continuous symmetry breaking gives _Goldstone modes_

- Common critical behaviour (e.g. temperature dependence of properties _near the critical point_) between different systems is the _principle of universality_
	- Example: the _Ising universality class_ includes _ferromagnetic_, _liquid-gas_, and _Mott-Hubbard metal-insulator transitions_
	- Example: the _XY universality class_ includes _superconductors_, _superfluids_, and _melting in 2D_

- Symmetry is typically _not sensitive to microscopic laws_, giving rise to _effective field theory descriptions_

- Descriptions at different length scales are connected by the _renormalisation group_

- There are _first order_ and _second order_ phase transitions
	- First order: a _discontinuous change_ in order parameter $M$
	- Second order: a _continuous order parameter_
![[Ising model phase diagram.png|400]]
- Two different phase diagrams may have the same _topology_ (Manifestation of universality)
	- e.g. Ising model and liquid-gas phases

- _Correlation lengths_ is some lengthscale over which _fluctuations are correlated_
- At a phase transition, the _correlation length will diverge_ $\to \infty$ such that thermodynamic properties become _singular_
- The system will therefore become _scale invariant_ at the transition
	- Manifestation: _critical opalescence_ during liquid-gas transition (bubbles at all lengthscales such that scattering occurs at all light wavelengths)

- As the system has _no characteristic lengthscale_, it can only be described by a _coarse grain theory_ based on symmetries
- This coarse graining leads to a description based on an _order parameter_
	- Example: _magnetisation_
- This is the foundation of _Ginzburg-Landau theory_

# Critical phenomena

## The liquid-gas transition and the Ising universality class
![[Liquid gas phase diagram.png]]
### Liquid-gas transition
- Characteristics of the liquid-gas transition:
	- In the $P-T$ plane, there is some _critical point_ beyond which there is _no liquid-gas phase transition_
	- For $T<T_{c}$ in the $P-V$ plane, there is a _co-existence interval_ where some _mixture_ of liquid and gas exist, at different _densities_ $\rho_{g}=1/v_{g}$ and $\rho_{l}=1/v_{l}$
	 - The liquid to gas transition for $T<T_{c}$ exhibits a _discontinuity_ in density, and an exchange in _latent heat_
	 - The _order parameter_ for the transition is the _difference in density_ $\Delta \rho$

 - However, one can go from liquid to gas _continuously_ by going _around the critical point_
	 - The _free energy_ in the $(P,T)$ plane is some _analytical function_, but with a _branch cut_ where the coexistence boundary is

- Characteristics _near the critical point_:
	- As $T\to T_{c}$, the _difference_ in density between the phases _vanishes_ $(\rho_{l}\to \rho_{g},T\to T_{c}^{-})$
	- The $(P,V)$ isotherms also become _flatter_ as $T\to T_{c}^{+}$, indicating that _isothermal compressibility_ $\kappa_{T}=(1/V)(\partial V/\partial P)|_{T}$ _diverges_
	- The fluid will also appear _milky_ due to _critical opalesence_, as _fluctuations_ of _all sizes_ appear and scatter light

### Ising model
- The _Ising model_ and _liquid-gas_ transitions have the same _topology_

- Below temperature $T_{c}$, the Ising ferromagnet is _spontaneously magnetised_
- It is a _second order transition_ as the order parameter $m$ evolves continuously

- There is a _discontinuity_ in magnetisation as the _external field_ $\boldsymbol{H}$ goes through zero
- Like the liquid-gas phase, the _line of discontinuous transitions_ will _terminate_ at some _critical point_

### Correspondence between models
![[Ising class paths.png|400]]
- Whether or not a transition is continuous is dependent on the _path taken_

- The _discontinuous boiling transition_ at _constant pressure_ is analagous to _changing external magnetic field_ at constant temperature $T<T_{c}$
	- Figure $(b)$ corresponding to figure $(c)$

- Meanwhile, the _critical isochore_ with _fixed density_ in a liquid/gas is analagous to _keeping external magnetic field zero_ in the Ising ferromagnet

## Critical behaviour
- Systems belonging in the _same universality class_ will display _similar critical behaviour_
- _Length scales_ must not play a role in critical behaviour

### Order parameter
- The _order parameter_ near the critical point may be dictated by the _critical exponents_
- Behaviour of _magnetisation_ in the Ising model near zero field:
$$m(T, H\to 0^{+})=\begin{cases}
0 &T>T_c \\ |t|^{\beta} &T<T_{c}
\end{cases}$$
- $t$ is the _reduced temperature_ $(T-T_{c})/T_{c}$

- Meanwhile, along the _critical isotherm_:
$$m(T=T_{c}, H)\propto H^{1/\delta}$$
### Response function
- Meanwhile, the _response functions_ can also be described by _critical exponents_, giving the _divergences_ near the critical point
	- Example: compressibility becoming infinite
- The _zero field susceptibility_:
$$\chi_{\pm}(T,H\to 0^{\pm})=\frac{\partial m}{\partial H}\Bigg|_{H=0^{\pm}}\propto|t|^{-\gamma_{\pm}}$$
- Often, the two _divergences_ have the _same power law_ $\gamma=\gamma_{+}=\gamma_{-}$

- Similarly, the _heat capacity_, as the _thermal response function_:
$$C_{\pm}=\frac{\partial E}{\partial T}\propto|t|^{-\alpha_{\pm}}$$
- There can be a _positive_ $\alpha$ giving a divergence
- Or, a _negative_ $\alpha$ gives a _finite_ $C$, with or without a _cusp_
### Correlation functions
- Divergences in the _response function_ also indicate that _fluctuations are correlated over long distances_

- The partition function for the Ising model, as a _generating functional_:
$$\mathcal{Z}(T,h)=\sum_{\{\sigma_{i}\}} \exp[-\beta(H-hM)]$$
- The _thermal average magnetisation_ can be found by some derivative:
$$\langle M \rangle=\frac{\partial \ln \mathcal{Z}}{\partial(\beta h)} =\frac{1}{\mathcal{Z}}\sum_{\{\sigma_{i}\}} M\exp[-\beta(H-hM)]$$
- The _susceptibility_:
$$\chi= \frac{1}{V}\frac{\partial \langle M \rangle }{\partial h}=\frac{\beta}{V}\left\{  \frac{1}{\mathcal{Z}} \sum_{\{\sigma_{i}\}}M^{2} e^{-\beta(H-hM)} -\left( \frac{1}{\mathcal{Z}}\sum_{\{\sigma_{i}\}}Me^{-\beta(H-hM)} \right)^{2}\right\}$$
- It is a _variance_:
$$\chi=\frac{\beta}{V}\mathrm{Var}(M)=\frac{\beta}{V}\left(\langle M^{2} \rangle-\langle M \rangle^{2}  \right)$$
- This is a _sum of separate magnetisations_, taking the _continuum limit_:
$$M=\int  d^3\boldsymbol{x}\,m(\boldsymbol{x}) $$
- Each magnetisation has the _same definition of susceptibility_:
$$k_{B}T\chi=\int  d\boldsymbol{x} \int  d\boldsymbol{x}'\,[\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle -\langle m(\boldsymbol{x}) \rangle\langle m(\boldsymbol{x}') \rangle  ]  $$
- As the system is _symmetric under translation_, $\langle m(\boldsymbol{x}) \rangle$ is a _constant_ $m$ while $\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle=G(\boldsymbol{x}-\boldsymbol{x}')$ is _only dependent on translation_

- The _connected correlation function_
$$\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle_{C}\equiv \langle (m(\boldsymbol{r})-\langle m(\boldsymbol{r}) \rangle)(m(\boldsymbol{r}')-\langle m(\boldsymbol{r}') \rangle)  \rangle  =G(\boldsymbol{r}-\boldsymbol{r}')-m^{2}$$
- Susceptibility:
$$k_{B}T\chi=\int  d\boldsymbol{x}\,\langle m(\boldsymbol{x})m(0) \rangle_{C}  $$

- The _correlation length_ is the lengthscale at which the _correlation function dies off_:
$$\langle m(\boldsymbol{x})m(0) \rangle_{C}\sim \exp(-|\boldsymbol{r}|/\xi) $$
- From the relation between $\chi$ and $\xi$, in $d$ dimensions:
$$k_{B}T\chi\sim m^{2}\xi^{d}$$

- As _response functions_ diverge, the _correlation length_ must also diverge
	- Leads to _critical opalescence_
$$\xi_{\pm}(T,H=0)\propto |t|^{-\nu_{\pm}}$$
- The _Greens function_ is also governed by some critical exponent:
$$G(r.T=T_{c})\sim \frac{1}{r^{d-2+\eta}}$$
# Ginzburg-Landau phenomenology
- Let there be some _coarse graining_ in the system, to _average out microscopic degrees of freedom_
	- There is some _information loss_ due to _averaging_ over some local volume

- The statistical field theory/universality class is governed by both _number of dimensions in the space_, and the _number of spin components_:
$$\boldsymbol{x} \in \mathbb{R}^{d}\qquad \boldsymbol{m} \in \mathbb{R}^{n}$$
- Examples:
	- $n=3$ describes _classical isotropic magnets_
	- $n=2$ describes _superconductivity, superfluidity_, and _planar magnets_
	- $n=1$ describes _liquid-gas transitions, binary mixtures_, and _uniaxial magnets_
	- Depending on if the theory applies to the _bulk, surfaces, wires_, or _spacetime_, $d$ takes different values

- The coarse graining means one can have a _functional integral description_ of the _coarse-grained field_
$$\mathcal{Z}[T,\boldsymbol{h}]=\int  \mathcal{D}\boldsymbol{m} \exp(-\beta H[\boldsymbol{m}])$$
## Effective field theories

### Requirements
- The field theory must be _local_:
$$\beta H[\boldsymbol{m}]=\int  d^dx\,f[\boldsymbol{m}(\boldsymbol{x}),\nabla \boldsymbol{m},\dots] $$
- It must also have _rotational invariance_ for the _order parameter_
- For some rotation matrix $R$:
$$\beta H[\boldsymbol{m}]=\beta H[R\boldsymbol{m}]$$
- In _real space_, there must be both _translational_ and _rotational symmetry_

- From these conditions, $\beta H$ must be some _analytical function_ of $m$ with these symmetries
	- $\beta$ is _not a factor_, $\beta H$ is _one function_
- With some _phenomenological parameters_:
$$\beta H[\boldsymbol{m}(\boldsymbol{x})]=\int  d^dx\left[ \frac{t}{2}m^{2}+um^{4}+\frac{K}{2}|\nabla \boldsymbol{m}|^{2}+\frac{L}{2}|\nabla^{2}\boldsymbol{m}|^{2}+\dots -\boldsymbol{h}\cdot \boldsymbol{m}\right] $$
- _Higher order_ field and gradient terms are assumed to be _small_ near the critical point

### The functional integral
- The functional integral is defined in the limit of:
	- $a$: _distance_ between sites $i$
	- $N$: number of sites
$$\int  \mathcal{D}\boldsymbol{m}(\boldsymbol{x}) f[\boldsymbol{m},\partial \boldsymbol{m}\dots]=\lim_{ a \to 0 ,N\to \infty} \int  \prod_{i=1}^{N} dm_{i} \,f\left[ m_{i},\frac{m_{i+1}-m_{i}}{a},\dots \right]   $$
- In general, it _does not necessarily converge_

### Mean field theory
- Employ a _saddle-point approximation_, where $\boldsymbol{m}$ simply takes the _value_ where $\beta H$ is at a _minimum_
$$\mathcal{Z}\equiv e^{-\beta F[T,\boldsymbol{h}]}\qquad \beta F[T,\boldsymbol{h}]\approx \mathrm{min}_{\boldsymbol{m}}[\beta H[\boldsymbol{m},h]]$$
- For _stability_, $K>0$
	- Analagous to _kinetic energy_
- Therefore, a _mean field_ requires that $\nabla \boldsymbol{m}=0$ (a _uniform field_ $m$)

- _Landau mean field theory_ then has the free energy density:
	- $\beta F$ _cannot be factorised_
$$f(m,h)\equiv\frac{\beta F}{V}=\frac{t}{2}m^{2}+um^{4}-hm$$
- For $t>0$, ignoring the _quartic term_, $h$ simply _shifts_ the minimum to $h/t$
	- The field describes a _paramagnet_ as $\bar{m}(h=0)=0$
	- $1/t$ is the _susceptibility_, diverging as $t\to 0$
- For $t<0$, $u$ must be _positive_ to keep the system _stable_
	- With $h=0$, there is _spontaneous breaking of rotational symmetry in spins_, with two _degenerate_ minima with nonzero $\bar{m}$
	- Switching on $h$ will _break the degeneracy_ and favour one state over the other

- wlog, $t$ can be identified with the _reduced temperature_:
$$t(T, \dots)=\frac{T-T_{c}}{T_{c}}+\mathcal{O}(T-T_{c})^{2}$$
- The other parameters can then be expanded as:
$$\displaylines{u(T, \dots)=u_{0}+u_{1}(T-T_{c})+\mathcal{O}(T-T_{c})^{2} \\ K(T,\dots)=K_{0}+K_{1}(T-T_{c})+\mathcal{O}(T-T_{c})^{2}}$$
### Finding critical exponents
- From the functional form of these parameters, find the _thermodynamic properties in the mean field theory_

- _Minimisation_ of the free energy density gives the _mean magnetisation_:
$$\frac{\partial f}{\partial m}\Bigg|_{m=\bar{m}}=0\implies t\bar{m}+4u\bar{m}^{3}-h=0$$
- The _zero field_ condition gives the $\beta$ _critical exponent_ as $1/2$
	- The _amplitude_ is still material dependent
$$\bar{m}=\begin{cases}
0&t>0 \\\sqrt{ -t/4u }&t<0
\end{cases}$$
- $\bar{m}$ is _continuous_ across the critical point

- This then gives the _minimum free energy density_ for $h=0$:
$$f(\bar{m},h=0)=\begin{cases}
0 & t>0 \\ -t^{2}/16u &t<0
\end{cases}$$
- The corresponding _internal energy_:
$$E=-\frac{\partial \ln \mathcal{Z}}{\partial\beta}\qquad \frac{\partial}{\partial\beta}=-k_{B}T^{2} \frac{\partial}{\partial T}\approx-k_{B}T_{c}\frac{\partial}{\partial t}$$
- Heat capacity _purely due to magnetisation_
$$C=\frac{\partial E}{\partial T}=\begin{cases}
0&t>0 \\ k_{B}/8u &t<0
\end{cases}$$
- It is a _discontinuous second derivaitve_ of the _free energy_

- The _susceptibility_:
$$\chi\equiv \frac{\partial \bar{m}}{\partial h}\Bigg|_{h=0} \qquad \chi^{-1}=\begin{cases}
t& t>0 \\ -2t &t<0
\end{cases}$$
- The _ratio_ of $\chi_{-}/\chi_{+}=2$ before and after $t$ is also _universal_

- The _equation of state_ at the critical temperature:
$$\bar{m} \sim h^{1/\delta}$$
## Gaussian functional integration
- Consider the Gaussian integral:
$$\mathcal{Z}_{1}=\int  d\phi\,\exp\left( -\frac{\phi^{2}}{2G}+h\phi \right)=\sqrt{ 2\pi G }\exp\left( \frac{h^{2}}{2G} \right) $$
- The _one-point correlation_, or some _average_, from treating the exponential as some _probabilistic weight_:
$$\langle \phi \rangle=\frac{\partial \ln \mathcal{Z}_{1}}{\partial h} =hG$$
### Moments and cumulants
- The higher order _moments_ $\langle \phi^{r} \rangle$ of the probability distribution are given by the _cumulant expansion_
$$\langle \phi^{r} \rangle_{c}=\frac{\partial^{r}}{\partial k^{r}}\Bigg|_{k=0} \ln \langle e^{k\phi} \rangle  $$
- $\langle e^{k\phi} \rangle$ is the _moment generating function_
- The moments are related to the cumulants by _summing over all partitions of the product_ $\langle \phi^{n} \rangle$ into _subsets_ $\langle \phi^{n_{\alpha}} \rangle$
$$\langle \phi^{n} \rangle=\sum_{P} \prod_{\alpha}\langle \phi^{n_{\alpha}} \rangle_{c}  $$

- For example, the _second cumulant_ $\langle \phi^{2} \rangle_{c}$
$$\langle \phi^{2} \rangle_{c}=\partial_{k}^{2}\Big|_{k=0}\ln \langle e^{k\phi} \rangle=\langle \phi^{2} \rangle -\langle \phi \rangle^{2}=G   $$
- For a _Gaussian_ distribution, _higher cumulants vanish_

### General cumulant expansion
- With $N$ variables:
$$\mathcal{Z}_{N}=\int_{-\infty}^{\infty}\prod_{i=1}^{N}\,d\phi_{i} \,\exp\left[ -\frac{1}{2}\phi^{T}\mathbf{G}^{-1} \phi+\mathbf{h}\cdot \phi\right]$$
- In general, $\mathbf{G}^{-1}$ is _real and symmetric_

- Let there be some _unitary transformation_ $\mathbf{U}$ that _diagonalises_ $\mathbf{G}$
	- Generally, the integral only _converges for positive-definite eigenvalues_
$$\tilde{\mathbf{G}}^{-1}=\mathbf{UG}^{-1}\mathbf{U}^{-1}$$
- Completing the square in the integrand:
	- $\mathbf{U}$ is _unitary_, therefore the _Jacobian_ is unity
$$\displaylines{\chi=\mathbf{U}\phi-\tilde{\mathbf{G}}\mathbf{Uh} \\ \begin{align}
\mathcal{Z}_{N}&=\int_{-\infty}^{\infty}\prod_{i=1}^{N}d\chi_{i}\,\exp\left[ -\frac{1}{2}\chi^{T}\tilde{\mathbf{G}}^{-1}\chi+\frac{1}{2}\mathbf{h}^{T}\mathbf{U}^{-1}\tilde{\mathbf{G}}\mathbf{Uh} \right] \\ &=\det(2\pi \mathbf{G})^{1/2} \exp\left[ \frac{1}{2}\mathbf{h}^{T}\mathbf{Gh} \right]
\end{align}}$$
- With $\mathcal{Z}_{N}$ as the _probability distribution for the $N$ variables_, the cumulant expansion is:
$$\langle \phi_{i}\dots \phi_{j} \rangle_{c}=\frac{\partial }{\partial k_{i}}\dots \frac{\partial}{\partial k_{j}}\Bigg|_{\mathbf{k}=0} \ln \langle e^{\mathbf{k}\phi} \rangle  $$
- The moment generating function is:
$$\langle e^{\mathbf{k}\phi} \rangle= \exp\left[ \mathbf{h}^{T}\mathbf{Gk}+\frac{1}{2}\mathbf{k}^{T}\mathbf{Gk} \right]$$
- This gives the _first two cumulants_:
	- The higher cumulants vanish
$$\langle \phi_{i} \rangle_{c}=G_{ij}h_{j}\qquad \langle \phi_{i}\phi_{j} \rangle_{c}=G_{ij}  $$
- Combining the results, for any _linear combination_ of variables $A=\mathbf{a\cdot}\phi$
$$\langle e^{A} \rangle=\exp\left( \langle A \rangle_{c}+\frac{\langle A^{2} \rangle_{c}}{2}   \right) $$

### Functional integration
- Consider the _continuum limit_ of the Gaussian integral, into a _functional integral_
$$\displaylines{\int \mathcal{D}\phi(\boldsymbol{x})\exp\left[ -\frac{1}{2}\int  d\boldsymbol{x}\int  d\boldsymbol{x}'\,\phi(\boldsymbol{x})G^{-1}(\boldsymbol{x}-\boldsymbol{x}')\phi(\boldsymbol{x}') +\int  d\boldsymbol{x} \,h(\boldsymbol{x})\phi(\boldsymbol{x})  \right] \\ G^{-1}(\boldsymbol{x}-\boldsymbol{x}')=\braket{ \boldsymbol{x} |G^{-1}| \boldsymbol{x}' } }$$
- Generalising the result above:
$$\propto \det(G)^{1/2}\exp\left[ \frac{1}{2}\int  d\boldsymbol{x}\int  d\boldsymbol{x}' \,h(\boldsymbol{x})G(\boldsymbol{x},\boldsymbol{x}')h(\boldsymbol{x}')\right]$$
- The _inverse kernel_ satisfies:
$$\int  d\boldsymbol{x}'\,G^{-1}(\boldsymbol{x},\boldsymbol{x}')G(\boldsymbol{x}',\boldsymbol{x}'')=\delta^{d}(\boldsymbol{x}-\boldsymbol{x}'') $$
- The _prefactor_ of the path integral does not matter as it is _cancelled out_ when calculating moments and cumulants

- From this, the cumulants generalise to:
$$\langle \phi(\boldsymbol{x}) \rangle_{c}=\int  d\boldsymbol{x}'\,G(\boldsymbol{x}-\boldsymbol{x}')h(\boldsymbol{x}') \qquad \langle \phi(\boldsymbol{x})\phi(\boldsymbol{x}') \rangle_{c}=G(\boldsymbol{x}-\boldsymbol{x}')   $$
- From this, it can be seen that $G(\boldsymbol{x}-\boldsymbol{x}')$ is a _Green's function_

### Quadratic form
- Useful for calculating _fluctuations_ given a _quadratic_ function
$$\beta H[\phi]=\frac{1}{2}\int  d\boldsymbol{x} [|\nabla \phi|^{2}+\xi^{-2}\phi^{2}]=\frac{1}{2} \int  d\boldsymbol{x} \int  d\boldsymbol{x}' \phi(\boldsymbol{x}')\delta^{d}(\boldsymbol{x}-\boldsymbol{x}')(-\nabla^{2}+\xi^{-2})\phi(\boldsymbol{x}) $$
- This implies the _operator kernel_:
$$G^{-1}(\boldsymbol{x},\boldsymbol{x}')=\delta^{d}(\boldsymbol{x}-\boldsymbol{x}')(-\nabla^{2}+\xi^{-2})\implies (-\nabla^{2}+\xi^{-2})G(\boldsymbol{x},\boldsymbol{x}')=\delta^{d}(\boldsymbol{x}-\boldsymbol{x}')$$
- $G(\boldsymbol{x},\boldsymbol{x}')$ is the _Greens function_ for the operator $(-\nabla^{2}+\xi^{-2})$

- When _Fourier transformed_:
$$G(\boldsymbol{q})=\frac{1}{q^{2}+\xi^{-2}}$$
- This is related to the Fourier transform of the correlation function:
$$\langle \phi(q)\phi(q') \rangle_{c}=(2\pi)^{d}\delta^{d}(q+q')G(q) $$