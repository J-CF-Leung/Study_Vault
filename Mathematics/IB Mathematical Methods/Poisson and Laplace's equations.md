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
- For _physical systems_, $\Phi$ is only a _potential_ and is _not necessarily periodic_
- However, $\Phi'$ is the measurable quantity and _must be periodic_
- Hence:
$$\displaylines{\lambda=n^2 \hspace{0.5cm},\hspace{0.5cm}n\in\mathbb{Z} \\ \Phi(\phi)=\begin{cases}A+B\phi &n=0 \\ A\cos\left(n\phi\right)+B\sin\left(n\phi\right)&n\neq0\end{cases}}$$
- From this, the solution for $R(r)$ is:
$$R(r)=\begin{cases}C+D\ln r &n=0 \\ Cr^n+D^{-n} & n\neq0\end{cases}$$
- When multiplying the solutions, note that $\nabla(\phi\ln(r))$ is _not periodic_
- Writing the _general linear combination_:
$$\psi(r,\phi)=A_0+B_0\phi+C_0\ln r+\sum_{n=1}^\infty \left(A_nr^n+B_nr^{-n}\right)\cos(n\phi)+\sum_{n=1}^\infty \left(C_nr^n+D_nr^{-n}\right)\sin(n\phi)$$
- One can also _relabel_ the sums:
$$\psi=A_0+B_0\phi+C_0\ln r+\sum_{\substack{n=-\infty \\ n\neq0}}^\infty r^n\left(A_n\cos(n\phi)+B_n\sin(n\phi)\right)$$
- The _boundary conditions_ can be used to find the coefficients
	- The basis functions are _orthogonal_

## Spherical polar coordinates with cylindrical symmetry
- Cylindrical symmetry: the solution _has no $\theta$-dependence_
- The Laplacian in this system, considering the cylindrical symmetry, is:
$$\nabla^2=\frac{1}{r^2}\pd{}{r}\left(r^2\pd{}{r}\right)+\frac{1}{r^2\sin\theta}\pd{}{\theta}\left(\sin\theta\pd{}{\theta}\right)$$
- Let the solution be $\psi=R(r)\Theta(\theta)$
- Separate the equation with _separation constant_ $\lambda$

- For the angular equation, let $u\equiv\cos\theta$
- One finds that it obeys:
$$\frac{d}{du}\left((1-u^2)\frac{d\Theta}{du}\right)+\lambda\Theta=0$$
- This is simply _Legendre's equation_
- For _well-behaved solutions_ at $\theta=0$ or $\pi$, it is required that $\lambda=l(l+1)$
- The resulting angular functions are the [[Special functions and orthogonal relations#Legendre polynomials|Legendre polynomials]] $P_l(u)$

- By substituting $\lambda=l(l+1)$ into the radial equation, one gets:
$$R(r)=A_lr^l+\frac{B_l}{r^{l+1}}$$
- From this, the _full solution_ is:
$$\psi(r,\theta)=\sum_{l=0}^\infty \left(A_lr^l+\frac{B_l}{r^{l+1}}\right)P_l(\cos\theta)$$
## Spherical polar coordinates (general)
- The _angular parts_ require _spherical harmonics_, which depend on two parameters $l$ and $m$
- The _radial part_ remains the same

# Boundary conditions and uniqueness
- Let the boundary surface be $S$

- _Dirichlet_ boundary conditions: specify the value over a boundary
$$\Psi(\bm{x})\Big|_S=f(\bm{x})$$
- _Neumann_ boundary conditions: normal derivative is specified over the boundary
$$\pd{\Psi}{\hat{\bm{n}}}\Bigg|_S=\hat{\bm{n}}\cdot\nabla\Psi=f(\bm{x})$$
- _Cauchy/mixed_ boundary conditions: the value or normal derivative is specified over the boundary

- _Conditions_ for determining a solution to Poisson's equations: 
	- _Either_ Dirichlet or Neumann boundary conditions are specified (A part of the surface can be at infinity)
	- Overdetermined if both are specified

- Examples:
	- Unbounded system: solution _tends to zero at infinity_
	- Conductor in electrostatics: potential must be _constant over the surface_

- It can be proven that if a solution _satisfies Dirichlet boundary conditions_, it must be _unique_
	- Let there be _two soloutions_, $\Psi_1$ and $\Psi_2$, with $\Psi\equiv\Psi_1-\Psi_2$
	- It can be shown that $\nabla\Psi=0$ everywhere, hence $\Psi=0$ everywhere since it must be 0 at the boundary
- For _Neumann_ boundary conditions, it is _unique up to an additive constant_

## Example: Conducting sphere in a uniform field
- Place a dipole in a uniform field
- There is a _spherical equipotential surface_ around the dipole

- The dipole can be _replaced by a spherical conductive shell_
- Electric field _polarizes_ the sphere into an induced dipole

## The other uniqueness theorem in electrostatics

# Green's functions
- A general discussion: [[Second order linear ODEs and Green's Functions]]
- Relies on [[Dirac Delta Function#Higher dimension Delta functions|higher dimensional Delta Functions]]
- Let the _Green's function_ satisfy, for $\bm{r}$ in the volume $V$:
$$\nabla_x^2G(\bm{x},\bm{x}')=\delta^3(\bm{x}-\bm{x}') $$
- If the above equation _is satisfied for all space_, then $G(\bm{x},\bm{x}'')$ is known as the _fundamental solution_

- The Green's function _must also satisfy the boundary conditions_
- _Dirichlet_ boundary conditions:
$$G(\bm{x},\bm{x}')\big|_S=0$$
- _Neumann_ boundary conditions:
$$\pd{G}{n}\Bigg|_S=\frac{1}{A}\to0$$
- $A=\oint dS$ is the _surface area_, which can _tend to infinity_

## Fundamental solution in 3D
- One requires that $G\to0$ as $|\bm{r}|\to\infty$
- From the [[Dirac Delta Function#Higher dimension Delta functions|definition of the 3-dimensional Delta Function]]:
$$\nabla_x^2G(\bm{x},\bm{x}')=\delta^3(\bm{x}-\bm{x}')=\frac{1}{4\pi}\nabla_x\cdot\left(\frac{\bm{x}-\bm{x}'}{|\bm{x}-\bm{x}'|^3}\right)$$
- From this, it can be deduced that:
$$G(\bm{x},\bm{x'})=-\frac{1}{4\pi}\frac{1}{|\bm{x}-\bm{x}'|}$$
- Therefore, from the _uniqueness theorem_, the solution to Poisson's equation is:
$$\displaylines{\nabla^2\Phi=\rho(\bm{x}) \\ \Phi(\bm{x})=\int -\frac{1}{4\pi}\frac{\rho(\bm{x})}{|\bm{x}-\bm{x}'|}\,d^3\bm{x}}$$

## Fundamental solution in 2D
- One requires that $G$ vanishes _on some circle around_ $\bm{x}'$, or $|\nabla G|\to0$ as $|\bm{r}|\to\infty$
- With a similar proof to 3D:
$$G(\bm{x},\bm{x}')=\frac{1}{2\pi}\ln|\bm{x}-\bm{x'}|+\text{const.}$$
 
# Method of images
- Uniqueness theorem: If a solution _satisfies the boundary conditions_, it must be the _only solution_
- Trick: Add an _image source_ to satisfy the boundary conditions

- _Dirichlet_ conditions: A source with _opposite sign_ (i.e. a _sink_)
	- Example: Conductor, wall of _constant temperature_
- _Neumann_ conditions: A source with _same sign_
	- Example: _Insulating_ wall

## Examples: half-spaces and quarter planes

### 3D half-space with Dirichlet boundary conditions
- Consider a _half-space_ in $\mathbb{R}^3$ with a boundary at $z=0$, and consider $x>0$
- The Green's Function must satisfy:
$$\displaylines{\nabla^2G=\delta^3(\bm{x}-\bm{x}') \\ G(z=0)=0 \\ G(|\bm{r}|\to\infty)=0}$$
- Trick: _remove boundary_ and _add an image source_ at:
$$\bm{x''}=(x',y',-z')$$
- The Green's function then satisfies:
$$\displaylines{\nabla_x^2G=\delta^3(\bm{x}-x')-\delta^3(\bm{x}-\bm{x}'')\\G=-\frac{1}{4\pi}\left(\frac{1}{|\bm{x}-\bm{x'}|}-\frac{1}{|\bm{x}-\bm{x}''|}\right)}$$
- This scales as $1/r^2$, like a _dipole_

### 3D half-space with Neumann boundary conditions
- The Green's function must satisfy:
$$\displaylines{\nabla^2G=\delta^3(\bm{x}-\bm{x}') \\ \pd{G}{z}(z=0)=0 \\ G(|\bm{r}|\to\infty)=0}$$
- In this case, the Green's Function is:
$$G(\bm{x},\bm{x}')=\frac{1}{4\pi}\left(\frac{1}{|\bm{x}-\bm{x'}|}+\frac{1}{|\bm{x}-\bm{x}''|}\right)$$

### 2D quarter-plane with Dirichlet boundary conditions
- The Green's function must satisfy:
$$\displaylines{\nabla^2G=\delta^3(\bm{x}-\bm{x}_0) \\ G(x=0)=G(y=0)=0 \\ G(|\bm{r}|\to\infty)=0}$$
- To satisfy all boundary conditions, _three images_ are required:
$$\displaylines{\bm{x}_1=(-x_0,y_0) \hspace{1cm} \bm{x}_2=(x_0,-y_0) \hspace{1cm} \bm{x}_3=(-x_0,-y_0) \\ G(\bm{x},\bm{x}_0)=\frac{1}{2\pi}\ln\frac{|\bm{x}-\bm{x}_0||\bm{x}-\bm{x}_3|}{|\bm{x}-\bm{x}_1||\bm{x}-\bm{x}_2|}}$$
- The _constant is zero from boundary conditions_

### Image in a sphere
- Solving for potential _inside a sphere_, for range $r<a$
- Dirichlet boundary conditions for a _sphere_:
$$\begin{aligned}\nabla^2G=\delta^3(\bm{x}-\bm{x}') \hspace{1cm}\text{for}\hspace{0.5cm}r<a \\ G=0\hspace{1cm}\text{for} \hspace{0.5cm}r=a\end{aligned}$$

- This is satisfied by placing the _image point_ at:
$$\bm{x}''=\frac{a^2}{r'^2}\bm{x}'$$
- The _strength_ that works is $-a/r'$
- Hence, the Green's function is:
$$G=-\frac{1}{4\pi}\left(\frac{1}{|\bm{x}-\bm{x}'|}-\frac{a}{r'}\frac{1}{|\bm{x}-\bm{x}''|}\right)$$
- This also works for finding potential _outside the sphere_

## In electrostatics
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

# Integral solution to Poisson's equation
- Green's Functions can be used to find the solution for _any arbitrary source distribution_, not just point sources
- For this, one needs _Green's identity_:
$$\int_V(\Phi\nabla^2\Psi-\Psi\nabla^2\Phi)\,dV=\oint_S(\Phi\nabla\Psi-\Psi\nabla\Phi)\cdot\,d\bm{S}\equiv\oint_S\left(\Phi\pd{\Psi}{n}-\Psi\pd{\Phi}{n}\right)\,dS$$
- For any _smooth_ functions $\Phi$ and $\Psi$, in any closed volume $V$ with surface $S$

- 2-dimensional version:
$$\int_S(\Phi\nabla^2\Psi-\Psi\nabla^2\Phi)\,dA=\oint_C\left(\Phi\pd{\Psi}{n}-\Psi\pd{\Phi}{n}\right)\,dl$$
## Dirichlet boundary conditions
- Let $\Phi$ satisfy Poisson's equation for source term $\rho(\bm{x})$ with boundary condition:
$$\begin{aligned}\nabla^2\Phi=\rho(\bm{x}) \hspace{1cm}\text{for }\bm{x} \text{ in }V\\ \Phi(\bm{x})=f(\bm{x})\hspace{1cm}\text{for }\bm{x} \text{ on }S\end{aligned}$$


## Neumann boundary conditions
