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
- The result _may depend on the contour_

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
- Some functions tend to a _well-defined limit for $z\to\infty$, irrespective of direction_ at which infinity is approached
- Example: $f(z)=1/z$ tends to $0$ as $z\to\infty$ for all directions

- In these cases, one can _model infinity as a single point_
- This requires a _stereographic projection_, where the complex plane is mapped onto the _Riemann sphere_, with $z=0$ as the South Pole:
![[Stereographic projection.png]]
- For _any point on the plane_, a line is drawn _to the North Pole_
- The _point_ at which the line _intersects with the sphere_ is the _equivalent point on the sphere_
- The _South Pole_ is projected onto the origin
- Circles of _fixed latitude_ are then projected onto _concentric circles around the origin_
- Meanwhile, the _North Pole_ is _projected onto all points at infinite radius_
	- It can be described as a _single point at infinity_

- Near the _point at infinity_, the function is studied by defining a new variable:
$$\zeta=\frac{1}{z}$$
- Then define:
$$g(\zeta)=f\left(\frac{1}{\zeta}\right)$$
- One can find a _Laurent expansion_ for $g$ around $\zeta=0$
- If there is a _singularity_ at that point, then $f$ has a _singularity at infinity_

- Example:
	$$f(z)=z^n \hspace{1cm} g(\zeta)=\zeta^{-n}$$
	- $g$ has a _pole of order_ $n$ at $\zeta=0$, hence $f$ has a pole of order $n$ at infinity

- Example:
	$$f(z)=\exp(z) \hspace{1cm} g(\zeta)=\exp(1/\zeta)$$
	- $g$ has an _essential singularity_ at $\zeta=0$, hence $f$ has an essential singularity at infinity

- Example:
	$$f(z)=1/z \hspace{1cm} g(\zeta)=\zeta$$
	- $g$ has a _simple zero_ at $\zeta=0$, hence $f$ has a simple zero at infinity

### Residues at infinity
- Care must be taken when applying the theorem to residues at infinity
- Strictly, the residue is a _property of $f\,dz$_ instead of just $f$

- For example, if $C$ is an _anticlockwise contour around the unit circle_ in the $z-$plane:
$$\frac{1}{2\pi i}\oint_C\frac{dz}{z}=1$$
- At the same time, it is a _clockwise unit circle_ in the $\zeta-$plane
- So it can be viewed as a contour _surrounding the point at infinity_
- Hence, the integral is equal to _minus the sum of residues outside $C$_, despite the fact that $1/z$ has _no singular points_ there
- Still, the _residue at $z=\infty$_ is $-1$
- This is because the residue is a property of:
$$\frac{dz}{z}=-\frac{d\zeta}{\zeta}$$

## Examples of applications
- The residue theorem is often used to calculate _definite integrals_

### Integrals with trigonometric functions
- Example integral (with $a>1$):
$$I=\int_0^{2\pi}\frac{d\theta}{2(a-\cos\theta)}$$
- Substitution, using a _circular contour_:
$$\displaylines{z=\exp(i\theta) \\ I=\oint_C \frac{i\,dz}{(z-z_+)(z-z_-)} \\ z_\pm=a\pm\sqrt{a^2-1}}$$
- As $0<z_-<1$ and $z_+>1$, only _one pole_ needs to be considered:
$$\res{z=z_-}\left(\frac{i}{(z-z_-)(z-z_+)}\right)=\frac{i}{z_--z_+}=-\frac{i}{2\sqrt{a^2-1}}$$
- Hence, from the _residue theorem_:
$$I=\frac{\pi}{\sqrt{a^2-1}}$$

### Closing contours at infinity
- Consider the integral:
$$I=\int_0^\infty \frac{dx}{x^2+1}$$
- Let $C$ be a _semicircular contour_ on the _upper half-plane_
	- A _straight segment_ from $z=-\infty$ to $z=\infty$
	- A _semicircular segment_ in the upper-half plane, with $R\to\infty$
- As $|z|$ tends to _infinity_, $|zf(z)|$ tends to _zero_, hence _only the straight segment contributes_:
$$I=\frac{1}{2}\int_{-\infty}^\infty\frac{1}{x^2+1}\,dx=\frac{1}{2}\oint_C\frac{dz}{z^2+1}=(\pi i)\sum [\text{residues of } f(z)\text{ in upper half plane}]$$
- Write $f(z)$ as:
$$\frac{1}{1+z^2}=\frac{1}{(z+i)(z-i)}$$
- Hence:
$$I=\frac{\pi}{2}$$
### Double poles
- Consider the integral:
$$I=\int_0^\infty\frac{dx}{(x^2+a^2)^2}$$
- Using the _same semicircular contour as above_:
$$I=\frac{1}{2}\oint_C\frac{dz}{(z+ia)^2(z-ia)^2}$$
- For double pole at $z=ia$, use the [[#Residues|above formula]]:
$$\res{z=ia} f(z)=\lim_{z\to ia}\frac{d}{dz}\frac{1}{(z+ia)^2}=-\frac{1}{4}ia^{-3}$$
- Therefore, the integral is:
$$I=\frac{\pi}{4a^3}$$

### Multiple poles
- Consider the integral:
$$I=\int_0^\infty\frac{dx}{1+x^4}$$
- Using the _same semicircular contour as above_:
$$\displaylines{I=\frac{1}{2}\oint_C\frac{dz}{(z-z_1)(z-z_2)(z-z_3)(z-z_4)}\\ z_1=\exp(i\pi/4)\hspace{1cm}z_2=\exp(3i\pi/4)\hspace{1cm}z_3=\exp(-i\pi/4)\hspace{1cm}z_4=\exp(-3i\pi/4)}$$
- Considering the residues in the _upper half plane_ ($z_1$ and $z_2$):
$$I=\frac{\pi}{2\sqrt{2}}$$

- Or, one can use a _quarter circle_ only encircling $z_1$
- The _real axis_ contribution is $I$, and the arc contribution still vanishes
- As the contour _goes down the imaginary axis_, that contribution is $-iI$

# Multi-valued functions and branch cuts

## Branch points and branch cuts
- _Not all complex functions_ have a _unique value_ for each point $r\exp(i\theta)$ on the _complex plane_
- Example: $\ln z$:
$$\displaylines{\ln z=\ln r+i\theta \\ \ln i=\dots,-\frac{3}{2}i\pi,\frac{1}{2}i\pi,\frac{5}{2}i\pi,\dots=\left(2n+\frac{1}{2}\right)i\pi}$$
- It can be seen that for any _closed contour_, which _does not encircle the origin_, the function _remains continuous and single-valued_
- If the contour _encircles the origin_, then it must either be _discontinuous_ or _multi-valued_

- A point that _cannnot be encircled by a curve_ is called a _branch point_
- The function is known to have a _branch point singularity_ at that point
- The _order_ of a branch point is the _number of paths around_ the point that must be taken before the function returns to its _original value_

- Examples:
	- $\ln(z-a)$ has a branch point at $z=a$
	- $z^\alpha$ where $\alpha$ is _not an integer_ also has a branch point at the _origin_
	- Specifically, $\sqrt{z}=\sqrt{r}\exp(i\theta/2)$ will _change sign_ if the origin is encircled as $\theta\to\theta+2\pi$

- To ensure a function is _single-valued_, it is necessary to introduce a _branch cut_, which _no curve is permitted to cross_
- Then, a _branch_ (allowed range) for a function is chosen:
![[ln z branches.png]]
- For $\ln z$, the _canonical branch cut_ is from $-\infty$ to the origin, such that $-\pi<\theta<\pi$
- Then, the value of $\ln z$ is known as the _principal value_:
$$\displaylines{z=x+i0^+\hspace{1cm} \ln z=\ln|x|+i\pi \\ z=x+i0^- \hspace{1cm} \ln z=\ln|x|-i\pi}$$
- For any curve that _does not cross the cut_, the function is _single-valued_ and _continuous_

- For some functions like $\ln z$, there can be an _infinite number_ of branches
- For $\sqrt{z}=\sqrt{r}\exp(i\theta/2)$, there are only _two branches_, which have _different signs_:
$$\sqrt{z}\,\Big|_{\theta+2\pi}=-\sqrt{z}\,\Big|_{\theta}$$

- The function is _analytic everywhere except for the branch cut_
- This also means that there _cannot be Laurent expansions about the branch point_
	- For $\ln z$ or $\sqrt{z}$, any _annulus_ centred _around the origin_ will _cross the branch cut_

- The choice of branch cut can be _arbitrary_:
	- They _need not be straight_
	- For $\ln z$, _any_ continuous, non-intersecting curve _from origin to infinity_ is fine, as long as a branch cut exists

## Multiple branch points
- Consider the function:
$$\displaylines{\sqrt{z^2-1}=\sqrt{z-1}\sqrt{z+1} \\ \sqrt{z-1}=\sqrt{r_1}\exp(i\theta_1/2) \hspace{1cm} \sqrt{z+1}=\sqrt{r_2}\exp(i\theta_2/2) \\ \sqrt{z^2-1}=\sqrt{r_1r_2}\exp\left[i(\theta_1+\theta_2)/2\right]}$$
- If a curve circles _either_ $z=1$ or $z=-1$, the function would have to _change sign_
	- Example: $\theta_1\to\theta_1+2\pi$, and $\theta_2\to\theta_2$
- However, if the curve encircles _both branch points_, then the function is _continuous_
	- $\theta_1\to\theta_1+2\pi$, and $\theta_2\to\theta_2+2\pi$

- This motivates a _branch cut_ on the _real axis_ from $z=-1$ to $z=1$
- Alternatively, the branch cut can be from $z=-\infty$ to $z=-1$, then $z=1$ to $z=\infty$
	- Technically _one branch cut_ that passes through the _point at infinity_

- In general, _multiple branch cuts may sometimes be necessary_

## Integration around a branch cut
- If the _integrand_ is a function with a branch cut, then the _integration contour must not cross it_
- Consider the integral:
$$I=\int_0^\infty\frac{x^p}{x^2+1}\,dx\;, \;0<p<1$$
- Use a _keyhole contour_:
$$\oint_C \frac{z^p}{z^2+1}\,dz$$
![[Keyhole contour.png]]
- The _small circle_ with radius $\epsilon$ gives a _negligible contribution_ as $\epsilon\to0$
- Similarly, the _large circle_ gives a negligible contribution as radius $R\to\infty$
- On the _upper straight contour_, $z=x$
- On the _lower straight contour_, $z=x\exp{(2i\pi)}$
- Hence:
$$\oint_C\frac{z^p}{z^2+1}\,dz=[1-\exp(2ip\pi)]I$$
- From the residue theorem:
$$I=\frac{\pi}{2\cos(p\pi/2)}$$
# Jordan's Lemma
- Consider the integral:
$$\lim_{R\to\infty} \oint_{C_R}g(z)\exp(i\lambda z)\,dz$$
- Where:
	- $\lambda>0$ is a _constant_
	- $g(z)$ is _analytic_ in the _upper half plane_, $\Im(z)>0$
	- The contour $C_R$ is a _semicircle_ of radius $R$ in the _upper half plane_, where $z=R\exp(i\theta)$

- Then, _Jordan's Lemma_ states that if $g(z)\to0$ uniformly on $C_R$ as $R\to\infty$, then:
$$\lim_{R\to\infty} \oint_{C_E}g(z)\exp(i\lambda z)\,dz=0$$
- For _negative_ $\lambda$, then the semicircle must be in the _lower half plane_
- The _condition_ of decreasing $g(z)$ can be expressed as:
$$|g(Re^{i\theta})|<G(R)\hspace{1cm}\text{for }0<\theta<\pi$$
	- where $G(R)$ tends to zero as $R\to\infty$

## Use in contour integration

### Oscillatory integral
- Consider the integral:
$$I=\int_0^\infty \frac{\cos x}{x^2+1}\,dx$$
- _Split_ the integral:
$$I=\frac{1}2{\left[\int_0^\infty\frac{\exp(ix)}{x^2+1}\,dx+\int_0^\infty\frac{\exp(-ix)}{x^2+1}\,dx\right]=\frac{1}{2}\int_{-\infty}^\infty\frac{\exp(ix)}{x^2+1}\,dx}$$
- Use a _semi-circular contour_, and from Jordan's lemma, the _curved segment has no contribution_:
$$I=2\pi i\sum \text{(residues in the upper-half plane)}=\frac{\pi}{2e}$$

### Singularity on contour
- Consider the integral:
$$I=\int_0^\infty \frac{\sin x}{x}\,dx$$
- _Split_ the integral:
$$I=\frac{1}{2i}{\left[\int_0^\infty\frac{\exp(ix)}{x}\,dx-\int_0^\infty\frac{\exp(-ix)}{x}\,dx\right]=\frac{1}{2i}\int_{-\infty}^\infty\frac{\exp(ix)}{x}\,dx}$$
- Use a contour that _avoids_ the singularity at $z=0$:
![[Contour avoiding origin.png]]
- From the _residue theorem_:
$$\oint\frac{\exp(iz)}{z}\,dz=0$$
- From Jordan's Lemma, the contribution on $C_2$ disappears
- On the _small semicircle_ $C_r$:
$$\int_\pi^0 \frac{\exp(ire^{i\theta})}{re^{i\theta}}d(re^{i\theta})=i\int_\pi^0[1+O(r)]\,d\theta=-i\pi+O(r)$$
- Using the result as $r\to0$:
$$\int_{-\infty}^\infty\frac{\exp(ix)}{x}\,dx=i\pi$$
- Hence:
$$I=\frac{\pi}{2}$$
## Gaussian integration lemma
- For any _real_ number $a$, it is known that:
$$\int_{-\infty}^\infty \exp[-(u+a)^2]\,du=\sqrt{\pi}$$
- For a _complex_ constant $a$, one must prove it via _contour integration_
- Let there be a variable $v=u+a$:
$$\int_{-\infty}^\infty\exp[-(u+a)^2]\,du=\int_{-\infty}^\infty \exp(-v^2)\,dv$$

- Let there be a _rectangular contour_ with vertices at $\pm R$ and $\pm R+i\,\text{Im } a$
- As the function is _analytic everywhere_, from Cauchy's Theorem:
$$0=\int_{-R}^R \exp(-u^2)\,du-\int_{-R+i\,\text{Im }a}^{R+i\,\text{Im }a}\exp(-v^2)\,dv+2\exp(-R^2)\int_0^{\text{Im }a}\exp(y^2)\sin(2Ry)\,dy$$
- Then as $R\to\infty$, one finds that for _any_ $a\in\mathbb{C}$:
$$\int_{-\infty}^\infty \exp[-(u+a)^2]\,du=\sqrt{\pi}$$

