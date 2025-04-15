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
$$m(T, h\to 0^{+})=\begin{cases}
0 &T>T_c \\ |t|^{\beta} &T<T_{c}
\end{cases}$$
- $t$ is the _reduced temperature_ $(T-T_{c})/T_{c}$

- Meanwhile, along the _critical isotherm_:
$$m(T=T_{c}, h)\propto h^{1/\delta}$$
### Response function
- Meanwhile, the _response functions_ can also be described by _critical exponents_, giving the _divergences_ near the critical point
	- Example: compressibility becoming infinite
- The _zero field susceptibility_:
$$\chi_{\pm}(T,h\to 0^{\pm})=\frac{\partial m}{\partial h}\Bigg|_{h=0^{\pm}}\propto|t|^{-\gamma_{\pm}}$$
- Often, the two _divergences_ have the _same power law_ $\gamma=\gamma_{+}=\gamma_{-}$

- Similarly, the _heat capacity_, as the _thermal response function_:
$$C_{\pm}=\frac{\partial E}{\partial T}\Bigg|_{h=0}\propto|t|^{-\alpha_{\pm}}$$
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
- Each microscopic magnetisation has the _same definition of susceptibility_:
$$k_{B}T\chi=\int  d\boldsymbol{x} \int  d\boldsymbol{x}'\,[\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle -\langle m(\boldsymbol{x}) \rangle\langle m(\boldsymbol{x}') \rangle  ]  $$
- As the system is _symmetric under translation_, $\langle m(\boldsymbol{x}) \rangle$ is a _constant_ $m$ while $\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle=G(\boldsymbol{x}-\boldsymbol{x}')$ is _only dependent on translation_

- The _connected correlation function_
$$\langle m(\boldsymbol{x})m(\boldsymbol{x}') \rangle_{C}\equiv \langle (m(\boldsymbol{r})-\langle m(\boldsymbol{r}) \rangle)(m(\boldsymbol{r}')-\langle m(\boldsymbol{r}') \rangle)  \rangle  =G(\boldsymbol{r}-\boldsymbol{r}')-m^{2}$$
- Susceptibility can then be expressed as:
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
	- $t$: a _free/inertial term_, similar to kinetic energy
	- $u$: an _interaction parameter_
	- $K,L$: punish _inhomogeneities_
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
- One can then add _fluctuations_ to $\beta H$ as deviations from $\beta F$

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
- The critical exponent:
	- $f(\bar{m})\propto t^{2-\alpha}$
$$\alpha_{+}=\alpha_{-}=0$$

- The _zero field susceptibility_:
$$\chi\equiv \frac{\partial \bar{m}}{\partial h}\Bigg|_{h=0} \qquad \chi^{-1}=\begin{cases}
t& t>0 \\ -2t &t<0
\end{cases}\implies \gamma=\gamma_{+}=\gamma_{-}=1$$
- For _mean field_, $\gamma_{+}=\gamma_{-}$

- The _equation of state_ at the critical temperature:
$$\bar{m} \sim h^{1/\delta}=h^{1/3}$$

- For _ferromagnets_, _mean field theory_ fails to agree with experiment
![[Mean field theory comparison.png]]
### Field theory for first order phase transition
$$\beta H=\int  d\boldsymbol{r}\,\left[ \frac{t}{2}m^{2}+um^{4}+vm^{6}+\frac{K}{2}|\nabla m|^{2}-h\cdot m \right] $$
- For $u>0$, there is a _second order phase transition_
- For $u<0$, there will be a _local minimum_ at $m^{*}\neq 0$, which for some $T_{c}$, there will be a _first order phase transition_
	- For $T>T_{c}$, there is a _metastable state_

- The point $v=u=0$ is the _tricritical point_, where the first and second order phase boundaries _intersect_
	- Example: type I and II superconductivity
![[Tricritical point.png]]

## Gaussian functional integration
- Consider the Gaussian integral:
$$\mathcal{Z}_{1}=\int  d\phi\,\exp\left( -\frac{\phi^{2}}{2G}+h\phi \right)=\sqrt{ 2\pi G }\exp\left( \frac{h^{2}G}{2} \right) $$
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
	- The higher cumulants vanish for a Gaussian distribution
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
## Hubbard-Stratonovich decoupling: from Ising model to Ginzburg-Landau
$$\beta H_\text{Ising}=-J\sum_{\langle ij \rangle }\sigma_{i}\sigma_{j}-h\sum_{i}\sigma_{i}$$
- The partition function is the _trace_
	- $K_{ij}$ is the coupling matrix, equal to $J$ for _neighbouring_ $i,j$
$$\mathcal{Z}=\mathrm{Tr}[e^{-\beta H}]=\sum_{\{\sigma_{i}\}}\exp\left[ \sum_{i,j}\sigma_{i}K_{ij}\sigma_{j}+h\sum_{i}\sigma_{i} \right]$$
- Introduce an _auxiliaru field_ $\phi$ via the _Hubbard-Stratonovich_ transformation:
$$\int  \mathcal{D}\phi \,\exp\left( -\frac{1}{2}\boldsymbol{\phi}\mathbf{K}^{-1} \boldsymbol{\phi+\boldsymbol{\phi}\cdot \boldsymbol{s}} \right)=\sqrt{ 2\pi \det K }\exp\left( \frac{1}{2}\boldsymbol{s} \mathbf{K}\boldsymbol{s}\right) $$
- The partition function, by doing the transformation in _reverse_ and introducing the _auxiliary field_ $\phi(\boldsymbol{r})$
	- Factor of $1/2$ compared to previous $\beta H$: double counting
$$\mathcal{Z}=\frac{1}{\sqrt{ 2\pi \det K }}\sum_{\{\sigma_{i}\}}\int \mathcal{D}\phi\exp\left[ -\frac{1}{2}\boldsymbol{\phi}\mathbf{K}^{-1} \boldsymbol{\phi}+ (\boldsymbol{h}+\boldsymbol{\phi})\cdot \boldsymbol{\sigma}\right] $$

- Summing over $\sigma_{i}=\pm 1$, the final formula for the partition function:
$$\mathcal{Z}\propto \int  \prod_{r}d\phi(r) \exp\left[ -\frac{1}{2}\sum_{r,r'}\phi(r)K^{-1}(r,r')\phi(r')+\sum_{r}\ln \cosh(\phi+h) \right] $$
- From _lattice translation symmetry_, with $d$ lattice vectors $\boldsymbol{a}_{j}$:
$$K(\boldsymbol{r},\boldsymbol{r}')=K(\boldsymbol{r}-\boldsymbol{r}')=J\sum_{j=1}^{d}\delta_{\mathbf{r}-\boldsymbol{r}',\boldsymbol{a}_{j}}+\delta_{\boldsymbol{r}-\boldsymbol{r}',-\boldsymbol{a}_{j}}$$

- Fourier transform of $K^{-1}$:
$$K^{-1}(\boldsymbol{r}-\boldsymbol{r}')=\int  \frac{d^dk}{(2\pi)^{d}}  \frac{\exp[i\boldsymbol{k}\cdot(\boldsymbol{r}-\boldsymbol{r}')]}{\tilde{K}(\boldsymbol{k})}$$
- Also Fourier transforming the fields, one can simply _integrate over the Brillouin Zone_
$$\frac{1}{2}\sum_{\boldsymbol{r},\boldsymbol{r}'}\phi(\boldsymbol{r})K^{-1}(\boldsymbol{r}-\boldsymbol{r}')\phi(\boldsymbol{r}')=\frac{1}{2}\int_\text{BZ} \frac{d^{d}k}{(2\pi)^{d}} \tilde{\phi}(\boldsymbol{k})^{*} \frac{1}{\tilde{K}(\boldsymbol{k})} \tilde{\phi}(\boldsymbol{k}) $$
- When _close to the critical point_, the relevant modes are _long wavelength_ compared to the _range of interaction_ $R$
$$\displaylines{|\boldsymbol{k}|R\ll 1 \\ \tilde{K}(\boldsymbol{k})=\tilde{K}(0)[1-(kR)^{2}+\mathcal{O}(k^{4})]\qquad \tilde{K}^{-1}=\frac{1}{\tilde{K}(0)}[1+k^{2}R^{2}+\mathcal{O}(k^{4})]}$$
- Going back to _real space_, with a _lattice spacing_ $a$
$$\sum_{\boldsymbol{r}}\to \int  \frac{d^dr}{a^{d}} \qquad k^{2}\to -\nabla^{2}$$
- From this, the partition function becomes:
$$\mathcal{Z}=\int  \mathcal{D}\phi \exp\left[-\int  \frac{d^{d}r}{a^{d}} \left( \frac{1}{2\tilde{K}(0)} \phi(1-R^{2}\nabla^{2})\phi\right)+\int  \frac{d^dr}{a^{d}}\ln[\cosh(\phi+h)]  \right] $$
- By _rescaling_ $\phi^{2}\to \tilde{K}(0)a^{d}\phi^{2}/R^{2}$
$$\displaylines{\mathcal{Z}=\int  \mathcal{D}\phi\,\exp\left[-\int  d^{d}r \left( \frac{1}{2}|\nabla \phi|^{2}+V(\phi) \right) \right] \\ \begin{align}
V(\phi)&=\frac{1}{2R^{2}}\phi^{2}-\frac{1}{a^{d}}\ln\left[ \cosh\left( \sqrt{ \frac{\tilde{K}(0)a^{d}}{R^{2}} }\phi+h \right) \right] \\ &=\frac{1}{2R^{2}} (1-\tilde{K}(0))\phi^{2}+\mathcal{O}\left( \frac{\tilde{K}(0)^{2}a^{d}}{R^{4}} \right)\phi^{4}
\end{align}}$$

- This links the _phenomenological parameters_ with microscopic parameters of the system

## Spontaneous symmetry breaking
- If a _Hamiltonian_ has some _continuous symmetry_ (e.g. translation, rotation), if the _ground state violates_ that symmetry, one has _spontaneous symmetry breaking_
- The ground states are _degenerate_ (e.g. aligned spins pointing in any dimension)
- The onset of _long-range order_ with the ground state is also associated with the _symmetry breaking_

- When spontaneous symmetry occurs, one can have _long wavelength excitations_, known as _Goldstone modes_
	- An _infinitely long wavelength_ excitation would simply _shift to a different degenerate ground state_

### Fluctuations in a 2-component spin model
- Take a _2-component spin model_
	- Ising model is 1-component, and does not have continuous symmetry
$$\beta H=\int  d^dx\,\left[ \frac{t}{2}\boldsymbol{m}^{2}+u\boldsymbol{m}^{4}+\frac{K}{2}|\nabla \boldsymbol{m}|^{2}-\boldsymbol{h}\cdot \boldsymbol{m} \right] $$
- For $t<2$, one has a _Mexican hat potential_, where there is some _set of degenerate ground states_

- Take for $T<T_{c}$:
$$\boldsymbol{m}=m \pmatrix{\cos\theta \\ \sin\theta}$$
- The free energy is then:
	- Only $\nabla\theta$ is a _Gaussian distributed variable_, $\theta$ itself is _uniformly distributed_
$$\beta H[\theta]=\beta H_{0}+ \frac{\bar{K}}{2}\int  d^d x|\nabla\theta|^{2}$$
- The field $\theta(\boldsymbol{x})$ is $2\pi-$periodic

- Take _fluctuations_ to be _small_ $(\ll 2\pi)$, in the _low temperature limit_ such that one can approximate this as a _Gaussian integral_
	- At higher temperatures, periodicity causes _topological effects_ such as _vortices_

- From the results of [[#Quadratic form|Gaussian functional integration]], the _correlation functions_ are:
$$\displaylines{\langle \theta(\boldsymbol{x}) \rangle=0 \\ G(\boldsymbol{x},\boldsymbol{x}')=\langle \theta(\boldsymbol{x})\theta(\boldsymbol{x}') \rangle=G(\boldsymbol{x}-\boldsymbol{x}')=-\frac{C_{d}(\boldsymbol{x}-\boldsymbol{x}')}{\bar{K}}  \\ \nabla^{2}C_{d}(\boldsymbol{x})=\delta^{d}(\boldsymbol{x})}$$

- $C_{d}$ is the _Coulomb potential_ for a $\delta-$function charge distribution
	- It should only depend on the _radial distance_
	- Here, $S_{d}x^{d-1}$ is the _surface area_ of a sphere in $d-$space
	- Result _does not apply_ for $d\leq 2$, where $C_{2}(x)\sim \ln|x|$
$$\displaylines{1=\int_{V}  d^{d}x \,\nabla^{2}C_{d}(\boldsymbol{x})=\oint d\boldsymbol{S}\cdot \nabla C_{d}=S_{d}\,x^{d-1}\,\frac{dC_{d}}{dx}  \\ \frac{dC_{d}}{dx}=\frac{1}{x^{d-1}S_{d}} \qquad C_{d}(x)=\frac{x^{2-d}}{(2-d)S_{d}}+\text{const.}}$$
- For _small distances_ in $d>2$, one has to introduce a _high momentum cut-off_ corresponding to the _lattice spacing_ $a$:
$$\langle \theta(0)^{2} \rangle=\frac{a^{2-d}}{(2-d)S_{d}} $$
### Long range order and the Mermin-Wagner theorem
- Calculating the _two-point correlation_ for the _order parameter_, from the [[#General cumulant expansion|cumulant expansion]], it is related to the _correlation for fluctuations_
$$\langle \boldsymbol{m}(\boldsymbol{x})\cdot \boldsymbol{m}(0) \rangle=\bar{m}^{2}\mathrm{Re} \langle \exp({i[\theta(\boldsymbol{x})-\theta(0)])} \rangle =\bar{m}^{2} \exp\left[ -\frac{1}{2}\langle [\theta(\boldsymbol{x})-\theta(0)]^{2} \rangle  \right]$$
- Interpretation: _large fluctuations_ will _reduce long-range order_

- Neglecting _topological (vortex)_ configurations, by plugging in the Greens function:
$$\displaylines{\langle \boldsymbol{m}(\boldsymbol{x})\cdot \boldsymbol{m}(0) \rangle=\bar{m}^{2}\exp\left[ -\frac{x^{2-d}-a^{2-d}}{\bar{K}(2-d)S_{d}} \right]  \\ \lim_{ |\boldsymbol{x}| \to \infty }  \langle \boldsymbol{m}(\boldsymbol{x})\cdot \boldsymbol{m}(0) \rangle=\begin{cases}
\bar{m}^{2} &d>2 \\ 0 & d\leq 2
\end{cases} }$$
- At $d>2$, fluctuations are _finite_ and have a _power law decay_, therefore the _saddle point approximation_ and mean field theory hold
- For $d\leq 2$, fluctuations _destroy long-range order_ and the saddle point approximation fails
	- For $d<2$, there is an _exponential decay_ in the correlation function

- A consequence of the _Mermin-Wagner theorem_:
- Systems with _continuous symmetry_ and _short-range interactions_ can _not have long-range order_ for _dimensions_ $\leq 2$

- $d=2$ is the _lower critical dimension_
	- In other models (e.g. superfluids), there is a _phase transition_ at this dimension without long range order
	- Correlation decays as a _power law_, not exponentially (_quasi-long range order_)
	- For _discrete symmetries_ (e.g. $\mathbb{Z}_2$), the lower critical dimension is $d=1$

## Fluctuations in mean field theory
- Back to Landau theory:
$$\beta H[\boldsymbol{m}(\boldsymbol{x})]=\int  d^dx \,\left[\frac{t}{2}m^{2}+um^{4}+\frac{\kappa}{2}|\nabla m|^{2} \right]$$
- Parametrise $\boldsymbol{m}$ as the _mean field_ value, as well as _longitudinal_ and _transverse_ fluctuations
$$\boldsymbol{m}(\boldsymbol{x})=(\bar{m}+ \varphi_{l}(\boldsymbol{x}))\hat{e}_{l}+\sum_{\alpha=2}^{n}\varphi_{t} \hat{e}_{\alpha}$$
### Fluctuation contribution to Hamiltonian
- Contributions to free energy, keeping only _quadratic_ terms in fluctuation:
$$\displaylines{|\nabla \boldsymbol{m}|^{2}=|\nabla \varphi_{l}|^{2}+|\nabla \varphi_{t}|^{2} \\ m^{2}=\bar{m}^{2}+2\bar{m}\varphi_{l}+\varphi_{l}^{2}+\varphi_{t}^{2} \\ m^{4}=\bar{m}^{4}+4\bar{m}^{3}\varphi_{l}+6\bar{m}^{2}\varphi_{l}^{2}+2\bar{m}^{2}\varphi_{t}^{2}}$$
- From this, _expand_ the Hamiltonian, to get the sum of the _mean field free energy_ and contributions from _fluctuations_
$$\begin{align}
\beta H=V\left( \frac{t}{2}\bar{m}^{2}+u\bar{m}^{4} \right)&+\int  d\boldsymbol{x}\,\left[ \frac{\kappa}{2}|\nabla \phi_{l}|^{2}+\frac{t+12u\bar{m}^{2}}{2}\phi_{l}^{2} \right] \\ &+ \int  d\boldsymbol{x} \left[ \frac{\kappa}{2}|\nabla \phi_{t}|^{2}+\frac{t+4u\bar{m}^{2}}{2}\phi_{t}^{2} \right] 
\end{align}$$
- The $l,t$ modes are _decoupled_ in the second order

- This can be seen as a combination of _kinetic terms_ and _potential terms_
	- $\kappa$ is the _stiffness_ due to inhomogeneities, hence why it is relevant for fluctuations
- One can then define a _characteristic lengthscale_:
$$\begin{align}
\frac{K}{\xi_{l}^{2}}&\equiv t+12u\bar{m}^{2}=\begin{cases}
t&t>0 \\ -2t &t<0
\end{cases}\\ \frac{K}{\xi_{t}^{2}}&\equiv t+4u\bar{m}^{2}=\begin{cases}
t&t>0 \\ 0&t<0
\end{cases}
\end{align}$$
- _Above_ the critical temperature, the system has _no preferred direction_, such that the _lengthscale is the same in both directions_
- The _transverse_ mode has _no energetic cost_, as it corresponds to the _Goldstone mode_ (moving among the degenerate ground states with _long wavelength_/correlation length)

- Considering the free energy in _reciprocal space_:
$$\beta H=\int  \frac{d\boldsymbol{q}}{(2\pi)^{d}} \frac{K}{2}[(q^{2}+\xi_{l}^{-2})|\phi_{l}(\boldsymbol{q})|^{2}+(q^{2}+\xi_{t}^{-2})|\phi_{t}(\boldsymbol{q})|^{2}]$$
### Fluctuations in reciprocal space and structure factor
- The _correlations_, where $\alpha,\beta=l,t$
$$C_{\alpha,\beta}(\boldsymbol{q},\boldsymbol{q}')=\langle \phi_{\alpha}(\boldsymbol{q})\phi_{\beta}(\boldsymbol{q}') \rangle $$
- Use the fact that the system is _translationally invariant_, from [[#Quadratic form|Gaussian integration]]
$$\langle \phi_{\alpha}(\boldsymbol{q})\phi_{\beta}(\boldsymbol{q}') \rangle=\delta_{\alpha\beta}(2\pi)^{d}\delta^{d}(\boldsymbol{q}+\boldsymbol{q}')G_{\alpha}(\boldsymbol{q})\qquad G_{\alpha}^{-1}(\boldsymbol{q})=K(q^{2}+\xi_{\alpha}^{-2}) $$
- This is a _Lorentzian_ 

- This is related to the _structure factor_, related to the _Fourier density_ of scatterers:
$$S(\boldsymbol{q})\propto \langle |\boldsymbol{m}(\boldsymbol{q})|^{2} \rangle $$
- It is a _peak due to long-range order_ at $q=0$, along with _fluctuations_:
$$S_{l,t}(\boldsymbol{q})\propto \langle |\phi_{l,t}(\boldsymbol{q})|^{2} \rangle+\bar{m}^{2}\delta^{d}(q \boldsymbol{}) $$
- As $t\to 0^{+}$, from the formula for $\xi$, one then gets:
$$S(\boldsymbol{q},T\to T_{c}^{+})\propto \frac{1}{q^{2}}$$
![[Ising fluctuations structure factor.png|500]]
- _Experimentally_, scattering at critical temperature follows a _power law_ with universal exponent $\eta$
$$S(\boldsymbol{q},T=T_{c})\propto \frac{1}{q^{2-\eta}}$$

### Fluctuations in real space and susceptibility
- The _real space correlator_: 
$$\langle \phi_{\alpha}(\boldsymbol{x})\phi_{\beta}(0) \rangle=-\frac{\delta_{\alpha\beta}}{K} I_{d}(\boldsymbol{x},\xi) \qquad I_{d}(\boldsymbol{x},\xi)=-\int  \frac{d\boldsymbol{q}}{(2\pi)^{d}} \frac{e^{i\boldsymbol{q}\cdot \boldsymbol{x}}}{q^{2}+\xi^{-2}} $$
- Inspect:
$$\nabla^{2}I_{d}=\delta^{d}(\boldsymbol{x})+\frac{I_{d}}{\xi^{2}}$$
- From this, one can get the asymptotic behaviour for _fluctuations_:
$$I_{d}(\boldsymbol{x},\xi)=\begin{cases}
C_{d}(\boldsymbol{x})=\frac{|\boldsymbol{x}|^{2-d}}{(2-d)S_{d}} &|\boldsymbol{x}|\ll \xi \\ \frac{\xi^{2-d}}{2-d} \frac{\exp(-|\boldsymbol{x}|/\xi)}{|\boldsymbol{x}/\xi|^{(d-1)/2}} &|\boldsymbol{x}|\gg \xi
\end{cases}$$
- One can then interpret $\xi$ as some _correlation length_ for _fluctuations_
- Correlation lengths _near criticality_:
$$\xi_{l}=\begin{cases}\sqrt{ K/t } &t>0 \\ \sqrt{ K/2|t| } &t<0\end{cases} \qquad \xi_{t}=\begin{cases}\sqrt{ K/t } &t>0 \\ \infty &t<0\end{cases}$$
- They can be described using:
	- Both $\nu$ and $B_{+}/B_{-}$ are _universal_, $\xi_{0}\propto \sqrt{ K }$ is _specific_ to the model
$$\xi_{\pm}\sim \xi_{0}B_{\pm}|t|^{-\nu_{\pm}} \implies \nu_{\pm}=\nu=\frac{1}{2} \qquad \frac{B_{+}}{B_{-}}=\sqrt{ 2 }$$
- The above also implies that for the _experimental decay exponent_ $\eta$:
$$\langle \phi(\boldsymbol{x})\phi(0) \rangle\sim \frac{1}{|\boldsymbol{x}|^{d-2}}\sim \frac{1}{|\boldsymbol{x}|^{d-2-\eta}}\implies \eta=0$$

- The Greens function then looks like:
![[Ising real space correlation.png|500]]
- The _longitudinal susceptibility_, with some _cut-off length_ $\xi_{l}$
$$\chi_{l}\propto\int  d^{d}\boldsymbol{x}\,G_{l}(\boldsymbol{x})\propto \int_{0}^{\xi_{l}}  d\boldsymbol{x} \frac{1}{|\boldsymbol{x}|^{d-2}} \propto \xi_{l}^{2} \sim A_{\pm} t^{-1}  $$
- The _transverse susceptibility_ for $T<T_{c}$, with cut-off being the _system size_ $L$:
	- $T>T_{c}: \chi_{l}=\chi_{t}$
$$\chi_{t}\propto \int_{0}^{L}  d\boldsymbol{x} \frac{1}{|\boldsymbol{x}|^{d-2}} \propto L^{2} $$
### Free energy correction due to fluctuations
- The _partition function_ contains a _correction_ due _fluctuations_ giving extra configurations
	- $\alpha$ counts _dimensions_, including both $l$ and $t$
$$\mathcal{Z}=\exp(-\bar{f}V) \int \frac{1}{a_{0}^{d}}  \prod_{\boldsymbol{q},\alpha}\,d\phi_{\boldsymbol{q}}^{\alpha}\,d\phi_{-\boldsymbol{q}}^{\alpha} \exp\left( -\frac{K}{2}\sum_{\boldsymbol{q}}(q^{2}+\xi_{\alpha}^{-2})|\phi_{\boldsymbol{q}}^{\alpha}|^{2} \right) $$
- Transforming to _real_ and _imaginary_ parts, and doing the Gaussian integrals, one gets the expected _decoupled_ partition function
$$\mathcal{Z}=\exp(-\bar{f}V)\prod_{\boldsymbol{q},\alpha} \sqrt{ \frac{2\pi}{Ka_{0}^{d}(q^{2}+\xi_{\alpha}^{-2})} }$$
- Alternatively, consider the identity:
$$\displaylines{\ln \det G=\mathrm{tr}\ln G \\ f=-\frac{\ln \mathcal{Z}}{V}=\bar{f}-\frac{1}{V}\ln\left(\int  \mathcal{D}\phi_{\boldsymbol{q}}^{\alpha} \exp\left( -\frac{K}{2}\sum_{\boldsymbol{q},\alpha} (q^{2}+\xi_{\alpha}^{-2})|\phi^{\alpha}_{\boldsymbol{q}}|^{2}\right) \right)}$$


- The _free energy density_ with fluctuation corrections, from either method:
$$f=-\frac{\ln \mathcal{Z}}{V}=\bar{f}+\frac{1}{2}\sum_{\alpha} \int  \frac{d\boldsymbol{q}}{(2\pi)^{d}} \ln[K(q^{2}+\xi_{\alpha}^{-2})]  $$
### Heat capacity due to fluctuations
- Corresponding heat capacity:
$$C\propto-\frac{d^{2}f}{dt^{2}}=\begin{cases}
0+\frac{n}{2}\int   \frac{d\boldsymbol{q}}{(2\pi)^{d}} (Kq^{2}+t)^{-2} &t>0 \\ \frac{1}{8u}+2\int  \frac{d\boldsymbol{q}}{(2\pi)^{d}} (Kq^{2}-2t)^{-2} &t<0 
\end{cases}$$
- For $d>4$, the _contribution_ from fluctuations will _diverge_, unless one implements a _high-momentum cut-off_ $a^{-1}$, in which case the _value at cutoff dominates_
- For $d<4$, the integral is _convergent_ regardless of cutoff

- The fluctuation heat capacity then follows the _power law_ (from _rescaling_ the integral):
$$C_\text{fluc}\sim \begin{cases}
a^{4-d}/K^{2} &d\geq4 \\ \xi^{4-d}/K^{2} &d<4
 \end{cases}$$
 ![[Fluctuation heat capacity.png|400]]
- For $d\geq 4$, there are _constant shifts_ in heat capacity

- For $d<4$, due to the _correlation length_ going to $0$, there is a _divergence in heat capacity_ at $T_{c}$ due to fluctuations near the saddle point
- There is an _upper critical dimension_ of $d_{u}=4$
	- _Between lower_ and _upper_ crititcal dimensions, _long-range order_ still _exists_ but the _critical behaviour_ is _modified_

### Ginzburg criterion
- For some materials (e.g. superconductors), the _experimental data matches mean field theory_ (see [[#Finding critical exponents|here]])
- The _experimental temperature resolution_ may _not be enough to resolve_ the _peak_ from fluctuations

- For some temperature $t<t_{G}$, fluctuations become important _relative to the mean-field discontinuity_ such that the _divergence can be detected_

- For a _given_ $t$, the _mean field_ description _becomes unfeasible_ if the _fluctuation contribution_ is _bigger_ than the _discontinuity from the mean field_
$$\frac{\Delta C_\text{fluc}}{\Delta C_\text{MF}}\gg 1$$
- Let the relevant _lengthscale_ when calculating $\Delta C_\text{fluc}$ be $\xi_{0}\sim \sqrt{ K }$, such that:
$$\left( \frac{\xi_{0}}{a} \right)^{-d}|t|^{(d-4)/2}\gg \left( \frac{\Delta C_\text{MF}}{k_{B}} \right)\implies |t|\ll t_{G} \sim \frac{1}{[(\xi_{0}/a)^{d}(\Delta C_\text{MF}/k_{B})]^{2/(4-d)}}$$
- If the _experimental resolution_ is _larger_ than $t_{G}$, measurements will _agree with mean field theory_

- For _superconductors_, $t_{G} \sim 10^{-16}$
- For _superfluids_, $t_{G} \sim 10^{-2}$

### Generalised criticality
- Let the _interaction term_ in the free energy be:
$$u_{2n}m^{2n}$$
- The _fluctuation heat capacity_ is _unchanged_
- However, the _mean field heat capacity_ has a different power law
- The upper critical dimension for the theory is then:
$$d_{u}=\frac{2n}{n-1}$$
- The _minimum_ value of $d_{u}$ is $d=2$

- The lower and upper critical dimensions, defined by _the effect of fluctuations_
![[Lower upper critical dimensions.png]]

# Scaling hypothesis

## Homogeneity
- Let the free energy be some _homogeneous function_
	- The presence of _critical points_ and _branch cuts_ (phase transition line) means one cannot use an analytic function
	- $p$ is the _order_ of the homogeneous function
$$f(\lambda t,\lambda h, \dots)=\lambda^{p}f(t,h, \dots)$$
- For the mean field theory:
$$f=\frac{t}{2}m^{2}+um^{4}-hm$$
- There is a _branch cut_, or a _coexistence line_ for $t<0,h=0$ which _terminates_ at critical point $t=h=0$
![[Free energy branch cut.png|250]]

- From _mean field_ theory:
$$f=\mathrm{min}_{\boldsymbol{m}}\left[ \frac{t}{2}m^{2}+um^{4}-hm \right]=\begin{cases}
-t^{2}/u &h=0,t\neq 0 \\ -h^{4/3}/u^{1/3} &h\neq 0,t=0
\end{cases}$$
- The homogeneous function can then be written as:
$$f_\text{mf}(t,h)=|t|^{2}g_{f}\left( \frac{h}{|t|^{\Delta}} \right)$$
- $\Delta$ is the _gap exponent_
- From comparing to the results of mean-field theory:
$$\displaylines{ \lim_{ x \to 0 } g_{f}(x)=-\frac{1}{u} \qquad \lim_{ x \to \infty }g_{f}(x)=\frac{x^{4/3}}{u^{1/3}} \\ \Delta=\frac{3}{2}}$$

### Exponent identities
- When taking _fluctuations_ into account, the _hypothesis_ for the part of _free energy_ with _singular behaviour_ is:
$$f_\text{sing.}=|t|^{2-\alpha}g_{f}\left( \frac{h}{|t|^{\Delta}} \right)$$
- Heat capacity:
	- The _derivative_ of a homogeneous function is _another homogeneous function_
	- As the function is _analytic outside the coexistence line_, $\alpha_{+}=\alpha_{-}$
$$\displaylines{E_\text{sing.}\sim\frac{\partial f}{\partial t}\sim |t|^{1-\alpha}\left[ (2-\alpha)g_{f}\left( \frac{h}{|t|^{\Delta}} \right)-\frac{\Delta h}{|t|^{\Delta}}g_{f}'\left( \frac{h}{|t|^{\Delta}} \right) \right]\equiv |t|^{1-\alpha }g_{E}\left( \frac{h}{|t|^{\Delta}} \right) \\ C_\text{sing.}\sim |t|^{-\alpha} g_{C}\left( \frac{h}{|t|^{\Delta}} \right)}$$
- This reproduces the typical _scaling_ of $C$ with $t$

- Magnetisation:
$$m(t,h)\sim \frac{\partial f}{\partial h}\sim |t|^{2-\alpha-\Delta}g_{m}\left( \frac{h}{|t|^{\Delta}} \right)$$
- In the limit of $x\to 0$, $g_{m}(x)$ is a _constant_:
$$m(t,h=0)\sim |t|^{2-\alpha-\Delta}$$
- For $x\to \infty$, $g_{m}(x)\sim x^{p}$, such that $m$ is _independent_ of $t$:
$$m(t=0,h)\sim |t|^{2-\alpha-\Delta} \left( \frac{h}{|t|^{\Delta}} \right)^p\sim h^{(2-\alpha-\Delta)/\Delta}$$
- Finally, _susceptibility_:
$$\chi(t,h)\sim\frac{\partial m}{\partial h}\sim |t|^{2-\alpha-2\Delta}g_{\chi}\left( \frac{h}{|t|^{\Delta}} \right)\implies \chi(t,h=0)\sim |t|^{2-\alpha-2\Delta}$$

- The assumption of _homogeneity_ then implies:
	- Exponents are the _same above and below transition_
	- The _same gap exponent_ $\Delta$ applies for all quantities
	- All _bulk critical exponents_ can be obtained from _two independent exponents_ $\alpha,\Delta$

- _Exponent identities_ from homogeneity:
$$\displaylines{\alpha+2\beta+\gamma=2 \\ \delta-1=\frac{\gamma}{\beta}}$$
## Hyperscaling
- Homogeneity is an assumption applied to _free energy_ in _mean-field theory_

- Account for _fluctuations_ and _correlations_
- For _correlation functions_ and their divergence, one needs to _further assume_:
	- Close to _criticality_, the _only relevant lengthscale_ is $\xi$, and is _solely responsible_ for divergences in thermodynamic quantities
	- Correlation length $\xi$ is a _homogeneous function_ 	$$\xi(t,h)\sim |t|^{-\nu}g\left( \frac{h}{|t|^{\Delta}} \right)$$
- $\ln Z$ is _extensive and dimensionless_, obtained by _adding contributions from units_ divided by either a _microscopic length-scale_, or the _correlation length_ 
$$\ln Z=\left( \frac{L}{\xi} \right)^{d}g_{s}+\dots+\left( \frac{L}{a} \right)^{d}g_{a}$$
- The _first term_ is responsible for _singular behaviour_, giving:
$$f_\text{sing.}(t,h)\sim \frac{\ln Z}{L^{d}}\sim \xi^{-d}\sim |t|^{d\nu}g_{f}\left( \frac{h}{|t|^{\Delta}} \right)$$
- The _singular behaviour_ arises from _homogeneity of correlation length_
- An additional _exponent relation_:
$$2-\alpha=d\nu$$
- This gives the _hyperscaling relations_ in terms of $d$

## Correlation functions and self-similarity
- Correlation functions only have the _relevant lengthscale_ of $\xi$, which _diverges_ at criticality

- The exponent $\eta$:
$$G_{c}(\boldsymbol{x})\equiv \langle \boldsymbol{m}(\boldsymbol{x})\cdot \boldsymbol{m}(0) \rangle-\langle m^{2} \rangle \sim \frac{1}{|\boldsymbol{x}|^{d-2+\eta}}  $$
- _Away from criticality_, the power laws are _cut-off_ for distances $|\boldsymbol{x}|\gg \xi$
- The _response function_ is then:
$$\chi \sim \int  d^d\boldsymbol{x}\, G_{c}(\boldsymbol{x})\sim \int^{\xi}  \frac{d^{d}\boldsymbol{x}}{|\boldsymbol{x}|^{d-2+\eta}}\sim \xi^{2-\eta}\sim t^{-\nu(2-\eta)}  $$

- Final exponent relation:
$$\gamma=(2-\eta)\nu$$

- Under a _change of scale_:
$$G_\text{crit}(\lambda \boldsymbol{x})=\lambda^{p}G_\text{crit}(\boldsymbol{x})$$

- This indicates _statistical self-similarity_
	- Apart from a _change of contrast_, the _statistical properties_ are the same
	- In 2D: can be accounted for with a _conformal field theory_
	- In other dimensions: the _renormalisation group_

# Renormalisation Group
- The only relevant lengthscale in a system is $\xi$

- Renormalisation: a method of _eliminating features at lengthscale_ $x\ll \xi$

## Renormalisation of spin models: the Migdal-Kadanoff method
## Renormalisation procedure
- First, _coarse-grain_ the system from _microscopic lengthscale_ $a$ to $ba$, where $b>1$
- This is accomplished by _integrating out fluctuations_ on lengthscales $<ba$
	- For $\boldsymbol{x}$, integrate _over a cell_ of width $ba$ centred on $\boldsymbol{x}$
$$\bar{\boldsymbol{m}}(\boldsymbol{x})=\frac{1}{(ba)^{d}} \int_\text{cell}  d\boldsymbol{y}\,\boldsymbol{m}(\boldsymbol{y}) $$
- The _new Hamiltonian_ is expressed in terms of the _coarse-grained magnetisation_ $\bar{\boldsymbol{m}}$

- Then, to _restore_ the resolution on the system, _rescale_ the system size:
$$\boldsymbol{x}'=\frac{\boldsymbol{x}}{b}$$

- The _relative size_ of features will have changed, therefore _rescale_ the order parameter by some factor $\zeta$
$$\boldsymbol{m}'(\boldsymbol{x}')=\frac{1}{\zeta}\bar{\boldsymbol{m}}(\boldsymbol{x}')$$
![[Renormalisation process.png|400]]
- At _criticality_, the _rescaled_ Hamiltonian is _still at criticality_

- When _off criticality_, the Hamiltonian is _taken further off criticality_ as $\xi'=\xi/b<\xi$

- Renormalisation is a _semi-group_ as the _short-scale information is lost_ in coarse-graining
### Brehaviour of renormalised parameters
- Renormalisation only _involves very short lengthscales_, therefore it _cannot cause singularities_, and the _renormalised parameters_ are _analytic functions_

- Assume that the _form_ of the Hamiltonian is the _same_, and can be sufficiently described by parameters $t,h$

- There are _no constant terms_ as the _critical point_ $t=h=0$ is _preserved_
$$\begin{align}
t(b;t,h)&=A(b)t+B(b)h+\dots \\ h(b;t,h)&=C(b)t+D(b)h+\dots
\end{align}$$

- To avoid _spontaneously broken symmetry_ during the transformation, the system should be invariant under $h\to-h,\,t\to t$
$$B(b)=C(b)=0$$

- The re-scaling process is _commutative_:
$$A(b_{1}b_{2})=A(b_{1})A(b_{2})$$
- Meanwhile, trivially:
$$A(1)=D(1)=1$$

- This implies the _functional form_ of the parameters under _rescaling_:
$$t(b)=b^{y_{t}}t\qquad h(b)=b^{y_{h}}h$$
- For $\xi$ to diminish, $y_{t},y_{h}>0$
### Recovering scaling relations
- After _renormalisation_, the _statistical weight_ of the _new configuration_ is some _sum_ of the old configuration

- The _partition function_, being a _sum of weights_, is _unchanged_:
$$\mathcal{Z}=\mathcal{Z}'$$
- The _free energy density_ is then:
$$f(t,h)=- \frac{\ln \mathcal{Z}}{V}=-\frac{\ln \mathcal{Z}'}{V'b^{d}}=b^{-d}f(b^{y_{t}}t,b^{y_{h}}h)$$
- The _free energy_ is a _homogeneous function_
- One can _choose_ $b$ such that:
$$b^{y_{t}}=1\implies f(t,h)=t^{d/y_{t}}f(1,h/t^{y_{h}/y_{t}})\equiv t^{d/y_{t}}g_{f}\left( \frac{h}{t^{y_{h}/y_{t}}} \right)$$
- One can then identify $y_{h}/y_{t}$ as the [[#Homogeneity|gap exponent]]

- $y_{h}$ and $y_{t}$ are the _independent variables required_ to find all critical exponents:
$$2-\alpha=\frac{d}{y_{t}}\qquad \Delta=\frac{y_{h}}{y_{t}}$$
- The same is true for the _correlation length_:
$$\xi(t,h)=b\xi(b^{y_{t}}t,b^{y_{h}}h)=t^{-1/y_{t}}g_{\xi}\left( \frac{h}{t^{y_{h}/y_{t}}} \right)\sim t^{-\nu}$$
- The [[#Hyperscaling|hyperscaling relation]] is then given:
$$2-\alpha=d\nu$$
- Magnetisation:
$$m(t,h)=-\frac{1}{V}\frac{\partial \ln Z(t,h)}{\partial h}=-\frac{1}{b^{d}V'}\frac{\partial \ln Z'(t',h')}{b^{-y_{h}}\partial h'}=b^{y_{h}-d}m(b^{y_{t}}t,b^{y_{h}}h)$$
- With $b=t^{-1/y_{t}}$, one gets:
$$\beta=\frac{y_{h}-d}{y_{t}}$$
- One also gets similar relations for _heat capacity_ and _susceptibility_

- In general, the _singular part_ of any physical quantity $X$ has the _homogeneous form_:
$$X(t,h)=b^{y_{X}}X(b^{y_{t}}t,b^{y_{h}}h)=t^{-y_{X}/y_{t}}g_{X}\left( \frac{h}{t^{y_{h}/y_{t}}} \right)$$
- For _conjugate variables_ that contribute $\int  d^dx\, FX$  to the _Hamiltonian_ (e.g. $m$ and $h$):
$$y_{X}=y_{F}-d$$
## Formal approach to renormalisation

### Formal renormalisation procedure
- Given the _most general Hamiltonian_ allowed by _symmetry_:
$$\beta H[\boldsymbol{m}]=\int  d^dx\left[ \frac{t}{2}m^{2}+um^{4}+vm^{6}+\dots+\frac{K}{2}|\nabla \boldsymbol{m}|^{2}+\frac{L}{2}|\nabla^{2}\boldsymbol{m}|^{2}+\dots \right] $$
- This Hamiltonian exists in some _parameter space_:
$$\boldsymbol{S}=(t,u,v,\dots K,L, \dots)$$
- The steps of _renormalisation_:
	1. _Coarse grain_ $\boldsymbol{m}$ by length factor $b$
	2. _Rescale_ $\boldsymbol{x}'=\boldsymbol{x}/b$
	3. _Renormalise_ $m'=m/\zeta$
- Giving the _change of variables_:
$$m'(\boldsymbol{x}')=\frac{1}{\zeta b^{d}} \int_{\text{cell centred at }b\boldsymbol{x}'}  d^{d}x\,m(\boldsymbol{x}) $$
- Given the _un-renormalised probabilities_ $\mathcal{P}[\boldsymbol{m}(\boldsymbol{x})]\propto \exp(-\beta H[\boldsymbol{m}])$, the _new theory_ is described by the probabilities $\mathcal{P}'[m'(\boldsymbol{x}')]$

- As renormalisation _preserves symmetry_, the Hamiltonian _lives in the same parameter space_ with _renormalised parameters_
$$\beta H'[\boldsymbol{m}']=f_{b}+\int  d^dx'\left[ \frac{t'}{2}m'^{2}+u'm'^{4}+v'm'^{6}+\dots+\frac{K'}{2}|\nabla \boldsymbol{m}'|^{2}+\frac{L'}{2}|\nabla^{2}\boldsymbol{m}'|^{2}+\dots \right]$$
- The _renormalised parameters_ are _functions of the original_:
	- In general, they are _non-linear_
$$t'=t(b;t,u,\dots)\qquad u'=u(b;t,u, \dots)$$
### Renormalisation group flow, fixed points, and basins
- Renormalisation is a _mapping in parameter space_
$$S'=\mathcal{R}_{b}S$$

- $\mathcal{R}_{b}$ describes the effects of _dilation_
- A _self-similar_ configuration is given by a _fixed point_ in parameter space
- As renormalisation _reduces correlation length_ by a factor of $1/b$, fixed points must be:
	- $\xi'=0$, describing _independent fluctuations_ at each point, meaning _complete disorder_ ($T\to \infty$) or _complete order_ $(T\to 0)$
	- $\xi'=\infty$, describing a _crtitical point_ $(T=T_{c})$

- Equations [[#Brehaviour of renormalised parameters|here]] describe a _2D parameter space_, where $t=h=0$ is a _fixed point_

- In general, _stability_ can be studied by _linearising the recursion relations_ around it
- The point $\boldsymbol{S}^{*}+\delta \boldsymbol{S}$ is _transformed_ under renormalisation:
$$S_{i}^{*}+\delta S_{i}'=S_{i}^{*}+\sum_{j}[\mathcal{R}_{b}]_{ij}\delta S_{j}+\dots \qquad [\mathcal{R}_{b}]_{ij}=\frac{\partial S_{i}'}{\partial S_{j}}\Bigg|_{\boldsymbol{S}^{*}}$$
- The matrix $\mathcal{R}_{b}$ can be _diagonalised_ to give eigenvectors $\mathcal{O}_{i}$ with their associated eigenvalues $\lambda(b)_{i}$
- From the _semi-group_ property:
$$\mathcal{R}_{b}\mathcal{R_{b'}}\mathcal{O}_{i}=\lambda(b)_{i}\lambda(b')_{i}\mathcal{O}_{i}=\mathcal{R}_{bb'}\mathcal{O}_{i}=\lambda(bb')_{i}\mathcal{O}_{i}$$
- Along with $\lambda(1)_{i}=1$, this gives:
$$\lambda(b)_{i}=b^{y_{i}}$$
- $\mathcal{O}_{i}$ are the _scaling directions_ associated with $\boldsymbol{S}^{*}$, with the corresponding _anomalous dimensions_ $y_{i}$

- A Hamiltonian in the vicinity of $\boldsymbol{S}^{*}$ are _renormalised_ as:
$$S=S^{*}+\sum_{i}g_{i}\mathcal{O}_{i}\longrightarrow S'=S^{*}+\sum_{i}g_{i}b^{y_{i}}\mathcal{O}_{i}$$
- To _classify_ the eigenvectors:
	- If $y_{i}>0$, $g_{i}$ will _increase_ under scaling such that $\mathcal{O}_{i}$ is a _relevant operator_
	- If $y_{i}<0$, $g_{i}$ will _decrease_ under scaling such that $\mathcal{O}_{i}$ is an _irrelevant operator_
	- If $y_{i}=0$, $\mathcal{O}_{i}$ is a _marginal operator_, and _higher order terms_ are required to track its relevance

- The dimension above which couplings become _irrelevant_ is the _upper critical dimension_
	- Above $d_{u}$, if $f$ is _non-analytic around the fixed point_, irrelevant couplings are still required to obtain the _critical exponents_
	- At $d_{u}$, one gets perfect agreement with the _Gaussian exponents_

- The _space_ spanned by the _irrelevant operators_ is known as the _basin of attraction_
	- As $\xi$ must always _decrease_ under renormalisation, and $\xi(\boldsymbol{S}^{*})=\infty$, it must also be _infinite for all points on the basin_

- The basin is a _surface defining the phase transition_
![[Renormalisation group attraction.png|500]]

### From renormalisation flow to universality
- In general, _near a fixed point_ $S^{*}$
	- $g_{i}$: coefficients for the _scaling directions_
$$\xi(g_{1},g_{2},\dots)=b\xi(b^{y_{1}}g_{1},b^{y_{2}}g_{2},\dots)$$
- For a _sufficiently large_ $b$, the _irrelevant operators vanish_
- Then, _index_ the _relevant operators_ by _decreasing anomalous dimension_ $y_{i}$:
$$y_{1}>y_{2}>\dots$$
- One can choose $b$ such that:
$$\displaylines{b^{y_{1}}g_{1}=1 \\ \xi(g_{1},g_{2},\dots)=g_{1}^{-1/y_{1}}\xi\left( \frac{g_{2}}{g_{1}^{y_{2}/y_{1}}},\dots \right)}$$
- The _crtitical exponent_ and _gap exponents_ are then:
$$\nu_{1}=\frac{1}{y_{1}}\qquad \Delta_{\alpha}=\frac{y_{\alpha}}{y_{1}}$$

- Consider the case of a _ferromagnet with no external field_
	- _Tune_ the temperature to give a line in parameter space
	- For it to go through a _phase transition_, it must _intersect the basin of attraction only once_
	- The basis of attraction has _co-dimension_ one, meaning $S^{*}$ has _one and only one relevant operator_

- In the presence of a magnetic field, _two parameters_ must be tuned to give criticality, corresponding to a _second relevant operator_

- In general, _universality_ occurs as the _microscopic details_ of a system make up the _space of irrelevant operators_ giving the basin of attraction

## Solution to the Gaussian model
- The _Gaussian_ theory for an _$n-$component spin_, with terms up to _quadratic order_:
	- It is only meaningful for $t>0$ since there is _no stablising quartic term_
	- Can only describe the phase transition _from the ordered side_
$$\mathcal{Z}=\int  \mathcal{D}\boldsymbol{m}(\boldsymbol{x})\,\exp\left\{ -\int  d^{d}x\left[ \frac{t}{2}m^{2}+\frac{K}{2}|\nabla \boldsymbol{m}|^{2} -\boldsymbol{h}\cdot \boldsymbol{m}\right]  \right\} $$
- It can also be _diagonalised in Fourier space_ to give:
$$\displaylines{\mathcal{Z}=\int  \mathcal{D}m(\boldsymbol{q})\,\exp(-\beta H[\boldsymbol{m}]) \\ \beta H[\boldsymbol{m}]=\int  \frac{d\boldsymbol{q}}{(2\pi)^{d}} \frac{1}{2}(t+Kq^{2})|\boldsymbol{m}(\boldsymbol{q})|^{2}-\boldsymbol{h}\cdot \boldsymbol{m}(\boldsymbol{q}=0) }$$
### Exact solution
- The _free energy density_ is obtained by Gaussian functional integration:
	- There is some _constant factor_ $(2\pi)^{nN/2}$ which is physically insignificant
$$f(t,h)=-\frac{\ln \mathcal{Z}}{V}=\frac{n}{2}\int  \frac{d\boldsymbol{q}}{(2\pi)^{d}}\ln(t+Kq^{2})-\frac{h^{2}}{2t} $$
- The _singular contributions_ to free energy arise from _long-wavelength modes_

- Therefore, the non-analytic contribution can be obtained by _approximating the domain of integration as a hypersphere_, with radius $\Lambda=\pi /a$, where $a$ is a _short lengthscale cut-off_

- The _functional form_ of the integral can be obtained by _rescaling_ $q$ with factor $\sqrt{ t/K }$, keeping the _singular part_, ignoring the upper limit, and logarithmic factors:
$$f_\text{sing}(t,h)\sim t^{d/2}\left[ A+B \frac{h^{2}}{t^{1+d/2}} \right]\equiv t^{2-\alpha}g_{f}\left( \frac{h}{t^{\Delta}} \right)$$
- The exponents are:
$$\alpha_{+}=2-\frac{d}{2} \qquad \Delta=\frac{2+d}{4}$$
- The _ordered phase_ is not accounted for in this model, therefore $\beta$ is undefined
- Susceptibility:
$$\chi \propto \frac{\partial^{2}f}{\partial h^{2}}\sim t^{-1}\implies \gamma_{+}=1$$
### Via the renormalisation group
- The _coarse-graining_ of fluctuations at scales $a<|\boldsymbol{x}|<ba$ corresponds to _averaging over Fourier modes_ of wavenumbers:
$$\frac{\Lambda}{b}<|\boldsymbol{q}|<\Lambda$$
- Separate the _field_ in terms of _slow_ and _fast_ varying functions:
$$\boldsymbol{m}(\boldsymbol{q})=\boldsymbol{m}_{>}(\boldsymbol{q})+\boldsymbol{m}_{<}(\boldsymbol{q}) \qquad \boldsymbol{m}(\boldsymbol{q})=\begin{cases}
\boldsymbol{m}_{<}(\boldsymbol{q}) &0<|\boldsymbol{q}|<\Lambda/b \\ \boldsymbol{m}_{>}(\boldsymbol{q}) &\Lambda/b<|\boldsymbol{q}|<\Lambda
\end{cases}$$
- The partition can be re-expressed as:
$$\mathcal{Z}=\int  \mathcal{D}\boldsymbol{m}_{<}(\boldsymbol{q})\int  \mathcal{D}\boldsymbol{m}_{>}(\boldsymbol{q})\,\exp(-\beta H[\boldsymbol{m}_{<},\boldsymbol{m}_{>}])  $$
- They are _separable_:
$$\displaylines{\mathcal{Z=\mathcal{Z_{>}}}\int  \mathcal{D}\boldsymbol{m}_{<}(\boldsymbol{q})\,\exp\left[-\int_{0}^{\Lambda/b} \frac{d\boldsymbol{q}}{(2\pi)^{d}} \frac{t+Kq^{2}}{2}|m_{<}(\boldsymbol{q})|^{2}+\boldsymbol{h}\cdot \boldsymbol{m}_{<}(0) \right] \\ \mathcal{Z}_{>}=\exp\left( -\frac{nV}{2}\int_{\Lambda/b}^{\Lambda} \frac{d\boldsymbol{q}}{(2\pi)^{d}}\ln(t+Kq^{2}) \right)}$$
- Then, when one _re-scales_ $\boldsymbol{x}'=x/b$, _momentum space_ is also re-scaled $\boldsymbol{q}'=b\boldsymbol{q}$ such that the _cut-off is restored to the original value_

- Finally, one has to _renormalise the magnetisation_ $\boldsymbol{m}'(\boldsymbol{x}')=\boldsymbol{m}_{<}(\boldsymbol{x})/\zeta$
- Alternatively, one can simply _renormalise the Fourier modes_:
$$\displaylines{\boldsymbol{m}'=\frac{\boldsymbol{m}_{<}(\boldsymbol{q}')}{z} \\ \mathcal{Z}=\mathcal{Z}_{>}\int \mathcal{D}\boldsymbol{m}'(\boldsymbol{q}')\,\exp(-\beta H'[\boldsymbol{m}'(\boldsymbol{q}')]) \\ \beta H'=\int_{0}^{\Lambda} \frac{d\boldsymbol{q}'}{(2\pi)^{d}} \, b^{-d}z^{2}\left( \frac{t+Kb^{-2}q'^{2}}{2} \right)|m'(\boldsymbol{q}')|^{2}-z\boldsymbol{h}\cdot \boldsymbol{m}'(0)}$$
- The _constant factors_ from the _Jacobian_ and $\mathcal{Z}_{>}$ can be _neglected_ as they do not affect singular contributions

- The _parameters_ are _re-mapped_:
	- In general, there can be _new terms_ in the Hamiltonian
$$\displaylines{\boldsymbol{S}=\{K,t,h\}\longrightarrow \boldsymbol{S}'=\{K',t',h'\} \\ K'
=Kb^{-d-2}z^{2}\qquad t'=tb^{-d}z^{2} \qquad h'=zh}$$
- The _singular point_ $(t=h=0)$ is a _fixed point_ as expected

- For the fluctuations to be _scale-invariant at the fixed point_, the only remaining parameter, $K$, must be _fixed_, giving the choice:
$$z=b^{1+d/2}\implies \begin{cases}
t'=b^{2}t &y_{t}=2 \\ h'=b^{1+d/2}h &y_{h}=1+d/2
\end{cases}$$

- Meanwhile, for the _fixed point_ $t=t'=\infty$, $K$ becomes _weaker_, marking an _uncorrelated high temperature phase_

- This gives the _free energy scaling_:
$$f_\text{sing}(t,h)=b^{-d}f_\text{sing}(b^{2}t,b^{1+d/2}h)=t^{d/2}g_{f}\left( \frac{h}{t^{1/2+d/4}} \right)$$
- This is the _same as the exact solution_

- One can also find the _renormalisation parameter in real space_, by the fact that the _Hamiltonian is scale invariant at the fixed point_:
$$\beta H^{*}=\frac{K}{2}b^{d-2}\zeta^{2}\int d\boldsymbol{x}'\,|\nabla \boldsymbol{m}'|^{2}\implies \zeta=b^{1-d/2}$$
- For a _small power law perturbation_:
$$\beta H^{*}+u_{p}\int d\boldsymbol{x}\,|m(\boldsymbol{x})|^{p}\longrightarrow \beta H^{*}+u_{p}b^{d}\zeta^{p}\int d\boldsymbol{x}'|m'(\boldsymbol{x}')|^{p}$$
- The perturbations scale as: 
$$u_{p}\longrightarrow u_{p}'=b^{d+p-pd/2}u_{p}\implies y_{p}=p-d\left( \frac{p}{2}-1 \right)$$
- Example:
	- The _quartic term_ becomes irrelevant for $d>4$
	- The _sixth order term_ becomes irrelevant for $d>3$

## Wilsonian perturbative renormalisation group
- Examine _higher order terms_ as a _perturbation of the Gaussian model_

- With a _quartic perturbation_:
$$\beta H[\boldsymbol{m}]=\underbrace{ \int\,d\boldsymbol{x}\,\left[ \frac{t}{2}m^{2}+\frac{K}{2}|\nabla m|^{2} \right] }_{ \beta H_{0} }+\underbrace{ u \int\,d\boldsymbol{x}\,m^{4} }_{ U }$$
- In _Fourier space_:
$$\displaylines{\beta H_{0}=\int \frac{d\boldsymbol{q}}{(2\pi)^{d}} \frac{1}{2}(t+Kq^{2})|m(\boldsymbol{q})|^{2} \\ U=u \prod_{j=1}^{4}\left( \int \frac{d\boldsymbol{q}_{j}}{(2\pi)^{d}}m(\boldsymbol{q}_{j}) \right)\delta^{d}(\mathbf{q}_{1}+\mathbf{q}_{2}+\mathbf{q}_{3}+\mathbf{q}_{4})}$$
- The _coarse-graining_, with $\langle  \rangle_{\boldsymbol{m}_{>}}$ indicating _averaging over short wavelength modes_
$$\begin{align}
\mathcal{Z}&=\mathcal{Z}_{0}^{>}\int\mathcal{D}\boldsymbol{m}_{<}\,\exp(-\beta H_{0}[\boldsymbol{m}_{<}]) \frac{1}{\mathcal{Z}_{0}^{>}}\int\mathcal{D}\boldsymbol{m}_{>}\exp(-\beta H_{0}[\boldsymbol{m}_{>}]-U[\boldsymbol{m}_{<},\boldsymbol{m}_{>}])  \\
&=\mathcal{Z}_{0}^{>}\int\mathcal{D}\boldsymbol{m}_{<}\,\exp(-\beta H_{0}[\boldsymbol{m}_{<}])\langle \exp(-U[\boldsymbol{m}_{<},\boldsymbol{m}_{>}]) \rangle_{\boldsymbol{m}_{>}}  \\
&=\mathcal{Z}_{0}^{>}\int\mathcal{D}\boldsymbol{m}_{<}\,\exp\Big(-\beta H_{0}[\boldsymbol{m}_{<}]+\ln\langle \exp(-U[\boldsymbol{m}_{<},\boldsymbol{m}_{>}]) \rangle_{\boldsymbol{m}_{>}}\Big)
\end{align}$$
### Perturbative renormalisation of couplings
- To deal with the lattter term in the exponent, using only the _leading term_ in the [[#General cumulant expansion|cumulant expansion]]
$$\beta H[\boldsymbol{m}_{<}]=\beta H_{0}[\boldsymbol{m}_{<}]-\ln[\mathcal{Z_{0}^{>}}]+\langle U \rangle_{\boldsymbol{m}_{>}}+O(u^{2}) $$
- The average $\langle U \rangle_{\boldsymbol{m}_{>}}$ has _contributions_ from 4 _types_ of terms
	- Only terms with _even order_ in $\boldsymbol{m}_{>}$ can contribute to the average
$$\begin{align}
C_{1}(\{\boldsymbol{q}_{i}\})&=\langle \boldsymbol{m}_{<}(\mathbf{q}_{1}) \cdot \boldsymbol{m}_{<}(\boldsymbol{q}_{2})\boldsymbol{m}_{<}(\boldsymbol{q}_{3})\cdot \mathbf{m}_{<}(\boldsymbol{q}_{4})\rangle_{\boldsymbol{m}_{>}}  \\
C_{2}(\{\boldsymbol{q}_{i}\})&=\langle \boldsymbol{m}_{>}(\mathbf{q}_{1}) \cdot \boldsymbol{m}_{>}(\boldsymbol{q}_{2})\boldsymbol{m}_{<}(\boldsymbol{q}_{3})\cdot \mathbf{m}_{<}(\boldsymbol{q}_{4})\rangle_{\boldsymbol{m}_{>}}  \\
C_{3}(\{\boldsymbol{q}_{i}\})&=\langle \boldsymbol{m}_{>}(\mathbf{q}_{1}) \cdot \boldsymbol{m}_{<}(\boldsymbol{q}_{2})\boldsymbol{m}_{>}(\boldsymbol{q}_{3})\cdot \mathbf{m}_{<}(\boldsymbol{q}_{4})\rangle_{\boldsymbol{m}_{>}}  \\
C_{4}(\{\boldsymbol{q}_{i}\})&=\langle \boldsymbol{m}_{>}(\mathbf{q}_{1}) \cdot \boldsymbol{m}_{>}(\boldsymbol{q}_{2})\boldsymbol{m}_{>}(\boldsymbol{q}_{3})\cdot \mathbf{m}_{>}(\boldsymbol{q}_{4})\rangle_{\boldsymbol{m}_{>}} 
\end{align}$$
- They can be represented _diagrammatically_, with the _dotted lines_ indicating _averaging over high frequency modes_
![[Wilsonian renormalisation quartic diagrams.png]]
- The first diagram is simply $U[\boldsymbol{m}_{<}]$, while the last term gives a _constant_

- For the _unperturbed_ Hamiltonian, from [[#Gaussian functional integration|functional integration]]:
	- Working to _leading order_, hence using the unperturbed correlator
$$\langle m_{\alpha}(\boldsymbol{q})m_{\beta}(\boldsymbol{q}') \rangle_{0}=\delta_{\alpha\beta}(2\pi)^{d} \delta^{d}(\boldsymbol{q}+\boldsymbol{q}')G_{0}(\boldsymbol{q}) \qquad G_{0}(\boldsymbol{q})=\frac{1}{t+Kq^{2}}$$
- From the above:
$$\begin{align}
C_{2}(\{q_{i}\})&=nG_{0}(\mathbf{q}_{1})(2\pi)^{d}(\mathbf{q}_{1}+\mathbf{q}_{2})\boldsymbol{m}_{<}(\mathbf{q}_{3})\cdot \boldsymbol{m}_{<}(\boldsymbol{q}_{4}) \\
C_{3}(\{q_{i}\})&=G_{0}(\mathbf{q}_{1})(2\pi)^{d}(\mathbf{q}_{1}+\mathbf{q}_{3})\boldsymbol{m}_{<}(\mathbf{q}_{2})\cdot \boldsymbol{m}_{<}(\boldsymbol{q}_{4})
\end{align}$$
- Add _all permutations_ of $C_{1},C_{2},C_{3}$ into the coarse-grained Hamiltonian
	- Permutations given by _Wick's Theorem_

- One finds that $K$ and $u$ are _un-renormalised_, meanwhile:
$$t\longrightarrow \tilde{t}=t+4u(n+2)\int_{\Lambda/b}^{\Lambda}\frac{d\boldsymbol{q}}{(2\pi)^{d}}G_{0}(\boldsymbol{q})$$
- Then, _rescale_ $\boldsymbol{q}'=b\boldsymbol{q}$
- Finally, _renormalise_ $\boldsymbol{m}'=\boldsymbol{m}_{<}(\boldsymbol{q}')/z$:
$$\begin{align}
\beta H'[\boldsymbol{m}']&=\int_{0}^{\Lambda}\frac{d\boldsymbol{q}'}{(2\pi)^{d}}b^{-d}z^{2}\left( \frac{\tilde{t}+Kb^{-2}\boldsymbol{q}'^{2}}{2} \right)|\boldsymbol{m}'(\boldsymbol{q}')|^{2} \\
&+uz^{4}b^{-4d}\prod_{j=1}^{4}\left( \int \frac{d\boldsymbol{q}_{j}}{(2\pi)^{d}}m(\boldsymbol{q}_{j}) \right)\delta^{d}(\mathbf{q}_{1}+\mathbf{q}_{2}+\mathbf{q}_{3}+\mathbf{q}_{4})
\end{align}$$
- The renormalised Hamiltonian is defined with parameters:
$$t'=b^{-d}z^{2}\tilde{t} \qquad K'=b^{-d-2}z^{2}K\qquad u'=b^{-3d}z^{4}u$$
- Then set $z=b^{1+d/2}$ such that $K=K'$, and there is a _fixed point_ at $t^{*}=u^{*}=0$

### Recursive relations and renormalisation flow
- The _recursion relations_ near the fixed point:
$$\displaylines{t'=t(b)=b^{2}\left[ t+4u(n+2)\int_{\Lambda/b}^{\Lambda} \frac{d^{d}q}{(2\pi)^{d}} G_{0}(\boldsymbol{q})\right] \\ u'=u(b)=b^{4-d}u}$$
- This _recursion_ can be converted into a _differential equation_ by setting $b=e^{l}$
$$t(b)\equiv t(1+\delta l+\dots)=t+\delta l\, \frac{dt}{dl}$$
- Using the recursion relations for both:
	- $K_{d}\equiv S_{d}/(2\pi)^{d}$
$$\displaylines{\frac{dt}{dl}=2t+\frac{4u(n+2)K_{d}\Lambda^{d}}{t+K\Lambda^{2}} \\ \frac{du}{dl}=(4-d)u}$$
- The second equation gives:
$$u(l)=u_{0}e^{(4-d)l}=u_{0} b^{4-d}$$

- In the vicinity of $t^{*}=u^{*}=0$
$$\frac{d}{dl}\pmatrix{\delta t\\\delta u}=\pmatrix{2&4(n+2)K_{d}\Lambda^{d-2}/K \\ 0&4-d}\pmatrix{\delta t\\\delta u}$$
- The _eigenvalues_ of this operator determine the _relevant operators_:
	- Zero elements on one side: eigenvalues are diagonal elements
$$y_{t}=2\qquad y_{u}=4-d$$
- However, the _eigendirections_ are different
- $y_{t}=2$ is associated with $u=0$
- $y_{u}=4-d$ is associated with $t=-4u(n+2)K_{d}\Lambda^{d-2}/K$

- For $d>4$, there is _only one relevant direction_ due to $y_{t}$, matching expectations of the _phase transition_
- For $d<4$, there are _two relevant directions_ and is _unstable_
- In this _one-loop approximation_:
![[One loop RG flow.png|400]]

- If one includes _quadratic perturbations_, there will be an _additional fixed point_ for $d<4$
	- $u^{2}$ perturbations to both $t$ and $u$ are _negative_ 

# Quantum phase transitions
- Deriving the _Ginzburg-Landau action_ using the _path integral_

## Path integrals and the quantum-classical mapping
- A _many-body quantum Hamiltonian_, accounting for _external potentials and inter-particle interactions_:
$$H=\sum_{i=1}^{N}\frac{p_{i}^{2}}{2m}+V(\boldsymbol{x}_1,\boldsymbol{x}_{2},\dots \boldsymbol{x}_{N})$$
- The _canonical commutation relations_:
$$[x_{\mu},p_{\nu}]=i\delta_{\mu \nu}$$
- The partition function can be written as a _path integral_:
$$\mathcal{Z}=\int \left( \prod_{i=1}^{N}\,d^{d}\boldsymbol{x}_{i} \right)\braket{ \boldsymbol{x}_{1},\boldsymbol{x}_{2},\dots \boldsymbol{x}_{N} | \exp(-\beta H) |\boldsymbol{x}_{1},\boldsymbol{x}_{2},\dots \boldsymbol{x}_{N}} $$
- Shorthand notation:
$$\displaylines{X\equiv \boldsymbol{x}_{1},\boldsymbol{x}_{2},\dots \boldsymbol{x}_{N} \qquad dX\equiv \prod_{i=1}^{N}\,d^{d}\boldsymbol{x}_{i} \\ X^{2}\equiv \sum_{i=1}^{N}\boldsymbol{x}_{i}^{2} \qquad X\cdot P\equiv \sum_{i=1}^{N}\boldsymbol{x}_{i}\cdot \boldsymbol{p}_{i}}$$
### Deriving the quantum-classical mapping
 - Split $\exp(-\beta H)$ into $N_{\tau}$ pieces:
$$\displaylines{\mathcal{Z}=\int dX\braket{ X|e^{-\beta H/N_{\tau}}\,\mathbb{I} \,e^{-\beta H/N_{\tau}}\,\mathbb{I}\dots \mathbb{I\,}e^{-\beta H/N_{\tau}}| X } \\ \mathbb{I}=\int dX\,\ket{X}\bra{X}  }$$
- For $N_{\tau}\to \infty$, expanding the exponentials, with $\epsilon=\beta/N_{\tau}$
$$\mathcal{Z}=\int\left( \prod_{i=1}^{N_{\tau}}dX_{i} \right)\braket{ X_{1}|\mathbb{I}(1-\epsilon H) |X_{2}  }\braket{ X_{2}|\mathbb{I}(1-\epsilon H) |X_{3}  }\dots \braket{ X_{N_{\tau}}|\mathbb{I}(1-\epsilon H) | X_{1} }   $$
- Then, by expanding the identity in _momentum space_:
$$\begin{align}
\mathcal{Z}=&\int\left( \prod_{i=1}^{N_{\tau}}dX_{i} \right)\int\left( \prod_{i=1}^{N_{\tau}}dP_{i} \right)\,\braket{ X_{1} | P_{1} } \braket{ P_{1} |1-\epsilon H| X_{2} } \times \\
&\braket{ X_{2} |P_{2}  }\braket{ P_{2}|1-\epsilon H |X_{3}  }\times\dots \times \braket{ X_{N_{\tau}} |P_{N_{\tau}}  }\braket{ P_{N_{\tau}}|1-\epsilon H |X_{1}  }    
\end{align}$$
- Use the inner products:
$$\displaylines{\braket{ X_{i} | P_{j} }=\exp(iX_{i}\cdot P_{j}) \\ \begin{align}
\braket{ P_{i} |1-\epsilon H| X_{i+1} }&=\left[ 1-\epsilon\left( \frac{P_{i}^{2}}{m}+V(X_{i+1}) \right) \right]\exp(-iP_{i}\cdot X_{i+1}) \\ &=\exp \left[ -\epsilon\left( \frac{P_{i}^{2}}{2m}+V(X_{i+1}) \right) \right]\exp(-iP_{i}\cdot X_{i+1})
\end{align}}$$
- Then, the partition function can be expressed as a _phase space integral_ in the limit of $N_{\tau}\to \infty$
	- $X_{N_{\tau}+1}=X_{1}$
$$\mathcal{Z}=\int\left( \prod_{i=1}^{N_{\tau}}dX_{i} \right)\left( \prod_{i=1}^{N_{\tau}}dP_{i} \right)\exp\left[ -i\sum_{i=1}^{N_{\tau}}P_{i}\cdot(X_{i+1}-X_{i})-\epsilon \sum_{i=1}^{N_{\tau}}\left( \frac{P_{i}^{2}}{2m}+V(X_{i}) \right) \right]$$
- Going to the _continuum limit_ with $\tau=(i-1)\epsilon$ gives the _functional integral_
$$\mathcal{Z}=\int_{X(\beta)=X(0)}\mathcal{D}X(\tau)\int\mathcal{D}P(\tau)\exp\left[-\int_{0}^{\beta}d\tau\left( iP(\tau)\cdot\partial_{\tau}X(\tau)+\frac{P^{2}}{2m}+V[X(\tau)] \right)\right]$$
- Then, one can _integrate out_ $P(\tau)$ with a Gaussian integral:
$$\displaylines{\mathcal{Z}=\int_{\boldsymbol{x}_{i}(\beta)=\boldsymbol{x}_{i}(0)}\mathcal{D}\boldsymbol{x}_{i}(\tau)\,\exp(-H[\boldsymbol{x}_{i}(\tau)]) \\ H[\boldsymbol{x}_{i}(\tau)]=\int_{0}^{\beta}d\tau\,\left[ \sum_{i=1}^{N} \frac{m|\partial_{\tau}\boldsymbol{x}_{i}|^{2}}{2}+V[\boldsymbol{x}_{i}(\tau)] \right]}$$

- A $d-$dimensional quantum system at _zero temperature_ $(\beta=\infty)$ can be _mapped onto_ a $d+1-$dimensional _classical system_
	- The extra dimension is given by the _imaginary time_ $\tau$
	- In the quantum picture, for $\beta=\infty$, one only need to account for the _ground state_
- For a _finite temperature_, the extra dimension has a _finite length_ $\beta$

- The system evolves with an _imaginary time_, such that the analagous _time evolution operator_ is $\exp(-H\tau)$
![[Quantum classical map.png]]

- The _ultraviolet cut-off_ for $\tau$ is $\Lambda_{\tau}=\infty$, such that _rescaling_ $\omega$ does not change it

- Example: a 2D harmonic oscillator can be mapped onto the _1D Ising model_

### Correlators in the ground state
- Given a _classical correlator_ for a $d-$dimensional system, depending on some _correlation length_:
$$\langle \boldsymbol{m}(\boldsymbol{x})\cdot \boldsymbol{m}(0) \rangle=f(|\boldsymbol{x}|,\xi) $$

- For a _quantum system_, taking the correlator at different _imaginary times_, can be extended into the imaginary time dimension:
$$\langle \boldsymbol{m}(\boldsymbol{x},\tau)\cdot \boldsymbol{m}(0,0) \rangle= f\left( \sqrt{ |\boldsymbol{x}|^{2}+\tau^{2} },\xi\right)$$
## O(2) quantum rotors
- The case of a _particle constrained on a ring_
- The possible orientations are generated by the $O(2)$ group:
$$\boldsymbol{x}=(\cos \phi,\sin \phi)$$
- Consider _many interacting rotors_ on a $d-$dimensional _cubic lattice_, with the _nearest neighbour interaction_:
$$V(\boldsymbol{x}_{i},\boldsymbol{x}_{j})=-g\boldsymbol{x}_{i}\cdot \boldsymbol{x}_{j}$$

- The Hamiltonian, with the _angular momentum operator_ $L$:
$$H_{O(2)}=\sum_{i}\frac{L_{i}^{2}}{2m}-g\sum_{\langle ij \rangle }\boldsymbol{x}_{i}\cdot \boldsymbol{x}_{j}$$
- A _quantum phase transition_ is _non-analytic behaviour_ in the _ground state_, only at _zero temperature_
- For $mg\gg 1$, the Hamiltonian favours _alignment_
	- The ground state is _degenerate_, leading to _gapless excitations_
	- The system can be expanded in terms of _fluctuations_ $\phi_{\boldsymbol{k}}$:
	$$H_{O(2)}\xrightarrow{mg\gg 1}\sum_{\boldsymbol{k}}\left[ \frac{1}{2m}L_{\boldsymbol{k}}L_{-\boldsymbol{k}}+\frac{1}{2}g|k|^{2}\phi_{\boldsymbol{k}}\phi_{-\boldsymbol{k}} \right]$$
	- It is a series of _harmonic oscillators_ with spectrum $\sqrt{ g/m }|k|$

- For $mg\ll 1$, the ground state is that of _zero momentum for all rotors_
	- The alignment term acts as a _perturbation_ to allow _mixing_ of states
	- There will be an _energy gap_ between the ground and first excited states

- There will be some _intermediate value_ of $mg$ to give the _transition_

- Mapping this Hamiltonian to the partition function:
	- The rotors are allowed to _wind_ between $\tau=0$ and $\tau=\beta$
$$\displaylines{\mathcal{Z}_{O(2)}=\int_{\phi_{i}(\beta)=\phi_{i}(0)+2\pi n}\mathcal{D}[\phi_{i}(\tau)]\,\exp(-H[\phi_{i}(\tau)]) \\ H[\phi_{i}(\tau)]=\int_{0}^{\beta}d\tau\,\left[ \sum_{i=1}^{N} \frac{m(\partial_{\tau}\phi_{i})^{2}}{2}-g\sum_{\langle ij \rangle }\cos(\phi_{i}-\phi_{j}) \right]}$$
- As it is mapped onto a $d+1-$dimensional Hamiltonian, the ground state will have a [[#Long range order and the Mermin-Wagner theorem|Goldstone mode]]
- Long-range order is _destroyed_ for a $d\leq1$ lattice of rotors

### Approximate treatment
- Expand the potential term _quadratically_ at zero temperature:
$$H[\phi_{i}(\tau)]=\int_{0}^{\infty} \frac{m}{2}\sum_{i}(\partial_{\tau}\phi_{i})^{2}+ \frac{g}{2}\sum_{\langle ij \rangle } (\phi_{i}-\phi_{j})^{2}$$
- After Fourier expansion:
$$H=\int_{-\infty}^{\infty}d\tau\, \sum_{\boldsymbol{q}} \left[\frac{m}{2}|\partial_{\tau}\phi_{\boldsymbol{q}}|^{2}+ \frac{g}{2}q^{2}|\phi_{\boldsymbol{q}}|^{2}\right]$$
- Then Fourier expanding in _imaginary time_:
$$H=\int_{-\infty}^{\infty}d\omega\,\sum_{\boldsymbol{q}\in \text{BZ}} \frac{1}{2}(m\omega^{2}+gq^{2})|\phi_{\boldsymbol{q}}(\omega)|^{2}$$
- This is a _simple harmonic oscillator_ with _dispersion_:
$$\omega=\sqrt{ \frac{g}{m} }|q|$$
- It is a _Goldstone mode_

- Then calculating the expectation value:
$$\langle \phi_{i}^{2} \rangle=\int d\omega \sum_{\boldsymbol{q} \in\text{ BZ}} \frac{1}{m\omega^{2}+gq^{2}}\sim \int_\text{BZ} \frac{d^{d}q}{(2\pi)^{d}} \frac{1}{|q|} $$
- It is _divergent_ if $d\leq 1$
### Ginzburg-Landau action for the O(2) rotor

#### Derivation of O(2) Gizburg-Landau action: H-S decoupling
- From [[#Hubbard-Stratonovich decoupling from Ising model to Ginzburg-Landau|Hubbard-Stratonovich decoupling]], transforming $\Psi_{i}$ and $\Psi_{i}^{*}$ independently:
$$\displaylines{\mathcal{Z}_{O(2)}=\mathcal{N}\int_{\phi_{i}(\beta)=\phi_{i}(0)+2\pi n}\mathcal{D}[\phi_{i}(\tau)]\,\mathcal{D}[\Psi_{i}(\tau),\Psi_{i}^{*}(\tau)]\,\exp(-S[\phi_{i}(\tau),\Psi _{i}(\tau)]) \\ \begin{align}
S[\phi_{i}(\tau),\Psi_{i}(\tau)]=\int_{0}^{\beta}d\tau\Bigg[ &\sum_{i} \frac{m(\partial_{\tau}\phi_{i})^{2}}{2}+[e^{i\phi_{i}(\tau)}\Psi_{i}(\tau)+e^{-i\phi_{i}(\tau)}{\Psi^{*}_{i}(\tau)}] \\ +&\sum_{ij}\Psi_{i}(\tau)G_{ij}^{-1}\Psi_{j}(\tau)\Bigg] \qquad G_{\langle ij \rangle }=\frac{g}{2}
\end{align}}$$
- Then _expand the exponential_ in the order parameter, keeping only terms which obey _global phase symmetry_ $\phi_{i}(\tau)\to \phi_{i}(\tau)+\chi$
	- Other terms _average_ to zero
	- Truncating to _fourth order_ in $\Psi$
$$\displaylines{\begin{align}
&\mathcal{Z}_{O(2)}=\mathcal{N}\mathcal{Z}_{\phi}\int\mathcal{D}[\Psi_{i}(\tau),\Psi_{i}^{*}(\tau)]\,\exp\left[-\int_{0}^{\beta}d\tau\sum_{ij}\Psi_{i}(\tau)G_{ij}^{-1}\Psi_{j}(\tau)\right] \times \\
\Bigg[&1+\sum_{i}\int_{0}^{\beta}d\tau\,d\tau'\,\Psi_{i}(\tau)\Psi_{i}^{*}(\tau') \langle e^{i\phi_{i}(\tau)-i\phi_{i}(\tau')} \rangle_{S[\phi_{i}(\tau)]}  \\
+&\frac{12}{4!}\sum_{i\neq j} \int_{0}^{\beta}d\tau_{1}d\tau_{2}d\tau_{3}d\tau_{4}\langle e^{i\phi_{i}(\tau_{1})-i\phi_{i}(\tau_{2})+i\phi_{j}(\tau_{3})-i\phi_{j}(\tau_{4})} \rangle_{S[\phi_{i}(\tau)]} \Psi_{i}(\tau_{1})\Psi_{i}^{*}(\tau_{2})\Psi_{j}(\tau_{3})\Psi_{j}^{*}(\tau_{4}) \\
+& \frac{6}{4!}\sum_{i} \int_{0}^{\beta}d\tau_{1}d\tau_{2}d\tau_{3}d\tau_{4}\langle e^{i\phi_{i}(\tau_{1})-i\phi_{i}(\tau_{2})+i\phi_{i}(\tau_{3})-i\phi_{i}(\tau_{4})} \rangle_{S[\phi_{i}(\tau)]} \Psi_{i}(\tau_{1})\Psi_{i}^{*}(\tau_{2})\Psi_{i}(\tau_{3})\Psi_{i}^{*}(\tau_{4})\Bigg]
\end{align} \\ \mathcal{Z}_{\phi}=\int\mathcal{D}[\phi_{i}(\tau)]\,\exp\left[-\int_{0}^{\beta}d\tau\,\sum_{i} \frac{m(\partial_{\tau}\phi_{i})^{2}}{2}\right] \\ \langle \cdot \rangle_{S[\phi_{i}(\tau)]} =\frac{1}{\mathcal{Z}_{\phi}}\int\mathcal{D}[\phi_{i}(\tau)]\exp\left[-\int_{0}^{\beta}d\tau\,\sum_{i} \frac{m(\partial_{\tau}\phi_{i})^{2}}{2}\right]\Big(\cdot\Big)}$$
#### Derivation: correlators and integrating out $\phi_{i}$
- Take the _zero temperature limit_ $\beta\to \infty$
	- Neglect boundary condition $\phi_{i}(\beta)-\phi_{i}(0)=2\pi n$
- Then, Gaussian integration can be used to get the _two-point correlators_:
$$\langle \phi(\tau)\phi(\tau') \rangle=\frac{1}{2m}|\tau-\tau'| \qquad \langle e^{i\phi(\tau)-i\phi(\tau')} \rangle=\exp\left( -\frac{1}{2m}|\tau-\tau'| \right)  $$
- The _quadratic term_ is then:
	- Use a _Taylor expansion_ and discard higher derivatives/higher order terms
$$\begin{align}
\int d\tau_{1}\,d\tau_{2}\,\Psi_{i}(\tau_{1})\Psi_{i}^{*}(\tau_{2})\langle e^{i\phi_{i}(\tau_{1})-i\phi_{i}(\tau_{2})} \rangle &=\int d\tau_{1}\,d\tau_{2} \Psi_{i}(\tau_{1})\Psi_{i}^{*}(\tau_{2}) \,e^{-|\tau_{1}-\tau_{2}|/2m} \\
&=\int d\tau\,du\,\Psi_{i}\left( \tau-\frac{u}{2} \right)\Psi_{i}^{*}\left( \tau+\frac{u}{2} \right)e^{-|u|/2m}  \\
&\approx\int d\tau\,du \,\left[ |\Psi_{i}(\tau)|^{2}- \frac{u^{2}}{2}|\partial_{\tau}\Psi_{i}|^{2} \right]e^{-|u|/2m} \\
&=\int d\tau\,[4m|\Psi_{i}(\tau)|^{2}-16m^{3}|\partial_{\tau}\Psi_{i}|^{2}]
\end{align}$$
- For a _four-point correlator_ of $i\neq j$, it _factorises_ into two-point correlators:
$$\begin{align}
&\int_{0}^{\beta}d\tau_{1}d\tau_{2}d\tau_{3}d\tau_{4}\langle e^{i\phi_{i}(\tau_{1})-i\phi_{i}(\tau_{2})+i\phi_{j}(\tau_{3})-i\phi_{j}(\tau_{4})} \rangle_{S[\phi_{i}(\tau)]} \Psi_{i}(\tau_{1})\Psi_{i}^{*}(\tau_{2})\Psi_{j}(\tau_{3})\Psi_{j}^{*}(\tau_{4}) \\
=&\left(\int d\tau \,(4m)|\Psi_{i}(\tau)|^{2} \right)\left(\int d\tau \,(4m)|\Psi_{j}(\tau)|^{2} \right)
\end{align}$$
- Consider the _four-point correlator_ with $i=j$, as a _ground state exponential value_ of some _quantum operator_
	- It can also be considered using the [[#General cumulant expansion|cumulant expansion]]
	- When it is _not in the ground state_, one has to consider _summing over states_ using the _density matrix_
$$\displaylines{\langle e^{i\phi_{i}(\tau_{4})-i\phi_{i}(\tau_{3})+i\phi_{i}(\tau_{2})-i\phi_{i}(\tau_{1})} \rangle_{S[\phi_{i}(\tau)]}=\langle 0|\mathcal{T}[e^{i\phi_{i}(\tau_{4})}e^{-i\phi_{i}(\tau_{3})}e^{i\phi_{i}(\tau_{2})}e^{-i\phi_{i}(\tau_{1})}] |0\rangle \\ e^{i\phi_{i}(\tau)}=e^{H_{0}\tau}e^{i\phi_{i}}e^{-H_{0}\tau} \qquad H_{0}=\sum_{i}\frac{(L^{z}_{i})^{2}}{2m}}$$
- The operators $\exp[\pm i\phi(\tau)]$ _raise_ and _lower_ $m_{l}$ from the ground state at time $\tau$
- They are _excitations_ from the ground state

- Taking the _propagators_ $\exp(\pm H_{0}\tau)$ into account, the four-point correlator can then be written as:
$$\langle e^{i\phi_{i}(\tau_{4})-i\phi_{i}(\tau_{3})+i\phi_{i}(\tau_{2})-i\phi_{i}(\tau_{1})} \rangle_{S[\phi_{i}(\tau)]}=\exp\left[ \frac{1}{2m}\int d\tau \,m_{l}(\tau)^{2}\right]$$
- The first case: $|m_{l}(\tau)|\leq 1$ at all times, such that it can be _factorised_ into _non-overlapping correlators_
	- The _excitations can be shifted_ as long as they _do not overlap_
![[O(2) four point correlator factosied.png|400]]
- wlog, take $\tau_{1,2}<\tau_{3,4}$ such that _raising_ are at $\tau_{1,3}$, and there are $2^{2}$ equivalent configurations ($\tau_{1}\leftrightarrow \tau_{3}, \tau_{2} \leftrightarrow \tau_{4}$) which preserve $|m_{l}(\tau)|\leq 1$
	- Take $t_{1}=(\tau_{1}+\tau_{2})/2,t_{2}=(\tau_{3}+\tau_{4})/2,u_{1}=\tau_{2}-\tau_{1},u_{1}=\tau_{4}-\tau_{3}$
- This gives the corresponding term in the action:
$$\frac{1}{2}\left(\int d\tau \,(4m)|\Psi_{i}(\tau)|^{2}\right)^{2}-32m^{3}\int d\tau\,|\Psi_{i}(\tau)|^{4}$$

- The second case: $|m_{l}(\tau)|=2$ during some interval such that the correlator _cannot be factorised_ into 2-point correlators
	- These are _higher energy excitations_ that often do not play a role in the _quantum phase transition_
![[4 point correlator overlap.png|400]]
- wlog take $\tau_{1,3}<\tau_{2,4}$, with another equivalent configuration (_simultaneous swap_ of $\tau_{1}\leftrightarrow \tau_{2},\tau_{3}\leftrightarrow \tau_{4}$)
	- Take $t_{1}=(\tau_{1}+\tau_{3})/2,t_{2}=(\tau_{2}+\tau_{4})/2,u_{1}=\tau_{3}-\tau_{1},u_{1}=\tau_{4}-\tau_{2}$
- This gives the contribution:
$$4m^{3}\int d\tau\,|\Psi_{i}(\tau)|^{4}$$
- All 2-point and 4-point correlator contributions give:
$$\begin{align}
\mathcal{Z}_{O(2)}&=\mathcal{NZ}_{\phi}\int\mathcal{D}[\Psi_{i}(\tau),\Psi_{i}^{*}(\tau)]\Bigg[1+\sum_{i}\int d\tau\big(4m|\Psi_{i}(\tau)|^{2}-16m^{3}|\Psi_{i}(\tau)|^{4}\big) \\
&+\frac{1}{2}\left( \sum_{i} \int d\tau\,(4m)|\Psi_{i}(\tau)|^{2} \right)^{2}-28m^{3}\sum_{i}\int d\tau\,|\Psi_{i}(\tau)|^{4}\Bigg] \\
&\times\exp\left[-\int_{0}^{\beta}d\tau\sum_{ij}\Psi_{i}(\tau)G_{ij}^{-1}\Psi_{j}(\tau)\right] 
\end{align}$$
#### Final O(2) Ginzburg-Landau action
- The Greens function in _Fourier space_:
$$\displaylines{\begin{align}
G_{\boldsymbol{q},\boldsymbol{q}'}=\frac{1}{N}\sum_{i,j}\exp[i(\boldsymbol{q}\cdot \boldsymbol{x}_{i}-\boldsymbol{q}'\cdot \boldsymbol{x}_{j})]G_{ij}&=\delta_{\boldsymbol{q}+\boldsymbol{q}'}\sum_{\mu=1,\dots d}2g\cos(q_{\mu}a) \\
&\approx2g\delta_{\boldsymbol{q}+\boldsymbol{q}'}\left( d-\frac{1}{2}|q|^{2}a^{2} \right)
\end{align} \\ G_{\boldsymbol{q},\boldsymbol{q}'}^{-1}=\delta_{\boldsymbol{q},\boldsymbol{q}'} \frac{1}{2gd}\left( 1+\frac{1}{2d}|q|^{2}a^{2} \right)}$$

- _Coarse-grain_ the system such that $\Psi$ is also a function of _position_:
$$\sum_{\boldsymbol{r}}\to \int \frac{d^{3}r}{a^{d}}$$

- Then _re-exponentiating_ contributions from the correlators gives the partition function:
$$\displaylines{\mathcal{Z}_{O(2)}=\mathcal{NZ}_{\phi}\int\mathcal{D}[\Psi_{i}(\boldsymbol{r},\tau),\Psi_{i}^{*}(\boldsymbol{r},\tau)]\exp(-S[\Psi(\boldsymbol{r},\tau)]) \\ \begin{align}
S[\Psi(\boldsymbol{r},\tau)]=\int \frac{d^{d}r}{a^{d}} \,d\tau \bigg[&t\,|\Psi(\boldsymbol{r},\tau)|^{2}+ \frac{a^{2}}{4gd^{2}} |\nabla \Psi(\boldsymbol{r},\tau)|^{2}  \\
+&16m^{3}|\partial_{\tau}\Psi(\boldsymbol{r},\tau)|^{2}+28m^{3}|\Psi(\boldsymbol{r},\tau)|^{4} \bigg] \\ &-\frac{1}{2}\left( \int \frac{d^{d}r}{a^{d}}\,d\tau \,4m|\Psi(\boldsymbol{r},\tau)|^{2}\right)^{2}
\end{align} \\ t=\frac{1}{2gd}-4m}$$
- $t=0$ corresponds to the _zero temperature transition_ where $g=(8md)^{-1}$
- $t=-4m$ corresponds to $g\to \infty$, the _classical limit_

- From the derivation, one sees that the _phase transition terms_ come from the $m_{l}=\pm 1$ _particle-hole excitations_
	- Phase transition: from the $mg\ll 1$ _gapped, zero angular momentum_ phase to the $mg\gg 1$ _ordered phase_
- The _stability_ of the Ginzburg-Landau action is ensured by the _quartic term_
	- From _hardcore repulsion_ between particle-hole pairs

- The _Bose-Hubbard model_ also falls into the $O(2)$ universality class
### The dynamical exponent
- The Ginzburg-Landau action for the $O(2)$ rotor is _isotropic_ in spacetime
- One can _rescale_:
$$\boldsymbol{r}\to \frac{a}{2 \sqrt{ g }d}\boldsymbol{r} \qquad \tau\to 4m^{3/2}\tau$$
- Correlations in both _time_ and _space_ will _diverge_ with the same exponent at $t=0$
$$\xi \sim \xi_{\tau} \sim \frac{1}{|t|^{\nu}}$$

- For _general systems_:
$$\xi \sim \frac{1}{|t|^{\nu}} \qquad \xi_{\tau} \sim \frac{1}{|t|^{z\nu}}$$
- $z$ is the _dynamical exponent_ of the system
- For the $O(2)$ quantum rotor, $z=1$

### Energy gap in O(2) rotors
- The _finite energy gap_ between the _ground and first excited states_ results in a _finite correlation length_ in imaginary time $\xi_{\tau}$ in the ground state
- Take the _ground state expectation value_:
	- wlog, $E_{0}=0$ and $E_{1}$ is the _energy gap_
$$\begin{align}
\langle A(\tau)B(\tau') \rangle_{S[\phi_{i}(\tau)]} &\equiv \sum_{n}\langle 0|A|n \rangle e^{-|\tau-\tau'|E_{n}/\hbar} \langle n| B|0\rangle  \\ &\xrightarrow{|\tau-\tau'|\to \infty} \langle 0|A|1 \rangle e^{-|\tau-\tau'|E_{1}/\hbar}\langle 1|B|0 \rangle  
\end{align}$$
- The _imaginary time correlation length_ is related to the _energy gap_:
$$\xi_{\tau}=\frac{\hbar}{E_{1}}$$