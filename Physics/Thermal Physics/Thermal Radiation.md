- Consider any body with some _finite temperature_ $T$
- The _motion of atoms_ give rise to an _acceleration of charged particles_
- They must then cause the _emission of electromagnetic radiation_

- This is known as _Blackbody Radiation_

- This is a _gas of photons_, where _surfaces_ will continually _emit, absorb and reflect_ photons
	- The _number of photons_ is _not fixed_
- Classically, it can be seen as a _superposition_ of many standing EM waves

- All photons have the _same speed_, but with _different energy and momenta_

## Energy and radiation pressure
- Consider a _cavity_ consisting of _adiathermal walls_, which is at temperature $T$ and in _equilibrium_ with the radiation inside

- Introduce the _spectral energy density_ $u_\lambda$, where the _energy per unit volume_ in wavelength range $\lambda$ to $\lambda+d\lambda$ is $u_\lambda\,d\lambda$
- It is a function of $\lambda$ and $T$
	- It is an _intrinsic property_ of the radiation
	- Let there be two boxes of _any material_, at _equal temperature_, connected to a filter that lets radiation with a _small range of $\lambda$_ through, there _cannot be any flow of heat or energy_
	- A _bigger box_ will have the _same_ $u_\lambda$, but create _more photons_ to raise total energy

- The _energy density_ $u$ is then:
$$u(T)=\int u_\lambda(\lambda, T)\,d\lambda$$

- Suppose the _number of photons per unit volume_ in the energy range $\epsilon$ to $\epsilon+d\epsilon$ is $n(\epsilon)\,d\epsilon$
	- The _energy per unit volume_ in that energy range is then $u_\epsilon=n(\epsilon)\epsilon\,d\epsilon$
- Consider the number of photons hitting a _unit area per unit time_, with energy in range $[\epsilon,\epsilon+d\epsilon]$ in _angle range_ $[\theta,\theta+d\theta]$:
$$dN=[n(\epsilon)d\epsilon](c\cos\theta)\frac{2\pi\sin\theta\,d\theta}{4\pi}$$
	- Numerator of latter fraction: _solid angle $d\Omega$ of thin ring_

- Using [[Relativity|Einstein's energy-momentum relation]], and the fact that _photons are massless_:
$$\epsilon=|\bm{p}|c$$
- For _perfectly reflecting surfaces_, $\Delta p$ on the surface is $2\epsilon\cos\theta/c$
- Hence, the _pressure_ is:
$$P=\int_{0}^\infty \int_0^{\pi/2}\epsilon n_\epsilon \cos^2\theta\sin\theta\,d\theta\,d\epsilon=\frac{1}{3}u$$
- For _absorbing surfaces_, the surface must also _radiate the energy it absorbs_, hence, for _all surfaces_, the result above holds

## Kirchoff's Law
- For a photon gas of _number density_ $n$, the _flux $\Phi$ of photons_ is:
$$\Phi=\int n(c\cos\theta)\frac{d\Omega}{4\pi}=\frac{1}{4}nc$$
- For a _narrow spectral range_ of radiation:
$$d\Phi_\epsilon=\frac{1}{4}n_\epsilon(\epsilon)c\,d\epsilon \hspace{1cm}d\Phi_\lambda=\frac{1}{4}n_\lambda(\lambda)c\,d\lambda$$
- The _incident power per unit area_ is then:
$$\epsilon\,d\Phi_\lambda=\frac{1}{4}u_\lambda c\,d\lambda$$

- Consider a _cavity_ in equilibrium with the _radiation_

- Define the _spectral absorptivity_ $\alpha_\lambda(\lambda)$ as the _fraction of incident radiation_ with _wavelength_ $\lambda$ that the surface _absorbs_
- Define the _spectral radiant exitance_ $e_\lambda(\lambda,T)$ where $e_\lambda\,d\lambda$ is the _power emitted per unit area_ for the wavelength range $[\lambda,\lambda+d\lambda]$
	- Also called tge _spectral emissive power_

- Then from the fact that the cavity is in _equilibrium_, one gets _Kirchoff's Law_:
$$\frac{e_\lambda}{\alpha_\lambda}=\frac{1}{4} u_\lambda c$$

- This means for a _fixed wavelength_, $e_\lambda\propto\alpha_\lambda$, or _good absorbers are good emitters_

- For a _black-body_, $\alpha_\lambda=1$, hence:
$$e_\lambda^{bb}=\frac{1}{4}u_\lambda c$$
- Kirchoff's law can then be re-written as:
$$e_\lambda=\alpha_\lambda e_\lambda^{bb}$$
- In other words, the _spectral emissivity_ of the surface is equal to the _spectral absorptivity_

## Stefan-Boltzmann Law
- The _internal energy_ of a cavity with volume $V$ is:
$$U=u(T)V$$
- Using the [[Classical Thermodynamics#The first master equation|first master equation]] for $U$ at _constant_ $N$, as well as a [[Classical Thermodynamics#Maxwell relations|Maxwell relation]]:
$$u=\left(\pd{U}{V}\right)_T=T\left(\pd{S}{V}\right)_T-p=T\left(\pd{p}{T}\right)_V-p$$
- Using the result from kinetic theory, then _rearranging_, one gets:
$$\frac{du}{u}=4\frac{dT}{T} \Longrightarrow u\propto T^4$$
- This also then gives the _equation of state_ for a photon gas, where $p\propto T^4$

- Then using _Kirchoff's law_, the _energy emitted per unit time_ for a _black-body_ is:
$$\int e_\lambda\,d\lambda=\sigma T^4$$
- This is the _Stefan-Boltzmann Law_
- $\sigma$ is a _proportionality constant_ that must be derived from statistical thermodynamics

## Gibbs Energy and chemical potential
- The [[Classical Thermodynamics#Gibbs Free Energy|Gibbs Energy]] of a photon gas is given by:
$$G=U+PV-TS$$
- Then, consider the _Gibbs Free Energy density_ $g$:
$$g=u+P-Ts$$
- From the results above, let $u=AT^4$
- To find $s$, integrate $ds$ over _constant volume_:
$$s=\int\frac{dq}{T}=\int\frac{du}{T}=\frac{4}{3}AT^3=\frac{4}{3}\frac{u}{T}$$
- Then, the _Gibbs Free Energy density_ becomes _zero_:
$$g=u+\frac{1}{3}u-\frac{4}{3}u=0$$
- This also means the _chemical potential_ $\mu$ is zero

- This can be understood by the fact that since _photon number does not need to be conserved_, at _equilibrium_, for _constant volume_, the _number of photons_ is such that Helmholtz Free Energy is at a _minimum_
$$\mu=\left(\pd{F}{N}\right)_{T,V}=0$$
