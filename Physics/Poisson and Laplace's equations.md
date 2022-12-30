## Poisson and Laplace's equations
### Electrostatics
- Using [[Electromagnetism#Electric flux and Gauss' Law for electrostatics|Gauss' Law]] and the definition of electric potential $\bm{E}=-\nabla V$, one gets Poisson's equation:

$$\nabla^2V=-\frac{\rho}{\epsilon_0}$$
- Laplace's equation is a special case of Poisson's equation, for a charge-free region:
$$\nabla^2V=0$$
### Newtonian gravity
- The _gravitational field_ $\bm{g}$ satisfies:
$$\displaylines{\bm{g}=-\frac{GM}{r^2}\hat{r} \\ \nabla\cdot\bm{g}=-4\pi G\rho \\ \nabla\wedge\bm{g}=0}$$
- Therefore, the field can be written as a gradient of the _gravitational potential_:
$$\bm{g}=-\nabla\varphi_g$$
- The gravitational potential _also satisfies Poisson's equation_
$$\nabla^2\varphi_g=4\pi G\rho$$


## Green's functions
- The solution to Poisson's equation can be written as:
$$V(\bm{r})=\frac{1}{\epsilon_0}\int G(\bm{r},\bm{r'}) \rho(\bm{r'})d^3\bm{r'}$$
- The Green's function for the Poisson equation is the solution of:
$$\nabla^2G(\bm{r}-\bm{r'})=-\delta(\bm{r}-\bm{r'})$$
	- Poisson's equation can be regained by applying the Laplace operator on both sides
	- The Green's function should satisfy homogeneous boundary conditions
- [[Second order linear ODEs and Green's Functions]]

- For free space, using the superposition principle:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\int\frac{\rho(\bm{r'})}{|\bm{r}-\bm{r'}|}\,d^3\bm{r'}$$
- From this, the Green's function is:
$$G(\bm{r},\bm{r'})=\frac{1}{4\pi|\bm{r}-\bm{r'}|}$$
	- Satisfies boundary conditions (goes to zero at infinity)

- The overall solution weighs all the Green's functions with $\rho(\bm{r'})$

## Boundary conditions and uniqueness
- Necessary conditions for uniqueness in 1D:
	- Potential at each end of an interval OR
	- Potential and its derivative at one end OR
	- potential at one end, derivative at the other

- _Dirichlet_ boundary conditions: specify the value over a boundary
- _Neumann_ boundary conditions: normal derivative is specified over the boundary
- _Cauchy/mixed_ boundary conditions: the value or normal derivative is specified over the boundary

- Conditions for a solution to Poisson's equations: 
	- _Either_ Dirichlet or Neumann boundary conditions are specified (A part of the surface can be at infinity)
	- Overdetermined if both are specified
	- For Neumann, it is undetermined to within an additive constant ($\bm{E}$ unchanged)

- Unbounded system: solution tends to zero at infinity
- Conductor: potential must be constant over the surface

- For Poisson's equation, the solution that satisfies the boundary conditions is unique

### Example: Conducting sphere in a uniform field
- Place a dipole in a uniform field
- There is a spherical equipotential surface around the dipole

- The dipole can be replaced by a spherical equipotential surface
- Electric field _polarizes_ the sphere into an induced dipole

## Method of images
- Uniqueness theorem: as long as boundary conditions are specified, the electric field is _uniquely determined_, and the charge distribution making the field does not affect the solution

- Consider a dipole:
	- Halfway between the charges, there is a plane of zero potential
	- If the plane is replaced with a conducting plane and one charge is removed, _the potential does not change_

- Replacing conducting planes with other charges is the _method of images_

### Charge next to conducting plane
- The conducting plane is an equipotential
- To recreate the boundary condition, place an opposite charge the same distance away on the other side

- Result: induced charges on the conducting plane, strengthening the field between the charge and the field

### Two line charges
- Consider two lines with opposite charge, where the distances to each are $r_1$ and $r_2$
- From the superposition principle, the potential from these two line charges is:
$$V(\bm{r})=\frac{\lambda}{2\pi\epsilon_0}\ln{\frac{r_2}{r_1}}$$
- Equipotential surfaces are cylinders where $r_2/r_1$ is constant 
- The centre of the cylinder is _not_ at the line charge
- Let the radius of the cylinder be $a$, and the distances from the centre to each charge be $b$ and $c$
- These lengths obey $a^2=bc$
- The potentials of these surfaces is:
$$V(\bm{r})=\frac{\lambda}{2\pi\epsilon_0}\ln\frac{a}{b}$$
- Symmetry plane at zero potential: cylinder with infinite radius


- When considering two cylinders of radius $a$, replace them with line charges with various distances satisfying the conditions above