#IB_Natsci 
- Typical independent variables: $x,y,z,t$
- Order: power of highest derivative
- Linearity: to the first degree in all independent variables and derivatives

# Linear second-order PDEs
- The most general form of a linear second-order PDE with two variables is:
$$\displaylines{L\psi(x,y)=g(x,y) \\ L\psi\equiv a(x,y)\pd{^2\psi}{x^2}+b(x,y)\pd{^2\psi}{x\partial y} +c(x,y)\pd{^2\psi}{y^2}+d(x,y) \pd{\psi}{x}+e(x,y)\pd{\psi}{y}+f(x,y)\psi}$$
- If $g=0$, the equation is _homogeneous_
- Can be generalised to more variables

- Consider the case where _the coefficients are constant_

- $L$ is a _linear operator_ since:
$$L(\alpha\psi+\beta\phi)=\alpha L\psi+\beta L\psi$$

- Principle of superposition:
	- If the equation is homogeneous, and both $\phi$ and $\psi$ are solutions, $\alpha\psi+\beta\phi$ is a solution
	- If a _particular integral_ $\psi_p$ satisfies the inhomogeneous equation, and the _complementary solution_ $\psi_c$ satisfies the homogeneous one, $\alpha\psi_c+\psi_p$ satsfies the inhomogeneous equation

## Example
- [[Fundamentals of quantum mechanics#The Schrödinger wave equation|The Schrödinger wave equation]]

- The wave equation:
$$\pd{^2y}{t^2}=v^2\nabla^2y$$
	- The physics: [[Waves]]

- [[Electromagnetism|Maxwell's equations]]
	- Can be shown that $\bm{E}$ and $\bm{B}$ satisfy the three-dimensional wave equation

- [[Poisson and Laplace's equations]]
	- Applies to both electrostatics and Newtonian gravity

- Diffusion equation for an inert chemical:
	- Let there be a _chemical mass source_ $Q(\bm{r},t)$ _per unit time per unit volume_
	- The mass _concentration_ is $C(\bm{r},t)$
	- The material _flux_ is $\bm{q}(\bm{r},t)$ 
	- Consider the chemical _flowing out of a volume_ during time interval $\delta t$:
	$$\left(\iint_S \bm{q}\cdot d\bm{S}\right)\delta t=-\frac{d}{dt}\left(\iiint_\mathcal{V} C\,dV\right)\delta t+\left(\iiint_\mathcal{V} Q\,dV\right)\delta t$$
	- Using the divergence theorem, and seeing that this is true for any volume:
	$$\pd{C}{t}=-\nabla\cdot \bm{q}+Q$$
	- The _empirical law_ for diffusion is _Fick's Law_:
	$$\bm{q}=-D\nabla C$$
	- $D$ is the _diffusion coefficient_
	- If $D$ is _constant_, the PDE governing diffusion is:
	$$\pd{C}{t}=D\nabla^2C+Q$$
	- $Q=0$, the system is in a steady state: Laplace's equation
	- The system is in a steady state: Poisson's equation
	- The _diffusion equation_ is the non-steady state case when $Q=0$:
	$$\pd{C}{t}=D\nabla^2 C$$
- _Temperature $\theta$ also obeys_ the above equations but with different constants (heat capacity $c_p$ and density $\rho$, and heat conductivity $k$)
	- Conditions: constant pressure
	$$\pd{\theta}{t}=\frac{k}{\rho c_p}\nabla^2\theta+\frac{Q}{\rho c_p}$$

- _Boundary conditions_ are _ALWAYS_ necessary to solve the problem (or even determine the functional form)

## Boundary conditions
- Dirichlet conditions: _specifying the value at the boundary_
$$\theta=g(\bm{r})$$
- Neumann conditions: _specifying the derivative_
$$\pd{\theta}{n}\equiv \hat{\bm{n}}\cdot(\nabla\theta)=h(\bm{r})$$
- Mixed conditions:
$$\alpha(\bm{r})\pd{\theta}{n}+\beta(\bm{r})\theta=d(\bm{r})$$


## Separation of variables
- Sometimes, solutions to PDEs can be written in _separable form_
$$f(x,y)=X(x)Y(y)$$
- Separability _is dependent on coordinate system_
	- $1/\sqrt{x^2+y^2+z^2}$ is not separable in Cartesian but separable in polar


### Example: 1-dimensional wave equation
- Let the solution be:
$$y(x,t)=X(x)T(t)$$
- Substituting this into the equation, then _dividing through by $\psi$_:
$$\frac{1}{c^2}\frac{\ddot{T}}{T}=\frac{X''}{X}$$
- As the left is a function of $t$, and the right is a function of $x$, they must equal a constant $\lambda$
- Then, one gets:
$$\ddot{T}-c^2\lambda T=0 \hspace{1cm} X''-\lambda X=0$$
- $\lambda=0$:
$$y=(A_0+B_0t)(C_0+D_0x)$$

- $\lambda=\sigma^2>0$:
$$y=\left(A_\sigma e^{\sigma ct}+B_\sigma e^{-\sigma ct}\right)\left(C_\sigma \cosh(\sigma x)+D_\sigma\sinh(\sigma x)\right)$$
	- The constants are _dependent on $\sigma$_

- $\lambda=-k^2<0$:
$$y=[A_k\cos(kct)+B_k\sin(kct)][C_k\cos(kx)+D_k\sin(kx)]$$

- Boundary and initial conditions: _restrictions_ on the constants
- As $L$ is linear, _use superposition to satisfy_ the boundary and initial conditions

- Typical boundary conditions for waves:
$$y(x=0,t)=y(x=L,t)=0$$
- For initial conditions, suppose there is some initial displacement and velocity:
$$y(x,0)=d(x) \hspace{1cm} \dot{y}(x,0)=v(x)$$
- $\lambda=0$:  _boundary conditions_ mean $C_0=D_0=0$
- $\lambda>0$: boundary values also imply $C_\sigma=D_\sigma=0$

- $\lambda<0$: boundary values mean $C_k=0$, and $D_k$ _can only take a discrete set of values_
 $$D_k=\frac{n\pi}{L}$$
	- $D_k$ are the [[Vectors and matrices|eigenvalues]] of the operator
- The solution becomes:
$$y=\sum_n\left(\mathcal{A}_n\cos\frac{n\pi ct}{L}+\mathcal{B}_n\sin\frac{n\pi ct}{L}\right)\sin\frac{n\pi x}{L}$$

- $\mathcal{A}_n$ and $\mathcal{B}_n$ are found by _substituting the initial conditions_
$$\displaylines{d(x)=y(x,t=0)=\sum_n \mathcal{A}_n\sin\frac{n\pi x}{L} \\v(x)=\pd{y}{t}(x,t=0)=\sum_n\frac{n\pi c}{L} 
 \mathcal{B}_n\sin\frac{n\pi x}{L}}$$
 - Use the _trig orthogonality relations_ to express $d(x)$ and $v(x)$ as [[Fourier series and transforms|Fourier series]], and find $\mathcal{A}_n$ and $\mathcal{B}_n$

### Example: Poisson's equation
- Solving:
$$\nabla^2\Theta=f$$
- Separate:
$$\Theta=X(x)Y(y)$$
- Substitute and divide:
$$\frac{X''}{X}=-\frac{Y''}{Y}-\frac{f}{XY}$$
- General solution: find a _particular solution_ $\theta_s$, then add the _complementary solutions_

### The general recipe
1. In the case of an inhomogeneous equation, use the principle of superposition to seek a particular solution to reduce the equation to one that is homogeneous. 
2. Seek separable solutions to the homogeneous equation. 
3. In the case of inhomogeneous boundary conditions seek a separable solution to reduce the boundary conditions to ones that are homogeneous. 
4. Use the boundary conditions to rule out certain of the separable solutions and to identify eigenvalues. 
5. Using the principle of superposition, seek a solution that is a sum of eigenfunctions. 
6. Determine unknown constants using the boundary conditions.

### Using Fourier transforms
- Applicable for problems with an infinite domain, and normalisable solution
- Apply a [[Fourier series and transforms#Properties of Fourier transforms|Fourier transform]] to both sides to convert a _spatial derivative to multiplication by $k$_
- Solve for the Fourier transform
- Invert the Fourier transform