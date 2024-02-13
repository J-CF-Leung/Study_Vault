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

## Lippmann-Schwinger equation
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
	- Also known as a _causal Green's function_, as the response is due to an _incoming wave_
- Solution given by the _convolution_:
$$\Psi_{k}^{\text{scatt}}(x)=\int \, dx' G_{k}^{+}(x-x')V(x')\Psi_{k}(x') $$
- This is the _Lippmann-Schwinger equation_, an _integral equation_ for $\Psi_{k}(x)$

- _Self-consistency_ requires:
$$\begin{align}\Psi_{k}(x)&=\exp(ikx)+\int  \, dx' G_{k}(x,x')V(x')\exp(ikx') \\ &+\int dx' \, dx'' \,G_{k}(x,x')G(x',x'')V(x')V(x'')\exp(ikx'') +\dots \end{align}$$
- This is the _Born series_

- _Fourier transform_ of the retarded Green's function:
$$G_{k}^{+}=\frac{1}{2\pi}\int_{-\infty}^{\infty}  \, dq \frac{\exp[iq(x-x')]}{E_{k}-\hbar^{2}q^{2}/2m} $$
- There are _poles_ on the _real axis_
- Due to [[Analytical classical mechanics#Propagators and causality|causality]], the negative pole is moved _down_ and the other is moved _up_
- For $x>x'$, close in the _upper half plane_, giving a _positive_ $q$, corresponding to an _right-moving wave_
- For $x<x'$, close in the _lower half plane_, corresponding to a _left-moving wave_

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

- The probability current in 3D:
$$\boldsymbol{j}(\boldsymbol{r})=- \frac{i\hbar}{2m}[\Psi^{*}\nabla \Psi-\Psi \nabla \Psi ^{*}]$$
- Outgoing probability current is then:
$$\boldsymbol{j}(\boldsymbol{r}) \xrightarrow{r\to \infty}$$
- Cross terms

- Differential cross section