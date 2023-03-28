- Heavily relies on results in [[Elementary Analysis#Analytic functions of a complex variable|complex analysis]]

# Results from analysis

## Differentiation
- The _differentiability_ of a _complex function_ $f(z)$ requires:
$$\frac{df}{dz}\equiv f'(z)=\lim_{\delta z\to0}\frac{f(z+dz)-f(z)}{\delta z}$$
- This must be _finite_, and be the same _regardless of the direction of the limit_

- _Separate_ the function into real and imaginary parts:
$$\displaylines{z=x+iy \\f(z)=u(x,y)+iv(x,y)}$$
- For a function to be differentiable, it must obey the _Cauchy-Riemann equations_:
$$\displaylines{\pd{u}{x}=\pd{v}{y} \\ \pd{v}{x}=-\pd{u}{y}}$$
- This also implies $u$ and $v$ are _harmonic_

## Laurent series
- Any function that is _analytic and single-valued_ throughout an _annulus_ $\alpha<|z-z_0|<\beta$ centred on $z_0$ has a _unique Laurent series_:
$$\begin{aligned}f(z)&=\sum_{n=-\infty}^\infty a_n(z-z_0)^n \\ &=\dots\frac{a_{-2}}{(z-z_0)^2}+\frac{a_{-1}}{z-z_0}+a_0+a_1(z-z_0)+\dots\end{aligned}$$
- The series converges for all $z$ _within the annulus_

- If $\alpha=0$, the function is analytic _within the disk_ (perhaps except the point $z_0$ itself, which may be a _single isolated singularity_)
- For $\alpha=0$, there are 3 possibilities:
	- If the _first non-zero term_ has $n\geq 0$, then the function is _analytic_ at $z=z_0$, and the Laurent series is _equivalent to the Taylor series_
	- If the _first non-zero term_ has $n=-N<0$, then $f(z)$ has a _pole of order $N$_ at $z=z_0$
	- If the series has an _infinite number of terms_ for $n<0$, then the function has an _essential singularity_ at $z=z_0$

# Contour integrals

## Definition
- Consider the integral of $f(z)$ along the _contour_ $C$ from $z=\alpha$ to $\beta$
- Aside from the _path_, the contour also includes the _travel direction_
- The result _may depend on the contour_\

- The _formal definition_ divides the interval $[\alpha,\beta]$ into $N$ parts:
$$\displaylines{\alpha=z_0<z_1<z_2<\dots<z_N=\beta \\ \delta z_k=z_k-z_{k-1} \\ \Delta=\max_k|\delta z_k|}$$
- The integral is then the limit as $N$ approaches infinity:
$$\int_C f(z)\,dz=\lim_{\Delta\to0}\sum_{k=0}^{N-1}f(z_k)\,\delta z_k$$

## Properties
- If $C_1$ is a contour from $\alpha$ to $\beta$, and $C_2$ is a contour from $\beta$ to $\gamma$, and $C$ is $C_1$ _followed by_ $C_2$:
$$\int_C f(z)\,dz=\int_{C_1} f(x)\,dz+\int_{C_2}f(z)\,dz$$
- If $C_+$ is a contour from $\alpha$ to $\beta$ and $C_-$ is the contour _in reverse_, then:
$$\int_{C_+}f(z)\,dz=-\int_{C_-}f(z)\,dz$$
- If $C$ is a _closed contour_, then _starting point is irrelevant_, but _direction matters_:
$$\oint_\text{clockwise}f(z)\,dz=-\int_\text{anticlockwise}f(z)\,dz$$
- An integral around a _closed contour_ can also be _split into two parts_

- If a contour has _length_ $L$, then:
$$\left|\int_C f(z)\,dz\right|\leq L\max_C|f(z)|$$
- Integration _by parts_ and by _substitution_ are still usable

# Cauchy's theorem
- A _simply connected domain_ (SCD) is a region $R$ of the complex plane _without any holes_
	- In other words, _any closed curve_ in $R$ encircles points _only in $R$_

- A _simple closed curve_ (SCC) is a _continuous closed curve of finite length_ which _has no self-intersections_
	- It must _divide_ the complex plane into an _interior_ and an _exterior_

- _Cauchy's theorem_ states that if a function $f(z)$ is _analytic_ in an SCD $R$, then for _any simple closed curve_ $C$ in $R$:
$$\oint_C f(z)\,dz=0$$
- Proof: Using Green's Theorem in a plane with the Cauchy-Riemann equations

## Deformation of contours
- Consider two points, $\alpha$ and $\beta$, with _two different contours_ $C_1$ and $C_2$ connecting them
- Then $C_1-C_2$ is a _closed curve_, and from Cauchy's theorem:
$$\int_{C_1}f(z)\,dz=\int_{C_2}f(z)\,dz$$
- Hence, _a contour can be deformed_ without changing the value of the integral, _as long as it is not moved across a singularity_
- This _also applies to closed contours_, as long as _no singularities are passed through_

## Integration of complex functions
- Suppose $f$ and $f'$ are _both analytic_ in some domain $R$, containing points $\alpha$ and $\beta$, along with the integration contour
- By _parametrising the contour using arc length_ $s$, one finds that:
$$\int_\alpha^\beta f'(z)\,dz=f(\beta)-f(\alpha)$$
- This is _independent of path_, as long as it is _within_ $R$
- Hence, in a simply connected region, _integration is done in the same sense as with a real variable_

- If $f$ is an _entire function_, then the integral _does not depend at all on the path taken_
- If $f$ is entire, then the Taylor expansion still applies:
$$\displaylines{f(z)=g'=\sum_{n=0}^\infty \frac{f^{(n)}(z_0)}{n!}(z-z_0)^n \\ g(z)=\sum_{n=0}^\infty \frac{f^{(n)}(z_0)}{(n+1)!}(z-z_0)^{n+1}}$$

- If $f$ is _has one or more singularities_, then _the contour must be specified to lie in a region where $f$ is analytic_

- These theorems _do not hold for closed curves containing singularities_

# Residues
- Recall the [[#Laurent series]] of a function:
$$\begin{aligned}f(z)&=\sum_{n=-\infty}^\infty a_n(z-z_0)^n \\ &=\dots\frac{a_{-2}}{(z-z_0)^2}+\frac{a_{-1}}{z-z_0}+a_0+a_1(z-z_0)+\dots\end{aligned}$$
- If a _pole_ has order _one_, then it is a _simple pole_
- The coefficient $a_{-1}$ is called the _residue_ of the pole

- The residue for a _simple pole_:
$$\res{z=z_0}\,f(z)\equiv a_{-1}=\lim_{z\to z_0}\left\{(z-z_0)f(z)\right\}$$
- The residue for a _pole of order $N$_:
$$\res{z=z_0}\,f(z)\equiv a_{-1}=\lim_{z\to z_0}\left\{\frac{1}{(N-1)!}\frac{d^{N-1}}{dz^{N-1}}\left[(z-z_0)^Nf(z)\right]\right\}$$
## Calculus of residues
- Consider the _contour integral anticlockwise around a pole_ at $z=z_0$
- Condition: _simple closed curve_ in a _simply-connected domain_

- Consider _each term of the Laurent series separately_
- For $n\geq0$, from [[#Cauchy's theorem]], it must _vanish_
- For $n\leq-1$, _shrink_ the contour to a _circle of radius_ $\epsilon$ around the pole, and substitute $z=z_0+\epsilon\exp(i\theta)$

- From this, the integral _vanishes for_ $n\leq-2$
- This leaves the $a_{-1}$ term, hence:
$$\oint_C f(z)\,dz=2\pi ia_{-1}=2\pi i\,\res{z=z_0}f(z)$$

- This leads to the _residue theorem_, which states that if a function $f(z)$ is _analytic_ in a _simply-connected domain_ $R$ except for a _finite number of poles_ $z=z_1,z_2,\dots,z_n$, and $C$ is a _simple closed curve_ encircling them in an _anticlockwise direction_:
$$\frac{1}{2\pi i}\oint_C f(z)\,dz=\sum_{k=1}^n \res{z=z_k}\,f(z)$$
- Proof: Split the contour into separate regions

## Cauchy's formula
- If $f(z)$ is _analytic_ in a region $R$ containing $z_0$, then _Cauchy's formula_ states:
$$f(z_0)=\frac{1}{2\pi i}\oint_C\frac{f(z)}{z-z_0}\,dz$$
- Here, $C$ has to be a _simple closed curve_ in $R$ encircling $z_0$ _anticlockwise_
- Proof: Residue theorem

- If $f(z)$ is known on $C$, then from this formula, it can be _known throughout the interior_

- From the Cauchy-Riemann equations, the _real and imaginary parts satisfy Laplace's Equation_
- Hence, this is _equivalent to the uniqueness theorem for Laplace's equation with Dirichlet boundary conditions_
- The formula above is _equivalent_ to the [[Poisson and Laplace's equations#Integral solution to Poisson's equation|integral solution to Poisson's equation]] in 2D, with _zero source term_ and Green's function $\ln|\bm{r}-\bm{r'}|/(2\pi)$

- If Cauchy's formula is differentiated $n$ times w.r.t. $z_0$:
$$f^{(n)}(z_0)=\frac{n!}{2\pi i}\oint_C\frac{f(z)}{(z-z_0)^{n+1}}\,dz$$
- Hence at any point where $f$ is _analytic_, it is _infinitely differentiable_, and _all its derivatives exist_

## The point at infinity and stereographic projection

## Examples of applications

# Multi-valued functions and branch cuts
