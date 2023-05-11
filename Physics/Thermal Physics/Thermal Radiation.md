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
	- Similar method to the [[Kinetic Theory of Gases]]

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
- $\sigma$ is a _proportionality constant_ that must be [[#Planck's Law|derived]] from statistical thermodynamics

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
## Density of states and the ultraviolet catastrophe
- Consider photons in a _cubic box_ of lengths $L$
- With the condition that $E_\parallel(x=0)=E_\parallel(x=L)=0$:
$$\bm{E}=\bm{E}_0\sin(k_xx)\sin(k_yy)\sin(k_zz)$$
- Where the wave-vector is:
$$\bm{k}=\frac{\pi}{L}(n_x\,n_y\,n_z)$$
- In $k-$space, each state has a _volume_ of $(\pi/L)^3=\pi^3/V$, which are _uniformly distributed_
- As photon energy depends on $|\bm{k}|$, _states of equal energy_ lie on _shells_ in $k-$space
- For each $k-$state, there are _two polarisations_

- To find the _density of states $g(k)$_ in $k$:
$$\displaylines{dN=g(k)\,dk=2\frac{4\pi k^2\,dk/8}{(\pi/L)^3} \\ g(k)=\frac{Vk^2}{\pi^2}}$$
- Then to find the _density of states $g(\epsilon)$_:
$$\displaylines{\epsilon=\hbar kc \\ g(\epsilon)=\frac{dN}{d\epsilon}=g(k)\frac{dk}{d\epsilon}=\frac{V\epsilon^2}{\hbar^3c^3\pi^2}}$$
- As for the _density of states in wavelength_ $g(\lambda)$:
$$\displaylines{\epsilon=\frac{hc}{\lambda} \\ g(\lambda)=\frac{V}{\hbar^3c^3\pi^2}\frac{h^2c^2}{\lambda^2}\frac{d\epsilon}{d\lambda}=\frac{8\pi V}{\lambda^4}}$$

- According to classical mechanics, the wave energy has _two terms_ in $E$ and $B$, hence each state has energy $k_BT$
- This gives the _energy density_:
$$u_\lambda=\frac{du}{d\lambda}=k_BT\,g(\lambda)=\frac{8\pi Vk_BT}{\lambda^4}$$
- This is the _Rayleigh-Jeans law_
- The energy density _diverges_ as $\lambda\to 0$
- This is known as the _ultraviolet catastrophe_

## Planck's Law
- It was proposed that radiation is emitted in _quanta_, or "packets" of energy
- The [[Statistical thermodynamics#The Partition Function|partition function]]and _internal energy_ for a blackbody radiating at frequency $\omega$ are:
$$\displaylines{Z=\sum_{n=0}^\infty \exp\left(-\frac{n\hbar\omega}{k_BT}\right)=\sum_{n=0}^\infty \exp(-n\beta\hbar\omega)=\frac{1}{1-\exp(-\beta\hbar\omega)} \\ U=-\frac{1}{Z}\frac{dZ}{d\beta}=\frac{\hbar\omega}{\exp(\beta\hbar\omega)-1}}$$
- To find the _total energy_, one needs the _density of states_ in $\omega$:
$$g(\omega)=g(\epsilon)\frac{d\epsilon}{d\omega}=\frac{V\omega^2}{c^3\pi^2}$$
- The _energy density_ for spectral range $\omega$ to $\omega+d\omega$ is then:
$$u(\omega,T)=g(\omega)\frac{U}{V}=\frac{\hbar\omega^3}{\pi^2c^3\left[\exp(\hbar\omega/k_BT)-1\right]}$$
- This is _Planck's law for radiation_

- Integrating $u$ over the _entire spectral range_:
$$u(T)=\frac{\hbar}{\pi^2c^3}\int_0^\infty \frac{\omega^3}{\exp(\beta\hbar\omega)-1}\,d\omega=\frac{\hbar}{\pi^2c^3}\left(\frac{k_BT}{\hbar}\right)^4\int_0^\infty\frac{x^3}{e^x-1}\,dx$$
- This gives the energy density:
$$u(T)=\frac{k_B^4\pi^2}{15\hbar^3c^3}T^4$$
- Then by considering [[#Kirchoff's Law]], one gets the [[#Stefan-Boltzmann Law]]:
$$\displaylines{\int\,e_\lambda\,d\lambda=\frac{c}{4}u(T)=\sigma T^4 \\ \sigma=\frac{k_B^4 \pi^2}{60\hbar^3 c^2}=5.67\times 10^{-8}\,\text{W m}^{-2}\text{ K}^{-4}}$$

## Wien's distribution and displacement laws
- By considering that $u_\omega\,|d\omega|=u_\lambda\,|d\lambda|$:
$$u_\lambda=u_\omega\left|\frac{d\omega}{d\lambda}\right|=\frac{8\pi ch}{\lambda^5}\frac{1}{\exp(hc/\lambda k_BT)-1}$$
- This is _Wien's distribution law_:
$$u_\lambda=\lambda^{-5}f(\lambda T)$$
- By _differentiating_ w.r.t $\lambda$. one obtains _Wien's displacement law_:
$$\displaylines{\frac{du_\lambda}{d\lambda}\Bigg|_{\lambda_\text{max}}=0 \\ \lambda_\text{max}T\approx 2.9\text{ mm K}}$$
