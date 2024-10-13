- The _merging_ of _quantum mechanics_ and _special relativity_
- One describes spacetime using _quantum fields_

- The principles of _locality_, _symmetries_, and _renormalisation_ can _constrain possible quantum field theories_ 

>[!Conventions]
>Natural units, where $[\text{L}]=[\text{T}]=[\text{M}]^{-1}$
>$$c=\hbar =1$$
>Minkowski metric:
>$$\eta_{\mu \nu}=\eta^{\mu \nu}=\mathrm{diag}(1,-1,-1,-1)$$

# Classical Field Theory
- See also: [[Classical Field Theory]]

## Recap
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
