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
	- The _quasi-particles_ from the interacting theory can often be _linked_ to the _bare particles_ of the _non-interacting theory_ via the principle of _adiabtic continuity_, as long as _symmetry_ remains

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
$$Q\ket{0}\neq 0\;\;,\;\;Q\ket{0}\neq\ket{0}   $$
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
	- Invariant under transformation of the fields $a_{i} \to Ua_{i}$
$$U=\exp(i\theta N)$$
- In the _thermodynamic limit_ $V\to \infty$, _fix_ the _average particle number per site_
$$n=\frac{\langle N \rangle}{V} $$

- $\langle N \rangle\neq 0$ _does not necessarily break_ the symmetry
- For _vacuum state_ $\ket{\phi}$, suppose there is a _ground state_ $\ket{0}$
$$\ket{0}=\prod_{i}(a^{\dagger}_{i})^{n_{i}}\ket{\phi}  \qquad N\ket{0}=\left( \sum_{i} n_{i}\right) \ket{0} $$
- A _finite system_ with a _fixed number_ of particles _does not break the symmetry_
- Example: the $U\gg t$ phase with _one boson per site_, and therefore is not a symmetry broken state

### U(1) symmetry breaking in superfluids
- Symmetry broken ground states _do not have definite particle number_
- States like that are _superfluids_

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

### XY model as the effective superfluid action
- Given $r<0$, the symmetry broken ground state has:
$$\bar{\rho}=-\frac{r}{2\lambda}$$
- Expanding $\rho=\bar{\rho}+\delta \rho$ in the Lagrangian:
$$\mathcal{L}=-\frac{\bar{\rho}}{2m}(\partial_{i}\theta)^{2}-\frac{1}{8m\bar{\rho}}(\partial_{i}\delta \rho)^{2}-\lambda(\delta \rho)^{2}+\delta \rho\partial_{t}\theta+\dots$$
- The mode for $\theta$ fluctuations is _gapless_
- Amplitude fluctuations are _gapped_
- There is also a _coupling term_

- At low energies (below the gap energy), one can _integrate out_ $\delta \rho$
$$\mathcal{Z}=\int\mathcal{D}\theta\,\mathcal{D}\delta \rho\,\exp(iS[\theta,\delta \rho])=\int\mathcal{D}\theta \,\exp(i\tilde{S}[\theta])$$
- Gaussian integral identities, to _exponential order_
	- In principle, this will _renormalise_ the constants of the theory without changing the terms present
$$\displaylines{\int\,dx\,\exp[-i\alpha x^{2}+i\beta x]\approx \exp\left( \frac{i\beta^{2}}{4\alpha} \right)}$$
- The _effective action_:
$$\displaylines{\tilde{S}[\theta]=\int\,dt\,d^{d}x\,\tilde{\mathcal{L}} \\ \tilde{\mathcal{L}}=-\frac{\bar{\rho}}{2m}(\partial_{i}\theta)^{2}+\partial_{t}\theta  \frac{1}{4\lambda-\partial_{i}^{2}/(2m\bar{\rho})}\partial_{t}\theta}$$
- By continuing to _expand in long wavelengths_, the derivatives in the denominator are neglected
- This gives the _XY model_ as the _effective field theory for gapless Goldstone bosons_
$$\mathcal{L}=\frac{\bar{\rho}}{2|r|}(\partial_{t}\theta)^{2}-\frac{\bar{\rho}}{2m}(\partial_{i}\theta)^{2}$$
- It is an _emergent Lorentz invariant theory_, with _linearly propagating modes_

- At low energies and _long wavelengths_, the effect of _couplings_ and _one-loop determinants_ is only to _re-normalise the low-energy parameters_
- The complete theory has some _propagator_ for $\delta \rho$
$$\frac{1}{8\lambda m\bar{\rho}+k^{2}}$$
- The _looped contributions_ are _analytic_ at _small $k$_ due to the presence of the _gap_

- The effective action must also _obey_ $U(1)$ symmetry, which _forbids mass terms_
- There may be _higher order terms_ which _break Lorentz invariance_, but they will never generate a gap/mass
### Plane wave solutions and supercurrents
- The plane wave solutions:
	- The velocity itself is _non-universal_
$$\displaylines{\theta\sim \exp[i(\omega t-\boldsymbol{k}\cdot \boldsymbol{x})]\implies \omega=\pm v|\boldsymbol{k}| \\ v=\sqrt{ \frac{|r|}{m} }}$$
- The gapless mode emerged from the $U(1)$ symmetry $\theta\to \theta+\tau$
- From _Noether's theorem_, the _conserved currents_:
$$\displaylines{n=J^{t}=\frac{\bar{\rho}}{|r|}\partial_{t}\theta \qquad J^{i}=\frac{\bar{\rho}}{2m}\partial_{i}\theta \\ \dot{n}+\partial_{i}J^{i}=0}$$
- The _current conservation_ is also the _equation of motion_ for the Goldstone boson

- Consider a _position-dependent phase_ $\theta=Ax$, which is also _time-independent_
- It gives a _current with constant particle density_
	- A _dissipationless supercurrent_

### Low dimension effects and the Coleman-Mermin-Wagner theorem
- At _low dimensions_, there can be _strong quantum mechanical effects_ at low energies

- _Classically_, the superfluid phase is _localised_ at each point in space, written as $\theta(\boldsymbol{x})$
- In quantum mechanics, there is some _variance_ in the phase:
	- Set $\langle \theta(x) \rangle=0$
$$(\Delta \theta)^{2}=\langle \theta^{2}(x) \rangle=\frac{1}{\mathcal{Z}}\int \mathcal{D}\theta \,\theta^{2}(x)\,\exp(i \tilde{S})$$
- Writing the Lagrangian as:
$$\mathcal{L}=\frac{\chi}{2}[(\partial_{t}\theta)^{2}-v^{2}(\partial_{i}\theta)^{2}]$$
- The variance in $d$ dimensions:
	- Treat $\boldsymbol{p}$ as some $(d+1)-$dimensional vector $(\omega,\boldsymbol{k})$
$$(\Delta\theta)^{2}=\frac{1}{\chi}\int \frac{d^{d+1}p}{(2\pi)^{d+1}} \frac{1}{\omega^{2}-v^{2}k^{2}}$$
- Implement some _high-momentum cutoff_ for the effective field theory
- For $d>1$, one can set the lower limit to $0$ without IR divergences
- For $d=1$, there is a _long wavelength (IR) divergence_:
$$(\Delta\theta)^{2}\sim \ln \frac{\Lambda _\text{UV}}{\Lambda _\text{IR}}$$
- Therefore, at 1D, the _phase does not remain localised_, and _spreads_ around the circle instead
- In $1+1$ dimensions, there is _no spontaneous symmetry breaking_ due to _quantum fluctuations_
- This is the _Coleman-Mermin-Wagner theorem_

### Long range order
- It _characterises_ spontaneous symmetry breaking
- When there is _long-range order_, the _two-point function_ for _infinite_ spatial separation is:
	- Also known as _off-diagonal long-range order_
$$\lim_{ |\boldsymbol{x}| \to \infty } \langle \Psi ^{\dagger}(\boldsymbol{x},0)\Psi(0,0) \rangle =\rho_{0}^{2}\neq 0$$
- This remains true even for _symmetric superpositions_ of the symmetry breaking state:
	- For a symmetric superposition, $\langle \Psi \rangle=0$ even _with_ SSB, due to _cancellations_ in phase
$$\ket{\Psi}=c_{1}\ket{\theta_{1}} +c_{2}\ket{\theta_{2}}+\dots+c_{1}\ket{-\theta_{1}}+   c_{2}\ket{-\theta_{2}} $$
- Hence, $\langle \Psi ^{\dagger}(\boldsymbol{x})\Psi(0) \rangle$ and _long range order_ is an _indicator for the presence of SSB_

- In the _disordered_ (symmetric) state, one typically finds that the two-point function _decays with some correlation length_ $l$
$$\lim_{ |\boldsymbol{x}| \to \infty } \langle \Psi ^{\dagger}(\boldsymbol{x},0)\Psi(0,0) \rangle\sim \exp(-|x|/l)  $$

- Example: in 1+1 dimensions, in the $r<0$ regime, one gets _algebraic long-range order_
$$\lim_{ |\boldsymbol{x}| \to \infty } \langle \Psi ^{\dagger}(\boldsymbol{x},0)\Psi(0,0) \rangle =\frac{A}{|\boldsymbol{x}|^{\alpha}} \qquad \alpha=\frac{1}{2\pi v\chi}$$
- There is an _infinite correlation length_ even as the system is _not strictly ordered_

## Quantum magnets
- The interactions of _spins_ in an insulator
	- The electrons themselves stay _fixed_
- The Heisenberg model:
$$H=J\sum_{\langle ij \rangle }\boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}$$
- This has an $SU(2)$ _spin symmetry_
	- An _internal symmetry_ of the spins, _unrelated_ to spatial rotations

- For $J<0$, the neighbouring spins _align_ to give a _ferromagnet_
- For $J>0$, the spins form an _anti-ferromagnet_
- In both cases, the spins pick some _orientation_, breaking $SU(2)$ down to $U(1)$
	- $U(1)$: rotations about the spin

- The Goldstone bosons parametrise the _coset_ $SU(2)/U(1)$, which is the _2-sphere_ $S^{2}$
- The gapless modes are then _parametrised_ by some vector $\boldsymbol{n}(\boldsymbol{x},t)$
$$\boldsymbol{n}\cdot \boldsymbol{n}=1$$

- One can then write the effective field theory _in terms of_ $\boldsymbol{n}$
- Then it can be linked back to the _spins_

### The Weiss-Zumino term
- Fields with constraints such as $|n|^{2}=1$ are known as the _non-linear $\sigma$ model_
- The _first order derivative terms_ must obey the symmetry while being _non-trivial_:
$$\boldsymbol{n}\cdot \frac{d\boldsymbol{n}}{dt}=\frac{1}{2} \frac{d}{dt}(\boldsymbol{n}\cdot \boldsymbol{n})=0$$
- Write:
$$n^{i}=\boldsymbol{z}^{\dagger}\sigma^{i}\boldsymbol{z}$$
- Here, $\sigma_{i}$ are the _Pauli matrices_
- $\boldsymbol{z}$ is a _complex_, two-component vector, with $z^{\dagger}z=1$
- Example parametrisation:
$$z=\pmatrix{e^{-i\phi}\cos(\theta/2) \\ \sin(\theta/2)}\implies \boldsymbol{n}=\pmatrix{\sin\theta \cos \phi \\ \sin\theta \sin \phi \\ \cos\theta}$$
- However, there is some _redundancy_ $z\to \exp(i\psi)z$
	- $z$ has 3 _free components_
	- The mapping from $z$ to $n$ is a _Hopf map_ from $S^{3}$ to $S^{2}$, where $\exp(i\psi)$ is a $U(1)$ _fibre_ over $S^{2}$

- An $SU(2)$ _spin rotation_ acting on $z$ becomes some _rotation matrix_ $R$ for $n$
$$\displaylines{z'=Uz \implies n'=Rn \\ R^{ij}\sigma^{j}=U^{\dagger}\sigma^{i}U \implies R^{T}R=1 \qquad \det R=1}$$
- Therefore, _any term in the Lagrangian_ has to be invariant under:
	- Unitary transformation $U$
	- Change in phase $\psi$ of $z$

- The _Weiss-Zumino term_ of the action is one that is _invariant under global rotations_, written in terms of $z$ as:
	- Ignoring _spatial variations_ for now
$$S_\text{W-Z}=2iS\int z^{\dagger}\cdot \frac{dz}{dt}dt$$
- The _fields_ of the theory are $\theta,\phi,\psi$, which _can be time-dependent_
- Therefore, to _impose_ invariance under $z\to \exp (i\psi)z$

- By parametrising $z$ with $\theta(t),\phi(t),\psi(t)$
$$S_\text{W-Z}=S\int dt\,\left[ (1+\cos\theta) \frac{d\phi}{dt}-2 \frac{d\psi}{dt} \right]=S\int d\phi\,\left[ (1+\cos\theta)-2 \frac{d\psi}{d\phi} \right]$$
- The two terms can each be interpreted as a _line integral_ on some 2-sphere $\phi,\theta$ or $\phi,\psi$
	- For a path integral in the $T\to{0}$ limit, the integral should be over _closed loops_ on $S^{2}$

- From _Stokes_ theorem, this can be expresed as an _area_
	- For loop $\gamma$ and area $\Sigma$
$$\int_{\gamma}A=\int_{\Sigma}dA$$
- This gives the action as the integral of an _area element_
	- The _curl of a gradient_ is $0$, cancelling out the second term
	- There are two _distinct_ areas over $S^{2}$, $\Sigma$ and $\Sigma'$, _inside_ and _outside_ the loop
$$\begin{align}
S_\text{W-Z}&=S\int_{\Sigma} \sin\theta\,d\theta \land d\phi \\
&=S \times \mathrm{Area}(\Sigma)=-S\times \mathrm{Area}(\Sigma')
\end{align}$$
- The Weiss-Zumino term is then _independent_ of $\psi$
- For the _partition function_ to be well-defined, as it is a path integral of $\exp(iS_\text{W-Z})$, the two expressions must _differ by an integer multiple_ of $2\pi$

- As the total area of $\Sigma+\Sigma'$ is $4\pi$, this gives that $S$ is some _integer or half-integer_
$$S=\frac{N}{2} \qquad N\in \mathbb{Z}$$
- The Weiss-Zumino term is _well-defined for integer or half-integer_ $S$
- $S$ corresponds to the _microscopic spin_

### The coherent state path integral
- Deriving the Weiss-Zumino term from a _microscopic spin_

- Consider one spin with a _vanishing Hamiltonian_
- The path integral is still _non-trivial_

- Let $\ket{\uparrow}$ be the _highest weight state_ of the spin $S$ irrep of $SU(2)$
$$S^{+}\ket{\uparrow}=0 $$
- Given _group element_ $g$ of the irrep, define the state $\ket{g}$
$$\ket{g}=g\ket{\uparrow}  $$
- The basis of coherent states:
	- Integration over the $SU(2)$ invariant _Haar measure_
	- $C$ is some _constant_
	- $\mathrm{Id}.$ is the _unit operator_ of the irrep
	- Proof: apply $h\, \in SU(2)$ to the left, rotate basis $g\to h^{-1}g$, pull $h$ to the right to prove that the operator _commutes_ with any group element
	- _Schur's lemma_: an operator commuting with any group element must be proportional to the _identity_
$$\int dg\, \ket{g}\bra{g}=C\times \mathrm{Id.}  $$
- The basis is _over-complete_
	- e.g. for spin $1/2$, $\ket{\uparrow}\bra{\uparrow}+\ket{\downarrow}\bra{\downarrow}=\mathrm{Id.}$ such that adding _other states_ $\ket{g}\bra{g}$creates other copies of the identity

- Then consider a _propagator_, broken up into _time-steps_
	- Take the states to also be _normalised_ $\braket{ g_{i} | g_{i} }=1$
$$\braket{ g(t) | g(0) } =\frac{1}{C^{N}} \prod_{i=1}^{N} \int dg_{i} \braket{ g(t) |g_{N}  } \braket{ g_{N} |g_{N-1}  }\bra{g_{N-1}} \dots \ket{g_{1}}  \braket{ g_{1} |g(0)  }  $$
- For some _small step_, the propagators:
$$\braket{ g_{N} | g_{N-1} }=1+\braket{ g_{N} |g_{N-1}  }-\braket{ g_{N-1} |g_{N-1}  } \approx \exp[\braket{ g_{N} |g_{N-1}  }-\braket{ g_{N-1} |g_{N-1}  }]  $$
- This gives the total propagator as
$$\braket{ g(t) |g(0)  }=\frac{1}{C^{N}} \prod_{i=1}^{N}\int dg_{i}\exp\left[ \sum_{i=0}^{N} \braket{ g_{i} |g_{i-1}  }-\braket{ g_{i-1} |g_{i-1}  } \right]$$
- In the _continuum limit_, this becomes a derivative:
$$\braket{ g(t) | g(0) }=\int \mathcal{D}g\,\exp\left[\int_{0}^{t} dt\,\Braket{ \frac{dg}{dt} | g }  \right] $$
- Use an _explicit representation_ of $g$, with _Euler angles_
$$\ket{g}=\exp(-i\phi S_{3})\exp(-i\theta S_{2})\exp(-i\psi S_{3})\ket{\uparrow}  $$
- From the $SU(2)$ algebra:
$$\braket{ g|S_{i} | g }=Sn_{i} \qquad n=\pmatrix{\sin\theta \cos \phi \\ \sin\theta \sin \phi \\ \cos\theta}$$
- The _expectation value_ is the position of some _classical spin_
- These states are a _good representation_ of _classical angular momentum_
	- _Localised_ in one direction, _smeared_ in the others as the $SU(2)$ algebra _does not commute_

- In the action:
$$\Braket{ \frac{dg}{dt} | g } =iS\cos\theta \frac{d\phi}{dt}$$
- This gives [[#The Weiss-Zumino term]] with $S$ corresponding to the _microscopic spin_

### Ferromagnetic spin waves
- Given the Weiss-Zumino term, one can then find an effective field theory for the _Goldstone modes_, characterised by normal vector $\boldsymbol{n}$
$$ \boldsymbol{n}=\pmatrix{\sin\theta \cos \phi \\ \sin\theta \sin \phi \\ \cos\theta}$$
- Then include _spatial derivatives_ in the Lagrangian
	- No _first derivative_ term as it violates reflection symmetry
	- There is _no potential term_ due to the constraint $n^{2}=1$
$$\mathcal{L}=s(1+\cos\theta)\frac{d\phi}{dt} +u|\nabla \boldsymbol{n}|^{2}+\dots$$
- Given some perturbation starting from the equator:
$$\theta=\frac{\pi}{2}-\delta \theta \qquad \phi=\delta \phi$$
- This gives the Lagrangian:
$$\mathcal{L}=S\,\delta\theta\,\delta \dot{\phi}-u\left[|\nabla\delta\theta|^{2}+|\nabla\delta \phi|^{2}\right]+\dots$$
- There is a _coupling term_ between $\delta \theta$ and $\delta \phi$
- The equations of motion:
$$S\delta \dot{\phi}+2u\nabla^{2}\delta\theta=0 \qquad -S\delta\dot{\theta}+2u\nabla^{2}\delta \phi=0$$
- Plane wave solutions will give the equation:
$$\pmatrix{-2uk^{2}&-i\omega S \\ i\omega S & -2uk^{2}}\pmatrix{\delta\theta_{0} \\ \delta \phi_{0}}=0 \quad \implies \quad \omega=\pm \frac{2u}{S}k^{2}$$
- Unlike the [[#Plane wave solutions and supercurrents|superfluid]], the dispersion is _quadratic_
	- From the Weiss-Zumino term: _one time derivative_ and two spatial derivatives
- This represents _ferromagnetic spin waves_

### Classical limit and the spatial gradient term
- Take the _large_ $S$ limit
- From generalised uncertainty:
$$\Delta S^{i}\Delta S^{j}\geq |\langle [S^{i},S^{j}] \rangle|=|\epsilon^{ijk}\langle S^{k} \rangle | $$
- From $|\langle S^{k} \rangle|\leq S$, quantum uncertainty gives:
$$\frac{\Delta S^{i}\Delta S^{j}}{S^{2}}\leq \frac{1}{S}$$
- _Quantum fluctuations_ of spins become _small_ at large $S$
	- At large $S$, _loop effects_ are also suppressed

- Take the Heisenberg model for large $S$
$$H=J\sum_{\langle ij \rangle }\boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}$$
- Add this to [[#The coherent state path integral]]

- The extra term in each _propagator_:
$$J\langle g|\boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}|g \rangle $$
- Consider _inserting_ a full set of basis states (as done in deriving the path integral), and using the _Euler angle representation_, this gives the term:
$$S^{2}\boldsymbol{n}_{i}\cdot \boldsymbol{n}_{j}=-\frac{S^{2}J}{2}(\boldsymbol{n}_{i}-\boldsymbol{n}_{j})^{2}+\text{const.}$$
- Taking the _continuum limit_:
$$\to \frac{S^{2}J}{2}a^{2}|\nabla \boldsymbol{n}|^{2}$$
- This gives the gradient term energy $u$ in the action
- This is _Bloch's law_:
$$\omega=\pm |J|Sa^{2}k^{2}$$
- $|J|$ sets the _energy scale_, while $a$ sets the _distance scale_
- Additional scaling factor $S$

### Antiferromagnetism and super-exchange
- Physical example: _super-exchange_ in the Hubbard model
$$H=t\sum_{\langle ij \rangle }c^{\dagger}_{is}c_{js}+U\sum_{i}n_{i\uparrow}n_{i\downarrow}$$
- Consider $U\gg t$, with _one electron per site_ (half filling)
- At $t=0$, there is a _very degenerate ground state_

- Use _degenerate second order perturbation theory_ in $t$
- If spins are _parallel_, there is _no hopping_ allowed
- For _anti-parallel_ spins, electrons are allowed to hop to create _double occupancy_, then _hop back_

- Inspect only a _pair_
$$H|_\text{pair}=\pmatrix{0&t\\t&U}$$
- This gives the energies up to second order:
$$E_{+}=U+\frac{t^{2}}{U} \qquad E_{-}=-\frac{t^{2}}{U}$$
- Second order processes will _reduce_ energy of _anti-alignment_, giving an _anti-ferromagnet_

- The antiferromagnetic state can be _frustrated_
	- e.g. a _triangular_ configuration of spins
	- Gives _emergent gauge fields_ in _spin ices and liquids_

- Restrict the system to a _bi-partite lattice_, where there are _sub-lattices_ $A$ and $B$ such that each site is _only connected to sites on the other lattice_
	- There is _no frustration_ in bipartite lattices

### Antiferromagnetic spin waves
- The action with a _Heisenberg term_ of $J>0$
$$S=\sum_{i}S_\text{W-Z}[\boldsymbol{n}_{i}]-S^{2}J\int dt\,\sum_{\langle ij \rangle }\boldsymbol{n}_{i}\cdot \boldsymbol{n}_{j}$$
- Consider spin configurations close to the _Neel state_
$$\boldsymbol{n}_{i}(t)=(-1)^{i} \boldsymbol{\tilde{n}}(\boldsymbol{x}_{i},t)+\boldsymbol{m}(\boldsymbol{x}_{i},t)$$
- Let $\boldsymbol{\tilde{n}}$ be a _slowly varying function_ of the lattice site
	- A _slow rotation_ of the ordering vector
	- $(-1)^{i}$ is _fast varying_ between sites as it is close to the Neel state
- Let $\boldsymbol{m}$ also be slowly varying, and impose:
$$|m|\ll|\tilde{n}| \qquad |\tilde{n}|^{2}=1 \qquad \boldsymbol{m}_{i}\cdot \tilde{\boldsymbol{n}}_{i}=0$$

- Plug into the _Heisenberg action_, expand, and take the continuum limit
	- The $(\tilde{\boldsymbol{n}}_{i}-\tilde{\boldsymbol{n}}_{j})^{2}$ becomes the spatial derivative term
	- The $\boldsymbol{m}_{i}\cdot \boldsymbol{m}_{j}$ term becomes a _sum over nearest neighbours_ to give $2d$ factor
	- Nearest neighbours: approximate $\boldsymbol{m}_{i}=\boldsymbol{m}_{j}$ as it is _slowly varying_
$$\sum_{\langle ij \rangle }\boldsymbol{n}_{i}\cdot \boldsymbol{n}_{j}\longrightarrow \int \frac{d^{d}x}{a^{d}}\left[  \frac{a^{2}}{2}|\nabla \tilde{\boldsymbol{n}}|^{2}+2d|\boldsymbol{m}|^{2} \right]$$

- [[#The Weiss-Zumino term]]: some _oriented area_ on the $2-$sphere carved out by $\boldsymbol{n}_{i}$
$$S_\text{W-Z}[\boldsymbol{n}]=S\Gamma[\boldsymbol{n}]$$
- The neighbouring _opposite spin_ $-\boldsymbol{n}_{i}$ will _cover the same area_:
	- Second term _drops out_ of path integral due to exponential
$$S_\text{W-Z}[-\boldsymbol{n}]=S\Gamma[-\boldsymbol{n}]=S[4\pi-\Gamma[\boldsymbol{n}]]=-S\Gamma[\boldsymbol{n}]+S({4}\pi)$$
- Consider the sum:
$$\sum_{i}(-1)^{i}S_\text{W-Z}[\tilde{\boldsymbol{n}}_{i}]$$
- As the Weiss-Zumino term of $\tilde{n}$ is _slowly varying_, this ends up _cancelling out_
	- Not in 1 dimension

- Meanwhile, for the _fluctuation_, variations in the Weiss-Zumino term in terms of $\delta \boldsymbol{n}$ are:
$$\int dt\,\delta\left( z^{\dagger}_{i} \frac{dz_{i}}{dt} \right)=-\frac{i}{2}\int dt\,\delta \boldsymbol{n}_{i}\cdot\left( \boldsymbol{n}_{i}\times \frac{d\boldsymbol{n}_{i}}{dt} \right)$$
- This gives
	- Variation: $\boldsymbol{m}$ to first order
$$S_\text{W-Z}=S\int dt\, \frac{d^{d}x}{a^{d}}\,\boldsymbol{m}\cdot\left( \tilde{\boldsymbol{n}}\times \frac{d\tilde{\boldsymbol{n}}}{dt} \right)$$
- The relevant _action_ terms that do not cancel out:
$$S=\int dt\,\frac{d^{d}x}{a^{d}} \left[ S \boldsymbol{m}\cdot(\tilde{\boldsymbol{n}}\times \dot{\tilde{\boldsymbol{n}}})-S^{2}J(2dm^{2})- \frac{S^{2}Ja^{2}}{2}|\nabla \tilde{\boldsymbol{n}}|^{2} \right]$$
- $\boldsymbol{m}$ has a _mass term_, and is therefore _gapped_
- Then _integrate out_ $\boldsymbol{m}$
	- First term: $|\tilde{\boldsymbol{n}}\times \dot{\tilde{\boldsymbol{n}}}|^{2}$ with the $\tilde{n}^{2}=1$ constraint
$$\int \mathcal{D}m\,\exp(iS[\boldsymbol{m},\tilde{\boldsymbol{n}}])=\exp\left\{i \int dt\,\frac{d^{d}x}{a^{d}} \frac{\dot{\tilde{n}}^{2}}{8Jd}-i \frac{S^{2}Ja^{2}}{2}|\nabla \tilde{\boldsymbol{n}}|^{2} \right\}$$
- The effective Lagrangian is then:
	- Still in the _large spin_ limit
	- Outside the limit: the same effective field theory, with a _different spin wave velocity_
$$\mathcal{L}_\text{EFT}=\frac{1}{8Jd}[\dot{\tilde{n}}^{2}-v^{2}|\nabla \tilde{\boldsymbol{n}}|^{2}]\qquad v=2\sqrt{ d }SJa$$
- This is the _relativistic non-linear $\sigma-$model_

- The _ferromagnetic_ and _antiferromagnetic_ field theories both _break_ $SU(2)$ into $U(1)$ but with _different dispersions_
	- Watanabe-Murayama
	- Ferromagnetic: there is a _macroscopic expectation value_ for the symmetry generator (the spin), giving a _quadratic mode_ instead of a linear mode

### Antiferromagnetic spin chains
- Spin chain: the $d=1$ case
- Here, the _leading term_ of the Weiss-Zumino term is nontrivial

- Sum over _pairs_:
$$S_\text{W-Z}=S\sum_{i}(-1)^{i}\Gamma[\tilde{\boldsymbol{n}}_{i}]=S\sum_{i \in 2\mathbb{Z}}(\Gamma[\tilde{\boldsymbol{n}}_{i+1}]-\Gamma[\tilde{\boldsymbol{n}}_{i}])$$
- In the _continuum limit_:
	- Derivative of the area: $\boldsymbol{n}_{i}\times \dot{\boldsymbol{n}}$ from variation of Weiss-Zumino term
$$\begin{align}
S_\text{W-Z}&=S\int dt\,\frac{dx}{2a} \Gamma'[\tilde{\boldsymbol{n}}](\nabla \tilde{\boldsymbol{n}}\cdot \boldsymbol{a}) \\ &= \frac{S}{2}\int dx\,dt\,\tilde{\boldsymbol{n}}\cdot(\partial_{t}\tilde{\boldsymbol{n}}\times \partial_{x} \tilde{\boldsymbol{n}})
\end{align}$$

- Define:
$$\theta=2\pi S$$
- Rewrite the action as
$$S_{\theta}= \frac{i\theta}{4\pi}\int dx\,dt \,\tilde{\boldsymbol{n}}\cdot(\partial_{t} \tilde{\boldsymbol{n}}\times \partial_{x}\tilde{\boldsymbol{n}})$$
- It is a _topological term_ in $d=1$

- In higher dimensions, the analagous term is _suppressed_ by _renormalisation flow_