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
- _Relate the coordinates_ using derivatives between each other

- Euclidean space:
$$s=\int |d\bm{r}|=\int \sqrt{dx^2+dy^2}=\int \sqrt{1+y'^2}\,dx$$



## Application to Sturm-Liouville theory
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

## Hamilton's Principle

# Constrained minimisation

# The Rayleigh-Ritz method