>[!quote]
>"ceiiinosssttuv"
>"Ut tensio, sic vis"
>-Robert Hooke

# Fundamental equations
- In the _elastic region_ of a body, any _deformation is reversible_
- Opposite: _plastic region_
	- [[Plastic deformation]]

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
- These are the _constitutive relations_ of the body

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
- Consider the _local distortion_ of a medium from $\bm{x}=(x,y,z)$ to $\bm{x}+\bm{X}(\bm{x})=(x+X,y+Y,z+Z)$
- The derivatives of $\bm{X}$ contain information about the _strain_

- The _normal strains_ are:
$$e_{ii}=\pd{X_i}{x_i}$$
- The _off-diagonal strain_ $e_{ij}$ is defined as _half of the shear angle_:
$$e_{ij}=e_{ji}=\frac{1}{2}\left(\pd{X_i}{x_j}+\pd{X_j}{x_i}\right)$$
- An _antisymmetric_ addition of the partial derivatives is simply a component of $\nabla\wedge \bm{X}$, hence it is a _rotation_
- Therefore, the _strain tensor_ is _symmetric_:
$$\dunderline{\bm{e}}=\begin{pmatrix}e_{xx} & e_{xy} & e_{xz} \\ e_{yx} & e_{yy}& e_{yz} \\ e_{zx} & e_{zy} & e_{zz} \end{pmatrix}$$
- The distortion $\delta\bm{X}$ in direction $\delta\bm{x}$ can be written as:
$$\delta\bm{X}=\dunderline{\bm{e}}\cdot\delta\bm{x}$$
- Since this tensor is symmetric, it can also be _diagonalised_
- If the medium is _isotropic_, the axes are the _same ones that diagonalise stress_

## Relating stress and strain, and Lamé's constants
- By using the _constitutive relations_, one can express $\tau_1$ as:
$$\tau_1=\frac{E}{(1+\sigma)(1-2\sigma)}[(1-\sigma)e_1+\sigma e_2+\sigma e_3]$$
- One can define _Lamé's first constant_ as:
$$\lambda\equiv \frac{E\sigma}{(1+\sigma)(1-2\sigma)}$$
- Hence:
$$\tau_1=\lambda(e_1+e_@+e_3)+2Ge_1$$
- There is part of the stress _proportional to strain_, and an additional _isotropic pressure_
- So, one can write:
$$\dunderline{\bm{\tau}}=\lambda\text{Tr}(\dunderline{\bm{e}})\dunderline{\bm{I}}+2G\dunderline{\bm{e}}$$

- In axes that are _not principal but still orthogonal_, the _normal components_ are related by:
$$Ee_{xx}=\tau_{xx}-\sigma\tau_{yy}-\sigma\tau_{zz}$$
- The off-diagonal _shear strains_ are related to the shear stresses by:
$$G(2e_{xy})=\tau_{xy}$$
- Lamé's first constant can also be written as:
$$\lambda=B-\frac{2}{3}G$$

# Material behaviour

## Energy stored in elastic strain
- Cosider a volume $(\Delta x, \Delta y, \Delta z)$
- Consider the _net distortion along the_ $x-$face, $\Delta x(e_{xx},e_{yx},e_{zx})$
- The _force_ along this face is $\Delta y \Delta z(\tau_{xx},\tau_{yx},\tau_{zx})$
- As the force is _proportional to displacement_, adding up _forces in all faces_:
$$U=\frac{1}{2}\Delta V(\tau_{xx}e_{xx}+\tau_{yy}e_{yy}+\tau_{zz}e_{zz}+2\tau_{xy}e_{xy}+2\tau_{xz}e_{xz}+2\tau_{yz}e_{yz})$$
- In terms of the _principal axes_:
$$U=\frac{1}{2}\Delta V(\tau_1 e_1+\tau_2e_2+\tau_3e_3)$$
- The elastic energy _per unit volume_ in a linear elastic medium can then be written as:
$$\begin{aligned}U(\dunderline{\bm{e}})&=\frac{1}{2}\left[\left(B-\frac{2}{3}G\right)(e_1+e_2+e_3)^2+2G\left(e_1^2+e_2^2+e_3^2\right)\right] \\ &=\frac{1}{2}\left[\lambda\text{Tr}(\dunderline{\bm{e}})+2G\text{Tr}(\dunderline{\bm{e}}^2)\right] \end{aligned}$$
## Beam bending
![[Beam bending parameters.png]]

- Let there be some _load per unit length_ $W(x)$, causing some overall _displacement_ $\eta(x)$ in the beam
	- Only consider _vertical loads_, meaning _no compressive or stretching forces_
	- For those, see [[#Buckling]] or the bending of _elastica_
- At some width across the beam, there is a _neutral plane_, where there is _no compression or tension_
- Then there is some _radius of curvature_ $\mathcal{R}=dx/d\theta$
- The _longitudinal strain_ can then be written as:
$$e_{xx}=\frac{z}{\mathcal{R}}\approx z\frac{d^2\eta}{dx^2}$$

- There is a _total bending moment_ $M(x)$ that can be written as:
$$M(x)=-EI\frac{d^2\eta}{dx^2}$$
- This is a moment _from the bending itself, not from external forces_
- Here, $I$ is the _second moment of area_, given by:
$$I=\int z^2\,dy\,dz$$

- At the same time, there is a _shear force_ $S$ in the beam to _maintain equilibrium_
- Also taking the _external load_ $W$ into account:
$$S=\frac{dM}{dx}\hspace{1cm} W=-\frac{dS}{dx}$$
- This can then be combined into:
$$W=EI\frac{d^4\eta}{dx^4}$$

- To solve for the deflection $\eta(x)$, one needs the proper _boundary conditions_:
	- The shear force _must vanish at the edge of the rod_, where $\eta'''=0$
	- _Free end_: there is _no force or couple_, hence $\eta''=\eta'''=0$
	- _Cantilever_: Force and coupled used to _maintain_ $\eta$ and $\eta'$ (usually at $0$)
	- _Hinge_: Force without couple, hence $\eta'\neq0$ but $\eta''=0$

### Reciprocity
![[Beam bending reciprocity.png|500]]
- Consider two situations:
	- A _load_ $F$ applied at $P$, causing a _deflection_ at $Q$, $\eta_{QP}$
	- A _load_ $F$ applied at $Q$, causing a _deflection_ at $P$, $\eta_{PQ}$

- Assume _linearity_, and that the deflections are _additive_ from different loads
- Consider _work done_ when applying $F$ at $Q$ first, then $P$:
$$W_{QP}=F\left(\frac{1}{2}\eta_{PP}+\frac{1}{2}\eta_{QQ}+\eta_{QP}\right)$$
- Then, consider applying at $P$ first, then $Q$:
$$W_{QP}=F\left(\frac{1}{2}\eta_{PP}+\frac{1}{2}\eta_{QQ}+\eta_{PQ}\right)$$

- Hence:
$$\eta_{QP}=\eta_{PQ}$$

## Buckling
- Consider a column being _compressed_ by a force $F$ on its two ends:
![[Buckled beam.png|600]]
- Set the _boundary conditions_ as:
$$\eta(0)=\eta(L)=0$$

- It can be shown that the _torque_ at each point _from the applied force_ is $-F\eta$
- Balancing it with the _bending moment_:
$$EI\frac{d^2\eta}{dx^2}=-F\eta$$
- The solutions to this are:
$$\displaylines{\eta=\eta_0\sin kx \\ k=\sqrt{\frac{F}{EI}}=\frac{n\pi}{L}}$$

- From this, the beam _buckles_ and take a _sinusoidal shape_ at:
$$F_\text{crit}=\frac{EI\pi^2}{L^2}$$
- At $F<F_\text{crit}$, there is no solution _except_ $\eta(x)=0$
	- The rod can _oscillate_ stably around the $n=0$ shape
- When $F=F_\text{crit}$, there is suddenly an _additional solution_ for $n=1$, which the rod can take the shape of once given a _perturbation_ in either direction
	- $n=0$ is a _neutral equilibrium_, and the rod can undergo a _zero-frequency motion_ towards $n=1$
- Once $F>F_\text{crit}$, $n=0$ becomes _unstable_, and the _arched state is a stable equilibrium_

- Consider the [[Classical Thermodynamics#Thermodynamic potentials|free energy]] of the rod $𝔙(\eta_0)$ by subtracting the _work done_ from the _total elastic energy_, it can be found to be:
$$𝔙(\eta_0)=\left(\frac{\pi\eta_0}{2L}\right)^2L\left[(F_\text{crit}-F)+\frac{1}{4}F_\text{crit} \left(\frac{\pi\eta_0}{2L}\right)^2 \right]+O\left[F_\text{crit}L\left(\frac{\pi\eta_0}{2L}\right)^6\right]$$
![[Elasticity bifurcation.png]]
- At $F_\text{crit}$, the number of equilibria _increases_ from one to three
- This is known as the _bifurcation of equilibria_

- If the beam was given _lateral stabilising forces_, solutions for higher $n$ can be formed, with $F=n^2F_\text{crit}$
	- In most cases, without stabilising forces, the beam _fails_ before it buckles to form those shapes

- Depending on the _boundary conditions_ (e.g. clamping), the beam can take different (not exactly sinusoidal) shapes

# Dynamics
- Consider a _volume element_ $(\delta x,\delta y, \delta z)$
- Considering _all faces_, the _net force in the $x-$direction_ is:
$$F_x=\Delta V \left(\pd{\tau_{xx}}{x}+\pd{\tau_{xy}}{y}+\pd{\tau_{xz}}{z}\right)$$
- Therefore, the _equation of motion_ is:
$$\displaylines{\rho\pd{^2X_i}{t^2}=\sum_j \pd{\tau_{ij}}{x_j} \\ \rho\pd{^2\bm{X}}{t^2}=\nabla\cdot\dunderline{\bm{\tau}}}$$
- Using the [[#Relating stress and strain, and Lamé's constants|relation between stress and strain]]:
$$\rho\pd{^2\bm{X}}{t^2}=\nabla\cdot\dunderline{\bm{\tau}}=\left(B+\frac{1}{3}G\right)\nabla(\nabla\cdot\bm{X})+G\nabla^2\bm{X}$$
## Elastic waves
- Substitute a _normal mode solution_:
$$\bm{X}=(X_0,Y_0,Z_0)\exp[i(\omega t-kx)]$$
