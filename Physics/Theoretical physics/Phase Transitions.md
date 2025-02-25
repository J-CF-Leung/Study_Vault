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
### Example: from Ising model to Ginzburg-Landau
$$\beta H_\text{Ising}=-J\sum_{\langle ij \rangle }\sigma_{i}\sigma_{j}-h\sum_{i}\sigma_{i}$$
- The partition function is the _trace_
	- $K_{ij}$ is the coupling matrix, equal to $J$ for _neighbouring_ $i,j$
$$\mathcal{Z}=\mathrm{Tr}[e^{-\beta H}]=\sum_{\{\sigma_{i}\}}\exp\left[ \sum_{i,j}\sigma_{i}K_{ij}\sigma_{j}+h\sum_{i}\sigma_{i} \right]$$
- Introduce the _Hubbard-Stratonovich_ transformation:
$$\int  \mathcal{D}\phi \,\exp\left( -\frac{1}{2}\boldsymbol{\phi}\mathbf{K}^{-1} \boldsymbol{\phi+\boldsymbol{\phi}\cdot \boldsymbol{s}} \right)=\sqrt{ 2\pi \det K }\exp\left( \frac{1}{2}\boldsymbol{s} \mathbf{K}\boldsymbol{s}\right) $$
- The partition function, by doing the transformation in _reverse_ and introducing the _auxiliary field_ $\phi(\boldsymbol{r})$
$$\mathcal{Z}=\frac{1}{\sqrt{ 2\pi \det K }}\sum_{\{\sigma_{i}\}}\int \mathcal{D}\phi\exp\left[ -\frac{1}{2}\boldsymbol{\phi}\mathbf{K}^{-1} \boldsymbol{\phi}+ (\boldsymbol{h}+\boldsymbol{\phi})\cdot \boldsymbol{\sigma}\right] $$

- Summing over $\sigma_{i}=\pm 1$, the final formula for the partition function:
$$\mathcal{Z}\propto \int  \prod_{r}d\phi(r) \exp\left[ -\frac{1}{2}\sum_{r,r'}\phi(r)K^{-1}(r,r')\phi(r')+\sum_{r}\ln \cosh(\phi+h) \right] $$
- From _lattice translation symmetry_:
$$K(\boldsymbol{r},\boldsymbol{r}')=K(\boldsymbol{r}-\boldsymbol{r}')$$

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

### Goldstone mode fluctuations in spin models
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
- Homogeneity is an assumption applied to _free energy_
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

