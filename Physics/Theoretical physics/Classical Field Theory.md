- The _degrees of freedom_ are represented by _fields_
- _Fields_ are _functions/maps between two sets of numbers_

- Notation: _natural units_, $\hbar=c=1$
	- Conversion: $\hbar c=0.2\,\text{GeV}\,\text{fm}$
	- $[\text{T}]=[\text{E}]^{-1}=[\text{M}]^{-1}$

- [x] Add bits from TP1 notes ⏫ 📅 2023-10-19 ✅ 2023-10-23
# Field theories in physics
- The dynamics of a _point particle_ is a classical field theory
	- The map: from a set in $\mathbb{R}$ (_time_) to a set in $\mathbb{R}^3$ (_space_)
- This also applies to a set of $n$ particles
	- From a set in $\mathbb{R}$ (time) to a set in $\mathbb{R}^{3n}$ 
	- As long as _collisions_ are _not accounted for_
- Or one can think of _waves on a string_
	- A map from $\mathbb{R}^2$ (_time_, _length_ along string) to $\mathbb{R}^2$ (_displacements_)

- _Electromagnetism_ is a classical field theory
	- A map from $\mathbb{R}^4$ (_spacetime_) to $\mathbb{R}^6$ (the _electric_ and _magnetic_ fields)
- _General relativity_ is a field theory
	- $\mathbb{R}^4$ (spacetime) to $\mathbb{R}^{10}$ (the _metric tensor_)
- _String theory_ is a field theory
	- Map from $\mathbb{R}^2$ or $\mathbb{R}$ (depending on if the string is _open or closed_) to $\mathbb{R}^{26}$
- Mathematically, _thermodynamics_ is also a field theory

- Ultimately, for a _Lorentz invariant_ theory, one takes $\mathbb{R}^4$, or _Minkowski spacetime_, as the _source_ of the map

# Lagrangian density

## The Euler-Lagrange equation
- Consider _longitudinal waves_ on an elastic rod, with density $\rho$ and some _elastic modulus_ $\kappa$
- Let there be a _field_ $\varphi(x,t)$ describing the _displacement_
- Set up the [[Analytical classical mechanics|Lagrangian]]:
$$L=T-V=\int\frac{1}{2}\rho\left(\pd{\varphi}{t}\right)^2\,dx-\int\frac{1}{2}\kappa\left(\pd{\varphi}{x}\right)\,dx$$
- The _action_ is then:
$$S=\int L\,dt=\int\Lagr\,dt\,dx$$
- $\Lagr$ is known as the _Lagrangian density_:
$$\Lagr\left(\varphi,\varphi',\dot{\varphi}\right)=\frac{1}{2}\rho\dot{\varphi}^2-\frac{1}{2}\kappa\varphi'^2$$
- In general, it is a function of the _field_, and its _time and space derivatives_
- Considering a _variation_ in $\varphi$ while fixing the _endpoints_, and using [[Analytical classical mechanics#Hamilton's Principle of Stationary Action|Hamilton's Principle]]:
$$\pd{\Lagr}{\varphi}-\pd{}{x}\left(\pd{\Lagr}{\varphi'}\right)-\pd{}{t}\left(\pd{\Lagr}{\dot{\varphi}}\right)=0$$
- This is the _Euler-Lagrange equation for the Lagrangian density_
- The form is the _same for $x$ and $t$_, as expected
	- This later leads to the fact that $\Lagr$ is _Lorentz invariant_

- Applying the above equation to the rod:
$$\kappa\varphi''-\rho\ddot{\varphi}=0$$
- This is simply the _wave equation_

- One can then define the _canonical momentum density_:
$$\pi(x,t)=\pd{\Lagr}{\dot{\varphi}}$$
- This _depends_ on the choice of _"time" coordinate_
	- Hence, it is _not a Lorentz invariant_

- One can then define a _Hamiltonian density_:
$$\Ham(\varphi,\pi,\varphi')=\pi\dot{\varphi}-\Lagr$$
- For the _elastic rod_, one gets:
$$\Ham=\frac{\pi^2}{2\rho}+\frac{1}{2}\kappa\varphi'^2$$

- If $\Lagr$ _does not depend explicitly on_ $\varphi$, from the Euler-Lagrange equation, one gets:
$$\pd{\pi}{t}+\pd{}{x}J(x,t)=0$$
- $J(x,t)=\partial\Lagr/\partial\varphi'$ can be interpreted as the _canonical momentum current_
- The change in _total canonical momentum_ is:
$$\frac{dp}{dt}=\int\pd{\pi}{t}\,dx-\int\pd{J}{x}\,dx=0$$
- The latter term is _zero_ if one has _periodic boundary conditions_
- This gives the _conservation of canonical momentum_
## Generalising to more dimensions
- For _more dimensions_, the action is:
$$S=\int\Lagr\left(\varphi,\pd{\varphi}{t},\nabla\varphi,x^\mu\right)\,dt\,dx_1dx_2\dots dx_d$$
- The Euler-Lagrange equation is then:
$$\pd{\Lagr}{\varphi}=\pd{}{t}\left(\pd{\Lagr}{\dot{\varphi}}\right)+\nabla\cdot\left(\pd{\Lagr}{(\nabla\varphi)}\right)$$
- The _conservation of canonical momentum_ is then:
$$\pd{\pi}{t}+\nabla\cdot\bm{J}=0$$
- As time and space are on _equal footing_, treat $t$ as _another coordinate variable_:
$$\displaylines{\Lagr=\Lagr(\varphi,\partial_\mu\varphi) \\ \pd{\Lagr}{\varphi}=\partial_\mu\left(\pd{\Lagr}{[\partial_\mu\varphi]}\right)}$$
- Then if $\partial\Lagr/\partial\varphi=0$:
$$\partial_\mu J^\mu=0$$

## Relativistic scalar field
- For a relativistic theory, the field used must be _Lorentz invariant_
- The field could be a _scalar_ or _vector_
	- $\varphi\in\mathbb{R}^2$: spin-1/2 particle
	- $\varphi\in\mathbb{R}^4$: photon

- The _action_ is the integration of $\Lagr$ with respect to an _element of spacetime_:
$$S=\int\Lagr\,dx^\mu$$
- The spacetime element is _Lorentz invariant_

- One writes down the _most general_ Lagrangian, up to _second order terms_
	- Dimension of $\Lagr$: $[M]^4$
$$\Lagr=\alpha(\partial^\mu\varphi)(\partial_\mu\varphi)+\beta\partial^\mu\partial_\mu\varphi+\gamma\varphi\partial^\mu\partial_\mu\varphi+\delta\varphi+\epsilon\varphi^2$$
- Impose the _boundary condition_ that $\varphi\to 0$ at _infinity_, and is _fixed_ for _two points in time_ (distant past and future)

- One can _rewrite_ this as:
$$\Lagr=(\alpha-\gamma)(\partial^\mu\varphi)(\partial_\mu\varphi)+\partial^\mu(\beta\partial_\mu\varphi+\gamma\varphi\partial_\mu\varphi)+\delta\varphi+\epsilon\varphi^2$$
- _Integrating_ this over a 4D surface, the second term gives a _constant_, which _does not affect_ the equations of motion

- One can then _define_ $\alpha-\gamma$ as $1/2$
- This leads to the _equation of motion_:
$$\partial^\mu\partial_\mu\varphi-\delta-2\epsilon\varphi=0$$
	- _Lower_ the index using the metric, making the $(\partial_\mu\varphi)(\partial^\mu\varphi)$ term contribute _twice_
- Then impose the boundary conditions to make $\delta$ _vanish_

- Then redefine $\epsilon$ as $-m^2/2$, getting the Lagrangian density as:
$$\Lagr=\frac{1}{2}(\partial^\mu\varphi)(\partial_\mu\varphi)-\frac{1}{2}m^2\varphi^2$$
- Writing it out in more detail:
$$\Lagr=\frac{1}{2c^2}\left(\pd{\varphi}{t}\right)^2-\frac{1}{2}(\nabla\varphi)^2-\frac{1}{2}m^2\varphi^2$$

- The equation of motion is then the _Klein-Gordon equation_:
$$\partial^\mu\partial_\mu\varphi+m^2\varphi=0$$
	- For a _different metric_, there is a _minus sign_

- One also gets the _canonical momentum density_:
$$\pi=\pd{\Lagr}{\dot{\varphi}}=\frac{1}{c^2}\left(\pd{\varphi}{t}\right)$$
- The _Hamiltonian density_ is then:
$$\Ham=\frac{c^2\pi^2}{2}+\frac{1}{2}(\nabla\varphi)^2+\frac{1}{2}m^2\varphi^2$$
- This can only be _positive-definite_ iff the $\varphi^2$ coefficient is _positive_
	- Negative: one gets states with _arbitrary large negative energy_, hence the state has _no stable ground state_, which is _unphysical_
	- This justifies $\epsilon=-m^2/2$

## Fourier analysis of Klein-Gordon equation
- For simplicity, take _one spatial dimension_
- Let there be a _plane wave solution_ to the Klein-Gordon equation:
$$\varphi=\exp[i(kx-\omega t)]$$
- This gives the condition:
$$\omega^2=k^2+m^2$$
- One can then _superimpose_ solutions (with $N(-k)=N(k)$ as a normalising factor)
	- Ensure $\varphi$ is _real_:
$$\varphi=\int\,dk\,N(k)\,\left[a(k)\exp[i(kx-\omega t)]+a^*(k)\exp[-i(kx-\omega t)]\right]$$
- One can then try to write the Hamiltonian:
$$H=\int\left(\frac{c^2\pi^2}{2}+\frac{1}{2}(\nabla\varphi)^2+\frac{1}{2}m^2\varphi^2\right)\,dx$$
- Using:
$$\int\,dx\exp[i(k\pm k')x]=2\pi\delta(k\pm k')\hspace{1.5cm} N(-k)=N(k)\hspace{1.5cm}\omega(-k)=\omega(k)$$
- One finds:
$$H=2\pi\int\,dk\,[N(k)\omega(k)]^2[a(k)a^*(k)+a^*(k)a(k)]$$
- The _explicit time dependence disappears_ as $\Lagr$ is _not explicitly dependent on time_
- In _quantum field theory_, $a(k)$ is a _ladder operator_ and $a$ and $a^*$ _may not commute_
- Choose $N(k)$:
$$N(k)=\frac{1}{2\pi}\frac{1}{2\omega}$$
- This _keeps the Hamiltonian Lorentz invariant_
- The Hamiltonian is then:
$$H=\int\,dk\,N(k)\frac{\omega(k)}{2}[a(k)a^
*(k){+a^*(k)a(k)}]$$
- In the _classical_ regime:
$$H=\int\,dk\,N(k)\omega(k)|a(k)|^2$$
- $N(k)$ can be interpreted as _number of modes_
- $\omega(k)$ is the _energy of modes_
- Each mode behaves as a _simple/quantum harmonic oscillator_
	- Energy is _relativistic_

- For _3 spatial dimensions_:
$$\varphi\propto\exp[i(\bm{k}\cdot\bm{r}-\omega t)]$$
- Normalisation:
$$N(k)=\frac{1}{(2\pi)^3}\frac{1}{2\omega(k)}$$
- The expression for the _Hamiltonian_ holds

## Complex scalar fields
- Let there be a general _complex scalar field_ $\varphi(x^\mu)$
- The Lagrangian must be _invariant_ with respect to adding a _phase_ to $\varphi$
- The most _general Lagrangian_:
$$\Lagr=\partial_\mu\varphi(\partial^\mu\varphi^*)-m^2\varphi^*\varphi$$
- Treating $\varphi$ and $\varphi^*$ as _independent_:
$$\pi=\pd{\Lagr}{\dot{\varphi}}=\dot{\varphi}^* \hspace{1.5cm} \pi^*=\pd{\Lagr}{\dot{\varphi^*}}=\dot{\varphi}$$
- The _Hamiltonian density_:
$$\Ham=\pi\dot{\varphi}+\pi^*\dot{\varphi^*}-\Lagr$$
- One then gets _separate Klein-Gordon equations_ for $\varphi$ and $\varphi^*$

- The Fourier decomposition:
$$\varphi=\int\,dk\,N(k)[a(k)\exp(ikx-i\omega t)+b^*(k)\exp(-ikx+i\omega t)]$$
- The Hamiltonian:
$$H=\int\,dk\,N(k)\omega(k)[|a(k)|^2+|b(k)|^2]$$
## Electromagnetic fields
- Consider a _field_ $A_\mu$ from spacetime $\mathbb{R}^4$ to $\mathbb{R}^4$
- Physical quantities must be _gauge invariant_:
$$A_\mu\longrightarrow A_\mu+\partial_\mu f(x^\mu)$$

- Make an _antisymmetric tensor_ which is _gauge invariant_
$$F_{\alpha\beta}=\partial_\alpha A_\beta-\partial_\beta A_\alpha$$
- This is the _Maxwell tensor_
	- The 4-vector $A^\mu$ is the _4-potential_
- These components are _not Lorentz invariant_
	- The indices are _not summed over_

- Writing out components:
$$F_{\alpha\beta}=\pmatrix{0 & E_x/c & E_y/c & E_z/c \\-E_x/c &0 & -B_z & B_y \\-E_y/c & B_z & 0 & -B_x \\ -E_z/c & -B_y & B_x & 0}$$
- Or, alternatively:
$$F_{i0}=-F_{0i}=E_i \hspace{1.5cm} F_{ij}=\epsilon_{ijk}B_k$$

- Constructing the _general Lagrangian_ by only allowing _second-order_ terms:
$$\Lagr= aF_{\alpha\beta}F^{\alpha\beta}-J^\mu A_\mu$$
- where $J^\mu$ is some _4-current density_
	- $J^0=\rho$
	- $J^{i}=\bm{J}\cdot\hat{\bm{e}}_i$
- Gauge-invariance _of the action_ requires that the current density is _divergenceless_ $(\partial_\mu J^\mu=0)$
	- Otherwise, _boundary terms_ appear in the action (integrate $-J^\mu A_\mu$ _by parts_)
	- $\Lagr$ is still _not gauge invariant_

- From the Euler-Lagrange equations:
$$J^\alpha+4a\partial_\mu F^{\mu\alpha}=0$$
- To make the Hamiltonian _positive-definite_:
$$a=-\frac{1}{4\mu_0}$$
- With natural units, treating $\mu_0=\epsilon_0=c=1$:
$$\displaylines{\Lagr=-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}-J^\mu A_\mu \\ J^\alpha-\partial_\mu F^{\mu\alpha}=0}$$

- With this constant, one recovers:
$$\text{div }\bm{E}=\frac{\rho}{\epsilon_0} \hspace{1.5cm} \text{curl }\bm{B}=\epsilon_0\mu_0\pd{\bm{E}}{t}+\mu_0\bm{J}$$
- The _continuity equation_ can be recovered from $\partial_\mu J^\mu=0$
- From the fact that $F_{\alpha\beta}$ is _anti-symmetric_:
$$\partial_\lambda F_{\mu\nu}+\partial_\nu F_{\lambda\mu}+\partial_\mu F_{\nu\lambda}=0$$
- One recovers the _other two Maxwell's equations_

- One can _fix_ the gauge of $A^\mu$
- The _Lorenz gauge_ is _Lorentz invariant_:
$$\partial_\mu A^\mu=0$$

- From this, the _general Lagrangian_ for a _group of particles_ in an _external field_:
$$S=\sum_\text{particles}\left\{-\int mc^2\,d\tau-\int eA_\mu\,dx^\mu(t)\right\}-\frac{1}{4}\int F_{\alpha\beta}F^{\alpha\beta}\,d^4x$$
# Symmetries and conservation laws
- The simplest conservation law from the Lagrangian is the _conservation of momentum density_ if $\Lagr$ does _not explicitly depend on_ $\varphi$:
$$\pd{}{\varphi}\left(\pd{\varphi}{[\partial_\mu\varphi]}\right)=0$$
- The momentum density is said to be a _conserved charge_

## Noether's theorem
- This links any _smooth, continuous symmetry_ to a _conserved charge_
	- A _Lie group_ symmetry
	- Example: translation, but not reflection

- Do it in $1+1$ dimensions
- Suppose the Lagrangian density $\Lagr$ is _invariant_ under the _infinitesimal_ change:
$$\varphi\to\varphi+\delta\varphi$$
- From this:
$$\delta\Lagr=\pd{\Lagr}{\varphi}\delta\varphi+\pd{\Lagr}{\varphi'}\delta\varphi'+\pd{\Lagr}{\dot{\varphi}}\delta\dot{\varphi}=0$$
- From the [[#The Euler-Lagrange equation|Euler-Lagrange equation]], and combining terms with the _product rule_:
$$\delta\Lagr=\pd{}{x}\left(\pd{\Lagr}{\varphi'}\delta\varphi\right) + \pd{}{t}\left(\pd{\Lagr}{\dot{\varphi}}\delta\dot{\varphi}\right)=0$$
- Then define the _charge and current_:
$$\displaylines{\rho=\pd{\Lagr}{\dot{\varphi}}\delta\varphi\hspace{1.5cm}\bm{J}=\pd{\Lagr}{\varphi'}\delta\varphi \\ \pd{\rho}{t}+\pd{J}{x}=0}$$
- _Generalise_ to arbitrary space dimensions, the _Noether current_ and its conservation:
$$J^\mu=\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi\hspace{1.5cm}\pd{\rho}{t}+\partial_\mu J^\mu=0$$

- For some _multi-component_ field, the Noether current _generalises_ to:
$$J^\mu=\pd{\Lagr}{(\partial_\mu\varphi_j)}\delta\varphi_j$$
- For multiple fields, the transformation can _mix_ them:
$$\delta\varphi_j=\epsilon t_{jk}\varphi_k\Longrightarrow J^\mu=\pd{\Lagr}{(\partial_\mu\varphi_j)}t_{jk}\varphi_k$$

## Phase symmetry
- The Lagrangian is _invariant uder a global phase change_

- The _positive_ and _negative_ Fourier components contribute _different signs_ to the conserved charge
	- This represents _particles_ and _anti-particles_

## Phase and gauge symmetry
- Suppose the _phase_ of the complex scalar field $\varphi$ is a _function of space-time coordinates_:
$$\varphi\to \exp(-i\epsilon(x^\mu))\varphi \Longrightarrow \partial^\mu\varphi\to$$
- It is _not a symmetry_ of the Klein-Gordon Lagrangian

- Let the transformation instead be:
$$\varphi\to \exp(-ie\epsilon(x^\mu))\varphi$$
- The _constant_ gives the _representation_ of the $U(1)$ group
	- $U(1)$ has _infinitely many_ irreducible represntations, characterised by a _constant_

- Simultaneously make the _gauge transformation_:

- Introduce the _covariant derivative_:
$$D_\mu=\partial_\mu+ieA_\mu\Longrightarrow D_\mu\varphi\to\exp(-i\epsilon)D^\mu\varphi$$
- The Lagrangian is then:
$$\Lagr=(D_\mu\varphi^*) (D^\mu\varphi)-m^2\varphi^*\varphi-\frac{1}{4\mu_0}\dots$$
- There is a $U(1)$ symmetry in the Lagrangian
- The _conserved charge_ for _constant_ $\epsilon$:
$$\delta\varphi=-ie\epsilon\varphi \hspace{1.5cm}\delta\varphi^*=ie\epsilon\varphi$$
- This gives:
$$J^\mu=-e\epsilon[\varphi D^\mu\varphi^*-\varphi^* D^\mu\varphi]$$

- For the Lagrangian to be _invariant under a spacetime dependent phase transformation_, one needs an _electromagnetic field_
- One must also introduce a _covariant derivative_
	- It represents _mechanical momentum_

## The energy-momentum tensor
- Let the Lagrangian vary by some _total derivative_
- Using the proof for Noether's theorem above:
$$\delta\Lagr=\partial_\mu\left(\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi\right)=\partial_\mu K^\mu$$
- The _conserved quantity_ is then:
$$\partial_\mu\left(\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi-K^\mu\right)=0$$

- Given a _transformation_ in _space-time_:
$$x^\mu\to x^\mu+\epsilon^\mu$$
- Then for a function of the coordinates, such as $\varphi$:
$$\varphi\to\varphi+\epsilon^\mu\partial_\mu\varphi$$
- Then provided that $\Lagr$ _does not depend explicitly_ on $x^\mu$:
$$\Lagr\to \Lagr+\epsilon^\mu\partial_\mu\Lagr$$
- _Explicit dependence_ will make it into a form that does not make the _conserved quantity_ above

- Stuff stuff stuff

- One then gets:
$$\partial^\nu\left(\pd{\Lagr}{(\partial^\nu\varphi)}\partial^\mu\varphi-\delta^\mu_\nu\Lagr\right)=0$$
- This gives the _energy-momentum tensor_ $\tenscom{T}{\mu}{\nu}$

### Longitudinal wave on an elastic rod
- From a [[#The wave on an elastic rod|previous derivation]]:
$$\Lagr=\frac{1}{2}\rho\dot{\varphi}^2-\frac{1}{2}\kappa\varphi^2$$
- From the formula for the energy-momentum tensor above:
$$\displaylines{\tenscom{T}{0}{0}=\tenscom{T}{1}{1}=\frac{1}{2}\rho\dot{\varphi}^2+}$$
- As the Lagrangian is _not Lorentz invariant_, $T$ is _not symmetric_

### Relativistic scalar field
$$\Lagr=\frac{1}{2}(\partial^\mu\varphi)(\partial_\mu\varphi)-\frac{1}{2}\varphi^2$$
- The _energy-momentum tensor_ is:
$$T^{\mu\nu}=(\partial^\mu\varphi)(\partial^\nu\varphi)-g^{\mu\nu}\Lagr$$
- From this, one gets that the tensor is _symmetric_

### Electromagnetic field
$$\Lagr=-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}=-\frac{1}{4}g^{\alpha\gamma}g^{\beta\delta}$$
- The tensor:

- The form of this tensor is _not gauge invariant_, and _not symmetric_
- From the derivation, one can _freely add_ any tensor of the form:
$$\partial_\lambda \Omega^{\lambda\mu\nu}\longrightarrow\partial$$
