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

- A _passive transformation_ on _coordinates_:
	- One would still have to transform the _fields_ (e.g. a scaling)
$$x\to x'=\Lambda x={\Lambda^{\mu}}_{\nu}x^{\nu}$$

- Coordinate and field _active transformations_:
	- _Coordinate system_ unchanged, but change _where field is evaluated_
	- Hence, coordinates rotate the _other way_ (to the coordinate _before rotation_, to retain the same value)

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
	- Aside from _evaluating_ it at the same point, it must also _rotate with the coordinates_
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
$$\pi(x^{\mu})=\dot{\phi}=\int  \frac{d^3k}{(2\pi)^{3}} \frac{1}{i}\sqrt{ \frac{\omega}{2} } \big[ a(\boldsymbol{k})\exp(-ik_{\mu}x^{\mu})-a^{*}(\boldsymbol{k})\exp(ik_{\mu}x^{\mu}) \big]$$

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

- It is also the _Greens function_ for the Klein-Gordon equation:
$$(\partial_{\mu}\partial^{\mu}+m^{2})\Delta_{F}(x-y)=-i\delta^{4}(x-y)$$

### Wick's Theorem
- Time ordering is equivalent to:
$$T[\phi(x)\phi(y)]=:\phi(x)\phi(y):+\Delta_{F}(x-y)$$
- Proof: split the field into $\phi^{+}$ and $\phi^{-}$ and _expand_ $T[\phi(x)\phi(y)]$
$$\displaylines{\phi=\phi^{+}+\phi ^{-} \\ \phi^{+}=\int  \frac{d^3p}{(2\pi)^{3}}\,\frac{1}{\sqrt{ 2\omega_{p} }} a_{p} \exp(-ipx) \qquad \phi^{-}=\int  \frac{d^3p}{(2\pi)^{3}}\,\frac{1}{\sqrt{ 2\omega_{p} }} a_{p}^{\dagger} \exp(ipx)\\ [\phi^{+}(x),\phi^{-}(y)]=D(x-y) \\T[\phi(x)\phi(y)]=\,:\phi(x)\phi(y):+D(x-y)}$$

- _Wick's Theorem_ for $N$ fields:
	- Proof by induction
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
- The $S-$matrix can be written as:
$$S=\mathcal{T}\left\{ \exp\left( -\frac{i}{\hbar}\int  d^4x \,\frac{\lambda}{4!} \phi^{4} \right) \right\}$$

- Let $\ket{\Omega}$ be the _vacuum state_
	- _Different_ from the vaccum of the _free theory_, $\ket{0}$
- A perturbative approach:
$$\displaylines{H=H_{0}+H_\text{int} \\ \mathcal{L}=\mathcal{L}_{0}+\mathcal{L}_\text{int}}$$

- Working in the _Heisenberg picture_, assume time evolution:
$$\displaylines{i\partial_{t}\phi=[\phi,H] \\ i\partial_{t}\mathcal{O}=[\mathcal{O},H]}$$

- Assume that at _some point_ $t=t_{0}$, one can _match_ the Hilbert space of $H_{0}$ to that of $H$:
	- The _mapping_ between the two spaces is _time-dependent_
$$a_{p}(t)=\exp[iH(t-t_{0})]a_{p}^{0}\exp[-iH(t-t_{0})]$$
- Then the field can be written in the _same way_ as the free field
	- Here, the ladder operators are _time dependent_ (unknown explicit form)
	- The _dispersion relation_ $\omega_{p}^{2}=m^{2}+p^{2}$ still applies
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
	- First equality: integrate the _spatial derivative_ by parts to get $p^{2}$
$$\begin{align}
i\int  d^4 x\,\exp(ipx)(\Box+m^{2})\phi(x)&=i \int  d^4 x\,e^{ipx}\,(\partial_{t}^{2}+\omega_{p}^{2})\phi(x) \\
&=\int  dt\,\partial_{t}[e^{i\omega_{p}t}\int  d^3x\,e^{-i\boldsymbol{p}\cdot \boldsymbol{x}}(i\partial_{t}+\omega_{p})\phi(x) ] 
\end{align}$$
- This is a _total derivative_, therefore it _only depends on the boundaries_
- Use results from the _free theory_ at _asymptotic times_, the identities:
$$\displaylines{f\overleftrightarrow{\partial_{t}}g\equiv f(\partial_{t}g)-(\partial_{t}f)g \\ \begin{align}
\sqrt{ 2\omega_{p} }a_{p}^{0}&=i \int  d^3x\,\exp(ipx) \overleftrightarrow{\partial_{t}}\phi \\ \sqrt{ 2\omega_{p} }{a_{p}^{0}}^{\dagger}&=-i \int  d^3x\,\exp(-ipx) \overleftrightarrow{\partial_{t}}\phi 
\end{align} }$$

- Rewriting the last line, one gets:
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
- The explicit _form_ of $a_{p}$ is _irrelevant_, even as it _evolves differently from the free theory_

- One then gets a _Lorentz invariant_ $S-$matrix
- This relates _correlation functions_ to the $S-$matrix

- Correlation functions given by the _Schwinger-Dyson_ equation below

### Example: 4-point correlation in the free theory
 - Examine the correlation function:
$$\braket{ \phi(x_{1})\phi(x_{2})\phi(x_{3})\phi(x_{4})  } \equiv\braket{ \phi_{1} \phi_{2}\phi_{3}\phi_{4} } $$
- Applying [[#Wick's Theorem]] to this:
$$\displaylines{\braket{  \phi_{1}\phi_{2}\phi_{3}\phi_{4}  }=\Delta_{12}\Delta_{34}+\Delta_{13}\Delta_{24}+\Delta_{14}\Delta_{23} \\
\Delta_{12}=\Delta_{F}(x_{1}-x_{2})}$$
- One can also derive it using the _Schwinger-Dyson_ equation for the free theory:
$$\braket{  \phi_{1} \phi_{2}\phi_{3} \phi_{4}} =\int  d^4x \,\delta^{4}(x-x_{1}) \langle \phi_{x} \phi_{2}\phi_{3}\phi_{4}\rangle  $$
- Then using the fact that in the free theory, $\Delta_{F}$ is the _Greens function_ for the Klein-Gordon Lagrangian, and $\mathcal{L}_\text{int}=0$, and _integrating by parts twice_:
$$\langle \phi_{1}\phi_{2}\phi_{3}\phi_{4} \rangle =i\int  d^4x \,\Delta_{F}(x-x_{1})(\Box_{x}+m^{2})\langle \phi _{x}\phi_{2}\phi_{3}\phi_{4} \rangle  $$
- After using _Schwinger-Dyson_, one gets the _same result_ as Wick's Theorem

- One can represent it _pictorally_ using _Feynman diagrams_, where _lines_ represent _propagators_ between points:
![[4 point Feynmna diagrams.png|500]]

### Example: cubic perturbation
- Consider the perturbation:
$$\mathcal{L}_\text{int}=\frac{g}{3!}\phi^{3}$$
- The _one-point correlation function_:
$$\langle \phi_{x} \rangle =\int  d^4y\,\delta^{4}(x-y)\langle \phi_{y} \rangle  $$
- Using the same strategy as the above derivation:
$$\langle \phi_{x} \rangle =\frac{ig}{2}\int  d^4y\,\Delta_{xy}\langle \phi_{y}^{2} \rangle +\mathcal{O}(g^{3})  =\frac{ig}{2}\int  d^4y\,\Delta_{xy}\Delta_{yy}  +\mathcal{O}(g^{2}) $$
![[cubic one point.png]]

- The _three point correlation_, from Schwinger Dyson:
$$\langle \phi_{1}\phi_{2}\phi_{3} \rangle= \frac{ig}{2}\left\{\int  d^4x\, \Delta_{x1}\langle \phi_{x}\phi_{x}\phi_{2}\phi_{3} \rangle+\int  d^4x\,\Delta_{x_{1}}\big[\delta(x-x_{2})\langle \phi_{3} \rangle+\delta(x-x_{3})\langle \phi_{4} \rangle  \big] \right\}  $$
- Expanding to the _lowest order_ in $g$, use an _approximation_ from the free theory for the _four point correlation_, and _relabelling_:
$$\begin{align}
\langle \phi_{1}\phi_{2}\phi_{3} \rangle&= \frac{ig}{2}\int  d^4x \, \Delta_{xx}(\Delta_{x1}\Delta_{23}+\Delta_{12}\Delta_{3x}+\Delta_{13}\Delta_{2x}) \\
&+ig \int  d^4x\,\Delta_{x1}\Delta_{x2}\Delta_{x3} +\mathcal{O}(g^{2})
\end{align}$$

- The _two-point correlation_
	- _Feynman propagator_ is _exclusively for the free theory_
$$\langle \phi_{1}\phi_{2} \rangle=i \int  d^4x\,\Delta_{1x}\left( \frac{g}{2} \langle \phi_{x}^{2}\phi_{2} \rangle -i\delta(x-x_{2}) \right)  $$
- Using the result of the three point correlation:
$$\begin{align}
\langle \phi_{1}\phi_{2} \rangle&=\Delta_{12} \\
&+(ig)^{2}\int  d^4x \int  d^4y  \left\{\Delta_{x1}\Delta_{y2}\left( \frac{1}{4}\Delta_{xx}\Delta_{yy}+\frac{1}{2}\Delta_{xy}^{2} \right)+\frac{1}{2} \Delta_{x1}\Delta_{x2}\Delta_{xy}\Delta_{yy}\right\} 
\end{align}$$
- They _perturbative terms_ correspond to:
![[cubic 12 feynman diagrams.png]]

## Schwinger-Dyson equation
- A way to calculate the $n-$point correlation function:
$$\braket{ \phi_{1}\dots \phi_{n}  } \equiv\braket{ \Omega|T\{\phi(x_{1})\dots \phi(x_{n})\} | \Omega } $$

- _Assume_ that at any given time, the Hilbert space of the _interacting theory_ can be _mapped_ onto the Hilbert space of the _free theory_
	- In general, the mapping is not invariant over time
$$[\phi(\boldsymbol{x},t),\phi(\boldsymbol{x}',t')]=0 \qquad [\phi(\boldsymbol{x},t),\partial_{t}\phi(\boldsymbol{x}',t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}')$$
- Fields must still obey the _Euler Lagrange equations_:
$$(\Box+m^{2})\phi-\mathcal{L}'_\text{int}[\phi]=0\qquad \mathcal{L}'_\text{int}[\phi]=\frac{\partial \mathcal{L}_\text{int}}{\partial \phi}$$
- For the 2-point correlation:
	- Proof: Expand out correlation, then use equal time commutator
$$(\Box_{x}+m^{2})\braket{  \phi_{x}\phi_{y}  } =\braket{  (\Box_{x}+m^{2})\phi_{x}\phi_{y}  }-i\delta^{4}(x-y) $$
- Using the Euler-Lagrange equation:
$$(\Box_{x}+m^{2})\braket{ \phi_{x}\phi_{y}  }=\braket{ \mathcal{L}_\text{int}' [\phi_{x}]\phi_{y}  }  -i\delta^{4}(x-y)$$


- Then, one gets the _Schwinger-Dyson equation_:
$$\begin{align}
(\Box_{x}+m^{2})\braket{  \phi_{x}\phi_{2} \dots \phi_{n} } =&\braket{ \mathcal{L}_\text{int}'[\phi _{x}] \phi_{2}\dots \phi_{n}  }  \\
&-i\sum_{j=2}^{n}\delta^{4}(x-x_{j}) \braket{  \phi_{2}\dots \phi_{j-1}\phi_{j+1}\dots\phi_{n}  } 
\end{align}$$
- The first term is a _classical effect_
- The latter term gives the _contact interactions_, which are a _quantum effect_
	- They also give rise to _contractions_, which create _loops_ in the Feynman diagram

- It is a _non-perturbative_ equation for _any interacting theory_

## Position-space Feynman rules
- From the above, one gets the _Feynman rules_ for calculating correlation functions, with a _perturbation_ of:
$$\mathcal{L}_\text{int}=\frac{\lambda_{n}}{n!}\phi^{n}$$
1. Start with the _external points_ $x_{i}$ at which the fields are _evaluated_, and start to _extend_ lines from those points
2. A line can:
	- _Contract_ (join) an _existing line_ to form a _propagator_ $\Delta$
	- _Split_ into a _vertex_ $x$, which represents the integral of order $\lambda$:
	$$(i\lambda_{n})\int  d^{4}x $$
3. For a _given order_ $i\lambda_{n}$, _add up_ all possible diagrams that have _all lines contracted_, and vertices integrated over
4. For each diagram, there is a _symmetry factor_ that causes the $1/n!$ factor to _not be completely cancelled out_, hence _divide_ by that factor
	- Determine from _interchanging_ the ends of lines, or the _equivalence of vertices_

# Scalar Yukawa Theory
- The _non-interacting_ Lagrangian, with a _real scalar_ and a _complex scalar_:
$$\mathcal{L}_{0}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}+(\partial_{\mu}\psi ^{\dagger})(\partial^{\mu}\psi)-M^{2}\psi ^{\dagger}\psi$$
- A _cubic interaction_:
$$\mathcal{L}_\text{int}=-g\psi ^{\dagger}\psi \phi$$
## The free theory
- The real scalar field $\phi$ still follows the _Klein-Gordon equation_:
$$\displaylines{\phi(x)=\int  \frac{d^{3}p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\omega_\boldsymbol{p} }}\big[a_\boldsymbol{p}\exp(-ipx)+a^{\dagger}_\boldsymbol{p}\exp(ipx)\big] \\ \omega_{\boldsymbol{p}}=\sqrt{ p^{2}+m^{2} }}$$
- The _complex field_:
$$\displaylines{\psi(x)=\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\tilde{\omega}_{p} }} [b_{p}\exp(-ipx)+c^{\dagger}_{p}\exp(ipx)]\\ \tilde{\omega}_{p}=\sqrt{ p^{2}+M^{2} }}$$

- The _canonical quantisation_
	- Derive the canonical momenta from $\mathcal{L}$
$$\displaylines{[\phi(\boldsymbol{x},t),\dot{\phi}(\boldsymbol{x}',t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}') \\ [\psi(\boldsymbol{x},t),\dot{\psi}^{\dagger}(\boldsymbol{x}',t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}')\qquad [\psi ^{\dagger}(\boldsymbol{x},t),\dot{\psi}(\boldsymbol{x}',t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}')}$$
- Then, the commutation relations between $a_{p},b_{p},c_{p}$ can be obtained:
$$\begin{align}
[a_{p}a_{p'}^{\dagger}]&=(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}') \\
[b_{p},b_{p'}^{\dagger}]&=(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}') \\
[c_{p}c_{p'}^{\dagger}]&=(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')
\end{align}$$

- The _normal ordered Hamiltonian_:
$$H_{0}=\int  \frac{d^3p}{(2\pi)^{3}} [\omega_{p}a^{\dagger}_{p}a_{p}+\tilde{\omega_{p}}b_{p}^{\dagger}b_{p}+\tilde{\omega}_{p}c_{p}^{\dagger}c_{p}] $$
- There is a $U(1)$ symmetry, with a _conserved charge_:
$$\displaylines{\psi\to \exp(i\alpha)\psi\\
Q=i\int  d^3x\, (\psi ^{\dagger}\psi-\psi \psi ^{\dagger}) =\int  \frac{d^3p}{(2\pi)^{3}}(c^{\dagger}_{p}c_{p}-b^{\dagger}_{p}b_{p}) \\ [H_{0},Q]=0}$$
- From this, there is a _distinction_ between $b$ and $c$, as they produce _different states_
- The number of _particles minus antiparticles_ is _conserved_

- One also gets the identities:
$$\begin{align}
\sqrt{ 2\omega_{p} }{a_{p}}&=i \int  d^3x\,\exp(ipx) \overleftrightarrow{\partial_{t}}\phi \\
\sqrt{ 2\tilde{\omega}_{p} }b_{p}&= i \int  d^3x\,\exp(ipx) \overleftrightarrow{\partial_{t}}\psi \\
\sqrt{ 2\tilde{\omega}_{p} }c_{p}&= i \int  d^3x\,\exp(-ipx) \overleftrightarrow{\partial_{t}}\psi ^{\dagger}
\end{align}$$
- Interpretation:
	- $\phi$ has operators $a,a^{\dagger}$ which can _create or destroy_ the _mesons_
	- $\psi$ has operators $b,c^{\dagger}$ which _creates nucleons_ or _destroys anti-nucleons_
	- $\psi ^{\dagger}$ has operators $b^{\dagger},c$ which _creates anti-nucleons_ or _destroys nucleons_
### The Fock space
- The _vacuum state_:
$$\displaylines{a_{p}\ket{0}=b_{p}\ket{0}=c_{p}\ket{0}=0    \\ H_{0}\ket{0}=\ket{0}  }$$
- The _meson states_ are _neutral_ states given by $a_{p}^{\dagger}$
$$\ket{\phi}=a_{p}^{\dagger}\ket{0}  \qquad H_{0}\ket{\phi}=\omega_{p}\ket{\phi} \qquad Q\ket{\phi}=0   $$
- The _nucleon states_ $\ket{\psi}$:
$$\ket{\psi}=c_{p}^{\dagger}\ket{0} \qquad H\ket{\psi}=\tilde{\omega}_{p}\ket{\psi}\qquad Q\ket{\psi}=+\ket{\psi}      $$
- The _anti-nucleon states_ $\ket{\psi^{*}}$
$$\ket{\psi^{*}}=b_{p}^{\dagger}\ket{0} \qquad H\ket{\psi^{*}}=\tilde{\omega}_{p} \ket{\psi^{*}}\qquad Q\ket{\psi^{*}}=-\ket{\psi^{*}}     $$
- One can then form _multi-particle states_ by applying more operators

### Feynman propagators
- Following the definitions of [[#The Feynman propagator]] for the _real scalar field_ $\phi$:
$$\Delta_{F}(x_{1}-x_{2})=\braket{ \phi_{1} \phi_{2} } =\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} \exp[-ip(x_{1}-x_{2})] \equiv\Delta_{12}$$


- The propagator for the _complex scalar field_ $\psi$:
$$\begin{align}
\Delta_{F}^{\psi}(x_{1}-x_{2})&=\braket{ \Omega|T\psi(x_{1})\psi ^{\dagger}(x_{2}) | \Omega } \\  &=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-M^{2}+i\epsilon}\exp[-ip(x_{1}-x_{2})]\equiv \hat{\Delta}_{12} 
\end{align}$$
- For the complex field in the free theory, $\langle \psi_{1}\psi_{2} \rangle = \langle \psi_{1}^{\dagger}\psi_{2}^{\dagger} \rangle=0$
	- $\langle \psi_{1}\psi_{2}^{\dagger} \rangle$ has $b^{\dagger}b$ and $c^{\dagger}c$ combinations

## The interacting theory
- The _equations of motion_:
$$\begin{align}
(\Box+m^{2})\phi&=-g\psi ^{\dagger}\psi \\ (\Box+M^{2})\psi&=-g\psi\phi \\ (\Box+M^{2})\psi ^{\dagger}&=-g\psi ^{\dagger} \phi
\end{align}$$
- The right hand side terms are $\mathcal{L}_\text{int}'$ for plugging into the [[#Schwinger-Dyson equation]]
$$\begin{align}
&(\Box_{x}+m^{2}) \langle \phi_{x}\phi_{2}\dots \phi _{n}\psi_{1}\dots \psi_{m}\psi_{1}^{\dagger} \dots \psi ^{\dagger}_{p}\rangle  \\
=&-g\langle \psi ^{\dagger}_{x}\psi_{x} \phi_{2}\dots \phi _{n}\psi_{1}\dots \psi_{m}\psi_{1}^{\dagger} \dots \psi ^{\dagger}_{p}\rangle  \\
&-i\sum_{j=2}^{n} \delta(x-x_{j}) \langle \phi_{2}\dots \phi_{j-1}\phi_{j+1}\dots \phi_{n} \psi_{1}\dots \psi_{m}\psi_{1}^{\dagger} \dots \psi ^{\dagger}_{p}\rangle 
\end{align}$$
- For the complex field, _contractions_ must be taken with the _conjugate_:
$$\begin{align}
&(\Box_{x}+M^{2})\langle \phi_{1}\phi_{2}\dots \phi _{n}\psi_{x}\psi_{2}\dots \psi_{m}\psi_{1}^{\dagger} \dots \psi ^{\dagger}_{p}\rangle  \\
=&-g \langle \phi_{1}\dots \phi_{n}\phi_{x}\psi_{x}\psi_{2}\dots \psi_{m}\psi_{1}^{\dagger}\dots \psi_{p}^{\dagger} \rangle  \\
&-i\sum_{j=2}^{p} \delta(x-x_{j}) \braket{  \phi_{1}\dots \phi_{n}\psi_{2}\dots \psi_{m}\psi_{1}^{\dagger}\dots \psi ^{\dagger}_{j-1}\psi ^{\dagger}_{j+1}\dots \psi_{p}^{\dagger}  } 
\end{align}$$
### Feynman diagrams
- Example: consider the 3-point function
$$\braket{ \phi_{1}  \psi_{2}^{\dagger}\psi_{3} } =-ig \int  d^4x\,\Delta_{1x} \braket{  \psi_{x}\psi_{x}^{\dagger}\psi_{2}^{\dagger}\psi_{3}  }  $$
- From an analagous [[#Wick's Theorem]], or (more conveniently) the _Schwinger-Dyson equation_ in the _free theory_, one gets the _lowest-order contribution_:
$$\braket{ \phi_{1}\psi_{2}^{\dagger}\psi_{3}  } =-ig \int  d^4x \,\Delta_{1x} \left( \hat{\Delta}_{xx} \hat{\Delta}_{23}+ \hat{\Delta}_{x2} \hat{\Delta}_{x3} \right)+\mathcal{O}(g^{2})$$
- The _directionality_ of the propagator matters:
![[Scalar yukawa three point.png]]
### Scattering
- Calculate the $S$ matrix:
$$\braket{ \text{final},\,+\infty | \text{initial},-\infty }=\braket{ f|S |i  }  $$
- The initial and final states are _asymptotic_

- With a proof similar to [[#LSZ reduction formula|in the free theory]], using the identity:
$$\sqrt{ 2\tilde{\omega}_{p} }[b_{p}^{\dagger}(\infty)-b_{p}^{\dagger}(-\infty)]=-i \int  d^4x\,\exp(-ipx)(\Box_{x}+M^{2})\psi ^{\dagger}(x) $$

#### Nucleon-nucleon scattering
- Take the case of _nucleon scattering_:
$$ \lim_{ t \to- \infty } \sqrt{ (2\tilde{\omega}_{1})(2\tilde{\omega}_{2}) }c^{\dagger}_{p_{1}}(t)c_{p_{2}}^{\dagger}(t)\ket{\Omega} \longrightarrow  \lim_{ t \to+\infty } \sqrt{ (2\tilde{\omega}_{3})(2\tilde{\omega}_{4}) }c^{\dagger}_{p_{3}}(t)c_{p_{4}}^{\dagger}(t)\ket{\Omega} $$
- The LSZ formula for this case:
$$\begin{align}
\braket{ f|S | i } =\left[\prod_{j} i\int  d^4x_{j} \right] &[\exp(-ip_{1}x_{1})(\Box_{1}+M_{1}^{2})]\dots[\exp(ip_{4}x_{4})(\Box_{4}+M_{4}^{2})] \\
&\times\braket{ \Omega|T\{\psi ^{\dagger}(x_{3})\psi ^{\dagger}(x_{4})\psi (x_{1})\psi (x_{2})\} | \Omega } 
\end{align} $$
- The correlation function:
	- From _Schwinger Dyson_, or inspection, there is _no contribution of order_ $g$
$$\begin{align}
\langle \psi_{1}^{\dagger}\psi_{2}^{\dagger}\psi_{3}\psi_{4} \rangle &=\hat{\Delta}_{13}\hat{\Delta}_{24}+ \hat{\Delta}_{14} \hat{\Delta}_{23}  \\
&+(-ig)^{2}\int  d^4x \,d^{4}y\left[ \hat{\Delta}_{24}\hat{\Delta}_{1x}\hat{\Delta}_{3x}\Delta_{xy}\hat{\Delta}_{yy}+\hat{\Delta}_{24}\hat{\Delta}_{1x}\Delta_{xy}\hat{\Delta}_{xy}\hat{\Delta}_{3y}+(3\leftrightarrow 4) \right] \\
&+(-ig)^{2} \int  d^4x\,d^{4}y\left[ \hat{\Delta}_{1x}\hat{\Delta}_{3x}\Delta_{xy}\hat{\Delta}_{2y}\hat{\Delta}_{4y}+(3\leftrightarrow 4) \right] 
\end{align}$$
- The second line consists of _disconnected diagrams_, which _do not represent scattering processes_, and can be _ignored when calculating $S$_
- The third line consists of _connected diagrams_, which take the interactions into account

- Replacing the _connected correlation function_ in the formula, the $(\Box+M^{2})$ operators act on the _propagators_ to produce _delta functions_
	- They effectively _put particles on-shell_
- For nucleon scattering, using the LSZ formula with the [[#The Feynman propagator|Feynman propagator]] gives:
$$\braket{ f|S |i  }_{C}=i(-ig)^{2}(2\pi)^{4}\left[ \frac{1}{(p_{3}-p_{1})^{2}-m^{2}}+\frac{1}{(p_{4}-p_{1})^{2}-m^{2}} \right]\delta^{4}(p_{1}+p_{2}-p_{3}-p_{4}) $$
- The delta function _ensures 4-momentum conservation_
	- Both _energy_ and _3-momentum_

### Momentum space Feynman rules
- Once the Feynman diagram is _drawn_, assign a _momentum_ to each line
- For each _internal line_ of momentum $k$ and _mass_ $m$, it adds a _factor to the $S$ matrix_:
$$\int  \frac{d^4k}{(2\pi)^{4}} \frac{i}{k^{2}-m^{2}+i\epsilon} $$
- To _each vertex_ with momenta $p_{1},p_{2},p_{3}$ (depending on direction), the factor to the $S$ matrix is:
$$(-ig)(2\pi)^{4}\delta(p_{1}-p_{2}+p_{3})$$
- Then, _sum over all diagrams_

- _Tree level diagrams_ have the _leading contribution_
	- _Looped_ diagrams have _self interaction_

- The _external particles_ are _on-shell_, where $p^{2}=m^{2}$
- The _internal particles_ are _off-shell_, where $k^{2}\neq m^{2}$, known as _virtual particles_

#### Nucleon-antinucleon scattering
- For _anti-nucleons_, the line of the _propagator_ and the momentum are _opposite_
![[Nucleon anti-nucleon scattering.png]]
$$\begin{align}
\braket{ f|S | i }_{C}=&(-ig)^{2}(2\pi)^{4}\delta^{4}(p_{1}+p_{2}-p_{3}-p_{4})\times \\
 &\left( \frac{i}{(p_{1}-p_{3})^{2}-m^{2}+i\epsilon}+\frac{i}{(p_{1}+p_{2})^{2}-m^{2}+i\epsilon} \right)
\end{align}$$
- For the second term, going to the _centre of mass frame_ gives:
$$(p_{1}+p_{2})^{2}-m^{2}=4M^{2}-m^{2}$$
- For $m<2M$, there is _no pole_, and the $+i\epsilon$ prescription is unecessary
- For $m>2M$, there is some $p_{1}$ such that there is a _pole_, corresponding to a _spike_ in the _scattering cross-section_
### Mandelstam variables
- Define the _Mandelstam variables_
$$\begin{align}
s&=(p_{1}+p_{2})^{2}=(p_{3}+p_{4})^{2} \\ t&=(p_{1}-p_{3})^{2}=(p_{2}-p_{4})^{2} \\ u&=(p_{2}-p_{3})^{2}=(p_{1}-p_{4})^{2}
\end{align}$$
- Transforming to the _centre of mass frame_:
$$\displaylines{p_{1}=(E,p,0,0) \qquad p_{2}=(E,-p,0,0) \\ p_{3}=(E,p\cos\theta,p\sin\theta,0) \qquad p_{4}=(E,-p\cos\theta,-p\sin\theta,0) \\ s=4E^{2}\qquad t=-2p^{2}(1-\cos\theta) \qquad u=-2p^{2}(1+\cos\theta)}$$
- $s$ gives the _total energy_ in the centre of mass frame
- $t$ and $u$ gives the _momentum exchanged_

- One also gets for an aribitrary scattering process with masses $M_{i}$:
$$s+t+u=\sum_{i}M_{i}^{2}$$
- For _nucleon-nucleon_ scattering, there is $t-$channel and $u-$channel scattering:
$$\mathcal{A}\sim (t-m^{2})^{-1}+(u-m^{2})^{-1}$$
- For _nucleon-antinucleon_ scattering, there is $t-$channel and $s-$channel scattering:
$$\mathcal{A}\sim (t-m^{2})^{-1}+(s-m^{2})^{-1}$$
# Classical Dirac fields

## Representations of the Lorentz group
- Recall the [[#Fields with Lorentz transformations|active transformation]]
$$\phi^{a}(x)\to D[\Lambda]^{a}_{b}\phi^{b}(\Lambda^{-1}x)$$
- Identify another _representation_ of $\Lambda$
$$D[\Lambda]=\exp\left( \frac{1}{2}\Omega_{\rho\sigma}R^{\rho\sigma} \right)$$
- $\Omega_{\rho\sigma}=-\Omega_{\sigma \rho}$ are the _parameters_, and $R^{\rho\sigma}$ are the [[Groups in physics#Tangent spaces and the exponential map|generators]] of the Lorentz group
	- 6 generators: 3 _boosts_ and 3 _rotations_
- The generators satisfy the Lie algebra:
$$[R^{\rho\sigma},R^{\tau \nu}]=\eta^{\sigma \tau}R^{\rho \nu}-\eta^{\rho \tau}R^{\sigma \nu}+\eta^{\rho \nu}R^{\sigma \tau}-\eta^{\sigma \nu}R^{\rho \tau}$$

### Example: infinite-dimensional representation
- Consider the generator:
$$L^{\rho\sigma}=x^{\rho}\partial^{\sigma}-x^{\sigma}\partial^{\rho}$$
- There are _infinite degrees of freedom_ $x$
- This satisfies the Lie algebra

### Example: 4x4 representation
- Consider the generator:
$${(M^{\rho\sigma})^{\mu}}_{\nu}=\eta^{\rho \mu}\delta^{\sigma}_{\nu}-\eta^{\sigma \mu}\delta^{\rho}_{\nu}$$
- The representation is:
$$\Lambda=D[\Lambda]=\exp\left( \frac{1}{2} \Omega_{\rho\sigma}M^{\rho\sigma}\right)$$
- It acts on _vectors_
$$V^{\mu}\to {D[\Lambda]^{\mu}}_{\nu}V^{\nu}={\Lambda^{\mu}}_{\nu}V^{\nu}$$
### The chiral representation and spinors
- Consider the _Clifford algebra_, defined by: 
$$\{\gamma^{\mu},\gamma^{\nu}\}\equiv\gamma^{\mu}\gamma^{\nu}+\gamma^{\nu}\gamma^{\mu}=2\eta^{\mu \nu}\mathbb{I}$$
- Properties: 
$$\displaylines{\gamma^{\mu}\gamma^{\nu}=-\gamma^{\nu}\gamma^{\mu} \qquad \text{for }\mu\neq \nu \\ (\gamma^{0})^{2}=1 \qquad (\gamma^{i})^{2}=-1}$$
- The _chiral representation_, the _smallest matrices_ that obey the Clifford algebra:
$$\gamma^{0}=\pmatrix{0&\mathbb{I}_{2\times2} \\ \mathbb{I}_{2\times 2}&0}\qquad \gamma^{i}=\pmatrix{0&\sigma^{i} \\ -\sigma^{i}&0}$$
- $\sigma^{i}$ are the _Pauli matrices_
$$\{\sigma_{i},\sigma_{j}\}=2\delta_{ij}$$
- Also define:
$$\sigma=(\mathbb{I},\sigma^{i}) \qquad \bar{\sigma}=(\mathbb{I},-\sigma^{i})\qquad \gamma^{\mu}=\pmatrix{0&\sigma^{\mu} \\ \bar{\sigma}^{\mu}&0}$$

- Make the _generators_ of the Lorentz group from:
	- Proof: plug into definition of Lie algebra, then use definition of Clifford algebra
$$S^{\rho\sigma}=\frac{1}{4}[\gamma^{\rho},\gamma^{\sigma}]$$
- The _chiral representation_, consisting of $4\times4$ matrices:
$$S[\Lambda]=\exp\left( \frac{1}{2}\Omega_{\rho\sigma}S^{\rho\sigma} \right)$$
- Objects that _transform_ under this representation are _spinors_
	- In general, they are _complex_
$$\psi^{a}(x)\to {S[\Lambda]^{a}}_{b}\psi^{b}(\Lambda^{-1}x)$$

#### Behaviour under rotation
- For _rotations_ around axis $k$, pick $\Omega_{ij}$ as the non-zero parameters
- From the definitions of $\gamma^{\mu}$:
$$S^{12}=-\frac{i}{2}\pmatrix{\sigma^{3}&0 \\ 0&\sigma^{3}}$$
- Picking $\Omega_{12}=2\pi$, one gets:
$$S[\Lambda]=\exp\left( \frac{1}{2}\Omega_{12}S^{12} \right)=-\mathbb{I}_{4\times 4}$$
- Under a $2\pi$ rotation, there is a _sign flip_

- Spinors _do not transform as vectors_

#### Behaviour under boosts
- For _boosts_ along axis $i$, pick $\Omega^{0i}$ as the non-zero parameter
$$S^{01}=\frac{1}{2}\pmatrix{-\sigma^{1}&0\\0&\sigma^{1}}$$
- With the _rapidity_ $\eta_{1}$, the group element:
$$S[\Lambda]=\pmatrix{\exp(\eta_{1}\sigma^{1}/2)&0\\0&\exp(\eta_{1}\sigma^{1}/2)}$$
- Under some general boost with rapidity $\boldsymbol{\eta}$:
$$S[\Lambda]=\pmatrix{\exp(\boldsymbol{\eta}\cdot \boldsymbol{\sigma}/2)&0\\0&\exp(-\boldsymbol{\eta}\cdot \boldsymbol{\sigma}/2)}$$
- This is _different_ from the ${\Lambda^{\mu}}_{\nu}$ for the _vector_ Lorentz transformation

### Transformations and the adjoint
- How spinors transform:
$$\psi(x)\to S[\Lambda]\psi(\Lambda^{-1}x)$$
- Find some _quantity_ $A$ that transforms as the _inverse_:
$$A\to AS[\Lambda]^{-1} \implies A\psi\to A\psi(\Lambda^{-1}x)$$
- Consider the _Hermitian conjugate_ of $\psi$:
$$\psi ^{\dagger}(x)\to \psi ^{\dagger}(\Lambda^{-1}x)S[\Lambda]^{\dagger}$$
- The Hermitian conjugate of $S$:
$$S[\Lambda]^{\dagger}=\exp\left( \frac{1}{2}\Omega_{\rho\sigma}(S^{\rho\sigma})^{\dagger} \right)$$
- In the _chiral representation_:
$$(\gamma^{0})^{\dagger}=\gamma^{0} \qquad (\gamma^{i})^{\dagger}=-\gamma^{i} \implies \gamma^{0}\gamma^{\mu}\gamma^{0}=(\gamma^{\mu})^{\dagger}$$
- From this:
$$\displaylines{(S^{\rho\sigma})^{\dagger}=\frac{1}{4}[(\gamma^{\sigma})^{\dagger},(\gamma^{\rho})^{\dagger}]=-\gamma^{0}S^{\rho\sigma}\gamma^{0} \\ S[\Lambda]^{\dagger}=\exp\left( -\frac{1}{2}\Omega_{\rho\sigma}\gamma^{0}S^{\rho\sigma}\gamma^{0} \right)=\gamma^{0}S[\Lambda]^{-1}\gamma^{0}}$$
- Therefore, $\psi ^{\dagger}\psi$ is _not Lorentz invariant_:
$$\psi ^{\dagger}(x)\to \psi ^{\dagger}(\Lambda^{-1}x)\gamma^{0}S[\Lambda]^{-1}\gamma^{0}$$

- Instead, define the _adjoint spinor_:
$$\bar{\psi}(x)\equiv \psi ^{\dagger}(x)\gamma^{0}$$
- $\bar{\psi}\psi$ is _Lorentz invariant_:
$$\bar{\psi}\psi\to \bar{\psi}(\Lambda^{-1}x)\psi(\Lambda^{-1}x)$$
- Meanwhile, $\bar{\psi}\gamma^{\mu}\psi$ _transforms as a vector_
	- Proof: _expand_ $S[\Lambda]$ in infinitesimal properties

- $\bar{\psi}\gamma^{\mu}\gamma^{\nu}\psi$ transforms as a _rank $2$ tensor_
- $\bar{\psi}\partial_{\mu}\psi$ transforms _covariantly_

## Dirac action and the Dirac equation
- Construct the action as a _real, Lorentz invariant quantity_, in its _simplest form_ with _minimal derivatives_

- Consider the Lagrangian:
$$\displaylines{\mathcal{L}=\bar{\psi}(i\gamma^{\mu}\partial_{\mu}-m)\psi \\ S=\int  d^4x\,(\bar{\psi}i\gamma^{\mu}\partial_{\mu}\psi-m\bar{\psi}\psi) }$$
- One then gets the _Dirac equation_:
$$\displaylines{i\gamma^{\mu}\partial_{\mu}\psi-m\psi=0 \\ i\gamma^{\mu}\partial_{\mu}\bar{\psi}+m\bar{\psi}=0}$$
- It is only _first order_ in $\partial_{\mu}$
- Notation:
$$\cancel{ \partial }=\gamma^{\mu}\partial_{\mu} \qquad \cancel{ p } =\gamma^{\mu}p_{\mu}$$

- $\psi$ also obeys the _Klein-Gordon equation_
$$(i\gamma^{\mu}\partial_{\mu}+m)(i\gamma^{\nu}\partial_{\nu}-m)\psi=0 \implies (\partial_{\mu}\partial^{\mu}+m^{2})\psi=0$$

## Symmetries
- The Dirac field is _symmetric under_:
	- _Lorentz_ transformations
	- $U(1)$ _internal symmetry_
	- _Translations_

- Under _translations_, one gets the _Dirac energy-momentum tensor_
	- It is evaluated _on-shell_, using the _equations of motion_
$$T^{\mu \nu}=\bar{\psi}i\gamma^{\mu}\gamma^{\nu}\psi$$


- Under the _Lorentz transformation_ ${\Lambda^{\mu}}_{\nu}$, with the _parameter_ $\omega^{\mu \nu}$:
$$\delta \psi_{a}=-\omega^{\mu \nu}\left( x_{\nu}\partial_{\mu}\psi_{a}-\frac{1}{2}(S_{\mu \nu})^{b}_{a}\psi_{b} \right)$$
- The former term is from the _scalar transformation_, while the latter is _unique to the spinor_
- The corresponding _conserved current_:
$$(J^{\mu})^{\lambda \nu}=-x^{\nu}T^{\mu\lambda}+x^{\lambda}T^{\mu \nu}+i\bar{\psi}\gamma^{\mu }S^{\lambda \nu}\psi$$
- The former two terms are from the _scalar field transformation_, while the latter gives rise to _spin_

- The _internal_, or _vector_ symmetry:
$$\psi\to \exp(i\alpha)\psi \qquad \bar{\psi}\to \exp(-i\alpha)\bar{\psi}$$
- The associated current:
$$J^{\mu}=\bar{\psi}\gamma^{\mu}\psi$$
- The $0$ component gives _electric charge_

## Plane wave solutions
- The solutions to the Dirac equation also follow the _Klein-Gordon equation_
- From this, use the ansatz:
$$\displaylines{\psi(x)=U(\boldsymbol{p})\exp(-ipx)+V(\boldsymbol{p})\exp(ipx) \\ p^{2}=m^{2}}$$
- The second term is a _negative frequency solution_, corresponding to an _antiparticle_

- From the Dirac equation:
$$\begin{align}
(-\cancel{ p }+m)U(p)&=0 \\ (\cancel{ p }+m)V(p)&=0
\end{align}$$

- In the _chiral representation_:
$$\displaylines{\pmatrix{m\mathbb{I}_{2}&-\boldsymbol{p}\cdot \boldsymbol{\sigma} \\ -\boldsymbol{p}\cdot\bar{\boldsymbol{\sigma}}&m\mathbb{I}_{2}}\pmatrix{U_{1}\\ U_{2}}=\pmatrix{0\\0} \\ mU_{1}=(\boldsymbol{p}\cdot \boldsymbol{\sigma})U_{2}}$$
- From this:
$$\displaylines{m^{2}=(\boldsymbol{p}\cdot \boldsymbol{\sigma})(\boldsymbol{p}\cdot  \boldsymbol{\bar{\sigma}}) \\ \sqrt{ \boldsymbol{p}\cdot \boldsymbol{\sigma} }U_{2}=\sqrt{ \boldsymbol{p}\cdot \bar{\boldsymbol{\sigma}} }U_{1}}$$
- The solutions (following a similar technique for $V$) are given using the _two-component spinors_, which give _particles_ and _antiparticles_
$$U^{S}(\boldsymbol{p})=\pmatrix{\sqrt{ \boldsymbol{p}\cdot \boldsymbol{\sigma}}\xi_{s} \\ \sqrt{ \boldsymbol{p}\cdot \boldsymbol{\bar{\sigma}} }\xi_{s}} \qquad  \qquad V^{S}(\boldsymbol{p})=\pmatrix{\sqrt{ \boldsymbol{p}\cdot \boldsymbol{\sigma}}\eta_{s} \\ -\sqrt{ \boldsymbol{p}\cdot \boldsymbol{\bar{\sigma}} }\eta_{s}}$$
- $\xi$ and $\eta$ are _two component spinors_

- The _basis set_ corresponds to different _spins_ (see below)
$$\xi_{1}=\pmatrix{1\\0} \quad \xi_{2}=\pmatrix{0\\1} \qquad \eta_{1}=\pmatrix{1\\0}\quad \eta_{2}=\pmatrix{0\\1}$$
## Weyl spinors and chirality
- In the chiral representation:
$$S[\Lambda _\text{rot}]= \pmatrix{\exp\left( i\frac{\boldsymbol{\varphi}\cdot \boldsymbol{\sigma}}{2} \right)&0\\0&\exp\left( i\frac{\boldsymbol{\varphi}\cdot \boldsymbol{\sigma}}{2} \right)}\qquad S[\Lambda _\text{boost}]=\pmatrix{\exp\left( \frac{\boldsymbol{\chi}\cdot \boldsymbol{\sigma}}{2} \right)&0\\0&\exp\left( -\frac{\boldsymbol{\chi}\cdot\boldsymbol{\sigma}}{2} \right)}$$
- The _4-component Dirac spinor_ is a _reducible representation_:
$$\psi(x)=\pmatrix{U_{+} \\ 0}+ \pmatrix{0\\U_{-}}$$
- Here, $U_{+}$ and $U_{-}$ are the _2-component Weyl spinors_ above

- Under _rotations_, the spinors behave the same way
$$U_{+}\to \exp\left( i\frac{ \boldsymbol{\varphi}\cdot \boldsymbol{\sigma}}{2} \right)U_{+} \qquad U_{-}\to \exp\left( i\frac{ \boldsymbol{\varphi}\cdot \boldsymbol{\sigma}}{2} \right)U_{-}$$

- Under _boosts_, they behave differently
$$U_{+}\to \exp\left( \frac{ \boldsymbol{\chi}\cdot \boldsymbol{\sigma}}{2} \right)U_{+} \qquad U_{-}\to \exp\left( -\frac{ \boldsymbol{\chi}\cdot \boldsymbol{\sigma}}{2} \right)U_{-}$$
- A manifestation of the _structure_ of the $\gamma$ matrices:
$$\gamma^{\mu}=\pmatrix{0&\sigma^{\mu}\\\bar{\sigma}^{\mu}&0}$$

- Define the _Lorentz invariant_ $\gamma^{5}$:
$$ \gamma^{5}\equiv-i\gamma^{0}\gamma^{1}\gamma^{2}\gamma^{3}\sim\epsilon_{\mu \nu\lambda \rho}\gamma^{\mu}\gamma^{\nu}\gamma^{\lambda}\gamma^{\rho}$$
- In the chiral representation:
$$\gamma^{5}=\pmatrix{\mathbb{I}_{2}&0\\0&-\mathbb{I}_{2}} \qquad (\gamma^{5})^{2}=\mathbb{I}_{4}$$

- It satisfies the (anti-)commutation relations:
$$\{\gamma^{5},\gamma^{\mu}\}=0 \qquad [S^{\mu \nu},\gamma^{5}]=0$$

- One can define the _projectors_:
$$\displaylines{\mathcal{P}_{+} =\frac{1}{2}(\mathbb{I}+\gamma^{5})=\pmatrix{\mathbb{I}_{2}&0\\0&0}\qquad \mathcal{P}_{-}=\frac{1}{2}(\mathbb{I}-\gamma^{5})=\pmatrix{0&0\\0&\mathbb{I}_{2}} \\ \mathcal{P}_{\pm}^{2}=\mathcal{P}_{\pm} \qquad \mathcal{P}_{\pm}\mathcal{P}_{\mp}=0}$$
- It _projects_ the Dirac spinor into the _Weyl spinors_
$$\psi_{+}=\mathcal{P}_{+}\psi=\pmatrix{U_{+}\\0} \qquad \psi_{-}=\mathcal{P}_{-}\psi=\pmatrix{0\\U_{-}}$$
- The _Lagrangian_:
	- Cannot contain $U_{+}^{\dagger}U_{+}$ terms as it is _not invariant under boosts_
$$\begin{align}
\mathcal{L}&=\bar{\psi}(i\cancel{ \partial }-m)\psi \\ &=iU_{-}^{\dagger}\sigma^{\mu}\partial_{\mu}U_{-}+iU_{+}^{\dagger}\sigma^{\mu}\partial_{\mu}U_{+}-m(U_{+}^{\dagger}U_{-}+U_{-}^{\dagger}U_{+})
\end{align}$$
- The Lagrangian is _not separable_ into components of non-zero chirality, as they couple through the _mass term_

- _Massless chiral particles_ are described by the _Weyl equation_
# Quantum Dirac fields

## Canonical quantisation in the free theory
$$\mathcal{L}=i\bar{\psi}\gamma^{\mu}\partial_{\mu}\psi-m\bar{\psi}\psi$$
- The _canonical momentum_ to $\psi$ is:
$$\pi=i\bar{\psi}$$
- From this, there are $4$ _independent components_ of the phase space
	- As opposed to have 4 scalar fields, where the _momenta_ are _also_ degrees of freedom
### Failure of bosonic quantisation
- Attempt canonical quantisation like the scalar field:
$$\displaylines{ [\psi_{a}(\boldsymbol{x},t),\pi_{b}(\boldsymbol{x}',t)]=i\delta_{ab}\delta(\boldsymbol{x}-\boldsymbol{y})\implies [\psi_{a}(\boldsymbol{x},t),\psi ^{\dagger}_{b}(\boldsymbol{y},t)]=\delta_{ab}\delta(\boldsymbol{x}-\boldsymbol{y}) \\ [\psi_{a}(\boldsymbol{x},t),\psi_{b}(\boldsymbol{y},t)]=0}$$
- The _plane wave solution_:
$$\psi(x)=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\omega_{p} }}[b_{\boldsymbol{p}}^{s}U^{s}(\boldsymbol{p})\exp(-ipx)+{c_{\boldsymbol{p}}^{s}}^{\dagger}V^{s}(\boldsymbol{p})\exp(ipx)] $$
- Form of the operators:
$$\begin{align}
b_{\boldsymbol{p}}^{s}&= \frac{1}{\sqrt{ 2\omega_{\boldsymbol{p}} }}\int  d^3x\,\exp(ipx)\bar{U}^{s}(\boldsymbol{p})\gamma^{0}\psi(x)  \\
{b_{\boldsymbol{p}}^{s}}^{\dagger}&= \frac{1}{\sqrt{ 2\omega_{\boldsymbol{p}} }}\int  d^3x\,\exp(-ipx)\bar{\psi}(x)\gamma^{0}U^{s}(\boldsymbol{p}) \\
c_{\boldsymbol{p}}^{s}&=\frac{1}{\sqrt{ 2\omega_{\boldsymbol{p}} }}\int  d^3x\,\exp(ipx)\bar{\psi}(x)\gamma^{0}U^{s}(\boldsymbol{p})  \\
{c_{\boldsymbol{p}}^{s}}^{\dagger}&= \frac{1}{\sqrt{ 2\omega_{\boldsymbol{p}} }}\int  d^3x\,\exp(-ipx)\bar{V}^{s}(\boldsymbol{p})\gamma^{0}\psi(x)
\end{align}$$

- This gives the commutation relations:
$$[b_{p}^{s},{b_{p'}^{s'}}^{\dagger}]=(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')\delta^{ss'} \qquad [c_{p}^{s},{c_{p'}^{s'}}^{\dagger}]=-(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')\delta^{ss'} $$
- The latter has an _opposite sign_ to the usual commutation relation
- Therefore, $c_{p}^{s}$ is the _creation operator_, unlike usual
	- Otherwise, states have a _negative norm_ which is _unphysical_

- The Hamiltonian:
$$H=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}} \omega_{p}({b_{p}^{s}}^{\dagger}b_{p}^{s}-c_{p}^{s}{c_{p}^{s}}^{\dagger}) $$

- From this, one gets the _commutation relation_ between _creation and annihilation operators_
	- From the commutation relation, $c_{p}^{s}$ is responsible for _creation_ in this case
$$[H,{b_{p}^{s}}^{\dagger}]=\omega_{p}{b_{p}^{s}}^{\dagger} \qquad [H,c_{p}^{s}]=-\omega_{p}c_{p}^{s}$$
- The Hamiltonian is now _not bounded below in energy_, hence it is _unstable_
### Fermionic quantisation
- Or, inspired by the _Clifford algebra_, use an _anti-commutation relation_:
$$\displaylines{\{\psi_{a}(\boldsymbol{x},t),\psi_{b}^{\dagger}(\boldsymbol{y},t)\}=\delta_{ab}\delta(\boldsymbol{x}-\boldsymbol{y}) \\ \{\psi_{a}(\boldsymbol{x},t),\psi_{b}(\boldsymbol{y},t)\}=0}$$
- Plane wave solution is the _same_:
$$\displaylines{\psi(x)=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2\omega_{p} }}[b_{\boldsymbol{p}}^{s}U^{s}(\boldsymbol{p})\exp(-ipx)+{c_{\boldsymbol{p}}^{s}}^{\dagger}V^{s}(\boldsymbol{p})\exp(ipx)] }$$
- Instead, use the _anti-commutation relations_:
$$\{b_{p}^{s},{b_{p'}^{s'}}^{\dagger}\}=(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')\delta^{ss'} \qquad \{c_{p}^{s},{c_{p'}^{s'}}^{\dagger}\}=-(2\pi)^{3}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')\delta^{ss'} $$
- $c_{p}^{s\dagger}$ is now a _creation operator_

- Manifestation of the _spin-statistics theorem_, where _half/integer_ spin leads to _fermions/bosons_
	- The _representation_ of the Lorentz group will lead to a _bosonic_ or _fermionic_ nature

- The Hamiltonian is now _stable_, with a _lower bound_ on energy:
$$\displaylines{\begin{align}
H&=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}} \omega_{p}({b_{p}^{s}}^{\dagger}b_{p}^{s}-c_{p}^{s}{c_{p}^{s}}^{\dagger}) \\
&=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}} \omega_{p}({b_{p}^{s}}^{\dagger}b_{p}^{s}+c_{p}^{s\dagger}{c_{p}^{s}})-\int  \frac{d^3p}{(2\pi)^{3}}(2\omega_{p})(2\pi)^{3}\delta^{3}(0) 
\end{align}\\ [H,{b_{p}^{s}}^{\dagger}]=\omega_{p}{b_{p}^{s}}^{\dagger} \qquad [H,c_{p}^{s\dagger}]=-\omega_{p}c_{p}^{s\dagger}}$$
- An _opposite sign_ on the _vacuum energy_
	- A theory with 4 _scalar fields_ and a spinor field (balancing degrees of freedom) would set vaccum energy to $0$

- The theory should still be _causal_
	- Observables are only _bilinear_, not _linear_, hence this still holds with anticommutation
$$[\mathcal{O}(x),\mathcal{O}(y)]=0 \quad \text{if }(x-y)^{2}<0$$

## Characteristics of the free theory
### Fock states
- _Normal ordering_ for the operators:
$$:b_{q}c_{q}b_{k}^{\dagger}:=b_{k}^{\dagger}b_{q}c_{q}=b_{q}^{\dagger}c_{q}b_{q}$$
- The _vacuum states_:
$$b_{p}^{s}\ket{0}=c_{p}^{s}\ket{0}=0  $$
- The single particle states:
$$\ket{b}=\sqrt{ 2\omega_{p}}b_{p}^{s\dagger}\ket{0}\qquad \ket{c}=\sqrt{ 2\omega_{p} }c_{p}^{s\dagger}\ket{0}    $$
- Due to _Fermi statistics_:
$$\ket{p_{1}s_{1},p_{2}s_{2}}=b_{p_{1}}^{s_{1}\dagger}b_{p_{2}}^{s_{2}\dagger}\ket{0}=-b_{p_{2}}^{s_{2}\dagger}b_{p_{1}}^{s_{1}\dagger}\ket{0} =-\ket{p_{2}s_{2},p_{1}s_{1}}   $$
### Conserved charges
- From the $U(1)$ internal symmetry: 
$$\displaylines{Q=\sum_{s}\int  \frac{d^3p}{(2\pi)^{3}}(b_{p}^{s\dagger}b_{p}^{s}-c_{p}^{s\dagger}c_{p}^{s}) \\ Q\ket{b}=\ket{b} \qquad Q\ket{c}=-\ket{c}    }$$
- For _angular momentum_, calculated in the _rest frame_:
$$J_{z}\ket{b^{s}}=\pm \frac{1}{2}\ket{b^{s}} \qquad J_{z}\ket{c^{s}}=\pm \frac{1}{2}\ket{c^{s}}  $$
### Fermionic propagator
- Inspect the quantity:
$$\braket{ 0 |\psi_{a}(x)\bar{\psi}_{b}(y)|0  } $$
- Subbing in the [[#Fermionic quantisation|plane wave expansion]]:
$$\begin{align}
\braket{ 0|\psi_{a}(x)\bar{\psi}_{b}(y) |0  }&=(i\cancel{ \partial_{x} }+m)_{ab}\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{2\omega_{p}}\exp[-ip(x-y)]   \\
&=(i\cancel{ \partial_{x} }+m)D(x-y)
\end{align}$$
- Here, $D(x-y)$ is the [[#The Feynman propagator|Feynman propagator]]

- Meanwhile:
$$\braket{0|\bar{\psi}_b(y)\psi_{a}(x)|0} =-(i\cancel{ \partial_{x} }+m)_{ab}D(y-x)$$
- From this, get the _time ordering_ for the Dirac field:
$$T\{\psi(x)\bar{\psi}(y)\}=\begin{cases}
\psi(x)\bar{\psi}(y) &x^{0}>y^{0} \\ -\bar{\psi}(y)\psi(x) &y^{0}>x^{0}
\end{cases}$$
- The _Feynman propagator_:
$$S_{F}(x-y)\equiv \braket{ 0|T\{\psi(x)\bar{\psi}(y)\} | 0 }=(i\cancel{ \partial_{x} }+m)\Delta_{F}(x-y) $$
- As a momentum integral, the Feynman propagator is:
$$S_{F}(x-y)=i \int  \frac{d^4p}{(2\pi)^{4}} e^{-ip\cdot(x-y)} \frac{\gamma \cdot p+m}{p^{2}-m^{2}+i\epsilon} $$

- It is a _Greens function_ for the Dirac equation:
	- Can see from Green's function definition for [[#The Feynman propagator|the Feynman propagator]]
$$(i\cancel{ \partial_{x} }-m)S_{F}(x-y)=i\delta^{4}(x-y) \qquad S_{F}(x-y)(i\overleftarrow{\cancel{ \partial }}_{y} +m)=-i\delta^{4}(x-y)$$
- Wick's Theorem:
$$\overbrace{\psi(x)\bar{\psi}(y)}=T\{\psi(x)\bar{\psi}(y)\} -:\psi(x)\bar{\psi}(y):=S_{F}(x-y)$$

## Interactions: Yukawa theory
- Consider the Lagrangian:
$$\begin{align}
\mathcal{L}_{0}&=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}\mu^{2}\phi^{2}+\bar{\psi}(i\gamma^{\mu}\partial_{\mu}-m)\psi \\
\mathcal{L}_\text{int}&=-\lambda \phi \bar{\psi}\psi
\end{align}$$
- Mass units:
$$[\mathcal{L}]=4\implies [\phi]=1 \qquad [\psi]=\frac{3}{2} \qquad [\lambda ]=0$$
- It is a [[#Couplings|marginal coupling]]

### Nucleon-antinucleon scattering and LSZ
- The _asymptotic states_:
$$\begin{align}
\ket{i,-\infty}&=\sqrt{ 2\omega_{p} }\sqrt{ 2\omega_{q} }b_{p}^{s\dagger}(-\infty)c_{q}^{r\dagger}(-\infty)\ket{\Omega }   \\
\ket{f,+\infty}&=\sqrt{ 2\omega_{p'} }\sqrt{ 2\omega_{q'} }b_{p'}^{s'\dagger}(+\infty)c_{q'}^{r'\dagger}(+\infty)\ket{\Omega }  
\end{align}$$
- The _scattering matrix_:
$$\braket{ f|S | i }=\sqrt{ 2\omega_{p} }\sqrt{ 2\omega_{q} }\sqrt{ 2\omega_{p'} }\sqrt{ 2\omega_{q'} }\braket{0|c_{q'}^{r'}(+\infty)b_{p'}^{s'}(+\infty)b_{p}^{s\dagger}(-\infty)c_{q}^{r\dagger}(-\infty)|\Omega}$$

- Relation between the creation operators:
$$i \int  d^4x\,\bar{\psi}(x)(i\overleftarrow{\cancel{ \partial }}+m)U_{s}(p)\exp(-ipx)=\sqrt{ 2\omega_{p} }(b_{p}^{s\dagger}(+\infty)-b_{p}^{s\dagger}(-\infty)) $$
- And 3 other relations

- With these, the scattering matrix element is:
	- _Left_ of correlation function: _outgoing_ $b$ and _ingoing_ $c^{\dagger}$ (associated with $\psi$)
	- _Right_ of correlation function: _ingoing_ $b^{\dagger}$ and _outgoing_ $c$ (associated with $\bar{\psi}$)
$$\begin{align}
\braket{ f|S|i}= \prod_{i=1}^{4}\,i \int  d^4x_{j} &\left[e^{ip'x_{3}}\bar{U}_{s'}(p')(-i\cancel{ \partial }_{4}+m)\right] \left[e^{-iqx_{2}}V_{r}(q)(-i\cancel{ \partial }_{2}+m)\right] \times \\
&\braket{ \Omega|T\{\bar{\psi}(x_{4})\psi(x_{3})\bar{\psi}(x_{1})\psi(x_{2})\} |  } \times \\
&\left[(i \overleftarrow{\cancel{ \partial }}_{1}+m)U_{s}(p)e^{-ipx_{1}}\right]\left[(i \overleftarrow{\cancel{ \partial }}_{4}+m)\bar{V}_{r'}(q')e^{iq'x_{4}}\right]
\end{align}$$
### Feynman rules in Yukawa Theory
- An _incoming particle_ $U_S(\boldsymbol{p}), b^{\dagger}$ or _antiparticle_ $\bar{V}_{S}(\boldsymbol{p}),c^{\dagger}$ are denoted with _opposite directions_ on a diagram
- Similarly for an _outgoing particle_ $\bar{U}_{S}(\boldsymbol{p}),b$ or _antiparticle_ $\bar{V}_{S}(\boldsymbol{p}),c$

- Each _vertex_ $p_{1} \to p_{2}+p_{3}$ gives a factor:
$$(-i\lambda)(2\pi)^{4}\delta(p_{1}-p_{2}-p_{3})$$
- Each _internal line_, depending on the propagator, give either:
$$\Delta_{\mu}=\int  \frac{d^4p}{(2\pi)^{4}}\, \frac{i}{p^{2}-\mu^{2}+i\epsilon} \qquad \Delta_{m}=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i(\cancel{ p }+m)}{p^{2}-m^{2}+i\epsilon}  $$
- Fermionic propagators are $4\times{4}$ matrices, indices must be _contracted over_ at each vertex
- Swapping _fermion momenta_ requires _changing sign due to fermionic statistics_

- Two diagrams may have _opposite signs_
	- "_Anti-commute_" the before-and-after particles
### Schwinger-Dyson equation in Yukawa theory
- Consider the 4-point function:
$$\braket{ \Omega|T\{\psi(x_{1})\psi(x_{2})\bar{\psi}(x_{3})\bar{\psi}(x_{4})\} |\Omega  }\equiv \braket{ \psi_{1}\psi_{2}\psi_{3}\psi_{4} }  $$
- Consider the _Schwinger-Dyson equation_ in the free theory, consisting of _contractions_
$$(i\cancel{ \partial_{x} }-m)\braket{ \psi(x)\bar{\psi}(x_{1})\dots } =i\sum_{j}\delta(x-x_{j})\dots$$
- For the [[#Propagator|fermion propagators]] $S_{F}$
$$(i\cancel{ \partial_{x} }-m)S_{F}(x-y)=i\delta^{4}(x-y)\qquad S_{F}(x-y)(i\overleftarrow{\cancel{ \partial }}_{y} +m)=-i\delta^{4}(x-y)$$
- Evaluating the 4-point function in the free theory, using _integration by parts_, then gives:
$$\begin{align}
\braket{ \psi_{1}\psi_{2}\bar{\psi}_{3}\bar{\psi}_{4}  }_{0}&=\int  d^4 y\,\delta(y-x_{1})\braket{ \psi_{y}\psi_{2} \bar{\psi}_{3}\bar{\psi}_{4} } \\
&=\int  d^4y\,\,iS_{F}(x_{1}-y)(i\overleftarrow{\cancel{ \partial }}_{y} +m)\braket{ \psi_{y}\psi_{2} \bar{\psi}_{3}\bar{\psi}_{4} }  \\
&=\int  d^4y\,\,iS_{F}(x_{1}-y)(-i\overrightarrow{\cancel{ \partial }}_{y} +m)\braket{ \psi_{y}\psi_{2} \bar{\psi}_{3}\bar{\psi}_{4} } 
\end{align}$$
- Using the Schwinger-Dyson equation, keeping the _order_ of operators:
$$\braket{ \psi_{1}\psi_{2}\bar{\psi}_{3}\bar{\psi}_{4}  }_{0}=S_{F}(x_{1}-x_{4})S_{F}(x_{2}-x_{3})-S_{F}(x_{1}-x_{3})S_{F}(x_{2}-x_{4})$$
- Then, for the _interacting theory_:
$$(i\cancel{ \partial_{x} }-m)\braket{ \psi(x)\bar{\psi}(y) \dots} =-\lambda \braket{ \phi(x)\psi(x)\bar{\psi}(y)\dots } +\{\text{signed contractions}\}$$
### Example: Nucleon scattering

### Example: Nucleon-antinucleon scattering

# Quantum Electrodynamics

## Classical electrodynamics
- Given the _Faraday tensor_:
$$F_{\mu \nu}=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}$$
- The _Lagrangian_:
$$\mathcal{L}=-\frac{1}{4}F_{\mu \nu}F^{\mu \nu}$$
- The _equations of motion_ come from the _Euler-Lagrange equation_ and the _Bianchi identity_
$$\displaylines{\partial_{\mu}\left( \frac{\partial \mathcal{L}}{\partial[\partial_{\mu}A_{\nu}]} \right)=0 \implies \partial_{\mu}F^{\mu \nu}=0\\ \epsilon_{\mu \nu \rho\sigma}\partial^{\mu}F^{\nu \rho}=0\implies \partial_{\lambda}F_{\mu \nu}+\partial_{\mu}F_{\nu\lambda}+\partial_{\nu}F_{\lambda \mu}=0}$$
### Gauge symmetry
- From the Euler-Lagrange equation, inspect the components of $\boldsymbol{A}$
$$\nabla^{2}A_{0}+\nabla\cdot \frac{\partial \boldsymbol{A}}{\partial t}=0\implies A_{0}(x)=\int  d^3x' \frac{\nabla\cdot\partial \boldsymbol{A}(\boldsymbol{x}')/\partial t}{|\boldsymbol{x}-\boldsymbol{x}'|} $$
- $A_{0}$ is _fully determined_ by $\boldsymbol{A}$
- This gives _three degrees of freedom_ in $\boldsymbol{A}$

- The theory is also _gauge symmetric_, meaning it is invariant under the transformation:
$$A_{\mu}\to A_{\mu}+\partial_{\mu}\lambda$$
- This is a _redundancy_ in the system
- Also comes from the fact that the Euler-Lagrange equation is _not invertible_
	- $A_{\mu}=\partial_{\mu}\lambda$ is a _trivial solution_ for any scalar field $\lambda$

- Using _Noether's Theorem_ for the transformation:
$$J^{\mu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}A_{\nu})}\partial_{\nu}\lambda=\partial_{\nu}(\lambda F^{\mu \nu})$$
- As it is a _total derivative_, this leads to _zero conserved charge_

- The redundancy actually leads to an _enlarged phase space_ of solutions
	- It can be visualised with a series of _gauge orbits_, where states _along the same orbit_ can be related by a _gauge transformation_
- One must then _fix the gauge_
	- Pictorally, it _cuts the gauge orbits_, with a representative from each orbit

- The _Lorenz gauge_ (which is _Lorentz invariant_):
$$\partial_{\mu}A^{\mu}=0$$
- Then given _another gauge field_ $A_{\mu}'$ where $\partial_{\mu}(A')^{\mu}=f$, one can always _transform back_ with $A_{\mu}=A_{\mu}'+\partial_{\mu}\lambda$ _given_:
$$\Box\lambda=-f$$
- This is a _nontrivial_ transformation, therefore the Lorenz gauge _is not unique_
	- Does not pick a unique representative from the gauge orbits

- The _Coulomb gauge_:
$$\nabla\cdot \boldsymbol{A}=0$$
- It is _not Lorentz invariant_
- From this, $A_{0}=0$, which _removes another degree of freedom_
- The _remaining_ 2 degrees of freedom are the _polarisation states_ of the photon

## Canonical quantisation of electromagnetism
- Use the _Coulomb gauge_ to get rid of redundancy

### Plane waves and polarisations
- From the Coulomb gauge, the _equations of motion_ give:
$$\Box A_{i}=0$$
- Choose a _massless plane wave solution_
$$A_{\mu}\sim \epsilon_{\mu}\exp(ip_{\mu}x^{\mu}) \qquad p^{2}=0$$
- The Coulomb gauge gives:
$$\epsilon_{0}=0 \qquad \boldsymbol{\epsilon}\cdot \boldsymbol{p}=0$$
- Plane waves also possible in Lorenz gauge, with polarisation defined differently

- There are _two orthonormal basis vectors for a given_ $\boldsymbol{p}$
$$\displaylines{\boldsymbol{\epsilon}_{r}\cdot \boldsymbol{p}=0 \qquad r=1,2 \\ \boldsymbol{\epsilon}_{r}\cdot \boldsymbol{\epsilon}_{s}=\delta_{rs}}$$
- They correspond to _polarisations_ in real space

- The completeness relation:
$$\sum_{r=1}^{2}\boldsymbol{\epsilon}^{i}_{r}(\boldsymbol{p})\boldsymbol{\epsilon}^{j}_{r}(\boldsymbol{p})=\delta^{ij}-\frac{p^{i}p^{j}}{|\boldsymbol{p}|^{2}}$$
- Plane wave _expansion_ with _creation_ and _annihilation_ operators:
$$\boldsymbol{A}(x)=\int  \frac{d^3p}{(2\pi)^{3}} \frac{1}{\sqrt{ 2|\boldsymbol{p}| }} \sum_{r=1}^{2}\boldsymbol{\epsilon}^{r}(a_{p}^{r}e^{-ipx}+a^{r\dagger}_{p}e^{ipx})$$
### Electric field as a canonical momentum
- Define a _canonical momentum_:
$$\pi_{i}=\frac{\partial \mathcal{L}}{\partial \dot{A}_{i}}=-F^{0i}=E^{i}$$
- The Coulomb gauge also implies $\nabla\cdot \boldsymbol{E}=0$

- To comply with the gauge, the commutation relation is:
	- Only using deltas will give $[\nabla\cdot \boldsymbol{A},\nabla\cdot \boldsymbol{E}]\neq 0$
$$\begin{align}
[A_{i}(\boldsymbol{x},t),\pi_{j}(\boldsymbol{y},t)]&=i\left( \delta_{ij}-\frac{\partial_{i}\partial_{j}}{\nabla^{2}} \right)\delta^{3}(\boldsymbol{x}-\boldsymbol{y})  \\
&=i \int  d^3p \left( \delta_{ij}-\frac{p_{i}p_{j}}{|\boldsymbol{p}|^{2}} \right)\exp[i\boldsymbol{p}\cdot(\boldsymbol{x}-\boldsymbol{y})]
\end{align}$$
- This also gives:
$$[\partial_{i}A_{i},\pi_{j}]=0 \qquad [A_{i}(\boldsymbol{x},t),A_{j}(\boldsymbol{y},t)]=0$$
- Then the commutation relation:
$$[a^{r}_{p},a^{s\dagger}_{q}]=(2\pi)^{3}\delta^{rs}\delta^{3}(\boldsymbol{p}-\boldsymbol{q})$$
### Electromagnetic Hamiltonian
- The Hamiltonian is then:
$$H=\int  d^3x \,(\pi^{i}\dot{A}_{i}-\mathcal{L})=\frac{1}{2}\int  d^3x\,(\boldsymbol{E}\cdot \boldsymbol{E}+\boldsymbol{B}\cdot \boldsymbol{B}) $$
- After normal ordering:
$$H=\int  \frac{d^3p}{(2\pi)^{3}}\,|\boldsymbol{p}| \sum_{r=1}^{2}a_{p}^{r\dagger}a_{p}^{r} $$
### Propagator in the Coulomb gauge
- The _Feynman propagator_ in the _Coulomb gauge_:
$$\braket{ 0|T\{A_{i}(x)A_{j}(y)\} |0  }=\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}+i\epsilon} \left( \delta_{ij}-\frac{p_{i}p_{j}}{|\boldsymbol{p}|^{2}} \right)\exp[-ip(x-y)] $$
### Propagator: the Lorentz invariant way
- Deriving the propagator from a more _Lorentz invariant_ way
- The propagator is a _Greens function_ for the equation of motion

- Maxwell:
$$\partial_{\mu}F^{\mu \nu}=J^{\nu}\implies \Box A^{\nu}-\partial_{\mu}\partial^{\nu}A^{\mu}=J^{\nu}$$
- Doing a _Fourier transform_:
$$(-p^{2}+p_{\mu}p^{\nu})A^{\mu}(p)=J^{\nu}(p)$$
- There are solutions with _zero eigenvalue_ (e.g. $p^{\nu}$), hence the operator is _non invertible_
	- This corresponds to the _gauge freedom_, where $\partial^{\mu}\lambda$ is a _trivial solution_

- Instead, add a _Lagrange multiplier_ to the Lagrangian
	- Gauge invariance is _broken_
$$\mathcal{L}=-\frac{1}{4}F_{\mu \nu}F^{\mu \nu}-\frac{1}{2\alpha}(\partial_{\mu}A^{\mu})^{2}$$
- Here, $\alpha$ is an _auxiliary field_ which is _non-propagating_ (constant in spacetime)
- Equation of motion w.r.t. $\alpha$ and $A_{\mu}$ respectively:
$$\displaylines{\partial_{\mu}A^{\mu}=0  \\ \left[ \eta^{\nu\lambda}\Box+\left( \frac{1}{\alpha}-1 \right)\partial^{\nu}\partial^{\lambda} \right]A_{\lambda}=0}$$

- Back to the _Greens function_ in Fourier space:
$$\left[ -\eta^{\nu\lambda}p^{2}-\left( \frac{1}{\alpha}-1 \right)p^{\nu}p^{\lambda} \right]A_{\lambda}(p)=J_{\lambda}(p)$$
- This has an _inverse_:
$$\displaylines{ \hat{\Pi}_{\mu \nu}=-\eta_{\mu \nu}p^{2}-\left( \frac{1}{\alpha}-1 \right)p_{\mu}p_{\nu} \\ \Pi_{\mu \nu}=\left( \hat{\Pi}^{-1} \right)_{\mu \nu}=-\frac{\eta_{\mu \nu}+(\alpha-1)p_{\mu}p_{\nu}/p^{2}}{p^{2}}}$$
- From this _Greens function_, construct the _propagator_:
$$\begin{align}
\braket{ 0|T\{A_{\mu}(x)A_{\nu}(y)\} | 0 } &=i \int  \frac{d^4p}{(2\pi)^{4}}\, e^{-ip(x-y)}\Pi_{\mu \nu} \\ &=-i \int  \frac{d^4p}{(2\pi)^{4}} \frac{1}{p^{2}+i\epsilon} \left( \eta_{\mu \nu}+\frac{(\alpha-1)p_{\mu}p_{\nu}}{p^{2}} \right)e^{-ip(x-y)}
\end{align}$$
- For $\mu,\nu=i,j$ the components _match_ the derivation from the Coulomb gauge

- $\alpha$ is an _unphysical quantity_, hence the $S$ matrix _should not depend on_ $\alpha$
	- $\alpha=1$: Feynman-'t Hooft gauge
	- $\alpha=0$: the Lorenz/Landau gauge (a strong enforcement of the Lorentz group)
	- $\alpha\to \infty$: the unitary gauge (for non-Abelian gauge fields)

## Coupling of light to matter
- Maxwell's equations:
$$\partial_{\mu}F^{\mu \nu}=J^{\nu}\implies \partial_{\mu}\partial_{\nu}F^{\mu \nu}=\partial_{\nu}J^{\nu}=0$$
- The source term is a _conserved current_
	- Often _independent_ of $A_{\mu}$
- Then consider the Lagrangian with coupling:
$$\mathcal{L}=-\frac{1}{4}F^{\mu \nu}F_{\mu \nu}-J^{\mu}A_{\mu}$$
- For a _conserved current_, the _action is still gauge invariant_

### Coupling to fermions
- Consider the [[#Quantum Dirac fields|Dirac Lagrangian]]
$$\mathcal{L}=\bar{\psi}(i\cancel{ \partial }-m)\psi$$
- It has the conserved current from $\psi\to \exp(i\alpha)\psi$
$$j^{\mu}=\bar{\psi}\gamma^{\mu}\psi $$
- Add it to the Lagrangian:
$$\begin{align}
\mathcal{L}&=-\frac{1}{4}F^{\mu \nu}F_{\mu \nu}+\bar{\psi}(i\cancel{ \partial }-m)\psi-ej^{\mu}A_{\mu} \\
&=-\frac{1}{4}F^{\mu \nu}F_{\mu \nu}+\bar{\psi}(i\cancel{ D }-m)\psi
\end{align}$$
- Here, $D_{\mu}$ is the _covariant derivative_:
$$D_{\mu}=\partial_{\mu}+ieA_{\mu }$$
- When making the gauge transformation:
$$\displaylines{A_{\mu }\to \partial_{\mu}\lambda(x) \\ \psi\to \exp(-ie\lambda(x))\psi \qquad \bar{\psi}\to \exp(ie\lambda(x))\bar{\psi}}$$
- From this:
$$D_{\mu}\psi\to \exp(-ie\lambda)D_{\mu}\psi \qquad \bar{\psi}\cancel{ D }\psi\to \bar{\psi}\cancel{ D }\psi$$
- The Lagrangian is _gauge invariant_

- From Noether's theorem, the _conserved charge_ from _gauge symmetry_:
$$Q=\int  d^3x\,F^{0i}\partial_{i}\lambda=-\int  d^3x \,\partial_{i} F^{0i}\lambda$$
- Then setting $\lambda=1$:
$$Q=-e\int  d^3x\,j^{0} $$
- This is a charge associated with a _global symmetry_ of the system
	- It is a _large gauge transformation_ as $\lambda$ does not vanish at infinity

- The _unit of charge_ $e$ is written in terms of _fine structure constant_ $\alpha$:
$$\alpha=\frac{e^{2}}{4\pi \hbar c}\approx \frac{1}{137} \qquad e\approx 0.3$$
### Scalar QED
- Attempt to couple a _complex scalar field_ to electromagnetism
- For it to be _gauge invariant_, the Lagrangian must be in the form:
	- Simply adding $j^{\mu}A_{\mu}$ with $j^{\mu}$ as the current for $U(1)$ symmetry does not make a gauge invariant Lagrangian
$$\displaylines{A_{\mu }\to \partial_{\mu}\lambda(x) \\ \varphi\to \exp(-ie\lambda(x))\varphi \qquad \varphi^{*}\to \exp(ie\lambda(x))\varphi^{*}}$$
$$\mathcal{L}=-\frac{1}{4}F_{\mu \nu}F^{\mu \nu}+D_{\mu}\varphi^{*}D^{\mu}\varphi-m^{2}|\varphi|^{2}$$
- This results in an _extra term_ in the conserved current

- _Minimal coupling_ is the act if _replacing derivatives with covariant derivatives_ when _coupling gauge fields to_ $U(1)$ _symmetry_

### QED Feynman rules

- The Lagrangian in QED:
$$\Lagr=-\frac{1}{4}F^{\mu \nu}F_{\mu \nu}+\bar{\psi}(i\cancel{ D }-m)\psi$$

- _Photon polarisation vectors_ for _external photon lines_:
$$\epsilon^{s}_{\mu}(p)$$
- _Fermions_ (incoming particles and antiparticles):
$$U^{s}(p),\bar{V}^{s}(p)$$

- Each _vertex_ gives a factor of:
$$-ie\gamma^{\mu}(2\pi)^{4}\delta(p_{1}-p_{2}-p_{3})$$
- The photon propagator:
$$\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}+i\epsilon} \left( -\eta_{\mu \nu}+(\alpha-1) \frac{p_{\mu}p_{\nu}}{p^{2}} \right) $$
- The second term _cancels out_ in diagrams

- The _fermion propagator_ (changes sign if swapped):
$$\int  \frac{d^4p}{(2\pi)^{4}} \frac{i}{p^{2}-m^{2}+i\epsilon} (\cancel{ p }+m) $$
- The S-matrix will be in the form:
$$\braket{ f|S-\mathbb{I} | i } \equiv i \mathcal{A}(2\pi)^{4}\delta\left( \sum_{f}p_{f}-\sum_{i}p_{i} \right)$$
- If there is an _internal photon_:
$$\mathcal{A}=A_{\mu \nu}\tilde{\Pi}^{\mu \nu}$$
- _Gauge invariance_ means that the answer must be independent of $\alpha$:
$$A_{\mu \nu}p^{\mu}p^{\nu}=0$$

- If there is an _external photon_:
$$\mathcal{A}=\epsilon^{\mu}_{s}\mathcal{A}_{\mu}$$
- They Lorentz transform as:
$$\mathcal{A}_{\mu}'={\Lambda^{\mu}}_{\nu}\mathcal{A}_{\nu} \qquad p_{\mu}'={\Lambda^{\nu}}_{\mu}p_{\nu}$$
- The _new polarisation vector_, to maintain $\epsilon \cdot p=0$
	- Group theory reason?
$$\epsilon'^{\mu }_{s}={\Lambda^{\mu}}_\nu\epsilon^{\nu}_{s}+cp^{\mu}$$
- The Lorentz invariant _Ward identity_:
$$p^{\mu}\mathcal{A}_{\mu}=0$$
### Spin sums

