- All particles and waves aare _excitations_ of a _quantum field_ over all spacetime

- Elementary particles are [[Identical Particles|identical]] as they are _excitations of the same field_
- Permutation groups are _constrained_, leading to Fermi-Dirac/Bose-Einstein statistics
- Particles are [[Identical particles and second quantisation#Creation and annihilation operators|created and annihilated]]

- A _field_ takes a _point in space-time_, then outputs some _object_ (scalar, vector, tensor etc.)

- Spacetime described by [[Special Relativity]], which is a [[Classical Field Theory]]
	- GR is also a classical field theory, but is still yet incompatible
	- Use all conventions from previous notes on classical field theory

## Conventions
- Convention for metric tensor:
$$g_{\mu \nu}=\mathrm{diag}(1,-1,-1,-1)$$

- Unit conventions:
$$c=\hbar=1$$
	- Conversion: $\hbar c=0.2\,\text{GeV}\,\text{fm}$
	- $[\text{T}]=[\text{E}]^{-1}=[\text{M}]^{-1}$
- Heaviside-Lorentz system:
$$\epsilon_{0}=\mu_{0}=1$$

- _Four-dimensional_ Fourier transforms:
$$\tilde{f}(k)=\int  d^{4}x\,\exp(ik\cdot x)\,f(x) $$
- Alternatively, with the $3+1$ split:
$$\tilde{f}(\omega,\boldsymbol{k})=\int   d^{3}x\,dt\,\exp[i(\omega t-\boldsymbol{k}\cdot \boldsymbol{x})] $$
- The inverse transform:
$$f(x)=\int  \, \frac{d^{4}k}{(2\pi)^{4}}\,\exp(-ik\cdot x)\,\tilde{f}(k) $$

# Functionals and Lagrangians
- Functional: function to scalar

- The _functional derivative_:
$$\frac{\delta F}{\delta f(x)}=\lim_{ \epsilon \to 0 } \frac{F[f(x')+\epsilon\delta(x'-x)]-F[f(x')]}{\epsilon} $$
- How much the _scalar_ returned by $F$ varies as $f(x)$ is varied

- Given some _Lagrangian_ $L$ of the motion $x(t)$, define a functional known as the _action_ $S$
	- Particle motion with no electromagnetic fields: $L=T-V$
$$S=\int L \, dt$$
- The _Principle of Least Action_ states that classical motion satisfies:
$$\frac{\delta S}{\delta x(t)}=0$$
- This gives the _Euler-Lagrange equation_:
$$ \frac{d}{dt} \frac{\partial L}{\partial \dot{x}} -\frac{\partial L}{\partial x}=0$$
- Define the _Lagrangian density_ $\mathcal{L}$:
$$L=\int \mathcal{L} \, d^{3}x $$
- This gives the action as:
	- This is _Lorentz invariant_
$$S=\int \mathcal{L} \, d^{4}x $$
- Given some _field_ $\phi(x^{\mu})$:
$$S=\int  \, d^{4}x\,\mathcal{L}(\phi,\partial_{\mu}\phi) $$
- The principle of least action then gives:
$$\frac{\partial \mathcal{L}}{\partial \phi}-\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi)} \right)=0$$

- In quantum mechanics, $S$ is associated with the _phase_ of a path
- Paths of _non-extremal action_ will _cancel out_ to give the _classical path_

# Second quantisation
- A more complete treatment: [[Identical particles and second quantisation]]

- _First quantisation_ is the description of _particles_ as _wave functions_
- _Second quantisation_: _wave-like_ phenomena can _behave like particles_

- Both particles and waves are part of a _quantum field_

## Oscillators
- Model everything as _harmonic oscillators_
- Annihilation and creation operators $a,a^{\dagger}$
- Number operator $a^{\dagger}a$

- Number eigenstate:
$$\ket{n}=\frac{1}{\sqrt{ n! }} (a^{\dagger})^{n}\ket{0} $$

- Let there be $N$ _uncoupled oscillators_ that one can put quanta into:
$$H=\sum_{k=1}^{N}\hbar\omega_{k}\left( a_{k}^{\dagger}a_{k}+\frac{1}{2} \right)$$
- There is a _vacuum state_ $a_{k}\ket{\text{VAC}}=0\,\,\,\forall k$

- A general state is _labelled by occupation numbers_:
$$\displaylines{\ket{n_{1},n_{2},\dots n_{N}} =\frac{1}{\sqrt{ n_{1}!n_{2}!\dots n_{N}! }} (a_{1}^{\dagger})^{n_{1}}(a^{\dagger}_{2})^{n_{2}}\dots(a_{N}^{\dagger})^{n_{N}}\ket{0,0\dots0}  \\ \ket{\{n_{k}\}} =\prod_{k} \frac{1}{\sqrt{ n_{k}! }}(a_{k}^{\dagger})^{n_{k}}\ket{\text{VAC}} }$$

## Coupled oscillators: phonons
- Hamiltonian for a _linear chain_ of $N$ atoms of mass $m$
$$H=\sum_{j} \frac{p_{j}^{2}}{2m}+\frac{1}{2}K(x_{j+1}-x_{j})^{2}$$
- The masses are _strongly coupled_ to their neighbours
- However, after a _Fourier transform_, the excitations are _uncoupled in reciprocal space_

- Fourier transforms:
$$\displaylines{x_{j}=\frac{1}{\sqrt{ N }}\sum_{j}x_{k}\exp(ikja)\hspace{1.5cm}p_{j}=\frac{1}{\sqrt{ N }}\sum_{j}p_{k}\exp(ikja) \\ x_{k}=\frac{1}{\sqrt{ N }}\sum_{j}x_{j}\exp(-ikja)\hspace{1.5cm}p_{k}=\frac{1}{\sqrt{ N }}\sum_{j}p_{j}\exp(-ikja)}$$
- Enforce _periodic boundary conditions_ such that $\exp(ikja)=\exp[ik(j+N)a]$
$$\frac{1}{N}\sum_{j}\exp(ikja)=\delta_{k0}$$
- From this definition and the _Hermiticity_ of $x_{j},p_{j}$
$$x_{k}^{\dagger}=x_{-k}$$
- From the commutation relation $[x_{j},p_{j}]=i\hbar\delta_{ij}$
$$[x_{k},p_{k'}]=i\hbar\delta_{k,-k'}$$

- The Hamiltonian can then be expressed as:
$$\displaylines{H=\sum_{k}\left[ \frac{1}{2m}p_{k}p_{-k}+\frac{1}{2}m\omega_{k}^{2}x_{k}x_{-k} \right] \\ \omega_{k}^{2}=\frac{4K}{m}\sin^{2}\left( \frac{ka}{2} \right)}$$

- Define the ladder operators:
$$a_{k}=\sqrt{ \frac{m\omega_{k}}{2\hbar} }\left( x_{k}+\frac{ip_{k}}{m\omega_{k}} \right)$$
- This gives the _boson commutation relations_:
$$[a_{k},a_{k'}^{\dagger}]=0 \hspace{1cm}[a_{k},a_{k'}]=[a_{k}^{\dagger},a_{k'}^{\dagger}]=0$$
- The Hamiltonian can be expressed as:
$$H=\sum_{k}\hbar\omega_{k}\left( a_{k}^{\dagger}a_{k}+\frac{1}{2} \right)$$
- Modes of different $k$ behave as _independent oscillators_, known as _phonons_
- Each phonon mode is an _oscillator_ with _quanta_ of energy $\hbar\omega_{k}$, like _particles_

- Therefore, _wave-like systems_ can have _particle-like behaviour_

## Occupation number representation
- Similar to labelling a _set of oscillators_ by the _number of quanta in each oscillator_, _any system_ can be labelled by the _occupation of each eigenstate_

- For distinguishable particles, to _build_ a general state from _operators_:
$$\ket{n_{1}n_{2}\dots}=\prod_{k} \frac{1}{\sqrt{ n_{k}! }}(a_{k}^{\dagger})^{n_{k}}\ket{\text{VAC}}  $$

### Fermions and bosons
- Under _particle exchange_, the wavefunction is either _symmetric_ (bosons) or _anti-symmetric_ (fermions)
$$a_{p_{1}}^{\dagger}a_{p_{2}}^{\dagger}=\pm a_{p_{2}}^{\dagger}a_{p_{1}}^{\dagger}$$
- In the case of _bosons_, using the above and in analogy with the harmonic oscillator:
$$[a_{i},a_{j}^{\dagger}]=\delta_{ij}\hspace{1cm}[a_{i},a_{j}]=[a_{i}^{\dagger},a_{j}^{\dagger}]=0$$
- The _order_ in which particles are created _does not matter_:
$$\ket{n_{1}n_{2}\dots}=\prod_{k} \frac{1}{\sqrt{ n_{k}! }}(a_{k}^{\dagger})^{n_{k}}\ket{\text{VAC}}$$
- In general:
$$\begin{align}
a_{i}^{\dagger}\ket{n_{1}\dots n_{i}\dots}&=\sqrt{ n_{i}+1 }\ket{n_{1}\dots n_{i}+1\dots} \\  a_{i}\ket{n_{1}\dots n_{i}\dots}&=\sqrt{ n_{i} }\ket{n_{1}\dots n_{i}-1\dots}  
\end{align}$$

- In the case of _fermions_:
$$\{c_{i},c_{j}^{\dagger}\}=\delta_{ij}\hspace{1cm}\{c_{i},c_{j}\}=\{c_{i}^{\dagger},c_{j}^{\dagger}\}=0$$
- The _order_ in which particles are put into states _matters_
- The _Pauli exclusion principle_ means that _no two identical fermions can occupy the same state_ $(n_{i}=0\text{ or }1)$
- The normalisation of the operators:
$$\begin{align}
c_{i}^{\dagger}\ket{n_{1}\dots n_{i}\dots} &=(-1)^{\Sigma_{i}}\sqrt{ 1-n_{i} }\ket{n_{1}\dots n_{i}+1\dots} \\ c_{i}\ket{n_{1}\dots n_{i}\dots} &=(-1)^{\Sigma_{i}}\sqrt{ n_{i} }\ket{n_{1}\dots n_{i}-1\dots} \\ \Sigma_{i}&=n_{1}+n_{2}+,,,+n_{i-1}
\end{align}$$

### Continuous state labels
- If eigenstates are labelled with a _continuous quantity_ (e.g. momentum)
$$[a_{\boldsymbol{p}},a_{\boldsymbol{q}}]_{\pm}=\delta^{3}(\boldsymbol{p}-\boldsymbol{q})$$
- To calculate energy:
$$H=\int  \, d^{3}p\,E_{\boldsymbol{p}}a_{\boldsymbol{p}}^{\dagger}a_{\boldsymbol{p}} $$

## Field operators
- One can _change basis_ for the ladder operators in order to create/annihilate particles at a _specific spatial location_
- The _field operators_, in terms of _energy ladder operators_, are:
	- One can also use _momentum ladder operators_, with _plane waves_ as the wave-functions
$$\begin{align}
\psi ^{\dagger}(\boldsymbol{x})&=\sum_{n}\phi_{n}^{*}(\boldsymbol{x})a_{n}^{\dagger} \\ \psi(\boldsymbol{x}) &=\sum_{n}\phi_{n}(\boldsymbol{x})a_{n}
\end{align}$$
## Second-quantising operators
- Typical operators $\mathcal{O}$ take states $\ket{\psi}$ in _Hilbert space_ into another state $\mathcal{O}\ket{\psi}$
- $n-$_particle operators_ depend on $n$ particle coordinates

- For a _single-particle operator_:
$$\mathcal{O}=\sum_{\alpha\beta}\mathcal{O}_{\alpha\beta}\ket{\alpha}\bra{\beta}  $$
- To have it describe a _many-particle state_:
$$O=\sum_{\alpha\beta}\mathcal{O}_{\alpha\beta}a_{\alpha}^{\dagger}a_{\beta}$$
- It lives in _Fock space_, the space of _all $N-$particle states_ for all $N$
	- The _subspaces_ of $n-$particle states must only include _symmetrised/anti-symmetrised_ states
- It effectively _sums over_ processes removing a particle from $\beta$ and _adding_ a particle to $\alpha$

- Tight-binding _kinetic energy_: _annihilate_ some particle at site $i$ then _create_ another at site $j$ to represent _movement_ with energy $t_{ij}$

- Two particles: _avoid double-counting_, abd use _normal ordering_ to eliminate _self-energy_

- Hubbard model: kinetic energy + _two-body interactions_

# Classical fields
- A _field_ is a _map_ living in 4-dimensional spacetime
- There can be _scalar fields_ $\phi$, or _complex scalar fields_, or _vector fields_, or _tensor fields_

## Recap of classical mechanics and field theory
- The _canonical momentum_ of a system:
$$p_{i}=\frac{\partial L}{\partial \dot{q}_{i}}$$
- The _Hamiltonian_:
$$H=p_{i}\dot{q}_{i}-L$$
- _Hamilton's equations_:
$$\frac{\partial H}{\partial q_{i}}=-\dot{p}_{i}\hspace{1.5cm}\frac{\partial H}{\partial p_{i}}=\dot{q}_{i}$$
- The _Poisson bracket_:
$$\{A,B\}_{PB}=\frac{\partial A}{\partial q_{i}} \frac{\partial B}{\partial p_{i}}-\frac{\partial A}{\partial p_{i}}\frac{\partial B}{\partial q_{i}}$$
- Rate of change:
$$\frac{dF}{dt}=\frac{\partial F}{\partial t}+\{F,H\}_{PB}$$
- Analogy with quantum mechanics:
$$\{A,B\}_{PB}=\frac{1}{i\hbar}\langle [A,B] \rangle $$

### Lagrangians of classical systems
- Typical system, non-relativistic, in the absence of electromagnetic fields:
$$L=T-V$$

- A _relativistic particle_, in the absence of external influence:
$$S=-mc\int  \, ds=-mc^{2}\int  \, d\tau=-mc^{2}\int  \, \frac{dt}{\gamma}\;\; \implies \;\;L=-\frac{mc^{2}}{\gamma}  $$
- A relativistic particle in an _electromagnetic field_:
$$\displaylines{S=\int  -mc\, ds-qA_{\mu}\,dx^{\mu}=\int \left( -\frac{mc^{2}}{\gamma}+q\boldsymbol{A}\cdot \boldsymbol{v}-qV \right) \, dt  \\A^{\mu}=\left( \frac{V(\boldsymbol{x})}{c},\boldsymbol{A} \right)\\ L=-\frac{mc^{2}}{\gamma}+q\boldsymbol{v}\cdot \boldsymbol{A}-qV\\\boldsymbol{p}=\gamma m\boldsymbol{v}+q\boldsymbol{A}}$$
- The _electromagnetic Lagrangian_:
$$\displaylines{F_{\mu \nu}=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu} \\ S=-\frac{1}{4}\int  \, d^{4}x\,F_{\mu \nu}F^{\mu \nu}\;\;\implies\;\; L=-\frac{1}{4}\int  \, d^{3}x\,F_{\mu \nu}F^{\mu \nu}  }$$

### Lagrangian and Hamiltonian density
- The _Lagrangian density_ $\mathcal{L}$ or _Hamiltonian density_ $\mathcal{H}$:
$$H=\int  d^{3}x\,\mathcal{H}\hspace{1.5cm}L=\int  d^{3}x\,\mathcal{L}  $$
- The _conjugate momentum density_:
$$\pi=\frac{\delta L}{\delta \dot{\phi}}=\frac{\partial \mathcal{L}}{\partial \dot{\phi}}$$
- Hamiltonian density can be written as:
$$\mathcal{H}=\pi \dot{\phi}-\mathcal{L}$$
- The principle of Least Action:
$$\frac{\partial \mathcal{L}}{\partial \phi}-\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi)} \right)=0$$
- Example: electromagnetic system with _4-current density_ $J^{\mu}=(c\rho,\boldsymbol{J})$
$$\mathcal{L}=-\frac{1}{4}F_{\mu \nu}F^{\mu \nu}-J^{\mu}A_{\mu}$$
- The Euler-Lagrange equation gives:
$$\partial_{\lambda}F^{\lambda \mu}=J^{\mu}$$
- This gives two of _Maxwell's equations_
	- Others come from Bianchi identity for the electromagnetic tensor $F^{\mu \nu}$
- 4-current is _conserved_:
$$\partial_{\mu}J^{\mu}=0$$
### Modes of oscillation
- The Euler-Lagrange equation gives _all allowed wave-vectors_ $k^{\mu}$
- The _most general_ field can be written as:
$$\phi(x^{\mu})=\sum_{k}a_{k}\exp(ik_{\mu}x^{\mu})$$
- These normal modes are simply _harmonic oscillators_, which can contain _quanta_
- _Particles_ are _excitations_ in the field, producing _quanta_ in certain modes

## The Klein-Gordon equation
- Attempt to make _quantum mechanics_ become _relativistic_
- Inspect the _Schrodinger equation_:
$$i\hbar \frac{\partial \psi}{\partial t}=-\frac{\hbar^{2}}{2m}\nabla^{2}\psi+V\psi$$
- Re-write in terms of new operators $E$ and $p$
$$E\psi=\frac{p^{2}}{2m}\psi+V\psi$$
- Then using the relativistic relation:
$$E^{2}=p^{2}c^{2}+m^{2}c^{4}$$
- One gets the _Klein-Gordon equation_ for some _scalar field_ $\phi$:
	- Take natural units $c=\hbar=1$
$$\frac{\partial^{2}\phi}{\partial t^{2}}- \nabla^{2}\phi+m^{2}\phi=0$$
- 4-vector notation:
$$(\partial_{\mu}\partial^{\mu}+m^{2})\phi=0$$
### Probability currents in the Klein-Gordon field
- Find some _probability current_ $j^{\mu}$ such that it is _conserved_:
$$\partial_{\mu}j^{\mu}=0$$
- In non-relativistic QM:
$$j^{\mu}=i[\phi^{*}\partial^{\mu}\phi-(\partial^{\mu}\phi^{*})\phi]$$
- Substituting a _plane wave_ function $\phi=N\exp(-i\boldsymbol{p}\cdot \boldsymbol{x})$
$$j^{0}=\rho=2|N|^{2}E$$
- Depending on the system, $E$ can be _negative_, hence $\rho$ _cannot be a probability density_

- The usual quantum mechanical notion of probability density _cannot be described_ by the Klein-Gordon equation

### Feynman-Stuckelberg interpretation
- _Negative energy_ states can be interpreted as _postive energy anti-particles_ moving _backwards in time_

- The _phase_ of the wave-function is $Et-\boldsymbol{p}\cdot \boldsymbol{x}$
- To convert $E\to -E$, _time_ must be _reversed_ $t\to -t$, hence $\boldsymbol{p}\to -\boldsymbol{p}$

- For _negative energy_, the _electric current_:
$$J^{\mu}_{\text{em}}=qj^{\mu}=2(+q)N^{2}(-|E|,\boldsymbol{p})=2(-q)N^{2}(|E|,-\boldsymbol{p})$$
- It appears the anti-particle has _opposite charge_ of the negative energy particle

- In _scattering_, the _absorption_ of a _negative energy particle_ corresponds to the _emission_ of a _positive energy anti-particle_

- Therefore, the _general solution_ to the Klein-Gordon equation, with a _positive energy_, consist of _incoming particles_ and _outgoing anti-particles_, both with $E>0$
$$\phi=A\exp[-i(Et-\boldsymbol{p}\cdot \boldsymbol{x})]+B\exp[i(Et-\boldsymbol{p}\cdot \boldsymbol{x})]$$

## Lagrangians from scratch
- Write down _simple Lagrangian (densities)_, then input into the _Euler-Lagrange equation_
$$\frac{\partial \mathcal{L}}{\partial \phi}-\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi)} \right)=0$$
- Consider the _symmetry_ of the system

### Quadratic scalar field
- The Lagrangian must depend on both the field itself $\phi$, as well as its _derivatives_ $\partial_{\mu}\phi$
- It must also be _Lorentz invariant_

- Limiting to _quadratic terms_:
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}$$
- From the Euler-Lagrange equation, one regains the _Klein-Gordon equation_:
$$(\partial^{2}+m^{2})\phi=0$$
- $m$ can be interpreted as _mass_

- The _solution_ is $\phi=\exp[-i(E_{\boldsymbol{p}}t-\boldsymbol{p}\cdot \boldsymbol{x})]$, with all _modes_ obeying the _dispersion relation_
$$E_{\boldsymbol{p}}^{2}=\boldsymbol{p}^{2}+m^{2}$$

- When _massless_, the solution is the _wave equation_ and the dispersion is _linear_

- A _linear_ equation of motion gives _no interactions with other identical particles_ (self-coupling)

### With a source current
- Let there be some _external potential_, described by a _source current_ $J(x^{\mu})$
- The Lagrangian is then:
$$\mathcal{L}=\frac{1}{2}(\partial^{\mu}\phi)(\partial_{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}+J\phi$$
- The equation of motion:
$$(\partial^{2}+m^{2})\phi=J$$
- An _inhomogeneous PDE_

### Self-coupling
- Let there be self-coupling, with the interaction strength given by parameter $\lambda$
$$\mathcal{L}=\frac{1}{2}(\partial^{\mu}\phi)(\partial_{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}+\frac{1}{4!}\lambda \phi^{4}$$
- Equation of motion:
$$(\partial^{2}+m^{2})\phi=-\frac{\lambda}{3!}\phi^{3}$$
### Two scalar fields
- Let there be _two fields_ $\phi_{1}$ and $\phi_{2}$, with the _same mass_ and interacting with strength $g$
$$\mathcal{L}=\frac{1}{2}(\partial^{\mu}\phi_{1})(\partial_{\mu}\phi_{1})+\frac{1}{2}(\partial^{\mu}\phi_{2})(\partial_{\mu}\phi_{2})-\frac{1}{2}m^{2}(\phi_{1}^{2}+\phi_{2}^{2})-g(\phi_{1}^{2}+\phi_{2}^{2})^{2}$$
- This gives both _self-coupling_, as well as _cross terms_ making the two fields interact

- If there is some _transformation_:
$$\pmatrix{\phi_{1}'\\ \phi_{2}'}=\pmatrix{\cos\theta&-\sin\theta\\ \sin\theta &\cos\theta}\pmatrix{\phi_{1}\\ \phi_{2}}$$
- The Lagrangian remains the _same_

- There is an _internal degree of freedom_ from this transformation
- The Lagrangian has an $SO(2)$ symmetry

### Complex scalar field
- Consider the Lagrangian above, but defining:
$$\psi=\frac{1}{\sqrt{ 2 }}(\phi_{1}+i\phi_{2})\hspace{1.5cm}\psi ^{\dagger}=\frac{1}{\sqrt{ 2 }}(\phi_{1}-i\phi_{2})$$
- The Lagrangian for a _complex scalar field theory_:
$$\mathcal{L}=(\partial^{\mu}\psi ^{\dagger})(\partial_{\mu}\psi)-m^{2}\psi ^{\dagger}\psi-g(\psi ^{\dagger}\psi)^{2}$$
- There are still _two independent fields_

- It is still _invariant to rotations_:
$$\psi\to \psi \exp(i\alpha)\hspace{1.5cm}\psi ^{\dagger}\to \psi ^{\dagger}\exp(-i\alpha)$$
- It is a $U(1)$ symmetry, which is _isomorphic_ to $SO(2)$
