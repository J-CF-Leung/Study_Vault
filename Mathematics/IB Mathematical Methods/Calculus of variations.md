# Functionals and extremisation
## Definition of functionals
- Consider an _integral involving some function_ $y(x)$:
$$G=\int_{\alpha}^\beta \left[y'(x)^2-y(x)^2\right]\,dx$$
- This integral is _independent of $x$_
- Instead, the value _depends on the function $y$_

- This is denoted a _functional_ $G[y]$

- A real _function takes a set of variables as input_, and gives a _real number as output_
$$f: \{y_k\}\to f(\{y_k\})\in\mathbb{R}$$
- A _functional takes a continuous infinity of variables as input_, and gives a _real number as output_
$$G:y(x)\rightarrow G[y]\in\mathbb{R}$$

- A functional can either _implicitly or explicitly_ depend on $x$
$$G[y]=\int_{\alpha}^\beta f(y,y',y'',\dots,;x)\,dx$$
- There may be _any number of dependent variables_ $\{y_i\}$ and _dependent variables_ $\{x_i\}$
- A typical functional is of the form:
$$G[y]=\int_\alpha^\beta f(y,y';x)\,dx$$
- A typical problem is to look for a _local extremum of a functional_
- Applications: _Fermat's Principle_ in optics, _Hamilton's Principle_ in mechanics

## Functional derivatives
- Consider the effect of changing a function $y(x)$ to a _nearby function_ $y(x)+\delta y(x)$
- The _first-order variation_ of $G$ is:
$$\begin{aligned}\delta G&=G[y+\delta y]-G[y] \\ &=\int_\alpha^\beta f(y+\delta y,y'+(\delta y)';x)\,dx-\int_\alpha^\beta f(y,y';x)\,dx \\ &=\int_\alpha^\beta \left[\pd{f}{y}\delta y+\pd{f}{y'} (\delta y)'\right]\, dx+\dots \\ &=\left[\delta y\pd{f}{y'}\right]_\alpha^\beta +\int_\alpha^\beta \delta y\left[\pd{f}{y}-\frac{d}{dx}\left(\pd{f}{y'}\right)\right]\,dx+\dots\end{aligned}$$
- If the _end-points are fixed_, meaning $\delta y(\alpha)=\delta y(\beta)=0$:
$$\delta G=\int_\alpha^\beta \delta y(x)\left[\pd{f}{y}-\frac{d}{dx}\left(\pd{f}{y'}\right)\right]\,dx+\dots$$
- Hence, one can define the _functional derivative_ of $G$:
$$\frac{\delta G}{\delta y(x)}\equiv \pd{f}{y}-\frac{d}{dx}\left(\pd{f}{y'}\right)$$
- This is a _function of $x$_
- Hence, $G$ is _stationary_ when:
$$\frac{d}{dx}\left(\pd{f}{y'}\right)=\pd{f}{y}$$
- This is the _Euler-Lagrange equation_
- The partial derivatives are _formal_, meaning $y$ and $y'$ change _independent of each other_
- $d/dx$ is a _full derivative_ w.r.t. $x$, meaning it brings changes in $y$ and $y'$:
$$\frac{df}{dx}=\pd{f}{x}+\pd{f}{y}y'+\pd{f}{y'}y''$$

- Application: the _geodesic_ (shortest distance) in a Euclidean plane
	- Euclidean metric: $y'=\text{const.}$, a straight line

- If the function $f$ is not _explicitly dependent on $x$_, i.e. $\partial f/\partial x=0$, the E-L equation can be _reduced to a first order DE_
$$\displaylines{\pd{f}{x}=0 \\ y'\pd{f}{y'}-f=\text{const.}}$$

## Multiple functions as input
- Let a functional take _multiple functions and their derivatives as input_:
$$G[y_i]=\int_\alpha^\beta f(y_1,y_1',\dots,y_2,y_2'\dots y_i,y_i'\dots)\,dx$$
- Then, to _minimise_ $G$ with appropriate _boundary conditions_, _each function follows the E-L equation_:
$$\frac{d}{dx}\left(\pd{f}{y_i'}\right)=\pd{f}{y_i}$$

# Applications
## Geodesics
- Write $|d\bm{r}|$ as a _function of infinitesimal change in coordinates_
- Use one coordinate as the _explicit variable_, with the others being the _input functions_

- _Euclidean_ space:
$$s=\int |d\bm{r}|=\int \sqrt{dx^2+dy^2}=\int \sqrt{1+y'^2}\,dx$$
- From using the Euler-Lagrange equations, the geodesic is a _straight line_:
$$y''=0\longrightarrow y=A+Bx$$

- On a _unit sphere_:
$$s=\int |d\bm{r}|=\int \sqrt{(d\theta)^2+\sin^2\theta(d\phi)^2}=\int\sqrt{1+\sin^2\theta(\phi')^2}\,dx$$
- One gets the geodesic as:
$$\cot\theta=a\cos(\phi-\phi_0)$$
- $a$ and $\phi_0$ depend on _end-points_
- This is a _great circle_, where the centre _coincides with the centre of the sphere_

## Sturm-Liouville theory
- The calculus of variations is not limited to considering functionals themselves, but also _functions of functionals_, such as _ratios_

- Consider functionals containing a [[Sturm-Liouville Theory#Adjointness and Sturm-Liouville operators|Sturm-Liouville operator]] $\Lagr$, with the [[Sturm-Liouville Theory#Weight functions and converting to Sturm-Liouville form|weight function]] $w$:
$$\displaylines{F[y]=\int_\alpha^\beta y\Lagr y\,dx=\int_\alpha^\beta \left\{\rho(x)(y')^2+\sigma(x)y^2\right\}\,dx \\ G[y]=\int_\alpha^\beta w(x)y^2\,dx}$$
- $G[y]$ can be considered the _norm of $y$_ w.r.t. weight function $w$

- Applying the equations above and _fixing the end-points_ such that the _boundary terms vanish_:
$$\displaylines{\frac{\delta F}{\delta y}=2\Lagr y \\ \frac{\delta G}{\delta y}=2wy}$$
- Consider the _ratio_:
$$\Lambda[y]=\frac{F[y]}{G[y]}$$
- Considering the _first-order variation_ of $\Lambda$:
$$\delta \Lambda=\frac{F+\delta F}{G+\delta G}-\frac{F}{G}=\frac{1}{G}\left[\delta F-\frac{F}{G}\delta G\right]$$
- Therefore, the _functional derivative_ is:
$$\frac{\delta\Lambda}{\delta y}=\frac{2}{G}\left[\Lagr y-\Lambda wy\right]$$
- So, when $\Lambda$ is _extremised_, with value $\lambda$:
$$\Lagr y=\lambda wy$$
- This is simply the _Sturm-Liouville eigenvalue problem_
- Therefore, $\Lambda[y]$ is _extremised by the eigenfunctions of $\tilde{\Lagr}=w^{-1}\Lagr$_, with the _eigenvalues being the extremum value_

## Fermat's Principle
- Fermat's Principle in [[Optics|optics]] states that the _path taken by a light ray_ between two points, in a material of _variable refractive index_ $\mu(\bm{r})$ will always be the path that _minimises the optical path length_ $P$
$$P=\int\mu(\bm{r})\,dl$$
- Using $x$ as the explicit variable, $P$ can be written as:
$$P[y,z]=\int\mu(y,z;x)\sqrt{1+(y')^2+(z')^2}\,dx$$
- The condition for a stationary path length is then:
$$\frac{\delta P}{\delta y(x)}=0 \hspace{1cm} \frac{\delta P}{\delta z(x)}=0$$
- For a _constant_ $\mu$, the condition is simply $y''=z''=0$ which is a _straight line_
- For a _variable_ $\mu$, the Euler-Lagrange equations lead to the condition:
$$\frac{\mu}{\sqrt{1+(y')^2}}=\mu\sin\theta=c$$

## Hamilton's Principle
- Let there be $n$ particles, so there are $3n-$degrees of freedom in general
- The degrees of freedom are characterised using _generalised coordinates_ $\{q_i\}$
- It has _kinetic energy_ $T$ and _potential energy_ $V$
- The _Lagrangian_ is defined as:
$$\Lagr=T-V$$
- The _action_ of a certain path is defined by:
$$S[\{q_i\}]=\int \Lagr(\{q_i(t)\},\{\dot{q}_i(t)\},\dots;t)\,dt$$
- _Hamilton's Principle_ states that motion alweays takes the _path of extremised action_
- The _Euler-Lagrange equation_ is then:
$$\frac{d}{dt}\left(\pd{\Lagr}{\dot{q}_i}\right)-\pd{\Lagr}{q_i}=0$$
- This leads to [[Analytical classical mechanics]]

# Constrained variation
## Lagrange multipliers
- From Taylor's theorem, a change in $f(\bm{x})$ can be written as:
$$\delta f=f(\bm{x}+\delta\bm{x})-f(x)=\nabla f\cdot\delta\bm{x}+\dots$$
- For small $\delta\bm{x}$:
$$df=\nabla f\cdot\delta\bm{x}$$
- Consider the _contours_ of $f$, where it has _constant value_ 
- Let there be some _path_ satisfying $p(\bm{x})=0$, _not reaching the extremum of $f$_

- At a _local extremum of $f$_, _any arbitrary displacement $d\bm{l}$ does not change $f$_:
$$\nabla f\cdot d\bm{l}=0 \hspace{0.6cm}\forall d\bm{l}\hspace{0.6cm}\text{ at the extremum}$$
- If one were to find the extremum of $f$ _along the path_, there is a _restriction_:
$$dp=\nabla p\cdot d\bm{l}=0$$
- At the highest point _on the path_, all $d\bm{l}$ that are orthogonal to $\nabla p$ must _also be orthogonal to $\nabla f$_
- Hence, $\nabla p$ and $\nabla f$ must be _parallel or anti-parallel_
- Defining the _Lagrange multiplier_ $\lambda$, this becomes:
$$\displaylines{\nabla f-\lambda\nabla p=0 \\ p(\bm{x})=0}$$
- This becomes an _unconstrained extremisation_ of the function $\phi$:
$$\displaylines{\phi(\bm{x},\lambda)=f(\bm{x})-\lambda p(\bm{x}) \\ \nabla\phi=0}$$

- If the function $f$ has $N$ variables $\{\xi\}$, subject to $k<N$ constraints $p_i(\{\xi\})$, then $k$ _Lagrange multipliers will be required_:
$$\phi(\{\xi\};\lambda_1,\lambda_2,\dots\lambda_k)=f(\{\xi\})-\sum_{i=1}^k \lambda_ip_i(\{\xi\})$$
## Generalisation to functionals
- To generalise to functionals, one can consider an _infinite number of variables_
- The problem is to extremise $G[y]$ while there is the constraint $P[y]=0$
- Then, the function to _extremise without constraint_ is:
$$\Phi_\lambda[y]=G[y]-\lambda P[y]$$
- To extremise, assuming _boundary terms are zero_, one can use the Euler-Lagrange equation:
$$\displaylines{\frac{\delta G}{\delta y}-\lambda \frac{\delta P}{\delta y}=0 \\ P[y]=0}$$
- Therefore, one would have to _solve the Euler-Lagrange equations for both $G$ and $P$_

### Example: Sturm-Liouville...again
- Another formulation of the Sturm-Lioville problem is to consider the _extremisation of $F[y]$_:
$$F[y]=\int_\alpha^\beta y\Lagr y\,dx=\int_\alpha^\beta \left\{\rho(x)(y')^2+\sigma(x)y^2\right\}\,dx$$
- This is subject to the _contraint_ that $y$ is of unit norm w.r.t. weight function $w$, or:
$$G[y]=\int_\alpha^\beta w(x)y^2\,dx=1$$
- This requires the _unconstrained extremisation_ of:
$$\Phi_\lambda[y]=F[y]-\lambda(G[y]-1)=(F[y]-\lambda G[y])+\lambda$$
- Using results [[#Application to Sturm-Liouville theory|above]], this gives:
$$2\Lagr y-2\lambda wy=0$$
- This gives an _eigenvalue problem_, same result as _maximising the ratio $\Lambda=F/G$_

# The Rayleigh-Ritz method
- Consider the _Sturm-Liouville problem_ of finding the eigenvalues $\lambda$
- $\lambda$ is an _extremal value of $\Lambda=F/G$_
- If $\rho>0$ and $\sigma\geq0$, then $\Lambda\geq0$
	- $w(x)$ is defined to be positive
- Therefore, _one of the extremal eigenvalue_ $\lambda_0$ is an _absolute minimum_:
$$\lambda_0=\Lambda[y_0]\geq0$$
- $y_0$ is the _eigenfunction_ corresponding to $\lambda_0$
- Assuming no degeneracy:
$$\Lambda[y]\geq\lambda_0$$
	- Equality holds iff $y=y_0$
	 - Proof: Expand $y$ _in terms of the eigenfunctions_

- This means one can find an _upper bound_ for $\lambda_0$
- Make an _educated guess for the eigenfunction_ $y_\text{trial}$, then:
$$\Lambda[y_\text{trial}]\geq\lambda_0$$
- Equality only holds _iff the trial function is exactly right_
- Since $\Lambda$ is _stationary at that point_, in most cases, it will be _close to the actual value_

- One can choose $y_\text{trial}$ to depend on _one or more parameters_ $\{a_1,a_2,\dots\}$
- The inequality _holds for all values of the parameters_
- Hence, the bound can be _refined by minimising $\Lambda$_ w.r.t. the parameters:
$$\lambda_0\leq \min_{\{a_i\}}\Lambda(\{a_i\})$$

- Application: the [[Topics in Quantum Mechanics#The Variational Principle|Variational Principle in Quantum Mechanics]]

- The _next-lowest eigenvalue_ $\lambda_1$ can be estimated using a _trial function orthogonal to $y_0$_
	- Proof: similar for lowest eigenvalue but $y_0$ is not included in the expansion due to _orthgonality_
	- Example: if $y_0$ is _even_, then the trial function for $y_1$ should be _odd_
