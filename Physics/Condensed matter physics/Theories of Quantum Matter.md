>[!Convention]
>$$\hbar =1$$

- _Simple_ quantum models of _many-body_ systems

- Actual Hamiltonian for atoms and electrons solid:
$$H=-\frac{1}{2m}\sum_{j=1}^{N}\nabla_{j}^{2} +\dots$$
- Find a _many-electron_ wavefunction
- Intractable for $N\sim N_{A}$

- Requirement for _simple models_ with solutions for $N\to \infty$ that produce physical behaviour
- Tools from [[Second quantisation|second quantisation]] and quantum field theory are needed to represent wave functions

 - Fermions: _anti-bunching_
 - Bosons: _bunching_

# Many-body wave-functions



- Single particle density:
$$\rho_1(x_1) = N \int dx_2\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
$$\rho(x)=\sum_{j}\delta(x-x_{j}) \qquad \rho_{1}(x)=\braket{ \Psi|\rho(x) |\Psi  } $$
- Single particle density matrix:
$$g(x,y) \equiv N\int dx_2\ldots dx_N \,\Psi^{}(x,x_2,\ldots,x_N)\Psi^{*}(y,x_2,\ldots,x_N)$$
- Pair correlations:
$$\rho_2(x_1,x_{2}) = N(N-1) \int dx_3\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
$$\rho_{2}(x_{1},x_{2})=\rho_{1}(x_{1})\rho_{2}(x_{2})-g(x_{1},x_{2})g(x_{2},x_{1})$$
# Quantum Hall Effect
- A _2D gas_ in a _magnetic field_

- Single particle Hamiltonian:
$$H=$$
- Use the _symmetric gauge_
	- The [[Charged Particles#Landau levels|Landau gauge]] leads to _harmonic oscillator states_ in one direction, _plane waves_ in the other
$$A_{x}=\qquad A_{y}=$$
## Landau levels
- Use _complex coordinates_
$$z=\qquad \bar{z}= \qquad \partial_{\bar{z}}f(z)=0$$
- Rewrite $H$:
$$H=$$
- The _cyclotron frequency_:
$$\omega_{c}\equiv \frac{qB}{m}$$
- States that satisfy:

- They have energy $\omega_{c}/2$ and are the _lowest Landau levels_ (LLL) $\psi(z,\bar{z})$
- They have the form:
$$\psi(z,\bar{z})=$$
- $f(z)$ is _arbitrary_, leading to _high degeneracy_

- Denoting by $f(z)$, write the _inner product_:
	- Use _magnetic length_
$$\braket{  |  } $$
- A possible _orthonormal basis_:
$$f_{n}(z)=\frac{z^{n}}{\sqrt{ 2^{n}n! }}$$
## Filling the Lowest Landau levels
- _Lift_ the degeneracy by adding the _harmonic potential_
$$V_\text{harm}(x,y)=\frac{v}{2}(x^{2}+y^{2})=\frac{v}{2}|z|^{2}$$
- As it is _not a function of_ $x+iy$, $V_\text{harm}f(z)$ is _not in the LLL subspace_

- Only _consider the LLL subspace_
	- Assume $\omega_{c}$ is the _largest energy scale_
- _Replace_ the harmonic potential with:
	- From considering _matrix elements_, and integrating by parts
$$V_\text{harm}\to v\partial_{z}z=v(1+z\partial _{z})$$
- Application to $f_{n}(z)$, $V$ gives an _energetic cost_ to each state:
$$V_\text{harm}f_{n}=v(1+n)f_{n}$$

- Then, consider _filling states_ from $n=0,1,\dots N-1$
- Analagous to the _1D Fermi gas_, where states are simply $z^{n}$
	- 1D - powers of plane wave states $z$ / 2D - $z$ living on complex plane
- Similar arguments give:

- The _single particle density_:

- At _small_ $|z|$, approximate by an _infinite sum_ such that $\rho_{1} \to 1/2\pi$
- Density is _fixed_ until $|z| \sim \sqrt{ 2N }$, after which it _falls_ to zero with _length scale_ $l_{B}$
- The filled LLLs can be described as a _circular droplet_
- Flux quantum

- A _different confining potential_ will change the _droplet shape_

## Laughlin wavefunction
- A _generalised Laughlin wavefunction_:
$$\Psi_{m}$$
- For $m\neq 1$, it is _not a product state_

- For $m$ _odd/even_, it is (anti)symmetric hence it is for _fermions/bosons_

### m=2 boson state
- For the _delta function repulsion_

- $m=2$ state has _zero interaction energy_ as the state _prevents bunching_

- Hence, _states with no interaction energy_ must have $\Psi_{2}$ as a _factor_
	- For a _higher degree wave-function_
	- $\Psi_{2}$ ground state?

- _Compared_ to an _uncorrelated sampling_, the Laughlin state results in _more uniform sampling_ due to the anti-bunching

### Plasma statistical analogy
