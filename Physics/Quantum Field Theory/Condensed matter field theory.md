- Matter is made up of _discrete lattices_
	- Let characteristic lattice constant be $a$, the _hopping energy_ be $t$
- Consider a _long wavelength_ $\lambda\gg a$ such that once can take a _continuum limit_
- Make a _field theory_, where operators previously labelled by _lattice site_ can then be put in terms of some _coordinate_
$$O_{i} \to O(\boldsymbol{x})$$

- Lattice-scale (microscopic) physics is typically _strongly coupled_:
	- Interaction energy comparable to kinetic energy
	- Example: _electrons_ in metals
$$E_\text{kin}\sim E_\text{int}$$
- Typically, one will consider some _low energy regime_ $E\ll t$, where one can have an _effective weakly coupled description_
	- Low energy modes: typically also _long wavelength_ modes such that one can go to a _continuum limit_

- This regime yields an _effective field theory_
- Then from [[Phase Transitions#Renormalisation Group|renormalisation group flow]], one can exploit _universality_

- In some cases, the low energy degrees of freedom might be _nontrivially related to microscopic degrees of freedom_
	- e.g. _quark confinement_, where baryons are an effective field
	- There may then need to be a _change of variables_ in the path integral of the field theory

- Under RG flow, there is typically a _relevant mass term_, giving an _energy gap_ or _zero point energy_
- This _limits the energy scale_ of _elementary excitations_ of the theory
- _Mechanisms_ than give _gapless excitations_:
	- _Spontaneous symmetry breaking_, which gives _Goldstone bosons_
	- _Quantum criticality_, where parameters are _finely tuned_
	- The presence of _Fermi surfaces_
	- _Emergent gauge fields_ (e.g. photons)

# Goldstone bosons
- A mechanism to produce _massless excitations_
- They occur in a system with _continuous symmetry breaking_
	- The symmetry is _internal_ and _global_
	- Not a gauge symmetry
- There is a _conserved charge_ $Q$ associated with the symmetry:
$$[H,Q]=0$$
- $Q$ is a _generator_

- Let $\ket{0}$ be the _ground state_ of $H$
$$H\ket{0}=0 $$
## Goldstone's Theorem
- _Spontaneous symmetry breaking_ occurs if there is some ground state with _non-zero charge_ $Q$, and is _not an eigenvector_ of $Q$
$$Q\ket{0}\neq 0,\ket{0}  $$
- From charge conservation, $Q\ket{0}$ is _also a ground state_
$$HQ\ket{0}= [H,Q]\ket{0}=0 $$
- Example: ground states of the _Mexican hat potential_

- From [[QFT#Noether's theorem|Noether's theorem]], the charge will be of the form:
$$Q=\int\,d^{d}x\,J^{0}(\boldsymbol{x},t)$$
- Then consider the states labelled by some vector $\boldsymbol{k}$
$$\ket{\boldsymbol{k}}=\int d^{d}x\,\exp(ikx)J^{0}(\boldsymbol{x},t)\ket{0}  $$
- They are associated with _momentum_ $\boldsymbol{k}$
	- $P^{i}=T^{0i}$, a component of the _energy-momentum tensor_
	- Assume the ground state is _translationally invariant_ such that $P^{i}\ket{0}=0$
	- By definition, $[P^{i},\phi(x)]=i\partial^{i}\phi$
	- Use _integration by parts_ in the last step
$$\begin{align}
P^{i}\ket{\boldsymbol{k}}&=\int d^{d}x \,\exp(ikx)P^{i}J^{0}(\boldsymbol{x},t)\ket{0}   \\
&=i\int \,d^{d}x\,\exp(ikx)\partial^{i}J^{0}\ket{0}  \\
&=\boldsymbol{k}\ket{\boldsymbol{k}} 
\end{align}$$
- In the _low momentum limit_, it is a _ground state_, indicating that $\ket{\boldsymbol{k}}$ are _gapless_
$$\lim_{ k \to 0 }\ket{\boldsymbol{k}}=Q\ket{0}   $$
- This is _Goldstone's Theorem_, where _spontaneous symmetry breaking_ guarantees the existence of _gapless, long wavelength states_

- This allows one to make an _effective field theory_ for these modes 

- Examples: 
	- SSB of $U(1)$ gives _number conservation_ in a _superfluid_
	- SSB of $SU(2)$ gives _spin_, and therefore _magnetism_

## Goldstone bosons in Landau-Ginzburg theory
- Goldstone bosons often arise as the "phase" of an _order parameter_
- The order parameter also has an _amplitude_, which is _fixed_ for all symmetry broken ground states

- _Change in amplitude_ will give a _gapped mode_
- _Change in phase_ gives a _gapless mode_
- Therefore, _effective field theories_ always have a gapped mode
- Example: the Mexican hat potential
	- There is a _phase_ where there is a circle of _distinct, degenerate ground states_ with one gapless mode and one gapped mode
	- There can be a _quantum phase transition_ where the circle _shrinks_ to a point, and there are _two gapped modes_

## Superfluids
- Arise from microscopic theories such as the _Bose-Hubbard model_
	- With both _hopping_ and _on-site repulsion_
$$H=t\sum_{\langle ij \rangle } a_{i}^{\dagger}a_{j}+U\sum_{i}a_{i}^{\dagger}a_{i}^{\dagger}a_{i}a_{i}$$
- There is a _conserved particle number_
$$N=\sum_{i}a_{i}^{\dagger}a_{i}$$
- It generates a $U(1)$ symmetry, with operator $U$, and parameter $\theta \in [0,2\pi)$
$$U=\exp(i\theta N)$$
- In the _thermodynamic limit_ $V\to \infty$, _fix_ the _average particle number per site_
$$n=\frac{\langle N \rangle}{V} $$

- $\langle N \rangle\neq 0$ _does not necessarily break_ the symmetry
- For _vacuum state_ $\ket{\phi}$, suppose there is a _ground state_ $\ket{0}$
$$\ket{0}=\prod_{i}(a^{\dagger}_{i})^{n_{i}}\ket{\phi}  \qquad N\ket{0}=\left( \sum_{i} n_{i}\right) \ket{0} $$
- A _finite system_ with a _fixed number_ of particles _does not break the symmetry_
- Example: the $U\gg t$ phase with _one boson per site_, and therefore is not a symmetry broken state

### U(1) symmetry breaking in superfluids
- Symmetry broken ground state _do not have definite particle number_
- The state is a _superfluid_

- Suppose there is some _regime_ of $t/U$ which undergoes SSB
- Consider _close to the phase transition_ such that one can write a Landau-Ginzburg theory

- Write some _Lagrangian_ with order parameter field $\Psi$
	- The field will be related to $a_{i}$ in some way
	- For a _real field_, the first term would give a _total derivative_
	- The Lagrangian must be _rotationally invariant_ due to the underlying lattice
	- Other higher order terms are expected to be _irrelevant_ due to renormalisation
$$\mathcal{L}=i\Psi ^{\dagger}\partial_{t}\Psi-\frac{1}{2m}(\partial_{i}\Psi)^{\dagger}(\partial_{i}\Psi)-r\Psi^{*}\Psi-\lambda(\Psi ^{\dagger}\Psi)^{2}$$
- The $U(1)$ symmetry is _generated_ by
$$N=\int d^{d}x\,\Psi ^{\dagger}\Psi$$
- There is SSB when $r<0$

- Set $\Psi$ to have an _amplitude_ and _phase_
$$\Psi=\sqrt{ \rho }\exp(-i\theta) \qquad N=\int d^{d}x\,\rho$$
- This gives the Lagrangian as:
	- _Neglect total derivatives_
$$\mathcal{L}=\rho\partial_{t}\theta-\frac{1}{2m}\left[ \frac{1}{4\rho}(\partial_{i}\rho)^{2}+\rho(\partial_{i}\theta)^{2} \right]-r\rho-\lambda \rho^{2}$$
- This implies $\rho$ is a _conjugate momentum_ to the phase
$$\pi_{\theta}=\frac{\partial \mathcal{L}}{\partial\dot{\theta}}=\rho$$
- This implies some _commutation relation_
$$[\rho(x),\theta(y)]=i\delta(x-y)$$
- The _average phase_ (the _zero Fourier mode_)
$$\theta_{0}=\int d^{d}x\,\theta$$

- Integrating over $x,y$, the commutator gives for some _volume_ $V$
$$\left[ \frac{N}{V},\theta_{0} \right]=i$$
- The uncertainty principle:
$$\frac{\Delta N}{V}\Delta\theta_{0}\geq 1$$
- Symmetry breaking requires a _localised phase_ $\Delta\theta_{0}\sim 0$, therefore a _large particle density fluctuation_ in $\Delta N/V$
