- In the _elastic region_ of a body, any _deformation is reversible_
- Opposite: _plastic region_

## Young's modulus and Poisson's ratio
- For _small elastic displacements_ of a body with original length $l$ and cross-sectional area $A$ obeying _Hooke's law_, the force $F$ required for deformation $\delta l$ is:
$$F=EA\frac{\delta l}{l}$$
- Here, $E$ is _Young's modulus_, which is _an intrinsic property of the material_

- The Young's modulus can be defined as the _ratio between stress and strain_:
$$\frac{F}{A}=E\frac{\delta l}{l}$$

- An _extension_ in one direction will result in a _compression_ in others:
![[Poisson's ratio.png]]
- Here, $\sigma$ is _Poisson's ratio_
	- Usually _positive_
	- A _negative_ Poisson's ratio will mean expansion in all directions

- For an _isotropic_ material, its elastic properties are _completely determined by_ $E$ and $\sigma$
- This includes all other elastic behaviour, such as _shear_ and _bulk_ behaviour

- Let there be a cube of material with _stresses_ $(\tau_1,\tau_2,\tau_3)$ producing _strains_ $(e_1,e_2,e_3)$
	- Consider stresses _normal to the plane_
![[Cube elastic stresses.png]]
- The stresses are _balanced on opposite sides_ so the body is in _equilibrium_
- A stress $(\tau_1,0,0)$ produces strains such that $E(e_1,e_2,e_3)=\tau_1(1,-\sigma,-\sigma)$
- Adding the strains and compressions for a _general stress pattern_:
$$\displaylines{Ee_1=+\tau_1-\sigma\tau_2-\sigma\tau_3 \\ Ee_2=-\sigma\tau_1+\tau_2-\sigma\tau_3 \\Ee_3=-\sigma\tau_1-\sigma\tau_2+\tau_3}$$

## Bulk modulus
- Consider an isotropic medium with _pressure_ $P$:
$$\tau_1=\tau_2=\tau_3=P$$
- Applying the _constitutive relations_:
$$e_1=e_2=e_3=-\frac{P(1-2\sigma)}{E}$$
- Defining the _bulk_ modulus $B$ such that:
$$\displaylines{P\equiv -B\frac{\delta V}{V} \\ B=\frac{E}{3(1-2\sigma)}}$$
- For the medium to be _stable_, $\sigma<1/2$

## Shear modulus
- Now consider stresses _applied parallel to a plane_:
![[Shear stresses.png]]
- The stresses must be _symmetric_, meaning $\tau_{xy}=\tau_{yx}$, so the body is _in equilibrium_
- The _shear stresses_ produce a _shear strain_, defned by a _shear angle relative to the undeformed body_

- A shear $\tau$ can be produced by a _combination of tension and compression_, with
$$\tau_1=-\tau_2=\tau$$
	- Consider a _unit cube_, with _projected_ shear force $\tau/\sqrt{2}$ on a side with length $1/\sqrt{2}$
	- Therefore, on that "inner side", it _expriences a shear_ of $\tau$

- The _strain_ is given by $Ee_1=\tau_1-\sigma\tau_2=\tau(1+\sigma)$
![[Shear strain construction.png|300]]
- From some geometry, the _shear angle_ is $2\theta=2e_1$
- Hence, the _shear modulus_ $G$ is:
$$G=\frac{E}{2(1+\sigma)}$$
- For _stability_, $\sigma>-1$

## Formal definition of stress
- _Stress_ is the _force per unit area transmitted across planes_
- If there is a force $d\bm{F}$ across an area of $d\bm{S}$, then stress is:
$$d\bm{F}=\dunderline{\bm{\tau}}\cdot d\bm{S}$$
- As a matrix, the stress is:
$$\begin{pmatrix}\tau_{xx} & \tau_{xy} & \tau_{xz} \\ \tau_{yx} & \tau_{yy}& \tau_{yz} \\ \tau_{zx} & \tau_{zy} & \tau_{zz} \end{pmatrix}$$
- $\tau_{ij}$ is the force per unit area in the $i-$direction in the $j-$plane
- The tensor is _symmetric_, $\tau_{ij}=\tau_{ji}$ such that the body is in _equilibrium_

- For an appropriate choice of _axes_, the stress tensor can be made _diagonal_, expressed in terms of _components_ $(\tau_1,\tau_2,\tau_3)$

## Formal definition of strain
![[Strains.png]]
- Consider the local distortion of a medium from $\bm{x}=(x,y,z)$ to $\bm{x}+\bm{X}(\bm{x})=(x+X,y+Y,z+Z)$
- The derivatives of $\bm{X}$ contain information about the _strain_

- The _normal strains_ are:
$$e_{ii}=\pd{X_i}{x_i}$$
- The _shear angle_ in the $i-j$ plane is defined as _half of the strain_ $e_{ij}$:
$$e_{ij}=e_{ji}=\frac{1}{2}\left(\pd{X_i}{x_j}+\pd{X_j}{x_i}\right)$$
- An _antisymmetric_ addition of the partial derivatives is simply a component of $\nabla\wedge \bm{X}$, hence it is a _rotation_
- Therefore, the _strain tensor_ is _symmetric_:
$$\dunderline{\bm{e}}=\begin{pmatrix}e_{xx} & e_{xy} & e_{xz} \\ e_{yx} & e_{yy}& e_{yz} \\ e_{zx} & e_{zy} & e_{zz} \end{pmatrix}$$
- The distortion $\delta\bm{X}$ in direction $\delta\bm{x}$ can be written as:
$$\delta\bm{X}=\dunderline{\bm{e}}\cdot\delta\bm{x}$$
- Since this tensor is symmetric, it can also be _diagonalised_
- If the medium is _isotropic_, the axes are the _same ones that diagonalise stress_