- The _degrees of freedom_ are represented by _fields_
- _Fields_ are _functions/maps between two sets of numbers_

- Notation: _natural units_, $\hbar=c=1$
	- Conversion: $\hbar c=0.2\,\text{GeV}\,\text{fm}$
	- $[\text{T}]=[\text{E}]^{-1}=[\text{M}]^{-1}$

- Convention for _Minkowski metric_:
$$\eta_{\mu\nu}=\pmatrix{1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&-1}$$
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
$$L=T-V=\int\frac{1}{2}\rho\left({\varphi}{t}\right)^2\,dx-\int\frac{1}{2}\kappa\left(\pd{\varphi}{x}\right)\,dx$$
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
$$\pd{\pi}{t}+\nabla\cdot\boldsymbol{J}=0$$


- As time and space are on _equal footing_, treat $t$ as _another coordinate variable_:
$$\displaylines{\Lagr=\Lagr(\varphi,\partial_\mu\varphi) \\ \pd{\Lagr}{\varphi}=\partial_\mu\left(\pd{\Lagr}{[\partial_\mu\varphi]}\right)}$$
- Define the 4-vector:
$$J^\mu=\pd{\Lagr}{[\partial_\mu\varphi]}$$
- Then if $\partial\Lagr/\partial\varphi=0$:
$$\partial_\mu J^\mu=0$$
- This gives rise to [[#Symmetries and conservation laws|Noether's Theorem]]

## Relativistic scalar field
- For a relativistic theory, the field used must be _Lorentz invariant_
- The field could be a _scalar_ or _vector_
	- $\varphi\in\mathbb{R}^2$: spin-1/2 particle
	- $\varphi\in\mathbb{R}^4$: photon

- The _action_ is the integration of $\Lagr$ with respect to an _element of spacetime_:
$$S=\int\Lagr\,dx^\mu$$
- The spacetime element is _Lorentz invariant_

### The relativistic Lagrangian density
- One writes down the _most general_ Lagrangian, up to _second order terms_
	- Dimension of $\Lagr$: $[M]^4$
$$\Lagr=\alpha(\partial^\mu\varphi)(\partial_\mu\varphi)+\beta\partial^\mu\partial_\mu\varphi+\gamma\varphi\partial^\mu\partial_\mu\varphi+\delta\varphi+\varepsilon\varphi^2$$
- Impose the _boundary condition_ that $\varphi\to 0$ at _infinity_, and is _fixed_ for _two points in time_ (distant past and future)

- One can _rewrite_ this as:
$$\Lagr=(\alpha-\gamma)(\partial^\mu\varphi)(\partial_\mu\varphi)+\partial^\mu(\beta\partial_\mu\varphi+\gamma\varphi\partial_\mu\varphi)+\delta\varphi+\varepsilon\varphi^2$$
- _Integrating_ this over a 4D surface, the second term gives a _constant_, which _does not affect_ the equations of motion

- One can then _define_ $\alpha-\gamma$ as $1/2$
- This leads to the _equation of motion_:
$$\partial^\mu\partial_\mu\varphi-\delta-2\varepsilon\varphi=0$$
	- _Lower_ the index using the metric, making the $(\partial_\mu\varphi)(\partial^\mu\varphi)$ term contribute _twice_
- Then impose the boundary conditions to make $\delta$ _vanish_

- Then redefine $\varepsilon$ as $-m^2/2$, getting the _Lagrangian density_ as:
$$\Lagr=\frac{1}{2}(\partial^\mu\varphi)(\partial_\mu\varphi)-\frac{1}{2}m^2\varphi^2$$
- Writing it out in more detail:
$$\Lagr=\frac{1}{2c^2}\left(\pd{\varphi}{t}\right)^2-\frac{1}{2}(\nabla\varphi)^2-\frac{1}{2}m^2\varphi^2$$
### Klein-Gordon equation
- The equation of motion is then the _Klein-Gordon equation_:
$$\partial^\mu\partial_\mu\varphi+m^2\varphi=0$$
	- For a _different metric_, there is a _minus sign_

- One also gets the _canonical momentum density_:
$$\pi=\pd{\Lagr}{\dot{\varphi}}=\frac{1}{c^2}\left(\pd{\varphi}{t}\right)$$
- The _Hamiltonian density_ is then:
$$\Ham=\frac{c^2\pi^2}{2}+\frac{1}{2}(\nabla\varphi)^2+\frac{1}{2}m^2\varphi^2$$
- This can only be _positive-definite_ iff the $\varphi^2$ coefficient is _positive_
	- Negative: one gets states with _arbitrary large negative energy_, hence the state has _no stable ground state_, which is _unphysical_
	- This justifies $\varepsilon=-m^2/2$

## Fourier decomposition of field
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
$$\int\,dx\exp[i(k\pm k')x]=2\pi\delta(k\pm k')\hspace{1cm} N(-k)=N(k)\hspace{1cm}\omega(-k)=\omega(k)$$
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
- Each mode behaves as a _simple/quantum harmonic oscillator_ with amplitude $a(k)$
	- Energy is _relativistic_

- For _3 spatial dimensions_:
$$\varphi\propto\exp[i(\bm{k}\cdot\bm{r}-\omega t)]$$
- Normalisation:
$$N(k)=\frac{1}{(2\pi)^3}\frac{1}{2\omega(k)}$$
- The expression for the _Hamiltonian_ holds

## Complex scalar fields
- Let there be a general _complex scalar field_ $\varphi(x^\mu)$
- The Lagrangian must be _invariant_ with respect to adding a _phase_ to $\varphi$

### Two fields
- The most _general Lagrangian_:
$$\Lagr=\partial_\mu\varphi(\partial^\mu\varphi^*)-m^2\varphi^*\varphi$$
- One can also get two _real fields_ $\varphi_i$ from considering:
$$\varphi=\frac{1}{\sqrt{2}}(\varphi_1+i\varphi_2)$$
- One can then _rewrite_ the Lagrangian as:
$$\Lagr=\sum_{i=1,2}\frac{1}{2}\partial_\mu\varphi_i\partial^\mu\varphi_i-\frac{m^2}{2}\varphi_i\varphi_i$$
- This shows that it is really _two independent fields_

### Equation and Fourier decomposition
- Treating $\varphi$ and $\varphi^*$ as _independent_, one gets _separate equations_ for both fields:
$$\partial_\mu\partial^\mu\varphi+m^2\varphi=0\hspace{1.5cm}\partial_\mu\partial^\mu\varphi^*+m^2\varphi^*=0$$

- Corresponding momentum densities:
$$\pi=\pd{\Lagr}{\dot{\varphi}}=\dot{\varphi}^* \hspace{1.5cm} \pi^*=\pd{\Lagr}{\dot{\varphi^*}}=\dot{\varphi}$$
- The _Hamiltonian density_:
$$\Ham=\pi\dot{\varphi}+\pi^*\dot{\varphi^*}-\Lagr$$


- The Fourier decomposition:
$$\varphi=\int\,dk\,N(k)[a(k)\exp(ikx-i\omega t)+b^*(k)\exp(-ikx+i\omega t)]$$
- The Hamiltonian:
$$H=\int\,dk\,N(k)\omega(k)[|a(k)|^2+|b(k)|^2]$$
- In _three dimensions_, the Fourier decomposition:
$$\varphi=\int\,dk N(k)[a(k)\exp(-ik\cdot x)+b^*(k)\exp(ik\cdot x)]$$
- Here:
$$k\cdot x=k^\mu x_\mu=\omega t-\bm{k}\cdot\bm{x}$$
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
$$F_{i0}=-F_{0i}=E_i \hspace{1.5cm} F_{ij}=\varepsilon_{ijk}B_k$$

- Constructing the _general Lagrangian_ by only allowing _second-order_ terms:
$$\Lagr= aF_{\alpha\beta}F^{\alpha\beta}-J^\mu A_\mu$$
- where $J^\mu$ is some _4-current density_
	- $J^0=\rho$
	- $J^{i}=\bm{J}\cdot\hat{\bm{e}}_i$
- _Gauge-invariance of the action_ requires that the current density is _divergenceless_ $(\partial_\mu J^\mu=0)$
	- Otherwise, _boundary terms_ appear in the action (integrate $-J^\mu A_\mu$ _by parts_)
	- $\Lagr$ is still _not gauge invariant_
	- Gauge invariance _must lead_ to a [[#Local phase (gauge) symmetry|conservation]], where $J^{\mu}$ is the conserved quantity

- From the Euler-Lagrange equations:
$$J^\alpha+4a\partial_\mu F^{\mu\alpha}=0$$
- To make the Hamiltonian _positive-definite_:
$$a=-\frac{1}{4\mu_0}$$
- With natural units, treating $\mu_0=\varepsilon_0=c=1$:
$$\displaylines{\Lagr=-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}-J^\mu A_\mu \\ J^\alpha-\partial_\mu F^{\mu\alpha}=0}$$

- With this constant, one recovers:
$$\text{div }\bm{E}=\frac{\rho}{\varepsilon_0} \hspace{1.5cm} \text{curl }\bm{B}=\varepsilon_0\mu_0\pd{\bm{E}}{t}+\mu_0\bm{J}$$
- The _continuity equation_ can be recovered from $\partial_\mu J^\mu=0$
- From the fact that $F_{\alpha\beta}$ is _anti-symmetric_, the _Bianchi identity_ states:
$$\partial_\lambda F_{\mu\nu}+\partial_\nu F_{\lambda\mu}+\partial_\mu F_{\nu\lambda}=0$$
- One recovers the _other two Maxwell's equations_
$$\text{div }\bm{B}=0\hspace{1.5cm}\text{curl }\bm{E}=-\pd{\bm{B}}{t}$$

- One can _fix_ the gauge of $A^\mu$
- The _Lorenz gauge_ is _Lorentz invariant_:
$$\partial_\mu A^\mu=0$$

- From this, the _general Lagrangian_ for a _group of particles_ in an _external field_:
$$S=\sum_\text{particles}\left\{-\int mc^2\,d\tau-\int eA_\mu\,dx^\mu(t)\right\}-\frac{1}{4}\int F_{\alpha\beta}F^{\alpha\beta}\,d^4x$$

- The _free-field_ Lagrangian can be written as:
$$-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}=\frac{1}{2}(|\bm{E}|^2-|\bm{B}|^2)$$

# Symmetries and conservation laws
- The _simplest_ conservation law from the Lagrangian is the _conservation of momentum density_ if $\Lagr$ does _not explicitly depend on_ $\varphi$:
$$\pd{}{\varphi}\left(\pd{\varphi}{[\partial_\mu\varphi]}\right)=0$$
- The momentum density is said to be a _conserved charge_

## Noether charge and current
- This links any _smooth, continuous symmetry of the field_ to a _conserved charge_
	- A _Lie group_ symmetry
	- Example: translation, but not reflection
- This involves _no change in spacetime coordinates_, only the _field itself_
	- Also known as an _internal symmetry_
	- A shift in spacetime results in a change in [[#The energy-momentum tensor|total derivative]]
	- Nother's theorem still gives _other conservations_, such as momentum

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
$$J^\mu=\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi\hspace{1.5cm}\partial_\mu J^\mu=0$$

- For some _multi-component_ field, the Noether current _generalises_ to:
$$J^\mu=\pd{\Lagr}{(\partial_\mu\varphi_j)}\delta\varphi_j$$
- For multiple fields, the transformation can _mix_ them:
$$\delta\varphi_j=\varepsilon t_{jk}\varphi_k\Longrightarrow J^\mu=\pd{\Lagr}{(\partial_\mu\varphi_j)}t_{jk}\varphi_k$$

- Given the current, one can define the _conserved charge_:
$$\displaylines{Q=\int_\text{all space} \rho\,d^3\bm{r}=\int J^0\,d^3\bm{r} \\ \frac{dQ}{dt}=\int\pd{\rho}{t}\,d^3\bm{r}=-\int\div\bm{J}\,d^3\bm{r}=-\int_{\infty\text{ sphere}}\bm{J}\cdot d\bm{S}=0}$$

- The conservation law allows for some _freedom_ in the current:
$$J^\mu\to J^\mu+\partial_\nu f^{\mu\nu}$$
- Here, $f^{\mu\nu}$ is an _antisymmetric tensor_
- This is _also conserved_ due to the antisymmetry 
## Global phase symmetry
$$\Lagr=(\partial_\mu\varphi)(\partial^\mu\varphi^*)-m^2\varphi\varphi^*$$
- The Lagrangian is _invariant uder a global phase change_
	- Global: the phase is _independent of coordinates_
$$\begin{aligned}\varphi&\longrightarrow\exp(i\varepsilon)\varphi\simeq\varphi+i\varepsilon\varphi \\ \varphi^*&\longrightarrow \exp(-i\varepsilon)\varphi^*\simeq \varphi^*-i\varepsilon\varphi^*\end{aligned}$$
- It is said to belong to the $U(1)$ symmetry group

- The corresponding Noether _current_:
$$J^\mu=\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi+\pd{\Lagr}{(\partial_\mu\varphi^*)}\delta\varphi^*=i(\partial^\mu\varphi^*)\varphi-i\varphi^*(\partial^\mu\varphi)$$

- The corresponding conserved charge:
$$Q=i\int\left(\pd{\varphi^*}{t}\varphi-\varphi^*\pd{\varphi}{t}\right)\,d^3\bm{r}$$
- Substitute the [[#Equation and Fourier decomposition|Fourier decomposition]]:
$$\varphi=\int d^3\bm{k}\,N(k)\left[a(\bm{k})\exp(-ik\cdot x)+b^*(\bm{k})\exp(ik\cdot x)\right]$$
- The charge is then found to be:
$$Q=\int d^3\bm{k}\,N(k)\left[|a(\bm{k})|^2-|b(\bm{k})|^2\right]$$

- The _positive_ and _negative_ Fourier components contribute _different signs_ to the conserved charge
	- This represents _particles_ and _anti-particles_ once the field is quantised
## Local phase (gauge) symmetry
- Suppose the _phase_ of the complex scalar field $\varphi$ is a _function of space-time coordinates_
$$\varphi\to \exp(-i\varepsilon(x^\mu))\varphi \Longrightarrow \partial^\mu\varphi\to\exp(-i\varepsilon)[(\partial^\mu\varphi)-i(\partial^\mu\varepsilon)\varphi]$$
- It is _not a symmetry_ of the Klein-Gordon Lagrangian
	- The _extra term_ is proportional to the _Noether current_
	- Could be cancelled out by some _interaction term_

### The gauge-invariant Lagrangian
- Instead, simultaneously make the _gauge transformation_:
$$A_\mu\to A_\mu+\frac{1}{e}\partial_\mu \varepsilon$$

- The _constant_ $e$ gives the _representation_ of the $U(1)$ group
	- $U(1)$ has _infinitely many_ irreducible represntations, characterised by a _constant_

- Introduce the _covariant derivative_:
$$D_\mu=\partial_\mu+ieA_\mu\Longrightarrow D_\mu\varphi\to\exp(-i\varepsilon)D^\mu\varphi$$
- To make the complex scalar field Lagrangian _gauge-invariant_, replace with _covariant derivatives_

- This implies a presence of an _electromagnetic field_, hence add the _free field term_
	- $\Lagr_\text{KG}$: the _gauge-invariant Klein-Gordon Lagrangian_
	- $\Lagr_\text{em}$: the [[#Electromagnetic fields| free electromagnetic field Lagrangian]] $-F_{\mu\nu}F^{\mu\nu}/4$
$$\begin{aligned}\Lagr&=\Lagr_\text{KG}+\Lagr_\text{em}=\Lagr_\text{KG}-\frac{1}{4}F_{\mu\nu}F^{\mu\nu}\\&=(D_\mu\varphi)^* (D^\mu\varphi)-m^2\varphi^*\varphi-\frac{1}{4}F_{\mu\nu}F^{\mu\nu} \\ &=(\partial_\mu\varphi)^*(\partial^\mu\varphi)-m^2\varphi^*\varphi+ieA_\mu[(\partial^\mu\varphi^*)\varphi-\varphi^*(\partial^\mu\varphi)]+e^2A_\mu A^\mu\varphi^*\varphi-\frac{1}{4}F_{\mu\nu}F^{\mu\nu} \end{aligned}$$
- The _field-current interaction terms_ are included _in the covariant derivative term_
	- Extra term in current: see below
	- The term _quadratic_ in potential is _required to preserve gauge invariance_, takes into account the coupling of the extra term in current
- There is a $U(1)$ symmetry in the Lagrangian

- For the Lagrangian to be _invariant under a spacetime dependent phase transformation_, one _needs an electromagnetic field_
- One must also introduce a _covariant derivative_
	- It represents _mechanical momentum_
### Conserved current
- The gauge transformation:
$$\varphi\to \varphi-i\varepsilon\varphi\hspace{1.5cm}A_\mu\to A_\mu+\frac{1}{e}\partial_\mu\varepsilon$$

- This gives the _conserved current_:
$$J^\mu=-i\pd{\Lagr}{(\partial_\mu\varphi)}\varepsilon\varphi+i\pd{\Lagr}{(\partial_\mu\varphi^*)}\varepsilon\varphi^*+\frac{1}{e}\pd{\Lagr}{(\partial_\mu A_\nu)}\partial_\nu\varepsilon$$
- This can be split into two contributions, which are _separately conserved_

- The first two terms give the _Klein-Gordon current_:
$$J^\mu_\text{KG}=i[\varphi^*(D^\mu\varphi)-(D^\mu\varphi)\varphi^*]=i[\varphi^*(\partial^\mu\varphi)-(\partial^\mu\varphi)^*\varphi]-2e^2A^\mu\varphi^*\varphi$$
- It is _modified in the presence of a field_, and this current is seen in the _two extra terms of $\Lagr_\text{KG}$

- The third term only gets a contribution from $\Lagr_\text{em}$:
$$J^\mu_\text{em}\propto -F^{\mu\nu}\partial_\nu\varepsilon=-\partial_\nu(F^{\mu\nu}\varepsilon)+(\partial_\nu F^{\mu\nu})\varepsilon$$
- The first term _vanishes_, as a _total derivative cannot contribute to the conserved charge_, and fields _vanish_ on the surface of the integration region
- The current is then:
$$J^\mu_\text{em}=\partial_\nu F^{\mu\nu}$$
- Conservation is automatic due to _antisymmetry of the field tensor_

## Shifts in space-time and the energy-momentum tensor
- Let the Lagrangian density vary by some _total derivative_
- The _action_ then shifts _only at the boundary of spacetime_, and the _motion_ is _unaffected_

### Lagrangian shift by total derivative
- Using the proof for [[#Noether's theorem]], let the total derivative be:
$$\delta\Lagr=\partial_\mu\left(\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi\right)=\partial_\mu K^\mu$$
- The _conserved quantity_ is then:
$$\partial_\mu\left(\pd{\Lagr}{(\partial_\mu\varphi)}\delta\varphi-K^\mu\right)=0$$
- $K^\mu$ is some _quantity_ depending on the _type of transformation_ causing the shift

- The transformation can be _functions of the coordinates itself_

- Consider conservations in [[Analytical classical mechanics|classical mechanics]] due to _translations_
	- Invariance after spatial translation: momentum
	- Invariance after time translation: energy
- This leads to the _energy-momentum tensor_

### Noether current for scale invariance
- Let there be some _active scaling_, to transform the field with _scaling dimension_ $D$:
$$\phi(x)\to \lambda^{-D}\phi(\lambda^{-1}x)$$
- The Lagrangian and action in $n$ spacetime dimensions:
$$\mathcal{L}=\frac{1}{2}(\partial^{\mu}\varphi )(\partial_{\mu}\varphi)-\frac{1}{p!}\phi^{p} \qquad S=\int  d^nx\,\mathcal{L} $$
- For the action to be _scale invariant_, one finds:
$$D=\frac{n-2}{2}$$


- Let the dilatation be _infinitesimal_:
$$\lambda\equiv 1+\epsilon$$
- The shift in Lagrangian density:
$$\delta \mathcal{L}=\lambda^{4}\mathcal{L}(x^{\mu}+\epsilon x^{\mu})-\mathcal{L}(x^{\mu})=4\epsilon \mathcal{L}+\epsilon x^{\mu}\partial_{\mu}\mathcal{L}=\epsilon\partial_{\mu}(x^{\mu}\mathcal{L})$$

- From this, the _conserved current_ becomes:
$$J^{\mu}=\frac{\partial \mathcal{L}}{\partial(\partial_{\mu}\varphi)}-x^{\mu}\mathcal{L}$$
### Constant shift in space-time
- Given a _transformation_ in _space-time_, where the shift is _constant_:
$$x^\mu\to x^\mu+\varepsilon^\mu$$
- Then for a function of the coordinates, such as $\varphi$:
$$\varphi\to\varphi+\varepsilon^\mu\partial_\mu\varphi$$
- Then provided that $\Lagr$ _does not depend explicitly_ on $x^\mu$:
$$\displaylines{\Lagr=\Lagr(\varphi,\partial^\mu\varphi) \\ \Lagr(x^{\mu})\to \Lagr(x^{\mu}+\varepsilon^{\mu})=\mathcal{L}+\varepsilon^\mu\partial_\mu\Lagr}$$
- _Explicit dependence_ will make it into a form that does not make the _conserved quantity_ above

- One can also expand $\delta \Lagr$ in terms of the fields:
$$\delta\Lagr=\varepsilon^\nu\pd{\Lagr}{\varphi}\partial_\nu\varphi +\varepsilon^\nu\pd{\Lagr}{(\partial_\mu\varphi)}\partial_\nu\partial_\mu\varphi $$

- By _equating the differentials_ and relabelling indices:
$$\partial_\mu\left(\pd{\Lagr}{(\partial_\mu\varphi)}\partial_\nu\varphi-\delta^\mu_\nu\Lagr\right)=\partial_\mu \tenscom{T}{\mu}{\nu}=0$$
- This gives the _energy-momentum tensor_ $\tenscom{T}{\mu}{\nu}$
	- There is _no symmetry_ as $\mu$ and $\nu$ are _different types of indices_

- One can _raise_ one of the indices to get:
$$T^{\mu\nu}=\pd{\Lagr}{(\partial_\mu\varphi)}(\partial^\nu\varphi)-g^{\mu\nu}\Lagr$$
- The conservation is then written as:
$$\partial_\nu T^{\mu\nu}=0$$

- Relates to the [[Special Relativity#Energy-momentum tensor|energy-momentum tensor in special relativity]]

- For _multiicomponent fields_ (such as electromagnetic and complex fields):
$$T^{\mu\nu}=\pd{\Lagr}{(\partial_\mu\varphi_\alpha)}(\partial^\nu\varphi_\alpha)-g^{\mu\nu}\Lagr$$

- The _divergenceless_ condition gives some degree of _freedom_ to the tensor:
	- One can always add $\partial_{\nu}B^{\mu \nu}$ to the _Noether current_, for $B^{\mu \nu}=-B^{\nu \mu}$
$$T^{\mu\nu}\to T^{\mu\nu}+\partial_\lambda \Omega^{\lambda\mu\nu}$$
- The tensor must be _antisymmetric_ w.r.t. indices $\mu,\lambda$
- This is _automatically also conserved_ due to the antisymmetry
- This also allows the energy-momentum to be _symmetric_ in $\mu,\nu$
### Longitudinal wave on an elastic rod
- From a [[#The wave on an elastic rod|previous derivation]]:
$$\Lagr=\frac{1}{2}\rho\dot{\varphi}^2-\frac{1}{2}\kappa(\varphi')^2$$
- From the formula for the energy-momentum tensor above:
$$\displaylines{\tenscom{T}{tt}{}=\tenscom{T}{xx}{}=\frac{1}{2}\rho\dot{\varphi}^2+\frac{1}{2}\kappa(\varphi')^2=\Ham \\ T^{tx}=-\rho\dot{\varphi}\varphi'\hspace{1.5cm}T^{xt}=-\kappa\dot{\varphi}\varphi'}$$
- As the Lagrangian is _not Lorentz invariant_, $T$ is _not symmetric_

- From the _conservation laws_ for $T^{\mu\nu}$:
$$\displaylines{\pd{T^{tt}}{t}=-\pd{T^{xt}}{x} \\ \pd{T^{xx}}{x}=-\pd{T^{tx}}{x}}$$
- These are verified using the [[#Lagrangian density|equations of motion]]
- The first law relates the _rate of change of energy density_ $T^{tt}$ with the _flow of energy_ $T^{xt}$
- The second relates the _momentum flow_ $T^{xx}$ with the _rate of change of momentum density_ $T^{tx}$

### Relativistic scalar field
$$\Lagr=\frac{1}{2}(\partial^\mu\varphi)(\partial_\mu\varphi)-\frac{1}{2}\varphi^2$$
- The _energy-momentum tensor_ is:
$$T^{\mu\nu}=(\partial^\mu\varphi)(\partial^\nu\varphi)-g^{\mu\nu}\Lagr$$
- From this, one gets that the tensor is _symmetric_

### Free electromagnetic field
$$\Lagr=-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}=-\frac{1}{4}g^{\alpha\gamma}g^{\beta\delta}(\partial_\alpha A_\beta-\partial_\beta A_\alpha)(\partial_\gamma A_\delta-\partial_\delta A_\gamma)$$
- The energy-momentum tensor:
$$T^{\mu\nu}=-F^{\mu\lambda}(\partial^\nu A_\lambda)-g^{\mu\nu}\Lagr$$

- The form of this tensor is _not gauge invariant_, and _not symmetric_
	- Not gauge invariant as it expressed in terms of _potential_, not _field_
- Use the freedom in adding an antisymmetric tensor:
$$\displaylines{T^{\mu\nu}\to T^{\mu\nu}+\partial_\lambda \Omega^{\lambda\mu\nu} \\ \Omega^{\lambda\mu\nu}=-F^{\lambda\mu}A^\nu}$$
- In a _free field_, the divergence of the field tensor vanishes, hence one gets:
$$T^{\mu\nu}=\tenscom{F}{\mu}{\lambda}F^{\lambda\nu}-g^{\mu\nu}\Lagr$$
- This is _gauge invariant_ as it expressed in terms of _field strengths_
- It is also _symmetric_
- It is also _massless_ ($T^{\mu \nu}$ is traceless)

- Its elements are:
$$\displaylines{\Lagr=\frac{1}{2}(|\bm{E}|^2-|\bm{B}|^2) \\ T^{00}=\Ham=\frac{1}{2}(|\bm{E}|^2+|\bm{B}|^2)\hspace{1cm}T^{i0}=T^{0i}=(\bm{E}\times\bm{B})_j}$$
- As expected $T^{00}$ is the _energy density_
- $T^{i0}$ is the [[Electromagnetism#Energy flow in electromagnetic waves|Poynting vector]], the energy/momentum _flow_

### In general relativity
- In general relativity, the _invariant element of space-time_ is $\sqrt{-g}$, where $g=\text{det}(g_{\mu\nu})$, and $g_{\mu\nu}$ is the _metric tensor_
	- For the _Minkowski metric_, $g=-1$
- The _Einstein-Hilbert action_ is:
$$S=\int\Lagr(g^{\mu\nu},\varphi_i,\partial_\mu\varphi_i)\sqrt{-g}\,d^4x$$
- The term $\sqrt{-g}\, d^4x$ is some _volume element_ given the metric

- One should replace derivatives with the _covariant derivatives_
- From consideration of the [[General Relativity#Einstein's equation|Einstein field equation]]:
$$\delta S=\frac{1}{2}\int T_{\mu\nu}\sqrt{ -g }\,\delta g^{\mu \nu}\,d^{4}x$$

- $1/2$ comes from the fact that $T_{\mu\nu}$ is _symmetric_
- The corresponding _shift in the metric_:
$$\delta g^{\mu\nu}=\partial^\mu\varepsilon^\nu+\partial^\nu\varepsilon^\mu$$
- Symmetry requires that for _any coordinate transformation_:
$$0=\frac{1}{2}\int(\partial^\mu\varepsilon^\nu+\partial^\nu\varepsilon^\mu)\left(\sqrt{-g}\,T_{\mu\nu}-2\frac{\delta S}{\delta g^{\mu\nu}}\right)$$
- The _energy-momentum tensor_ is then:
$$T_{\mu\nu}=\frac{2}{\sqrt{-g}}\frac{\delta S}{\delta g^{\mu\nu}}$$

- By manipularing $\delta g_{\mu \nu}$, one can also obtain:
$$T_{\mu \nu}=2\frac{\partial \mathcal{L}}{\partial g_{\mu \nu}}-g_{\mu \nu}\mathcal{L}$$

## Angular momentum
- Define the antisymmetric tensor:
$$M^{\lambda\mu\nu}=x^\mu T^{\lambda\nu}-x^\nu T^{\lambda\mu}$$
- The _derivative_ w.r.t. $\lambda$, using the fact that $\partial_\mu T^{\mu\nu}=0$:
$$\partial_\lambda M^{\lambda\mu\nu}=\delta^\mu_\lambda T^{\lambda\nu}-\delta^\nu_\lambda T^{\lambda\mu}=0$$
- This is valid as long as $T$ is _symmetric_
- In other words, $M$ is also _conserved_

- This _conserved quantity_ is linked to some _rotation_

### Total angular momentum tensor
- Considering that $T^{0i}$ are the components of _momentum density_, define the _total angular momentum tensor_ $J^{\mu\nu}$
	- Example: $M^{012}=xT^{02}-yT^{01}$ gives the $z-$component of angular momentum density
$$J^{\mu\nu}=\int d^3\bm{r}M^{0\mu\nu}$$
- The familiar _3-angular momentum_, from the antisymmetric nature of $J^{\mu\nu}$:
$$J_{i}=\frac{1}{2}\varepsilon_{ijk}J^{jk}$$
- The _other non-zero components_:
$$J^{0j}=-J^{j0}=\int M^{00j} \, d^{3}\boldsymbol{r}=tP_{j}-R_{j}E $$
- If this quantity is conserved in time:
$$R_{j}=V_{j}t+\text{const.}$$
- In other words, the _centre of mass_ moves at _constant speed_ $V_j=P_j/E$

### Spin
- The _total angular momentum_ includes both the _orbital_ and _intrinsic_ parts
- In the _rest frame_ of an object, the _intrinsic angular momentum_ is known as the _spin_

- The _spin 4-vector_:
$$S^\mu=-\frac{1}{2}\varepsilon^{\mu\nu\alpha\beta}U_{\nu}J_{\alpha\beta}$$
- In the _rest frame_, as $U_0=1$ and $U_i=0$, one gets $S^{0}=0,S^i=J^i$, giving the _intrinsic angular momentum_

- $S^{\mu}$ is _always orthogonal_ to the 4-velocity, as $S^{\mu}U_{\mu}=0$, therefore it _only has 3 components_ in any frame

- There is _no covariant way_ to separate orbital and spin angular momentum, as $J$ is a 4-tensor and $S$ is a 4-vector

# Quantum fields
- Transitioning from _classical_ to _quantum_ fields is known as _second quantisation_

- _First quantisation_ is the process of _replacing_ classical variables with quantum _operators_:
$$[\hat{q},\hat{p}]=i$$
- Natural units: $\hbar=1$

- _Second quantisation_ replaces the _field variable_ $\varphi(x,t)$ and and the _conjugate momentum density_ $\pi(x,t)$ by operators:
$$[\hat{\varphi}(x,t),\hat{\pi}(x',t)]=i\delta(x-x')$$
- $x$ and $x'$ are _not dynamical variables_ but are only _labels_ for _values_ of the fields

## Fourier decomposition to second quantisation
- The _field_ satisfying the Euler-Lagrange equation is replaced by an _operator_, and the [[#Fourier decomposition of field|Fourier expansion]] _coefficients_ are also _operators_:
$$\hat{\varphi}(x,t)=\int  \, dk\,N(k)\Big[\hat{a}(k)\exp[i(kx-\omega t)]+\hat{a}^{\dagger}(k)\exp[-i(kx-\omega t)]\Big] $$
- While $\hat{\varphi }$ is _Hermitian_, $\hat{a}$ is _not_

- The _Hamiltonian_ is then:
$$\hat{H}=\int  \, dk\,N(k) \frac{1}{2}\omega(k)\big[\hat{a}(k)\hat{a}^{\dagger}(k)+\hat{a}^{\dagger}(k)\hat{a}(k)\big] $$
- Comparing with the [[Quantum Harmonic Oscillator]]:
$$\hat{H}=\frac{1}{2}\omega(\hat{a}\hat{a}^{\dagger}+\hat{a}^{\dagger}\hat{a})$$
- Hence, $\hat{a}(k)$ can be identified as the _annihilation operator_
- $\hat{a}^{\dagger}(k)$ can be identified as the _creation operator_
- They _add/remove_ one _quantum of excitation_ from the _mode_ $k$
- The quanta can be interpreted as _particles_

- Example: the _electromagnetic field_ can be [[Quantum electrodynamics|quantised]], with the particles being _photons_

- The _ladder operators_ of the QHO satisfy:
$$[\hat{a},\hat{a}^{\dagger}]=1$$
- Analagously, the commutation relation for field ladder operators is:
$$\begin{align}N(k)[\hat{a}(k),\hat{a}^{\dagger}(k')]&=\delta(k-k') \\ [\hat{a}(k),\hat{a}^{\dagger}(k')]&= (2\pi)\,2\omega(k)\,\delta(k-k')\end{align}$$

- In 3 spatial dimensions:
$$[\hat{a}(\boldsymbol{k}),\hat{a}^{\dagger}(\boldsymbol{k}')]=(2\pi)^{3}\,2\omega(\boldsymbol{k})\,\delta^{3}(\boldsymbol{k}-\boldsymbol{k}')$$
- Trivially,
$$[\hat{a}(\boldsymbol{k}),\hat{a}(\boldsymbol{k}')]=[\hat{a}^{\dagger}(\boldsymbol{k}),\hat{a}^{\dagger}(\boldsymbol{k}')]=0$$
- By _expanding_ both $\hat{\varphi}$ and $\hat{\pi}$, one can derive:
$$[\hat{\varphi}(\boldsymbol{r},t),\hat{\pi}(\boldsymbol{r},t)]=i\,\delta^{3}(\boldsymbol{r}-\boldsymbol{r}')$$
- Other commutation relations:
$$[\hat{\varphi}(\boldsymbol{r},t),\hat{\varphi}(\boldsymbol{r}',t)]=[\hat{\pi}(\boldsymbol{r},t),\hat{\pi}(\boldsymbol{r}',t)]=0$$

## Intepretation
- The _positive frequency_ term of the field is associated with _annihliation_:
$$\hat{a}(\boldsymbol{k})\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]$$
- Energy $\hbar\omega$ is _released_ in the annihilation process

- Similarly, the _negative frequency_ term is associated with _creation_:
$$\hat{a}^{\dagger}(\boldsymbol{k})\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]$$
- Energy $\hbar\omega$ is _absorbed_ in the creation process

## Antiparticles
- A _Hermitian_ field describes particles that are _identical to their antiparticles_

- A _complex/non-Hermitian_ field describes particles with corresponding _antiparticles_
- The [[#Global phase symmetry|conserved charge]] and Hamiltonian:
$$\begin{align}\hat{Q}&=\int  \, d^{3}\boldsymbol{k}\,N(\boldsymbol{k})\Big[\hat{a}^{\dagger}(\boldsymbol{k})\hat{a}(\boldsymbol{k})-\hat{b}^{\dagger}(\boldsymbol{k})\hat{b}(\boldsymbol{k})\Big] \\ \hat{H}&=\int  \, d^{3}\boldsymbol{k}\,N(\boldsymbol{k})\omega(\boldsymbol{k})\Big[\hat{a}^{\dagger}(\boldsymbol{k})\hat{a}(\boldsymbol{k})+\hat{b}^{\dagger}(\boldsymbol{k})\hat{b}(\boldsymbol{k})\Big]\end{align}$$

- Particles _created_ by $\hat{a}$ and $\hat{b}$ have the _same energy_, but _opposite charge_
- Hence, in $\hat{\varphi}$:
	- The _positive frequency_ part will _annihilate a particle_
	- The _negative frequency_ part will _create an antiparticle_
- The _opposite_ is true in $\hat{\varphi}^{\dagger}$ 
	- _Create a particle_ and _annihilate an antiparticle_

# Symmetry breaking
- One breaks the symmetry of the _solutions/trajectories_, instead of the Lagrangian
	- The _dynamical laws_ are invariant under symmetry, but the _particular solutions_ are not
- In _quantum states_, one can get _spontaneous symmetry breaking_ for the _ground state_

- Types of symmetries to break:
	- _Global symmetry_ (spacetime _invariant_)
	- _Gauge symmetry_ (_dependent_ on spacetime coordinates)

## Breaking of the global U(1) symmetry
- The [[#Complex scalar fields|complex Klein-Gordon field]]:
$$\Lagr=(\partial^\mu\varphi^*)(\partial_\mu\varphi)-m^2\varphi^*\varphi$$
- Consider adding an _additional term_ with _higher powers_ of the field
	- Keep the _global symmetry_
$$\displaylines{V(\varphi)=m^2\varphi^*\varphi+\frac{\lambda}{2}(\varphi^*\varphi)^2 \\ \Lagr=\partial^\mu\varphi\partial_\mu\varphi-m^2\varphi^*\varphi-\frac{\lambda}{2}(\varphi^*\varphi)^2}$$
- The _equation of motion_:
$$\partial_\mu \partial^\mu\varphi+m^2\varphi+\lambda(\varphi^*\varphi)\varphi=0$$
- The term can be seen as a _self-interaction_ with _strength_ $\lambda$

- The corresponding _Hamiltonian density_:
$$\Ham=\pi^*\pi+m^2\varphi^*\varphi+\frac{\lambda}{2}(\varphi^*\varphi)^2$$
- For a positive-definite, $\Ham$, $\lambda>0$
- This also gives the _possibility_ that $m^2<0$
- With $-m^2>0$, one _shifts_ the state of _minimum energy_
	- The original equilibrium state is now an _unstable equilibrium_
![[Mexican hat potential.png]]
- There are then _infinitely many ground states_ given:
$$\varphi_0^*\varphi_0=\frac{-m^2}{\lambda}$$

- Each state _does not obey the symmetry on its own_, so the symmetry is said to be _spontaneously broken_
	- The phase transformation _changes the state_
	- The _phase_ of the state is _spontaneously chosen_ by the system, and can take _any value_

- Choose the state (and choose _sign convention_ such that $m^2>0$)
	- $V(\varphi)=-m^2(\varphi^*\varphi)+(\lambda/2)(\varphi^*\varphi)^2$
$$\varphi_0=\sqrt{\frac{m^2}{\lambda}}$$

### Goldstone's Theorem
- Given a _complex variation_ in the field, dependent on the _new, real fields_ $\chi_1$ and $\chi_2$:
$$\varphi=\varphi_0+\frac{1}{\sqrt{2}}(\chi_1+i\chi_2)$$
- The fields are a _shift from equilibrium_, with directions _along_ and _perpendicular_ to the _line of minima_ respectively

- One can then write the Lagrangian and Hamiltonian as:
$$\displaylines{\Lagr=\frac{1}{2}(\partial^\mu\chi_1)(\partial_\mu\chi_1)+\frac{1}{2}(\partial^\mu\chi_2)(\partial_\mu\chi_2)-V(\varphi_0)-m_1\chi_1^2+O(\chi^3) \\ \\ \Ham=\frac{1}{2}\left(\pd{\chi_1}{t}\right)^2+\frac{1}{2}\left(\pd{\chi_2}{t}\right)^2+\frac{1}{2}\left|\nabla\chi_1\right|^2+\frac{1}{2}\left|\nabla\chi_2\right|^2+V(\varphi_0)+m_1\chi_1^2+O(\chi^3)}$$
- The corresponding _Klein-Gordon equations_:
$$\partial_\mu\partial^\mu\chi_1+2m^2\chi_1=0\hspace{1.5cm}\partial_\mu\partial^\mu\chi_2=0$$
- There is _no term for the imaginary part_, while the real part has a _positive quadratic term_
- This _asymmetry_ corresponds to the _energy cost_ in different directions of the potential energy function

- By _inspecting_ the equations, one gets that for $\chi_1$, the _dispersion relation_ is:
$$\omega=\pm\sqrt{k^2+2m^2}$$
- For the field $\chi_2$, one gets that the particle is _massless_
	- Corresponds to dispersion $\omega=k$
	- It is known as the _Goldstone field_ (creating the Goldstone boson)

- _Goldstone's Theorem_ states that for _every spontaneously broken symmetry_, there will be a _field of massless quanta_

## Breaking (local) gauge symmetry
- For the _local gauge transformation_:
$$\varphi\to\exp(i\varepsilon(x^\mu))\varphi$$
- The Lagrangian must have some _coupling to an electromagnetic field_
- Also add the quartic term in the _potential_ above:
$$\Lagr=-\frac{1}{4}F_{\alpha\beta}F^{\alpha\beta}+(D_\mu\varphi)^*(D^\mu\varphi)-V(\varphi)$$
- Once again, this _triggers_ spontaneous symmetry breaking and _non-zero_ $\varphi_{0}$

- With $\varphi_0\neq0$, the _covariant derivative_ contributes an extra term
$$(ieA_\mu\varphi_0)^*(ieA^\mu\varphi_0)=\frac{e^2m^2}{\lambda}A_\mu A^\mu$$
- In the _Lorenz gauge_ where $\partial_\mu A^\mu=0$
	- E-L equation for the system _in the ground state_
$$\partial_\nu\partial^\nu A_\mu+\frac{2e^2m^2}{\lambda}A_\mu=0$$
- The _dispersion relation_ for $A_\mu$ is then:
$$\omega=\pm\sqrt{k^2+2e^2m^2/\lambda}$$
- The field $A_\mu$ is said to _gain mass_ $em\sqrt{2/\lambda}$

## Higgs mechanism
- Write the perturbation:
$$\varphi=\varphi_0+\frac{1}{\sqrt{2}}(\chi_1+i\chi_2)$$
- The _covariant derivative_ becomes:
$$D_{\mu}\varphi=\frac{1}{\sqrt{ 2 }}\left({\partial}_{\mu}\chi_{1}+i\partial_{\mu}\chi_{2} \right)+ie\varphi_{0}A_{\mu}+\dots$$

- Then make the _gauge transformation_:
$$
A_{\mu}\to A_{\mu}-\frac{1}{\sqrt{ 2 }e\varphi_{0}}\partial_{\mu }\chi_{2}
$$

- This _removes all_ $\chi_2$ terms ("eats" the Goldstone boson):
$$
\begin{aligned}
\mathcal{L}&=-\frac{1}{4}F_{\mu \nu} F^{\mu \nu}+e^2\varphi_{0}^2A_{\mu}A^\mu+\frac{1}{2}(\partial_{\mu}\chi_{1})(\partial^{\mu}\chi_{1})-V(\varphi) \\ &=-\frac{1}{4}F_{\mu \nu} F^{\mu \nu}+\frac{e^2m^{2}}{\lambda}A_{\mu}A^\mu+\frac{1}{2}(\partial_{\mu}\chi_{1})(\partial^{\mu}\chi_{1})-m^{2}\chi_{1}^{2}-V(\varphi_{0})
\end{aligned}
$$
- This is also equivalent to a _change of phase_ of the scalar field, making it _real_ and removing $\chi_2$
	- For a _local phase change_, one can make a different change at every point to _remove $\chi_2$ at every point_
- In summary, for a _local_ gauge symmetry broken, the _previously massless_ field will "eat" the Goldstone field then _gain mass_

- The [[Rotations and Lie Algebra|Lie group]] works on an $\mathbb{R}^n$ manifold instead of a set
- If symmetry is _broken_ into some _subgroup $H$_, that is on an $\mathbb{R}^m$ manifold
	- For _global symmetry_, there are $n-m$ _Goldstone bosons_
	- For _local gauge symmetry_, there are $m$ _massive particles_ formed from originally massless quanta

## The standard model
- In the _standard model_, the electromagnetic and weak interactions are given by the _Lie group_ $SU(2)\otimes U(1)$

# The propagator
## The quantum particle
- The _Lagrangian density_:


- This produces the _non-relativistic, time-dependent Schrodinger equation_

- With some _interaction/forcing term_:
$$i\hbar\pd{\Psi}{t}+\frac{\hbar^2}{2m}\pd{^2\Psi}{x^2}=F(x,t)$$
- Following the approach of a similar [[Analytical classical mechanics#Propagators and causality|classical problem]], write down the _Green's function_:
$$\psi=\int\,dt'\int\,dx'G(x,t,x',t')\,F(x',t')$$
- Conduct _Fourier transforms_ with the functions $\exp{(-ipx/\hbar)}$ and $\exp{(-iEt/\hbar)}$
- This gives:
$$\displaylines{\left(E-\frac{p^2}{2m}\right)G(p,E)=1 \\ G(p,t,t')=\int\exp\left(-\frac{iE}{\hbar}(t-t')\right)\frac{1}{E-p^2/2m}\,\frac{dE}{2\pi\hbar}}$$
- This gives _a pole on the real axis_:
![[Quantum greens function pole.png|400]]
- From _causality_, the integration contour for $t>t'$ must pass _above_ the pole
## Klein-Gordon field
- The Green's function:
$$G(x^\mu)=\int\,dp^\nu\frac{\exp(-ip_\mu x^\mu)}{p^\mu p_\mu-m^2}$$
- It is _Lorentz invariant_
- The _poles_ arise when $p_0^2-p_i p^i=m^2$
- On the $p_0$ _axis_, the poles are at $\pm\sqrt{p_i^2+m^2}$ 

- One can use the $i\varepsilon$ _prescription_, moving both poles _up the axis_:
$$p^0\to p^0+i\varepsilon$$

- Causality dictates that $G(x^\mu)$ _disappears outside the forward light cone_

## Feynman prescription
- In quantum fields, to preserve causality, use the _Feynman prescription_:
$$G(x^\mu)=\int\,dp^\nu\frac{\exp(-ip_\mu x^\mu)}{p^\mu p_\mu-m^2+i\varepsilon}$$
- This gives _one pole for each half-plane_
- The Feynman propagator is _non-zero everywhere_
- This corresponds to _having antiparticles travelling backwards in time_
- This _does not affect causality of measurement_
![[Feynman poles.png]]
# The Dirac field
- Spacetime is _Lorentz invariant_
- The Lorentz transformation:
$$x^\mu\longrightarrow\tenscom{\Lambda}{\mu}{\nu}x^\nu$$
- The transformations form the _Lorentz group_

- The _most general Lagrangian_ for a field _transforming as its representations_ must then be able to describe relativistic objects

- The _representations_ of the group:
$$1,$$
- One can have a _scalar field_ transforming according to the _identity representation_
- This leads to the [[#Relativistic scalar field|Klein-Gordon field]]

- The Dirac equation reflects the fact that _numbers of particles can change_

## The purely quantum mechanical field
- Let there be the Lagrangian:
$$\Lagr=\Psi^*\partial_0\Psi+(\nabla\Psi)^*(\nabla\Psi)+$$
- This leads to the _time-dependent Schrodinger equation_

- It respects $U(1)$ symmetry:
$$\Psi\to$$
- The _conserved current_ is:
$$\pd{\Lagr}{}=\Psi^*\Psi$$
- As the _probability current_ is conserved, one _cannot change the number of particles_

## Klein-Gordon but quantum mechanical
- Take the [[#Complex scalar fields|complex scalar field]]:
$$\Lagr=(\partial_\mu\varphi^*)(\partial^\mu\varphi)-m^2\varphi^*\varphi$$
- The _Fourier solution_ $\exp[i(\omega t-kx)]$ reflects that the relativistic relation:
$$E^2=p^2+m^2$$
- However, this means there is _no lower bound to energy_

- The _Noether current_ from the $U(1)$ symmetry is:
$$J^0=i\partial^0\varphi^*\varphi$$
- This is _not positive-definite_ and therefore _cannot be interpreted as a probability density_

## The Dirac equation
- To construct an equation which has _only first derivatives_
- Establishing _arbitrary constants_ $\gamma^\nu$ and $m$:
$$(i\gamma^\nu\partial_\nu-m)\psi=0$$
- Applying $(i\gamma^\mu\partial_\mu+m)$ on _both sides_, recognising the symmetry of the first term and using an _anticommutator_
$$\left(\frac{1}{2}\{\gamma^\mu,\gamma^\nu\}\partial_\mu\partial_\nu-m^2\right)\psi=0$$
- In order to reproduce the _Klein-Gordon equation_:
$$\{\gamma^\mu,\gamma^\nu\}=\gamma^\mu\gamma^\nu+\gamma^\nu\gamma^\mu=2\eta^{\mu\nu}$$
- Where $\eta^{\mu\nu}$ is the _Minkowski metric_

- One can then see that $\gamma^\mu$ are _not scalars_
- Instead, they are $4\times 4$ _matrices_:
$$\gamma^0=\pmatrix{I_2&0 \\ 0&I_2}\hspace{1cm}\gamma^j=\pmatrix{0&\sigma_j \\ -\sigma_j &0}$$
- Where $I_2$ is the $2\times2$ _identity matrix_, and $\sigma_j$ are the _Pauli spin matrices_

- $\psi$ is then a _4-component complex vector_
	- They represent the _spin states of the particle and antiparticle_

## The Dirac Lagrangian
- The Dirac equation is the _Euler-Lagrange equation_ of the Dirac Lagrangian:
$$\Lagr=i\bar\psi\gamma^\mu\partial_\mu\psi-m\bar\psi\psi$$
- Here, to make $\bar\psi\psi$ _Lorentz invariant_:
$$\bar\psi=\psi^\dagger\gamma^0$$
- One can _add a total derivative_ to make the Lagrangian _symmetric_ in $\bar\psi$ and $\psi$

- The _equation of motion_ for $\bar\psi$:
$$0=\pd{\Lagr}{\bar\psi}=(i\gamma^\mu\partial_\mu-m)\psi$$
- The corresponding equation for $\psi$:
$$i\partial_\mu\bar\psi\gamma^\mu=-m\bar\psi$$

### The Hamiltonian
- The corresponding _Hamiltonian_, taking into account that it is a _scalar_
$$\displaylines{\Ham=\pi\pd{\psi}{t}+\pd{\bar\psi}{t}\bar\pi-\Lagr \\ \pi=\pd{\Lagr}{\dot\psi}=i\bar\psi\gamma^0=i\psi^\dagger\hspace{1cm}\bar\pi=0}$$
- Putting everything together:
$$\displaylines{\Ham=\psi^\dagger(-i\bm{\alpha}\cdot\nabla+\beta m)\psi \\ \gamma^0=\beta\hspace{1cm}\gamma^i=\beta\alpha^i}$$
- The Hamiltonian is _not Loentz invariant_
## Dirac energy-momentum tensor
- Computing the tensor:
$$T^{\mu\nu}=\pd{\Lagr}{(\partial_\mu\psi)}\partial^\nu\psi-\eta^{\mu\nu}\Lagr=i\bar\psi\gamma^\mu\partial^\nu\psi$$
- It is _not symmetric in its indices_

- The _angular momentum tensor_:
$$M^{\lambda\mu\nu}=x^\mu T^{\lambda\nu}-x^\nu T^{\lambda\mu}=i\bar\psi()$$
- This quantity is _not conserved_
- This only corresponds to _angular momentum_

- To create a _conserved quantity_, add:
$$S^{\lambda\mu\nu}=\frac{i}{4}\bar\psi()$$
- The _total_ of these two tensors is _conserved_

- The classical angular momentum:
$$\displaylines{\bm{J}=\int\,d^3\bm{x}\left[\psi^\dagger()\right] \\ \Sigma_i=\pmatrix{\sigma_i&0\\0&\sigma_i}}$$
- The _eigenvalues_ of $\Sigma_i$ are the values of _spin_
- The two "parts" reflect the _particles and antiparticles_

## Conserved current
- From the U(1) symmetry of the Lagrangian:
$$J^\mu=\bar\psi\gamma^\mu\psi$$

## External fields
- To couple to an _external field_:
$$\displaylines{ D_\mu=\partial_\mu+ieA_\mu \\ \Lagr=i\bar\psi\gamma^\mu D_\mu\psi-m\bar\psi\psi}$$
- The resulting _equation of motion_:

- Where:
$$[\gamma^\mu,\gamma^\nu]=\sigma^{\mu\nu}$$
- This is the effect of _spin-orbit coupling_