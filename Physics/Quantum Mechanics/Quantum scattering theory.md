- Completely different from [[Scattering|Classical scattering]]
- There is _no longer_ a one-to-one correspondence between _impact parameter_ $b$ and _scattering angle_ $\theta$
- It is inherently _probabilistic_

- _Quantum effects_ become important when the _wavelength_ $\lambda$ is _comparable_ to the _interaction range_ of the potential
- Assume that the scattering is _elastic_
- Hence, _energy_ is a well-defined quantity and can be used to characterise _eigenstates_ at _all times_ in the scattering process

# The Born Approximation
- For _high energy_ scattering from a _small potential_ $V(\boldsymbol{r})$, one can use the _Born approximation_
	- Small potential: in terms of _contribution to the Hamiltonian_
- One can use [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]] in the limit $\omega\to 0$
	- The _perturbation_ $\hat{H}'(t)$ becomes the potential $V(\boldsymbol{r})$

## Scattering geometry
- In the _initial state_ $\ket{\psi_{i}}$, a _free particle_ approaches with wave-vector $\boldsymbol{k}$
- In the _final state_ $\ket{\psi_{f}}$, the free particle leaves with wave-vector $\boldsymbol{k}'$
![[Scattering angle.png]]
- In the limit $\omega\to 0$, the collision is _elastic_, hence:
$$|\boldsymbol{k}|=|\boldsymbol{k}'|$$

- _Approximate_ the incoming and outgoing particles as _plane waves_
	- _Normalise_ to unity within a cube of volume $L^3$
$$\psi_{i}(\boldsymbol{r},t)=\frac{1}{L^{3/2}}\exp\left[ i\left( \boldsymbol{k}\cdot \boldsymbol{r}-\frac{E}{\hbar}t \right) \right]\hspace{1.25cm}\psi_{f}(\boldsymbol{r},t)=\frac{1}{L^{3/2}}\exp\left[ i\left( \boldsymbol{k}'\cdot \boldsymbol{r}-\frac{E}{\hbar}t \right) \right]$$
- The _incoming flux_ is given by the [[Principles of quantum mechanics#Probability flow|probability flow]] of the plane wave:
$$\boldsymbol{J}=-\frac{i\hbar}{2m}[\psi(\boldsymbol{r})^{*}\nabla \psi(\boldsymbol{r})-\psi(\boldsymbol{r})\nabla \psi(\boldsymbol{r})^{*}]=\frac{\hbar\boldsymbol{k}}{mL^{3}}$$

- Define the wave-vector difference $\boldsymbol{q}$:
![[Wave-vector difference.png]]
- This gives the _momentum transfer_ in the collision
- The _magnitude_ of the momentum change:
$$q=2k\sin\left( \frac{\theta}{2} \right)$$
## Calculating the scattering cross-section
- [[Time-dependent quantum mechanics#Continuum of states|Fermi's Golden Rule for continuous states]] gives the _scattering rate_ as:
$$\Gamma(i\to f)=\frac{2\pi}{\hbar}|\braket{ \psi_{f}|V(\boldsymbol{r}) | \psi_{i} }|^{2}g(E) $$

- From approximating the wave functions as _plane waves_, the matrix element is then:
$$\braket{ \psi_{f}|V(\boldsymbol{r}) |\psi_{i}  }=\frac{1}{L^{3}}\int V(\boldsymbol{r})\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) \, d^{3}\boldsymbol{r}  $$
- It is the _Fourier transform_ of $V(\boldsymbol{r})$ with respect to $\boldsymbol{q}$

- Calculating the _density of state_ from the _particle in a box_ approximation, and _restricting_ to solid angle $d\Omega$:
$$g(E)=\frac{L^{3}mk}{2\pi \hbar^{2}}\frac{d\Omega}{4\pi}=\frac{L^{3}mk}{8\pi^{2}\hbar^{2}}d\Omega$$
- One can then calculate the [[Scattering#Differential cross-section|differential scattering cross-section]]:
$$\frac{d\sigma}{d\Omega}=\frac{\Gamma(i\to f)}{|\boldsymbol{J}|d\Omega }=\left( \frac{m}{2\pi \hbar^{2}} \right)^{2}\left|\int V(\boldsymbol{r})\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) \, d^{3}\boldsymbol{r} \right|^{2}$$
- One can then get the _scattering amplitude_:
$$f(\theta,\phi)=\frac{m}{2\pi \hbar^{2}}\int V(\boldsymbol{r})\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) \, d^{3}\boldsymbol{r} $$

## An isotropic potential
- To calculate the Fourier transform, let $\theta'$ be the _angle between_ $\boldsymbol{q}$ and $\boldsymbol{r}$
$$\displaylines{\boldsymbol{q}\cdot \boldsymbol{r}=qr\cos\theta' \\ d^{3}\boldsymbol{r}=2\pi r^{2}dr\,d(\cos\theta')}$$

- If the potential is _isotropic_, $V(\boldsymbol{r})=V(r)$, one calculates the FT by:
$$\begin{align}
\int V(\boldsymbol{r})\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) \, d^{3}\boldsymbol{r}&=\int V(r)\exp(iqr\cos\theta')2\pi r^{2}\,dr\,d(\cos\theta')   \\
&=\frac{4\pi}{q}\int _{0}^{\infty}V(r)r\sin(qr) \, dr 
\end{align}$$

### Screened Coulomb potential
- Consider the _scattering_ of 2 particles of charge $Z_1e$ and $Z_2e$ with the _screened Coulomb potential_:
$$V(r)=\frac{Z_{1}Z_{2}e^{2}}{4\pi\epsilon_{0}r}\exp(-\lambda r)$$
- Using the formula for an isotropic potential, ans substituting for $q$:
$$\frac{d\sigma}{d\Omega}=\left( \frac{m}{2\pi \hbar^{2}} \right)^{2}\left[ \frac{Z_{1}Z_{2}e^{2}}{\epsilon_{0}}\frac{1}{4k^{2}\sin(\theta/2)+\lambda^{2}} \right]^{2}$$

- Taking the $\lambda\to0$ limit, one gets the cross-section for the _pure Coulomb potential_:
$$\frac{d\sigma}{d\Omega}=\left( \frac{Z_{1}Z_{2}me^{2}}{8\pi\epsilon_{0}p^{2}\sin^{2}(\theta/2)} \right)^{2}$$
- It is the _same_ as the [[Scattering#Coulomb scattering|classical case]]

- In the _general case_, it is _different from the classical case_

# Scattering in 1D
- At _infinity_, there is _zero potential_ $V(x\to \pm \infty)=0$
- Upon reaching the _interaction region_ where $V(x)\neq 0$, the wave can be _transmitted_ and _reflected_ into _other plane waves_ at infinity, on _both sides_
	- Given an incoming wave from $-\infty$, there is a _transmission_ $t_{LR}$ and _reflection_ $r_{LL}$
	- Given an incoming wave from $\infty$, there is a _transmission_ $t_{RL}$ and _reflection_ $r_{\mathbb{R}}$

## Scattering matrix
- The _general case_, with a _linear combination_ of _incoming waves from both sides_:
$$\Psi_{k}(x)=\begin{cases} a_{+}\exp(ikx)+a_{-}\exp(-ikx) &x\ll 0 \\ b_{+}\exp(ikx)+b_{-}\exp(-ikx)&x\gg 0\end{cases}$$
- The _scattering matrix_ $S(k)$ gives the _amplitude of the outgoing waves_ as a function of the _amplitudes of the incoming waves_
$$\begin{pmatrix}a_{-} \\ b_{+}\end{pmatrix}=\begin{pmatrix}
r_{LL} & t_{RL} \\ t_{LR} & r_{RR}\end{pmatrix}\begin{pmatrix}
a_{+}\\ b_{-}
\end{pmatrix}$$
- For _elastic scattering_, the scattering matrix must be _unitary_:
	- Otherwise, _probability current_ is _not conserved_
$$SS^{\dagger}=I$$

- Consider the _continuity equation_ for probability:
$$\partial_{t}P(x,t)+\partial_{x}j(x,t)=0$$
- The probability current is given by:
$$j(x,t)=-\frac{i\hbar}{2m}[\Psi^{*}\partial_{x}\Psi-\Psi\partial_{x}\Psi^{*}]$$
- For a _stationary state_, $P$ is constant and the current is _divergenceless_
$$\partial_{x}j=0$$
- Integrate over a region $[-L,L]$ including the _interaction region_:
$$\frac{\hbar k}{m}\left[\left| a_{+} \right|^{2}-\left| a_{-} \right|^{2}  \right]=\frac{\hbar k}{m}\left[ |b_{+}|^{2}-|b_{-}|^{2} \right] $$
- The _norm_ of the vectors is _constant_, hence $S(k)$ must be _unitary_

## Transfer matrix
- Another matrix giving the _same information_ as $S(k)$ is the _transfer matrix_ $T(k)$
- It gives the _amplitudes on one side of the scatterer_ as a linear transformation of the amplitudes on the _other side_:
$$\begin{pmatrix}b_{+}\\b_{-}\end{pmatrix}=T(k)\begin{pmatrix}a_{+}\\a_{-}\end{pmatrix}=$$

- Property:
## Channels and phase shifts
- As $S$ is _unitary_, it can be _diagonalised_:
$$USU^{\dagger}=\begin{pmatrix}\exp(2i\delta_{1})&0 \\ 0&\exp(2i\delta_{2})\end{pmatrix}$$
- This defines the _phase shifts_ $\delta_{1},\delta_{2}$

- The apply the _unitary transformation_ $U$ to the ingoing and outgoing kets:
$$\begin{pmatrix}a_{+}\\ b_{-}\end{pmatrix}=U^{\dagger} \begin{pmatrix}c^{\text{in}}_{1}\\c^{\text{in}}_{2}\end{pmatrix} \hspace{1cm}\begin{pmatrix}a_{-}\\ b_{+}\end{pmatrix}=U^{\dagger} \begin{pmatrix}c^{\text{out}}_{1}\\c^{\text{out}}_{2}\end{pmatrix} $$
- The ampliudes are then given by:
$$c_{1,2}^{\text{out}}=\exp(2i\delta_{1,2})c_{1,2}^{\text{in}}$$
- An eigenstate is then a _linear combination_ of the _scattering channels_ $1,2$
- The channels _do not mix_

- The channels typically reflect the _symmetry_ of the problem, as they are _simultaneous eigenstates_ of the _Hamiltonian_, and the _symmetry operator_

### Reflection symmetry
- Consider a system with _reflection symmetry_:
$$V(x)=V(-x)$$
- The Hamiltonian _commutes with the parity operator_:
$$\left[ \hat{H} ,\hat{\mathcal{P}}\right]=0$$
- Therefore, they must have a _common eigenbasis_:
$$\hat{H}\psi_{k,\pm}=E\psi_{k,\pm}\hspace{1.5cm}\hat{\mathcal{P}}\psi_{k,\pm}=\pm \psi_{k,\pm}$$
- Parity is _conserved_ throughout the scattering process
- These then give the _channels_ for this symmetry

- This gives the channels:
$$\displaylines{a_{+}=b_{-}=\frac{c^\text{in}_{+}}{\sqrt{ 2 }}\hspace{1.5cm}a_{-}=b_{+}=\frac{c^\text{out}_{+}}{\sqrt{ 2 }} \\ a_{+}=-b_{-}=\frac{c_{-}^\text{in}}{\sqrt{ 2 }} \hspace{1.5cm}a_{-}=-b_{+}=\frac{c^\text{out}_{-}}{\sqrt{ 2 }}}$$

- The linear transformation to the $c$ coefficients is given by $U$:
$$U=\frac{1}{\sqrt{ 2 }}\begin{pmatrix}1&1\\1&-1\end{pmatrix}$$

- Take the _linear combination_ of even and odd eigenstates:
$$\displaylines{\Psi_{k}(|x|\gg 0)=c_\text{even}\cos(k|x|+\delta _\text{even})+\text{sgn}(x)c_\text{odd}\sin(k|x|+\delta _\text{odd}) \\ c_\text{even,odd}=\frac{1}{\sqrt{ 2 }}c^{\text{in}}_\text{even,odd}\exp(i\delta _\text{even,odd})}$$

## 1D Lippmann-Schwinger equation
- The time-independent Schrodinger equation:
$$-\frac{\hbar^{2}}{2m}\frac{\partial^{2}}{\partial x^{2}}\Psi(x)+V(x)\Psi(x)=E\Psi(x)$$
- Elastic regime: _ingoing_ and _outgoing_ plane waves
- Write the solutions in the form:
$$\Psi_{k}(x)=\exp(ikx)+\Psi_{k}^{\text{scatt}}(x)$$
- This then gives the equation:
$$\left[ E_{k}+\frac{\hbar^{2}}{2m}\partial_{x}^{2} \right]\Psi_{k}^{\text{scatt}}(x)=V(x)\Psi_{k}(x)$$
- Then define the _Green's function_:
$$\left[ E_{k}+\frac{\hbar^{2}}{2m}\partial_{x}^{2} \right]G_{k}^{+}(x-x')=\delta(x-x')$$
- The _retarded Green's function_ satisfying _boundary conditions_
	- Also known as a _causal Green's function_, as the response is due to an _incoming wave_ $\exp(ikx)$
- Solution given by the _convolution_:
$$\Psi_{k}(x)=\exp(ikx)+\int \, dx' G_{k}^{+}(x-x')V(x')\Psi_{k}(x') $$
- This is the _Lippmann-Schwinger equation_, an _integral equation_ for $\Psi_{k}(x)$

- _Self-consistency_ requires:
$$\begin{align}\Psi_{k}(x)&=\exp(ikx)+\int  \, dx' G_{k}^{+}(x,x')V(x')\exp(ikx') \\ &+\int dx' \, dx'' \,G_{k}(x,x')^{+}G(x',x'')^{+}V(x')V(x'')\exp(ikx'') +\dots \end{align}$$
- This is the _Born series_
- With only _first order terms_, this is the [[#The Born Approximation|Born Approximation]]

### Green's function via Fourier transform
- _Fourier transform_ of the retarded Green's function:
$$G_{k}^{+}(x,x')=\frac{1}{2\pi}\int_{-\infty}^{\infty}  \, dq \frac{\exp[iq(x-x')]}{E_{k}-\hbar^{2}q^{2}/2m} $$
- There are _poles_ on the _real axis_
- Due to [[Analytical classical mechanics#Propagators and causality|causality]], the negative pole is moved _down_ and the other is moved _up_
- For $x>x'$, close in the _upper half plane_, giving a _positive_ $q$, corresponding to a wave with phase $ik(x-x')$
- This can also be given by the $\pm i\epsilon$ prescription:
	- Origin: consideration of the _transfer matrix_
$$G^{\pm}_{k}(x,x')= \lim_{\epsilon \to 0 }  \frac{1}{2\pi} \int _{-\infty}^{\infty} \, dq \frac{\exp[iq(x-x')]}{E_{k}-\hbar^{2}q^{2}/2m \pm i\epsilon} $$

- This gives:
$$G_{k}^{+}(x,x')=-\frac{im}{\hbar^{2}k}\exp(ik\left| x-x' \right| )$$

# Scattering in 3D
- The potential from the scatterer is $V(\boldsymbol{r})$
- Let the _incoming wave_ be along the $z-$axis
- Let it be _scattered_ by angle $\theta$
- Same ansatz as the Lippmann-Schwinger equation:
$$\Psi_{k}(\boldsymbol{r})\xrightarrow{r\to \infty}\exp(ikz)+\frac{f(\theta,\phi)}{r}\exp(ikr)$$
- There is an _outgoing_ scattered wave
- $f(\theta,\phi)$ is the _scattering amplitude_
![[3D scattering geometry.png]]
## Scattering amplitude cross section
- The probability current in 3D:
$$\boldsymbol{j}(\boldsymbol{r})=- \frac{i\hbar}{2m}[\Psi^{*}\nabla \Psi-\Psi \nabla \Psi ^{*}]$$
- Outgoing probability current is then:
$$\boldsymbol{j}(\boldsymbol{r}) \xrightarrow{r\to \infty}\frac{\hbar k}{m}\left[ \hat{z}+ \frac{|f(\theta,\phi)|^{2}}{r^{2}}\hat{r} \right]+(\text{cross terms} \propto \exp[\pm ik(z-r)])$$
- There are also _higher order terms_ from the angular part of the gradient, $\propto 1/r^{3}$
- For the _cross terms_, at high $r$, the _angular resolution_ of typical detectors lead to them being _canceled out_ due to rapid oscillation
	- The case of $\theta=0$ has to be treated more carefully, leading to the _optical theorem_ below

- For an _infinite_ wave, normalise with flux:
$$\boldsymbol{j}(\boldsymbol{r})\xrightarrow{r\to \infty} j\left[ \hat{z}+ \frac{|f(\theta,\phi)|^{2}}{r^{2}}\hat{r} \right]$$

- Consider the _probability per unit time_ for a _scattered particle_ to hit a region of _solid angle_ $d\Omega$ at  $(\theta,\phi)$:
$$d\sigma_{j}=j|f(\theta,\phi)|^{2}\,d\Omega$$
- For the quantity to be  _independent of scatterer_, normalise by the _flux_
- This gives the _differential cross-section_:
$$\frac{d\sigma}{d\Omega}=|f(\theta,\phi)|^{2}$$
- The _total cross-section_ is then:
$$\sigma _\text{tot}=\int  \frac{d\sigma}{d\Omega}\,d\Omega =\int |f(\theta,\phi)|^{2} \, d\Omega $$

## Optical theorem
- Consider integrating over integrating $\boldsymbol{j}$ for a _stationary state_ (i.e. $\nabla\cdot \boldsymbol{J}=0$), for a sphere centred in the _origin_
- Plane wave constribution goes to _zero_ as inward flux is cancelled out by outward flux
- This gives:
$$\int |f(\theta,\phi)|^{2} \, d\Omega=\sigma _\text{tot}=0 $$
- Therefore, one must reconsider the formula above
- This is mainly due to contributions from $\theta=0$

- In the _forward direction_, the _flux_ is determined by _interference_ between $\exp(ikz)$ and the $\theta=0$ scattered term
- Therefore, the _total scattering_ must influence the forward flux

- Consider a _screen_ of radius $R$ at distance $z$ in front of the scatterer
- Let $z\gg R$ such that it covers a _small solid angle_
- The _probability density_:
$$|\Psi_{k}(\boldsymbol{r})|^{2}=1+ \frac{2\mathrm{Re}\{f(\theta,\phi)\exp[ik(r-z)]\}}{r}+\frac{\left| f(\theta,\phi) \right|^{2}}{r^{2}} $$
- The last term can be _neglected_ at large distances
- Make the approximation:
$$r=\sqrt{ x^{2}-+y^{2}+z^{2} }\approx z-\frac{x^{2}+y^{2}}{2z}$$
- On the _screen_, make the approximation:
$$\displaylines{f(\theta,\phi)\approx f(\theta=0) \\ |\Psi_{k}(\boldsymbol{r})|^{2}=1+ \frac{2\mathrm{Re}\{f(\theta=0)\exp[-ik(x^{2}+y^{2})/(2z)]\}}{z}}$$
- Then integrating _over the screen_:
	- Assume $kR^{2}/z \gg 1$
$$\begin{align}
\int _\text{Screen}|\Psi_{k}(\boldsymbol{r})|^{2} \, dS&= \int _{0}^{R} \, 2\pi r\,dr \left[ 1+\frac{2\mathrm{Re}\{f(\theta=0)\exp[-ikr^{2}/(2z)]\}}{r} \right] \\ &= \pi R^{2}-\frac{4\pi}{k}\mathrm{Im}[f(\theta=0)] 
\end{align}$$
- The second term is the _loss_ due to scattering
- From this:
$$\sigma _\text{tot}=\frac{4\pi}{k}\mathrm{Im}[f(\theta=0)]$$
- This guarantees _flux conservation_ 
	- _Decrease_ in flux in _forward direction_ is equal to an increase in other directions)
	- Typically irrelevant if the detector is _off axis_
- This can also be derived using [[#Finding the differential cross-section|partial wave analysis]]
## 3D Lippmann-Schwinger equation
- In _analogy_ with 1D, the [[#1D Lippmann-Schwinger equation|Lippmann-Schwinger equation]] in 3D:
$$\Psi_{\boldsymbol{k}}(\boldsymbol{r})=\exp(ikz)+\int  \, d^{3}\boldsymbol{r}' \,G_{k}^{+}(\boldsymbol{r},\boldsymbol{r}')V(\boldsymbol{r}')\Psi_{k}(\boldsymbol{r}') $$
- The Green's function in this case, also using _Fourier_ methods:
$$\displaylines{\left[ E_{k}+\frac{\hbar^{2}}{2m}\nabla^{2} \right]G_{\boldsymbol{k}}^{+}(\boldsymbol{r},\boldsymbol{r}')=\delta(\boldsymbol{r}-\boldsymbol{r}') \\ G_{\boldsymbol{k}}^{+}=- \frac{m}{2\pi \hbar^{2}} \frac{\exp(ik|\boldsymbol{r}-\boldsymbol{r}'|)}{|\boldsymbol{r}-\boldsymbol{r}'|}}$$
- Can also be derived by considering the $\boldsymbol{r}\to \boldsymbol{r}'$ limit, and identifying it as the Green's function for _Laplace's equation_
	- $E_{k}$ term is not involved in producing the Delta function

- Examine behaviour of the wave _far away_ $(|\boldsymbol{r}|\gg|\boldsymbol{r}'|)$
$$|\boldsymbol{r}-\boldsymbol{r}'|=r-\hat{\boldsymbol{r}}\cdot \boldsymbol{r}'+\dots$$
- Define $\boldsymbol{k}_{f}=k \hat{\boldsymbol{r}}$ as the _final outgoing wave-vector_ for an eleastically scattered particle:
$$G_{k}^{+}(\boldsymbol{r},\boldsymbol{r}')\approx -\frac{m}{2\pi \hbar^{2}} \frac{\exp(ikr)}{r} \exp(-i\boldsymbol{k}_{f}\cdot \boldsymbol{r}')$$
- Replacing this in the Lippmann-Schwinger equation:
$$\Psi_{k}(\boldsymbol{r})=\exp(ikz)- \frac{m}{2\pi \hbar^{2}} \frac{\exp(ikr)}{r} \int  \, d^{3}\boldsymbol{r}'\,V(\boldsymbol{r}') \exp(-i\boldsymbol{k}_{f}\cdot \boldsymbol{r}')\Psi_{k}(\boldsymbol{r}')  $$
- This agrees with the ansatz as [[#Scattering in 3D|above]]

- From this, identify the _scattering amplitude_:
$$f(\theta,\phi)=-\frac{m}{2\pi \hbar^{2}} \int  \, d^{3}\boldsymbol{r}'\,V(\boldsymbol{r}')\exp(-i\boldsymbol{k}_{f}\cdot \boldsymbol{r}') \Psi_{k}(\boldsymbol{r}') $$


## First Born approximation
- The _lowest order approximation_ has $\Psi_{k}(\boldsymbol{r}')$ as an _unscattered plane wave_
- Defining the _momentum transfer_ $\boldsymbol{q}=\boldsymbol{k}_{f}-\boldsymbol{k}$, one gets the _first Born approximation_:
$$f(\theta,\phi)=-\frac{m}{2\pi \hbar^{2}} \int  \, d^{3}\boldsymbol{r}'\,V(\boldsymbol{r}')\exp(-i\boldsymbol{q}\cdot \boldsymbol{r}')$$
- This is a _Fourier transform_ of $V(\boldsymbol{r}')$ 
	- Scattering depends on the _mode content_ of the potential

- Identify the _differential cross-section_:
$$\frac{d\sigma}{d\Omega}\Bigg|_\text{Born}=\left| \frac{m}{2\pi \hbar^{2}} \int  \, d^{3}\boldsymbol{r}'\, V(\boldsymbol{r}')\exp(-i\boldsymbol{q}\cdot \boldsymbol{r}')  \right|^{2} $$
- This can also be derived using [[#Calculating the scattering cross-section|Fermi's Golden Rule]]

- Example: _spherical potential_:
$$\displaylines{V(\boldsymbol{r})=\begin{cases}V_{0}& |\boldsymbol{r}|<a_{\circ} \\ 0 & |\boldsymbol{r}|>a_{\circ}\end{cases} \\ f(\theta)=\frac{2mV_{0}}{\hbar^{2}q^{3}} (\sin qa_{\circ}-qa_{\circ}\cos qa_{\circ})}$$

- Its _validity_ depends on the _range_ of interaction $r_{c}$ and the "typical" energy $V_{c}$
- The approximation holds when the interaction is comapratively _weak_ in the range of interaction, so for _low energies_:
	- For an _attractive potential_, this means it is _too weak_ to form a bound state
$$\frac{f}{r_{c}}\ll 1 \implies V_{c}\ll \frac{\hbar^{2}}{mr_{c}^{2}}$$
- At _high energies_, $kr_{c}\gg 1$ and the wave _oscillates in the interaction region_, leading to the condition:
$$V_{c}\ll kr_{c} \frac{\hbar^{2}}{mr_{c}^{2}}$$
## Second Born approximation
- By _iterating_ the [[#3D Lippmann-Schwinger equation|Lippmann-Schwinger equation]] a second time, the _second correction_ to the scattered wave is:
$$\psi_{\boldsymbol{k}}^{(2)}(\boldsymbol{r})=\left( \frac{m}{2\pi \hbar^{2}} \right)^{2} \int  \, d^{3}\boldsymbol{r}_{1}\,d^{3}\boldsymbol{r}_{2} \frac{\exp\left[ ik|\boldsymbol{r}-\boldsymbol{r}_{1}|\right]}{|\boldsymbol{r}-\boldsymbol{r}_{1}|}V(\boldsymbol{r}_{1})\frac{\exp\left[ ik|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|\right]}{|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|}V(\boldsymbol{r}_{2})\exp(i\boldsymbol{k}\cdot \boldsymbol{r}_{2}) $$
- This gives a contribution to the _scattering amplitude_:
$$f^{(2)}=\left( \frac{m}{2\pi \hbar^{2}} \right)^{2} \int  \, d^{3}\boldsymbol{r}_{1}\,d^{3}\boldsymbol{r}_{2} \exp[-i\boldsymbol{k}_{f}\cdot \boldsymbol{r}_{1}]V(\boldsymbol{r}_{1})\frac{\exp\left[ ik|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|\right]}{|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|}V(\boldsymbol{r}_{2})\exp(i\boldsymbol{k}\cdot \boldsymbol{r}_{2}) $$

## Partial wave analysis
- For a 1D potential, one can define [[#Channels and phase shifts|channels]] due to symmetry (such as parity), where waves in each channel only get _phase shifts_
- In 3D, let there be a _spherically symmetric potential_ (rotational symmetry)
$$V(\boldsymbol{r})=V(r)$$
- The _rotation operators_ must _commute_ with the Hamiltonian
- Therefore, find eigenstates of _well-defined angular momentum_

- Solution to the time-dependent Schrodinger equation:
$$-\frac{\hbar^{2}}{2m}\nabla^{2}\Psi_{k}(\boldsymbol{r})+V(r)\Psi_{k}(\boldsymbol{r})=E_{k}\Psi_{k}(\boldsymbol{r})$$
- The solution can be _expanded_ in terms of the functions:
$$\Psi(\boldsymbol{r})= \sum_{l=0}^{\infty} \sum_{m=-l}^{l} c_{lm}Y_{lm}(\theta,\phi)R_{l}(r)$$
- The terms are _partial waves_
	- _Spherical harmonics_ $Y_{lm}$ give the well-defined _angular momenta_
- The radial part must obey the equation:
$$\frac{d^{2}R_{l}}{dr^{2}}+ \frac{2}{r} \frac{dR_{l}}{dr} + \left[ k^{2}- \frac{l(l+1)}{r^{2}} \right]R_{l}= \frac{2mV(r)}{\hbar^{2}}R_{l}$$

- In _general_, this gives the _complete solution_ for the radial wave-function
- _Continuity_ must still hold everywhere, including at the boundary of the potential

### Wave function when far away
- _Beyond_ the interaction region, the particle is _free_, hence $V(r)=0$
- In this case, writing the equation as $R_{l}(r)=r_{l}(\rho)$ where $\rho=kr$:
$$\rho^{2} \frac{d^{2}r_{l}}{d\rho^{2}}+ 2\rho\frac{ dr_{l}}{d\rho}+ [\rho^{2}-l(l+1)]r_{l}=0$$
- The solutions are the _spherical Bessel functions_ $j_{l}(\rho)$ and the _spherical Neumann functions_ $n_{l}(\rho)$:
$$r_{l}(\rho)=Aj_{l}(\rho)+Bn_{l}(\rho)$$

- Each _partial wave_ is a _channel_ of conserved angular momentum given by $l$
- They each have their own _phase shift_

- Can be more neatly packaged into the _spherical Hankel functions_:
$$h_{l}^{(1)}(\rho)=j_{l}(\rho)+in_{l}(\rho)\hspace{1.5cm}h_{l}^{(2)}(\rho)=[h_{l}^{(1)}(\rho)]^{*}$$

- Formulae for the functions:
$$j_{0}(\rho)=\frac{\sin \rho}{\rho}\hspace{1cm}n_{0}(\rho)=-\frac{\cos \rho}{\rho}\hspace{1cm}h_{0}^{(1)}(\rho )=\frac{\exp(i\rho)}{i\rho}$$
$$j_{l}(\rho)=(-\rho)^{l}\left( \frac{1}{\rho} \frac{d}{d\rho} \right)^{l}\frac{\sin \rho}{\rho}\hspace{1cm}n_{l}(\rho)=-(-\rho)^{l}\left( \frac{1}{\rho} \frac{d}{d\rho} \right)^{l} \frac{\cos \rho}{\rho}$$
- Limits at _small_ and _large_ arguments:
$$\displaylines{j_{l}(\rho)\xrightarrow{\rho\to 0}\frac{\rho^{l}}{(2l+1)!!} \hspace{1.5cm} n_{l}(\rho)\xrightarrow{\rho\to 0} -\frac{(2l-1)!!}{\rho^{l+1}} \\ j_{l}(\rho)\xrightarrow{\rho\to \infty} \frac{1}{\rho}\sin\left( \rho-\frac{l\pi}{2} \right)\hspace{1.5cm}n_{l}(\rho)\xrightarrow{\rho\to \infty} -\frac{1}{\rho}\cos\left( \rho-\frac{l\pi}{2} \right)}$$
### Expanding to the plane wave
- Connect to the formula:
$$\Psi_{k}(r)=\exp(ikz)+ \frac{f(\theta,\phi)}{r}\exp(ikr)$$
- It can be _expanded_ in terms of the partial waves, then the _phase shifts_ can be found

- The plane wave can be expanded as:
	- Does not include $n_{l}(kr)$ as they have a _singularity_ at $\rho=0$
$$\exp(ikz)=\exp(ikr\cos\theta)=\sum_{l=0}^{\infty} i^{l}(2l+1)j_{l}(kr)P_{l}(\cos\theta)$$
- Here, $P_{l}$ are the _Legendre polynomials_

- Taking $kr\to \infty$, using the limit of the _spherical Bessel function_:
	- Can be achieved using the _Hankel functions_
$$\exp(ikz)=\sum_{l=0}^{\infty} i^{l}(2l+1)P_{l}(\cos\theta) \left[  \frac{\exp[i(kr-l\pi/2)]}{2ikr}-\frac{\exp[-i(kr-l\pi/2)]}{2ikr} \right]$$
- This is the _exact wave-function_ in terms of the _channels_ for $V(r)=0$ everywhere
- The second term corresponds to some _incoming wave_

### Final wave-function and phase shifts
- After scattering, the _first term_ (outgoing wave) experiences _phase shift_ described by $S_{l}$
$$\displaylines{\begin{align}\Psi_{k}(\boldsymbol{r})&=\sum_{l=0}^{\infty} i^{l}(2l+1)P_{l}(\cos\theta) \left[ S_{l} \frac{\exp[i(kr-l\pi/2)]}{2ikr}-\frac{\exp[-i(kr-l\pi/2)]}{2ikr} \right] \\ &=\exp(ikz)+ \frac{f(\theta,\phi)}{r}\exp(ikr) \end{align}\\ S_{l}=\exp(2i\delta_{l})}$$

- The phase-shifted wave function can be written in terms of:
$$\Psi_{k}(\boldsymbol{r})=\sum_{l=0}^{\infty}i^{l}(2l+1)P_{l}(\cos\theta)\exp(i\delta_{l})[j_{l}(kr)\cos\delta_{l}-n_{l}(kr)\sin\delta_{l}]$$
- The _radial part_ can be expressed as:
$$R_{l}(kr)=\exp(i\delta_{l})\cos(\delta_{l})[j_{l}(kr)-n_{l}(kr)\tan(\delta_{l})]$$
- Compare to the [[#Wave function when far away|solution to Schrodinger's equation]] when far away:
$$R_{l}(kr)=Aj_{l}(kr)+Bn_{l}(kr)$$
- Comparing:
$$\tan(\delta_{l})=-\frac{B}{A}$$

- Let the _boundary_ of the potential be $r=a$, and set the wave function in the potential as $Cj_{l}(k'r)$, defining:
$$\gamma=\frac{R_{l}'(a)}{R_{l}(a)}$$
- Marching _boundary conditions_, one gets:
$$\tan\delta_{l}=\frac{kj_{l}'(ka)-\gamma j_{l}(ka)}{kn_{l}'(ka)-\gamma n_{l}(ka)}$$
- For $k\to 0$, $\delta_{l}$ scales as $k^{2l+1}$

### Differential cross-section
- From the form of the wave function, one gets:
$$\begin{align}f(\theta)&= \frac{1}{2ik} \sum_{l=0}^{\infty} (2l+1) [\exp(2i\delta_{l})-1]P_{l}(\cos\theta) \\ &= \frac{1}{k}\sum_{l=0}^{\infty} (2l+1)\exp(i\delta_{l})\sin\delta_{l}P_{l}(\cos\theta)\end{align}$$

- Using the _orthogonality_ of the Legendre polynomials:
$$\sigma _\text{tot}=\int |f(\theta)|^{2} \, \sin\theta\,d\theta\,d\phi= \frac{4\pi}{k^{2}}\sum_{l=0}^{\infty}(2l+1)\sin^{2}\delta_{l} $$
- From this, each _partial wave_ has a _limited scattering cross-section_:
$$\sigma_{l}\leq \frac{4\pi}{k^{2}}(2l+1)$$
- This is the _unitarity bound_
- For $\delta_{l}=(n+1/2)\pi$, it is _saturated_, and _resonant scattering_ occurs

- Consider the _imaginary part_ of $f(\theta=0)$:
$$\mathrm{Im}[f(\theta=0)]=\frac{1}{k}\sum_{l=0}^{\infty} (2l+1)\sin^{2}\delta_{l}=\frac{k}{4\pi}\sigma _\text{tot}$$
- This connects to the [[#Optical theorem]]
	- The contribution to the probability density "going through" is _proportional_ to the _total cross-section_

### Example: spherical potentials
- [[#Finding phase shifts|Radial part]] of the wave-function, _far away_ from the scatterer:
$$R_{l}(kr)=\exp(i\delta_{l})\cos(\delta_{l})[j_{l}(kr)-n_{l}(kr)\tan(\delta_{l})]$$
- The _hard-sphere_ potential:
$$V(\boldsymbol{r})=\begin{cases}\infty& |\boldsymbol{r}|<a_{\circ} \\ 0 & |\boldsymbol{r}|>a_{\circ}\end{cases} $$
- The radial part must _vanish_ at the boundary of the potential, giving:
$$\tan(\delta_{l})=\frac{j_{l}(ka_{\circ})}{n_{l}(ka_{\circ})}$$
- For $l=0$, the phase shift is exactly:
$$\delta_{0}=-ka_{\circ}$$
- For _small_ $k$, using the [[#Wave function when far away|limits]] of the functions:
$$\delta_{l}(k) \to -\frac{(ka_{\circ})^{2l+1}}{(2l+1)[(2l-1)!!]^{2}}$$
- Then one finds that the low $k$ limit of $\sigma _\text{tot}$ is:
$$\sigma _\text{tot}(k\to 0)=4\pi a_{\circ}^{2}$$
- It is four times the _projected geometrical area_ of the sphere

- Take a weaker spherical potential:
$$V(\boldsymbol{r})=\begin{cases}V_{0}& |\boldsymbol{r}|<a_{\circ} \\ 0 & |\boldsymbol{r}|>a_{\circ}\end{cases}$$
- From the _Schrodinger equation_, $r_{0}$ inside and outside:
$$r_{0}=\begin{cases}Cj_{0}(k'r) & r<a_{\circ} \\ D\exp(i\delta_{0})\cos(\delta_{0})[j_{0}(kr)-n_{0}(kr)]\tan\delta_{0} &r>a_{\circ}\end{cases}$$
- The wavenumber:
$$k'^{2}=k^{2}-\frac{2mV_{0}}{\hbar^{2}}\implies k'=\frac{\sqrt{ 2m(E-V_{0}) }}{\hbar}$$
- The phase shift for $l=0$:
$$\delta_{0}(k)=\arctan\left( \frac{k}{k'}\,\tan k'a_{\circ} \right)-ka_{\circ}$$
## Low energy scattering
- From above, one sees that at _low energies_, the $s-$wave dominates

- Consider the [[#Partial wave analysis|radial equation]] again:
$$\frac{d^{2}R_{l}}{dr^{2}}+ \frac{2}{r} \frac{dR_{l}}{dr} + \left[ k^{2}- \frac{l(l+1)}{r^{2}} \right]R_{l}= \frac{2mV(r)}{\hbar^{2}}R_{l}$$
- Define $R_{l}\equiv u_{l}/r$:
$$\left[ -\frac{d^{2}}{dr^{2}}+ \frac{l(l+1)}{r^{2}}+ \frac{2m}{\hbar^{2}}V(r) \right]u_{l}=k^{2}u_{l}$$
- Consider the _low energy limit_, $k\to 0$
- The _centrifugal term_ $l(l+1)/r^2$ has a _length scale_ $\sqrt{ l(l+1) }/k$
- Compare with the length scale for the _potential_, $r_{c}$

- For big $l$, the _centrifugal term_ becomes _too strong_ for the particle to _experiencing_ $V(r)$
- For _low energies_, only $l=0$ is _significant_ in terms of _scattering_, as expected

- The _total cross section_ is _dominated_ by the $l=0$ channel:
$$\sigma _\text{tot} \to \frac{4\pi}{k^{2}}\sin^{2}\delta_{0}$$
- This is known as $s-$_wave scattering_
### Scattering length
- Radial equation:
$$\left[ -\frac{d^{2}}{dr^{2}}+ \frac{2m}{\hbar^{2}}V(r) \right]u_{0}=k^{2}u_{0}$$
- From partial wave analysis, _far away_ from the potential:
$$u_{0} \propto \exp(2i\delta_{0}) \frac{\exp(ikr)}{ikr}- \frac{\exp(-ikr)}{ikr} \sim \sin(kr+\delta_{0})$$
- For low $k$, the solution from the _radial equation_ is:
$$u_{0} \sim A(r-a)$$
- From expanding $\sin(kr+\delta_{0})$ for small $k$:
$$\delta_{0}(k)\xrightarrow{k\to 0} -ka$$
- This gives the _total cross-section_:
$$\sigma_{tot} \to 4\pi a^{2}$$
- $a$ is of a _different scale_ to the _range_ of the potential $r_{c}$

### Variation of scattering length
- Let there be a _potential step_:
$$V(r)=\begin{cases}V_{0} & r\leq R \\ 0 &r>R\end{cases}$$
- It can be _attractive_ or _repulsive_

- For a _repulsive_ potential, there is an _exponential_ inside the well
	- It goes to _zero_ at $r\to 0$ to not let $R_{0}$ diverge
$$u_{0}=\begin{cases}A\sinh(kr) & r<R \\ B\sin(kr+\delta_{0}) & r>R\end{cases}$$
- Matching _boundary conditions_:
$$\frac{a}{R}=1- \frac{\tanh(kR)}{kR}$$
- For _high_ $R$, $a/R$ goes to $1$ 
	- The _scattering length_ matches the _range_ of the potential
	- The potential can also be modelled as a _hard wall_, therefore $u$ _drops off quickly_
- For _low_ $R$, $a/R$ goes to $0$
	- The _scattering length_ goes to $0$ (as expected as there is no scattering, and $u$ is _linear everywhere_)

- For an _attractive potential_, with the same strategy:
$$\frac{a}{R}=1- \frac{\tan(kR)}{kR}$$
- There are _branch cuts_ for this function
- The scattering length _diverges_ for $kR= (2n+1)\pi/2$
- It can also be both _positive_ and _negative_

- As $a$ _diverges_, the particle is _bound_ in the potential well
- As the potential increases further, the particle _remains bound_
- The cross-section varies as:

$$\sigma _\text{tot}\to \frac{4\pi}{k^{2}}$$
![[Scattering lengths.png]]