- The _merging_ of _quantum mechanics_ and _special relativity_
- One describes spacetime using _quantum fields_

- The principles of _locality_, _symmetries_, and _renormalisation_ can _constrain possible quantum field theories_ 

>[!Conventions]
>Natural units, where $[\text{L}]=[\text{T}]=[\text{M}]^{-1}$
>$$c=\hbar =1$$
>Minkowski metric:
>$$\eta_{\mu \nu}=\eta^{\mu \nu}=\mathrm{diag}(1,-1,-1,-1)$$

# Classical Field Theory recap
- See also: [[Classical Field Theory]]

## Actions, Lagrangians, and Fields
- Based on _extremisation_ of the _action_, a time integral of the _Lagrangian_:
$$S=\int dt \, L $$
- In _classical dynamics_:
$$L=T-V=\frac{1}{2}\sum m_{i} \left|\frac{d\boldsymbol{x}_{i}}{dt}\right|^{2} -\sum V(\boldsymbol{x}_{i})$$
- Then, one _imposes external boundary conditions_

- A _field_ $\phi_{a}(x^{\mu})$ is defined _locally_ (at spacetime coordinate $x^{\mu}$) as a _mapping_:
	- There are _infinite degrees of freedom_ due to the number of spacetime points
$$\phi_{a}(x^{\mu})=\phi_{a}(t,\boldsymbol{x}): \mathbb{R}^{3+1}\to \mathbb{R} \text{ or }\mathbb{C} \text{ or }\mathbb{R}^{n}$$

- Example: [[Classical Field Theory#Electromagnetic fields|electromagnetic fields]]
	- The _equations of motion_ (derived later) are the _Maxwell equations_
$$A^{\mu}=(\phi(x^{\mu}), \boldsymbol{A}(x^{\mu}))$$
- The _time integral_ is _not Lorentz invariant_ (space and time are the same)
- Instead, define the _Lagrangian density_:
$$L=\int \,d^{3}\boldsymbol{x}\,\mathcal{L} \qquad S=\int  \, d^{4}x\,\mathcal{L}  $$
- The Lagrangian density is a _function_ of _fields_, and its _derivatives_:
$$\mathcal{L}=\mathcal{L}(\phi_{a},\partial_{\mu}\phi_{a}\dots)$$
- The _equation of motion_ for the fields come from _extremising_ $S$ w.r.t. each field
- Assuming $\mathcal{L}$ _does not depend on_ any _higher order derivatives_, using integration by parts, one gets the [[Classical Field Theory#The relativistic Lagrangian density|Euler-Lagrange equation]]:
$$\frac{\partial \mathcal{L}}{\partial \phi_{i}}=\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi_{i})} \right)$$
- Example: the [[Classical Field Theory#Klein-Gordon field|Klein-Gordon field]], or the _free massive scalar field_:
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}$$
- One gets the _Klein-Gordon equation_:
$$(\partial_{\mu}\partial^{\mu}+m^{2})\phi=\left( \frac{\partial^{2}}{\partial t^{2}}-\nabla^{2}+m^{2} \right)\phi=(\Box+m^{2})\phi=0$$

## Hamiltonian
- The _canonical momentum density_ is defined as:
$$\pi_{a}=\frac{\partial \mathcal{L}}{\partial \dot{\phi}_{a}}$$
- The _Hamiltonian density_:
$$\mathcal{H}={\pi_{a}}\dot{\phi}_{a}-\mathcal{L}$$
- The Hamiltonian:
$$H=\int  \, d^{4}x\,\mathcal{H} $$
- Example:
$$\mathcal{L}=\frac{1}{2}(\partial^{\mu}\phi)(\partial_{\mu}\phi )-V(\phi) \implies \mathcal{H}=\frac{1}{2}\dot{\phi}^{2}+\frac{1}{2}|\nabla \phi|^{2}+V(\phi)$$

## Lorentz invariance
- Symmetries dictate the _possible actions_ $S$, the _class of fields/operators_ used, and the observables 
	- Examples: $U(1)$, Poincare group (spacetime translations and rotations), Lorentz group

- A _Lorentz transformation_:
$$x^{\mu} \implies x'^{\mu}={\Lambda^\mu}_{\nu}x^{\nu}$$
- It must preserve _intervals_:
$$x_{\mu}x^{\mu}=x'_{\mu}x'^{\mu} \implies\eta_{\mu \nu}{\Lambda^{\mu}}_{\rho}{\Lambda^{\nu}}_{\sigma}=\eta_{\rho\sigma}$$
- Example: _Lorentz boosts_
$$\Lambda=\pmatrix{\cosh\alpha &\sinh\alpha&0&0\\ \sinh\alpha&\cosh\alpha&0&0\\0&0&1&0\\0&0&0&1}$$
- In general:
$$\mathrm{\det}(\Lambda)^{2}=1$$
- For $\det(\Lambda)=1$, the boost is _proper_
	- It is _continuously connected to the identity_, with $\varepsilon$ known as the _generator_
$${\Lambda^{\mu}}_{\nu}={\delta^{\mu}}_{\nu}+{\varepsilon^{\mu}}_{\nu}+O(\varepsilon^{2})$$
- For $\det(\Lambda)=-1$, it is _improper_

- The condition of _preserving intervals_ above, with the expansion, implies the generator is _antisymmetric_:
$$\varepsilon_{\mu \nu}=-\varepsilon_{\nu \mu}$$
- In 4 spacetime dimensions, there are _6 independent generators_, corresponding to _3 boosts and rotations each_

## Fields with Lorentz transformations
- A field: dependent on _coordinates_, and has a _definite transformation_
- Coordinate and field _active transformations_:
	- _Coordinate system_ unchanged, but change _where field is evaluated_
	- Hence, coordinates rotate the _other way_ (to the coordinate _before rotation_)
$$x\to x'=\Lambda x$$
$$\phi_{a}(x)\to \phi_{a}'(x)=D[\Lambda]^{b}_{a}\phi_{b}(\Lambda^{-1} x)$$
- Here, $D$ is a _representation_ of the Lorentz group, satisfying:
$$\begin{align}
D[\Lambda_{1}]D[\Lambda_{2}]&=D[\Lambda_{1}\Lambda_{2}] \\ D[\Lambda^{-1}]&=D[\Lambda]^{-1} \\ D[\mathbb{I}]&=1
\end{align}$$
- Example: the _trivial representation_ $D[\Lambda]=1$
$$\phi(x)\to\phi(\Lambda^{-1} x)$$
- This represents a _scalar field_ $\phi$

- Alternatively, use the representation:
$$D[{\Lambda^{\mu}}_{\nu}]={\Lambda^{\mu}}_{\nu}$$
- This gives _vector fields_
- Example: the _Maxwell field_ $A^{\mu}=(\phi, \boldsymbol{A})$
$$A^{\mu}(x)\to A'^{\mu}={\Lambda^{\mu}}_{\nu}A^{\nu}(\Lambda^{-1}x)$$
- Or, the _derivative_ of a scalar field:
$$\partial_{\mu}\phi \to \partial_{\mu}\phi'=({\Lambda^{\mu}}_{\nu})^{-1}\partial_{\nu}\phi(\Lambda^{-1}x)$$

- Example: the _Klein Gordon Lagrangian_ is invariant
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2} \quad, \quad \mathcal{L}'(x)=\mathcal{L}(\Lambda^{-1}x)$$
- From $\det(\Lambda)=1$, the spacetime element $d^{4}x$ is constant, hence _action is invariant_

## Noether's theorem
- _Symmetries_ of a system lead to _conserved quantities_

- Every _continuous symmetry_ of the _Lagrangian_ $\mathcal{L}$ gives rise to a _current_ $J^{\mu}$, where the _Euler-Lagrange equations_ imply _conservation_:
$$\partial_{\mu}J^{\mu}=\frac{\partial J^{0}}{\partial t}+\nabla\cdot \boldsymbol{J}=0$$

- Given suitable _boundary conditions_, there will be a _conserved charge_ $Q$:
$$Q=\int  d^{3}x\, J^{0} $$

### Transformation and symmetry
- A transformation is _continuous_ if there can be an _infinitesimal parameter_ describing it
- There can be _internal transformations_, which act on _fields, not coordinates_
- _Local transformations_ act on _coordinates and fields_
	- Example: Lorentz transformations act on both

- In both cases, define the _infinitesimal change of field_:
	- _Fixed position_
$$\delta \phi\equiv \phi'(x)-\phi(x)$$
- For a _symmetry_ of the system, the _action_ must be _invariant_:
$$\delta S=S[\phi']-S[\phi]=0$$
- This implies the Lagrangian changes by a _total derivative_:
$$\delta \mathcal{L}=\mathcal{L}'(x)-\mathcal{L}(x)=\partial_{\mu}F^{\mu}$$
### Conserved current
- Change in Lagrangian:
$$\delta \mathcal{L}=\frac{\partial \mathcal{L}}{\partial \phi_{a}}\delta \phi_{a}+\frac{\partial \mathcal{L}}{\partial(\partial_\mu \phi_{a})}\delta(\partial_{\mu}\phi _{a})$$
- Using the Euler-Lagrange equation, one can re-write the _condition for symmetry_ as:
$$\delta \mathcal{L}=\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi_{a})}\delta \phi_{a} \right)=\partial_{\mu}F^{\mu}$$
- From this:
$$J^{\mu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi_{a})}\delta \phi_{a}-F^{\mu}$$

### Conserved charge
$$Q= \int  d^3 x\, J^{0}   $$
- From conservation of the current, with _boundary conditions_ of vanishing on the surface:
$$\frac{dQ}{dt}=\int  d^3 x\, \frac{\partial J^{0}}{\partial t}=-\int  d^3 x \,\nabla\cdot \boldsymbol{J}=-\int  d\boldsymbol{S}\cdot \boldsymbol{J}=0 $$

### Local symmetry: energy-momentum tensor
- Local transformation: _translations_ by a _constant vector_
$$x^{\mu}\to x'^{\mu}=x^{\mu}-\varepsilon^{\mu}$$
- Transformation of the _fields_:
	- _Inverse_ transformation of coordinate argument
$$\delta\phi_{a}(x)=\varepsilon^{\mu}\partial_{\mu}\phi_{a}$$
- Lagrangian shifts by a _total derivative_:
$$\delta \mathcal{L}=\varepsilon^{\mu}\partial_{\mu}\mathcal{L}=\partial_{\mu}(\varepsilon^{\mu}\mathcal{L})$$
- The _conserved current_ is then:
$$J^{\mu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi_{a})} \varepsilon^{\nu}\partial_{\nu}\phi_{a}-\varepsilon^{\mu}\mathcal{L}=\varepsilon^{\nu}{T^{\mu}}_{\nu}$$
- From this, extract the _energy-momentum tensor_:
	- One can _raise and lower indices_
$${T^{\mu}}_{\nu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\phi_{a})}\partial_{\nu}\phi_{a}-{\delta^{\mu}}_{\nu}\mathcal{L}$$
- The _conservation_ $\partial_{\mu}J^{\nu}=0$ then gives:
$$\partial_{\mu}{T^{\mu}}_{\nu}=0$$
- The _energy_ and _momenta_:
	- Set any component of $\varepsilon^{\mu}$ to be non-zero
	- Arbitrary scale factor
$$E=\int  d^3 x\,T^{00} \qquad P^{i}=\int  d^3 x\, T^{0i}$$
- For the _free massive scalar field_:
$$T^{00}=\frac{1}{2}\dot{\phi}^{2}+\frac{1}{2}|\nabla \phi|^{2}+\frac{1}{2}m^{2}\phi^{2}$$
$$T^{0i}=\int  d^3 x\,\dot{\phi} \,\partial^{i}\phi$$
- $T^{\mu \nu}$ is _not necessarily symmetric_
- However, one can add an _arbitrary_ tensor to assure symmetry:
$$\Theta^{\mu \nu}=T^{\mu \nu}+\partial_{\rho} \mathcal{T}^{\rho \mu \nu} \qquad \mathcal{T}^{\rho \mu \nu}=-\mathcal{T}^{\mu \rho \nu}$$

- In _general relativity_:
$$\Theta^{\mu \nu}=\left( \frac{2}{\sqrt{ -g }} \frac{\partial}{\partial g_{\mu \nu}}(\sqrt{ -g }\mathcal{L}) \right) \Bigg|_{g=\eta}$$
### Internal symmetry: complex scalar field
- Let there be a _complex scalar field_, a linear combination of _two real scalar fields_ $\phi_{i}$
$$\psi(x)=\frac{1}{\sqrt{ 2 }}[\phi_{1}(x)+i\phi_{2}(x)]$$
- Possible Lagrangian:
$$\mathcal{L}=(\partial_{\mu}\psi)(\partial^{\mu}\psi^{*})-V(|\psi|^{2})$$
- Equations of motion:
$$\partial_{\mu}\partial^{\mu}\psi+ \frac{\partial V}{\partial \psi^{*}}=0 \qquad \partial_{\mu}\partial^{\mu}\psi^{*}+\frac{\partial V}{\partial \psi}=0$$
- The _internal symmetry_ of the Lagrangian, _only acting on the fields_:
	- $\alpha$ is a _real constant_
$$\psi(x)\to \psi'(x)=\exp(i\alpha)\psi(x) \qquad \psi^{*}(x)\to {\psi^{*}}'(x)=\exp(-i\alpha )\psi^{*}(x)$$
- Infinitesimal transformations:
$$\delta \psi=i\alpha \psi \qquad \delta \psi^{*}=-i\alpha \psi^{*}$$
- Since $F^{\mu}=0$, the _Noether current_:
$$J^{\mu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\psi)}\delta \psi +\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\psi^{*})}\delta \psi^{*}$$
- Removing the _scale factor_ of $\alpha$:
$$J^{\mu}=i(\psi \partial^{\mu}\psi ^{*}-\psi^{*}\partial^{\mu}\psi)$$
- The corresponding conserved charge is the _electric charge_

- One can also write it in terms of only the scalar fields:
$$\pmatrix{\phi_{1} \\ \phi_{2}} \to \pmatrix{\phi_{1}' \\ \phi_{2}'}=\pmatrix{\cos\alpha & -\sin\alpha \\ \sin\alpha& \cos\alpha} \pmatrix{\phi_{1}\\ \phi_{2}}$$

# Free theory of quantum fields
- Take a _Hamiltonian approach_ to classical field theory, then follow the rules of _quantum mechanics_

- Postulate of quantum mechanics:
$$[x^{i},p^{j}]=i\hbar\delta^{ij}$$
- Then to _quantise_ a _field_ $\phi_{a}(x)$ and the _canonical momentum_ $\pi^{a}(x)$:
$$[\phi_{a}(t,\boldsymbol{x}), \pi^{b}(\boldsymbol{y},t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{y})\delta^{b}_{a}$$

- Here, use the [[Principles of quantum mechanics#The Schrödinger and Heisenberg pictures|Heisenberg picture]]:
$$\frac{dA^{(H)}}{dt}=\frac{1}{i\hbar}[A^{(H)},\Ham^{(H)}]+\pd{A^{(H)}}{t}$$
## Canonical quantisation
- The Klein-Gordon Lagrangian:
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}$$
$$(\partial_{\mu}\partial^{\mu}+m^{2})\phi=0$$

### General form of the Klein-Gordon field
- This gives _plane wave_ solutions, with a _dispersion relation_ for the 4-wavevector given by the Klein-Gordon equation:
$$\phi\sim \exp(ik_{\mu}x^{\mu})=\exp(i\omega t-i\boldsymbol{k}\cdot \boldsymbol{x})$$
- Take the _positive_ solution to the Klein-Gordon equation:
$$|\boldsymbol{k}|^{2}=\omega^{2}-m^{2} \implies \omega\equiv \sqrt{ k^{2}+m^{2} }$$
- Taking a _super-position_ of a plane wave solutions along with the negative frequencies, the _most general solution_ for $\phi$:
$$\phi(\boldsymbol{x},t)=\int  \frac{d^3 k}{(2\pi)^{3}}[a(\boldsymbol{k})e^{i(\boldsymbol{k}\cdot \boldsymbol{x}-\omega t)}+b(\boldsymbol{k})e^{i(\boldsymbol{k}\cdot \boldsymbol{x}+\omega t)}]$$
- $\phi$ is constrained to be _real_, so the most general $a$ and $b$ are:
$$a^{*}(-\boldsymbol{k})=b(\boldsymbol{k}) \qquad b^{*}(-\boldsymbol{k})=a(\boldsymbol{k})$$
- Then, along with a [[#Relativistic normalisation|normalisation factor]]:
$$\phi(x^{\mu})=\int  \frac{d^{3}k}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\omega(\boldsymbol{k}) }}\big[a(\boldsymbol{k})\exp(-ik_{\mu}x^{\mu})+a^{*}(\boldsymbol{k})\exp(ik_{\mu}x^{\mu})\big] $$
- One can also find the _canonical momentum_:
$$\pi(x^{\mu})=\dot{\phi}=\int  \frac{d^3k}{(2\pi)^{3}} \frac{1}{i}\sqrt{ \frac{\omega}{2} } \big[ a(\boldsymbol{k})e(-ik_{\mu}x^{\mu})-a^{*}(\boldsymbol{k})\exp(ik_{\mu}x^{\mu}) \big]$$

### Quantisation
- Then, one can _declare_:
$$\begin{align}
[\phi(\boldsymbol{x},t),\phi(\boldsymbol{x}',t)]&=0 \\ [\pi(\boldsymbol{x},t), \pi(\boldsymbol{x}',t)]&=0 \\ [\phi(\boldsymbol{x},t),\pi (\boldsymbol{x}',t)]&=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}')
\end{align}$$

- This implies that $a$ can be treated as an _operator_, with $a^{*}$ being $a^{\dagger}$:
$$\begin{align}
[a(\boldsymbol{k}),a(\boldsymbol{k}')]&=0 \\ [a^{\dagger}(\boldsymbol{k}),a^{\dagger}(\boldsymbol{k}')]&=0 \\ [a(\boldsymbol{k}),a^{\dagger}(\boldsymbol{k}')]&=(2\pi)^{3}\delta^{3}(\boldsymbol{k}-\boldsymbol{k}')
\end{align}$$

- _Either_ set of commutation relations will _imply_ the other
## Hamiltonians
- The Hamiltonian:
$$H=\int  d^3 x\,\mathcal{H}=\frac{1}{2}\int  d^3 x\,[\pi^{2}+|\nabla \phi|^{2}+m^{2}\phi^{2}]$$
- Preserving the _order_ of operators:
$$H=\frac{1}{2}\int  \frac{d^3p}{(2\pi)^{3}} \omega(a_{p}a^{\dagger}_{p}+a^{\dagger}_{p}a_{p}) $$
- Another form:
$$H=\int  \frac{d^3p}{(2\pi)^{3}}\omega \,a_{p}^{\dagger}a_{p}+\int  \frac{d^3p}{(2\pi)^{3} } \frac{\omega}{2} (2\pi)^{3}\delta^{3}(0) $$
- Applying it to a _vacuum state_, the second term is _infinite_

- The $\delta^{3}(0)$ gives the _infrared divergence_
- Transforming $\delta^{3}$ into an _integral over space_, it appears as an _infinite volume_ with a _constant energy density_

- Integrating $\omega=\sqrt{ p^{2} + m^{2} }$ with $0<p<\infty$ gives the _ultraviolet divergence_
- The integral should be _cut off_ at _short distances/high momentum_

- To focus on _energy differences_, introduce _normal ordering_ of operators, which puts _all creation operators on the left_
$$:H:=\int  \frac{d^3 p}{(2\pi)^{3}} \omega\,a_{p}^{\dagger}a_{p}$$
## Fock space

### One-particle states
- Given the _vacuum state_ $\ket{0}$, construct _excited states_
- The creation and annihilation operators _raise_ and _lower_ energy respectively
$$[H,a_{p}^{\dagger}]=\omega_{p}a_{p}^{\dagger} \qquad[H,a_{p}]=-\omega_{p}a_{p}$$
- Let the _single particle state_ $\ket{p}$ be:
$$\ket{p}=a^{\dagger}_{p}\ket{0}  $$
- An eigenstate of the _Hamiltonian_:
$$H\ket{p}=\omega_{p}\ket{p}  \qquad \omega_{p}^{2}=p^{2}+m^{2}$$
- Consider the _momenta_ from the [[#Local symmetry energy-momentum tensor|energy-momentum tensor]]:
$$\boldsymbol{P}=: \int  d^{3}x\,\pi \,\nabla \phi: = \int  \frac{d^3 k}{(2\pi)^{3}}\,\boldsymbol{k}\,a_{k}^{\dagger}a_{k}\implies  \boldsymbol{P}\ket{p}=\boldsymbol{p}\ket{p}  $$
- One can also consider _angular momentum_:
$$J^{i}\ket{p}=0 $$
- This is a particle of _spin_ $0$

### n-particle states and the Fock space
- Then, construct an $n-$particle state
	- The creation operators _commute_
$$\ket{p_{1}\dots p_{n}}=a^{\dagger}(p_{1})\dots a^{\dagger}(p_{n})\ket{0}  $$
- The _Fock space_ of the particle is formed by all combinations of $a^{\dagger}$ acting on $\ket{0}$

- The _number operator_:
$$\displaylines{N=\int  \frac{d^3p}{(2\pi)^{3}} a_{p}^{\dagger}a_{p}\qquad [N,H]=0  \\ N\ket{p_{1}.,,p_{n}}=n\ket{p_{1}\dots p_{n}}  }$$
- The Fock space is:
$$\oplus \sum_{n} \mathcal{H}_{n}$$

### Relativistic normalisation
- Normalised vacuum state:
$$\braket{ 0 | 0 }=1$$
- For $\ket{p}=a_{p}^{\dagger}\ket{0}$, from the commutation relation, one might get:
$$\braket{ p | q }\neq(2\pi)^{3} \delta^{3}(p-q)$$
- This relation should be _Lorentz invariant_

- If one applies a _unitary transformation_ $U(\Lambda) \ket{p}$, the _normalisation should not change_

- Normal construction of the identity (Lorentz invariant) must be _constructed by Lorentz invariant quantities_
	- Neither the measure or the kets are Lorentz invariant
$$\mathbb{I}\neq\int  \frac{d^3p}{(2\pi)^{3}}\ket{p} \bra{p}  $$

- Instead, consider the Lorentz invariant integral:
	- Consider Lorentz transformations _continuously connected to the identity_, hence the step function $\Theta$
$$\int  d^{4}p\,\delta^{4}(p_{0}^{2}-\boldsymbol{p}^{2}-m^{2})\Theta(p^{0}) =\int  \frac{d^3p}{2\sqrt{ p^{2}+m^{2} }}=\int  \frac{d^3p}{2\omega_{p}}  $$
- From this:
$$\mathbb{I}=\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{2\omega_{p}} \ket{p}\bra{p}   $$
- The _normalised one particle state_ is then:
$$\ket{p}=\sqrt{ 2\omega_{p} } a^{\dagger}_{p}\ket{0}  $$
- Normalisation:
$$\braket{ p | q }=(2\pi)^{3}2\omega_{p}\delta^{3} (p-q)$$
## Causality
- From the principle of _causality_, _measurements_ which have _spacelike_ separation _should not influence each other_

- In other words, if $x$ and $y$ are _spacelike separated_:
$$\Delta(x-y)=[\phi(x),\phi(y)]=0\quad \forall (x-y)^{2}<0$$
- It _does not vanish_ for timelike separations $(x-y)^{2}>0$
	- Prove for one timelike vector, then _Lorentz invariance_ means it is true for all timelike vectors
- Measurements with _timelike interval_ (within the _light cone_) _can influence each other_

- It _vanishes_ for _spacelike_ separations $(x-y)^{2}<0$
	- Prove for one spacelike vector, then use Lorentz invariance

## Propagators
- Consider the quantity:
$$\braket{ 0|\phi(x)\phi(y) | 0 } =\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{2\omega_{p}} \exp[-ip\cdot(x-y)]\equiv D(x-y) $$
- For _spacelike_ events:
$$\displaylines{D(x-y)\sim \exp[-m(x-y)]\neq 0 \\ [\phi(x),\phi(y)]=D(x-y)-D(y-x)=0}$$
### The Feynman propagator
$$\Delta _{F}(x-y)=\braket{ 0|T\phi(x)\phi(y) |0  } \equiv \begin{cases} 
D(x-y)& x^{0}> y^{0} \\
D(y-x) &y^{0}>x^{0}
\end{cases}$$
- $T$ is the _time ordering operator_, making sure the _amplitude_ is in the correct order (past to future)

- Time ordering can be implemented with a _step function_:
$$\braket{ 0|T\phi(x)\phi(y) | 0 }=\braket{ 0|\phi(x)\phi(y) |0  }\Theta(x^{0}-y^{0})+ \braket{ 0|\phi(y)\phi(x) |0  }\Theta(y^{0}-x^{0})  $$
- Making the _expansion_, one can prove that it is equal to the expression below, with $\epsilon\to 0$
$$\Delta_{F}(x-y)=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} \exp[-ip(x-y)]$$

- It is also the _Greens function_ for the Klein-Gorfon equation:
$$(\partial_{\mu}\partial^{\mu}+m^{2})\Delta_{F}(x-y)=-i\delta^{4}(x-y)$$

### Wick's Theorem
- Time ordering is equivalent to:
$$T\phi(x)\phi(y)=:\phi(x)\phi(y):+\Delta_{F}(x-y)$$
- Proof: split the field into $\phi^{+}$ and $\phi^{-}$ and _expand_ $T[\phi(x)\phi(y)]$
$$\displaylines{\phi=\phi^{+}+\phi ^{-} \\ \phi^{+}=\int  \frac{d^3p}{(2\pi)^{3}}\,\frac{1}{\sqrt{ 2\omega_{p} }} a_{p} \exp(-ipx) \qquad \phi^{-}=\int  \frac{d^3p}{(2\pi)^{3}}\,\frac{1}{\sqrt{ 2\omega_{p} }} a_{p}^{\dagger} \exp(ipx)\\ [\phi^{+}(x),\phi^{-}(y)]=D(x-y) \\T[\phi(x)\phi(y)]=\,:\phi(x)\phi(y):+D(x-y)}$$

- _Wick's Theorem_ for $N$ fields:
$$T[\phi(x_{1})\dots \phi(x_{N})]=:\phi(x_{1})\dots \phi(x_{N}):+\text{ all possible contractions}$$
- The _contractions_ are all possible combination of _propagators_:
$$\overbrace {\phi_{i}\phi_{j}}=\Delta_{F}(x_{i}-x_{j})$$
- Example:
$$\begin{align}
T(\phi(x_{1})\phi(x_{2})\phi(x_{3})\phi(x_{4}))&=\,:\phi(x_{1})\phi(x_{2})\phi(x_{3})\phi(x_{4}):  \\
&+\overbrace{ \phi(x_{1})\phi(x_{2}) }:\phi(x_{3})\phi(x_{4}):+\overbrace{ \phi(x_{1})\phi(x_{3}) }:\phi(x_{2})\phi(x_{4}): \\
&+ \text{ 4 other combinations} \\
&+\overbrace{ \phi(x_{1})\phi(x_{2}) }\overbrace{ \phi(x_{3})\phi(x_{4}) }+\overbrace{ \phi(x_{1})\phi(x_{3}) }\overbrace{ \phi(x_{2})\phi(x_{4}) } \\
&+\overbrace{ \phi(x_{1})\phi(x_{4}) }\overbrace{ \phi(x_{2})\phi(x_{3}) }
\end{align}$$
# Interacting fields
- For _free theories_, one can _construct_ the _Fock space explicitly_

- Consider _more general Lagrangians_, where the _equation of motion might not be solved_
- Then, _one may not construct the Hilbert/Fock space_

- Instead, a _perturbative approach_:
$$\mathcal{L}=\mathcal{L}_{0}+\mathcal{L}_\text{int}$$
- Example:
$$\begin{align}
\mathcal{L}_{0}&=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2} \\ \mathcal{L}_\text{int}&=-\sum_{n=3} \frac{\lambda^{n}}{n!}\phi^{n}
\end{align}$$
## Couplings
- From the fact that $[S]=[\hbar]=1$, the units of the Lagrangian are $[\mathcal{L}]=[M]^{4}$
- From this:
$$[\lambda_{n}]=4-n$$
- For some _energy scale_ $E$ of the system, check the _dimensionless quantity_:
$$\frac{\lambda_{n}}{E^{4-n}}$$

- For $n=3$, the coupling is _relevant_ at _low energies_ $(\lambda_{n}\gg E)$

- For $n=4$, the coupling is _marginal_ if  $\lambda_{n}\ll 1$

- For $n\geq 5$, the coupling is _small at low energies_, hence it is _irrelevant_

- _Quantum_ corrections can _change_ the nature of the perturbation term

## LSZ reduction formula
- Let there be some _scattering process_
	- Number of particles can _change_ (e.g. decays)

- The _in_ and _out_ states are related by the $S-$matrix (scattering matrix)
	- They are _asymptotic_ states, far away/long time after the scattering

- In the _Schrodinger_ or _Heisenberg_ picture:
$$\braket{ \text{final},t_{f} | \text{initial} ,t_{i}}_{S}=\braket{ f|S |i  }_{H}  $$

- Let $\ket{\Omega}$ be the _vacuum state_
	- _Different_ from the vaccum of the _free theory_, $\ket{0}$
- A perturbative approach:
$$\displaylines{H=H_{0}+H_\text{int} \\ \mathcal{L}=\mathcal{L}_{0}+\mathcal{L}_\text{int}}$$

- Working in the _Heisenberg picture_, assume time evolution:
$$\displaylines{i\partial_{t}\phi=[\phi,H] \\ i\partial_{t}\mathcal{O}=[\mathcal{O},H]}$$

- Assume that at _some point_ $t=t_{0}$ before the scattering, one can _match_ the Hilbert space of $H_{0}$ to that of $H$:
$$a_{p}(t)=\exp[iH(t-t_{0})]a_{p}^{0}\exp[-iH(t-t_{0})]$$
- Then the field:
$$\phi _\text{int}(x)=\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\omega_{p} }} \big(a_{p}(t)e^{-ipx}+a_{p}^{\dagger}(t)e^{ipx}\big) $$

- Then write the states as:
	- 2 particles in, 2 particles out (can be generalised easily)
$$\begin{align}
\ket{\text{initial},t_{i}}&=\sqrt{ 2\omega_{1} }\sqrt{ 2\omega_{2} }a_{p_{1}}^{\dagger}(t_{i})a_{p_{2}}^{^{\dagger}}(t_{i})\ket{\Omega}  \\
\ket{\text{final},t_{f}}&=\sqrt{ 2\omega_{3} }\sqrt{ 2\omega_{4} }a_{p_{3}}^{\dagger}(t_{i})a_{p_{4}}^{^{\dagger}}(t_{i})\ket{\Omega}
\end{align}$$
- The _asymptotic states_, where there are _no interactions_ as $t_{i}\to -\infty$ and $t_{f}\to \infty$
$$\lim_{ t \to \pm\infty } a_{p}^{\dagger}(t)={a_{p}^{0}}^{\dagger}$$

- Then _relating_ the states, taking care to _time order_ the product:
$$\braket{ f|S | i } =\left[ \prod_{i}\sqrt{ 2\omega_{i} } \right]\braket{ \Omega |T[a_{p_{3}}(\infty) a_{p_{4}}(\infty)a_{p_{1}}^{\dagger}(-\infty)a_{p_{2}}^{\dagger}(-\infty)]|\Omega } $$
- Consider this integral at _asymptotic times_:
$$\begin{align}
i\int  d^4 x\,\exp(ipx)(\Box+m^{2})\phi(x)&=i \int  d^4 x\,e^{ipx}\,(\partial_{t}^{2}+\omega_{p}^{2})\phi(x) \\
&=\int  dt\,\partial_{t}[e^{i\omega_{p}t}\int  d^3x\,e^{-i\boldsymbol{p}\cdot \boldsymbol{x}}(i\partial_{t}+\omega_{p})\phi(x) ] 
\end{align}$$
- This is a _total derivative_, therefore it _only depends on the boundaries_
- Then _expanding_ $\phi$, and using that $a_{\boldsymbol{p}}(t)$ is _constant_ at $t\to \pm \infty$:
$$\begin{align}
i\int  d^4 x\,\exp(ipx)(\Box+m^{2})\phi(x)&=\sqrt{ 2\omega_{p} }[a_{p}(\infty)-a_{p}(-\infty)]\\
-i\int  d^4 x\,\exp(-ipx)(\Box+m^{2})\phi(x)&=\sqrt{ 2\omega_{p} }[a_{p}^{\dagger}(\infty)-a_{p}^{\dagger}(-\infty)]
\end{align}$$
- Due to _time ordering_, and $\ket{\Omega}$ being the _vacuum state_, one can re-write the formula as:
$$\begin{align}
\braket{ f|S | i } =\left[ \prod_{i}\sqrt{ 2\omega_{i} } \right] \langle \Omega |&T\{[a_{p_{3}}(\infty)-a_{p_{3}}(-\infty)][a_{p_{4}}(\infty)-a_{p_{4}}(-\infty)]\\ 
&\times[a^{\dagger}_{p_{1}}(-\infty)-a^{\dagger}_{p_{1}}(\infty)][a^{\dagger}_{p_{2}}(-\infty)-a^{\dagger}_{p_{2}}(\infty)]\} |\Omega\rangle
\end{align}$$

- Then using the identity, one gets the _LSZ reduction formula_:
$$\begin{align}
\braket{ f|S | i } =\left[\prod_{j} i\int  d^4x_{j} \right] &[\exp(-ip_{1}x_{1})(\Box_{1}+m_{1}^{2})]\dots[\exp(ip_{4}x_{4})(\Box_{4}+m_{4}^{2})] \\
&\times\braket{ \Omega|T\{\phi(x_{3})\phi(x_{4})\phi(x_{1})\phi(x_{2})\} | \Omega } 
\end{align} $$
- It is a _product_ of operators, as well as an _$n-$point correlation function_ for $n$ total particles
- $\exp(-ipx)(\Box+m^{2})$ is _pulled out_ of the inner product
	- This leads to _contact terms_ which are physically irrelevant

- One then gets a _Lorentz invariant_ $S-$matrix

## Schwinger-Dyson equation