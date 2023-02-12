- Poisson and Laplace's equations are [[Partial differential equations]]
- Poisson's Equation is:
$$\nabla^2\Psi=\rho(\bm{x})$$
- $\rho(\bm{x})$ is known as the _source term_
- The source term is often _zero in most regions of space_
- Laplace's Equation is a _special case_ of Poisson's Equation:
$$\nabla^2\Psi=0$$
# Physical origins

## Electrostatics and magnetostatics
- In _electrostatics_, the field is _irrotational_, and can be written using an electric _potential_ $\Phi$:
$$\bm{E}=-\nabla\Phi$$
- Using [[Electromagnetism#Electric flux and Gauss' Law for electrostatics|Gauss' Law]], one gets Poisson's equation:
$$\nabla^2\Phi=-\frac{\rho(\bm{x})}{\epsilon_0}$$
- Laplace's equation is a special case of Poisson's equation, for a charge-free region:
$$\nabla^2\Phi=0$$
- For _magnetostatics_ in a _current-free region_, $\bm{B}=\nabla\psi$, and $\phi$ _also satisfies Laplace's equation_

## Newtonian gravity
- The _gravitational field_ $\bm{g}$ satisfies:
$$\displaylines{\bm{g}=-\frac{GM}{r^2}\hat{r} \\ \nabla\cdot\bm{g}=-4\pi G\rho \\ \nabla\wedge\bm{g}=0}$$
- Therefore, the field can be written as a gradient of the _gravitational potential_:
$$\bm{g}=-\nabla\varphi_g$$
- The gravitational potential _also satisfies Poisson's equation_
$$\nabla^2\varphi_g=4\pi G\rho$$
## Diffusion
- Let $u(\bm{x},t)$ be a _scalar_ quantity that _diffuses_
- The _flux_ of the flow of $u$ is given by _Fick's first law_:
$$\bm{F}=-\kappa\nabla u$$
- From _continuity_, for a _constant_ $\kappa$, with some _source_ $S(\bm{x})$one can obtain the _diffusion equation_:
$$\pd{u}{t}=\kappa\nabla^2 u+S(\bm{x})$$
- For the _steady state_, one then gets:
$$\nabla^2u=-\frac{S(\bm{x})}{\kappa}$$
## Ideal fluid flow
- The _flow_ of a fluid can be described using a _vector field_ of the fluid's _velocity_ $u(\bm{x},t)$
- If the flow is _irrotational_ and _non-viscous_, then the velocity can also be modelled with a _potential_:
$$\bm{u}=\nabla\phi$$
- If the fluid is _incompressible_, then it must have a _uniform density_ $\rho$, and from continuity, the velocity must also be _divergenceless_
- Hence, the potential _also satisfies Laplace's equation_:
$$\nabla^2\phi=0$$
- This is known as _potential flow_

# Separation of variables for Laplace's equation
- In _Cartesian_ coordinates, the Laplacian is:
$$\nabla^2=\pd{^2}{x^2}+\pd{^2}{y^2}+\pd{^2}{z^2}$$
- _Separation of variables_ in Cartesian coordinates means the solution is written in the form:
$$\psi(x,y,z)=X(x)Y(y)Z(z)$$
- The general solution can then be written as a _linear superposition_ of these solutions
- Details and examples: [[Partial differential equations#Separation of variables]]

- In curvilinear coordinates, one needs the form of the Laplacian derived [[Vector calculus in 3-dimensions#Laplacian in orthogonal curvilinear coordinates|here]]

## Plane polar coordinates
- The Laplacian in this coordinate system is given by:
$$\nabla^2=\frac{1}{r}\pd{}{r}\left(r\pd{}{r}\right)+\frac{1}{r^2}\pd{^2}{\phi^2}$$
- Also applies for _cylindrical polar coordinates_ where there is _no $z-$dependence_

- By substituting the solution $\psi=R(r)\Phi(\phi)$ with _separation constant_ $\lambda$:
$$\displaylines{\Phi''=-\lambda\Phi \\ r\frac{d}{dr}\left(r\frac{dR}{dr}\right)=\lambda R}$$
- The solution for $\Phi$ is:
$$\Phi(\phi)=\begin{cases}A+B\phi &\lambda=0 \\ A\cos\left(\sqrt{\lambda}\phi\right)+B\sin\left(\sqrt{\lambda}\phi\right)&\lambda\neq0\end{cases}$$
- For _physical systems_, $\Phi$ is only a _potential_ and is _not necessarilt periodic_
- However, $\Phi'$ is the measurable quantity and  _must be periodic_
- Hence:
$$\displaylines{\lambda=n^2 \hspace{0.5cm},\hspace{0.5cm}n\in\mathbb{Z} \\ \Phi(\phi)=\begin{cases}A+B\phi &n=0 \\ A\cos\left(n\phi\right)+B\sin\left(n\phi\right)&n\neq0\end{cases}}$$
- From this, the solution for $R(r)$ is:
$$R(r)=\begin{cases}C+D\ln r &n=0 \\ Cr^n+D^{-n} & n\neq0\end{cases}$$
- When multiplying the solutions, note that $\nabla(\phi\ln(r))$ is _not periodic_
- Writing the _general linear combination_:
$$\psi(r,\phi)=A_0+B_0\phi+C_0\ln r+\sum_{n=1}^\infty \left(A_nr^n+B_nr^{-n}\right)\cos(n\phi)+\sum_{n=1}^\infty \left(C_nr^n+D_nr^{-n}\right)\sin(n\phi)$$
- One can also _relabel_ the sums:
$$\psi=A_0+B_0\phi+C_0\ln r+\sum_{\substack{n=-\infty \\ n\neq0}}^\infty r^n\left(A_n\cos(n\phi)+B_n\sin(n\phi)\right)$$

## Spherical polar coordinates with cylindrical symmetry
- Cylindrical symmetry: the solution _has no $\theta$-dependence_



# Green's functions
- A general discussion: [[Second order linear ODEs and Green's Functions]]
- The solution to Poisson's equation can be written as:
$$V(\bm{r})=\frac{1}{\epsilon_0}\int G(\bm{r},\bm{r'}) \rho(\bm{r'})d^3\bm{r'}$$
- The _Green's function_ for the Poisson equation is the solution of:
$$\nabla^2G(\bm{r}-\bm{r'})=-\delta(\bm{r}-\bm{r'})$$
	- Poisson's equation can be regained by applying the Laplace operator on both sides
	- The Green's function should satisfy homogeneous boundary conditions



- For free space, using the superposition principle:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\int\frac{\rho(\bm{r'})}{|\bm{r}-\bm{r'}|}\,d^3\bm{r'}$$
- From this, the Green's function is:
$$G(\bm{r},\bm{r'})=\frac{1}{4\pi|\bm{r}-\bm{r'}|}$$
	- Satisfies boundary conditions (goes to zero at infinity)

- The overall solution weighs all the Green's functions with $\rho(\bm{r'})$

# Boundary conditions and uniqueness
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

## Example: Conducting sphere in a uniform field
- Place a dipole in a uniform field
- There is a spherical equipotential surface around the dipole

- The dipole can be replaced by a spherical equipotential surface
- Electric field _polarizes_ the sphere into an induced dipole

## The other uniqueness theorem in electrostatics

# Methods of images
- Uniqueness theorem: as long as boundary conditions are specified, the electric field is _uniquely determined_, and the charge distribution making the field does not affect the solution

- Consider a dipole:
	- Halfway between the charges, there is a plane of zero potential
	- If the plane is replaced with a conducting plane and one charge is removed, _the potential does not change_

- Replacing conducting planes with other charges is the _method of images_

## Charge next to conducting plane
- The conducting plane is an equipotential
- To recreate the boundary condition, place an opposite charge the same distance away on the other side

- Result: induced charges on the conducting plane, strengthening the field between the charge and the field

## Two line charges
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

