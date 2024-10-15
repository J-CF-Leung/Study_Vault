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
$$\phi'(x)=\phi(\Lambda^{-1} x)$$
- This represents a _scalar field_ $\phi$


- Alternatively, use the representation:
$$D[{\Lambda^{\mu}}_{\nu}]={\Lambda^{\mu}}_{\nu}$$
- This gives _vector fields_
- Example: the _Maxwell field_ $A^{\mu}=(\phi, \boldsymbol{A})$
$$A^{\mu}(x)\to A'^{\mu}={\Lambda^{\mu}}_{\nu}A^{\nu}(\Lambda^{-1}x)$$
- Or:
$$\partial_{\mu}\phi \to \partial_{\mu}\phi'=({\Lambda^{\mu}}_{\nu})^{-1}\partial_{\nu}\phi(\Lambda^{-1}x)$$

- Example: the _Klein Gordon Lagrangian_ is invariant
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2} \quad, \quad \mathcal{L}'=\mathcal{L}$$
- From $\det(\Lambda)=1$, the spacetime element $d^{4}x$ is constant, hence _action is invariant_