- Completely different from [[Scattering|Classical scattering]]
- There is _no longer_ a one-to-one correspondence between _impact parameter_ $b$ and _scattering angle_ $\theta$
- It is inherently _probabilistic_

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