#IB_Natsci 
>[!quote]
>"We decided that vectors and matrices was as dry as the Sahara. This is about as dry as the moon."
>-Dr. S. J. Cowley, 2022

# Sequences and Limits
- A _sequence_ is a set of real or complex numbers, $s_n$, defined for all integers $n\geq n_0$ and occuring in order. 
- If it is unending, it is an _infinite sequence_

## Behaviour of infinite sequences
- Possible behaviours as $n\to\infty$:
	- Tending to a particular value
	- Not tending to any value but remaining bounded in magnitude
	- Becoming unlimited in magnitude

### Limit
- $s_n$ tends to some limit $s$ if for any positive number $\epsilon$, there exists some $N\equiv N(\epsilon)$ such that:
$$|s_n-s|<\epsilon \text{   for all } n>N$$
- In other words, _the members of the sequence are eventually contained within an arbitrarily small disk centred on s_:
$$\lim_{n\to\infty}s_n=s$$

- Cauchy's Principle of Convergence: A _necessary and sufficient condition for a sequence $s_n$ to converge_, for any positive $\epsilon$ is that $|s_{n+m}-s_n|<\epsilon$ _for all positive integers $m$, for sufficiently large $n$_
	- Does not need knowledge of $s$

### Boundedness
- The sequence $s_n$ is _bounded_ as $n\to\infty$ if there exists some positive number $K$ such that $|s_n|<K$ for _sufficiently large $n$_

- An _increasing sequence_ either _tend to a limit_ or to $+\infty$, hence a _bounded increasing sequence has to tend to a limit_
$$s_{n+1}>s_n\text{, and } s_n<\kappa\in\mathbb{R} \text{ for all } n \text{, then }s=\lim_{n\to\infty}s_n\text{ exists}$$
### Flying off to infinity
- A sequence $s_n$ is said to tend to infinity if for any given $A$, however large, there exists $N\equiv N(A)$ such that
$$s_n>A \text{   for all } n>N$$
- Then, one can write:
$$s_n\to\infty \text{ as }n\to\infty$$
- Equivalent condition for tending to $-\infty$

### Oscillating sequence
- If a sequence does not tend to a limit or $\pm\infty$, then $s_n$ is said to _oscillate_
	- If it is bounded, it _oscillates finitely_
	- If it is not bounded, it _oscillates infinitely_


## Convergence of infinite series
- Given an infinite sequence of numbers $u_1,u_2,\dots,u_n$:
- The partial sum $s_n$ is defined as:
$$s_n=\sum_{r=r_0}^n u_r$$
- If as $n\to\infty$, $s_n$ tends to a finite limit $s$, then the infinite series _converges_, and $s$ is the sum:
$$s=\sum_{r=r_0}^\infty u_r$$
- An infinite series that is not convergent is _diverent_

- Convergence or divergence _does not depend on $r_0$_ but only on behaviour at _large $r$_
- According to Cauchy's Principle, a _necessary and sufficient condition_ for convergence is that for _any_ $\epsilon>0$:
$$|s_{n+m}-s_n|=|u_{n+1}+u_{n+2}+\dots+u_{n+m}|<\epsilon$$
	for all positive integers $m$, for sufficiently large $n$

## Conditions for convergence
- A _necessary condition_ for convergence is that $u_r\to0$ as $r\to\infty$
	- Proof: consider $u_r=s_{r}-s_{r-1}$ 
	- It is necessary but _NOT SUFFICIENT_

- A series $\sum u_r$ _converges absolutely_ if:
$$\sum_{r=1}^\infty|u_r|\hspace{0.5cm}\text{ converges}$$
- If $\sum|u_r|$ converges, $\sum u_r$ converges

- _Conditional convergence_: if $\sum|u_r|$ _diverges_, then $\sum u_r$ _may or may not converge_. If it does, it is said to do so _conditionally_

## Tests for convergence

### Comparison test
- Applies to non-negative real numbers
- Suppose $v_r>0$ and $\sum v_r$ is _convergent_
- Then suppose for some sequence $u_r$ and $\mathcal{K}$ _independent of $r$_:
$$0<u_r<\mathcal{K}v_r$$
- Then the infinite series of $u_r$ is _also convergent_

### Ratio test
- Uses a comparison between a given series $\sum u_r$ of complex terms and a geometric series $\sum v_r=\sum\rho^r$ where $\rho>0$
- Suppose all $u_r$ are real and positive
- Suppose the _ratio between successive terms tends to a limit_ as $r\to\infty$:
$$\lim_{r\to\infty} \frac{u_{r+1}}{u_r}=\rho$$
- The series _converges if $\rho<1$ and diverges if $\rho>1$_
>[!quote]
"If it's less than 1, we know it converges! If it's bigger than 1, we know it diverges! If it's 1, we cry!" 
>-Dr. S. J. Cowley, 2022
- If the series has vanishing terms, they must be eliminated before using the test

### Cauchy's test
- Suppose $u_r>0$ and:
$$\lim_{r\to\infty} u_r^{1/r}=\rho$$
- The series $\sum u_r$ _converges if $\rho<1$ and diverges if $\rho>1$_

# Functions of a continuous variable
## Limits and continuity
- The function $f(z)$ _tends to the limit $L$_ as $z\to z_0$ if, for _any positive number_ $\epsilon$, there exists some positive number $\delta$, depending on $\epsilon$, such that $|f(z)-L|<\epsilon$ _for all $z$_ such that $|z-z_0|<\delta$
- The limit is written as:
$$\lim_{z\to z_0}f(z)=L \hspace{1cm}\text{ or }\hspace{1cm} f(z)\to L \text{ as }z\to z_0$$
- The function $f(z)$ is _continuous_ at the point $z=z_0$ if $f(z)\to f(z_0)$ as $z\to z_0$
- The function $f(z)$ is _bounded_ as $z\to z_0$ if there exists some positive number $\mathcal{K}$ and $\delta$ such that $|f(z)|<\mathcal{K}$ for all $z$ with $|z-z_0|<\delta$
- The function $f(z)$ tends to a limit $L$ as $z\to\infty$, if for any $\epsilon$, there exists a positive number $R$, depending on $\epsilon$, such that $|f(z)-L|<\epsilon$ for all $z$ with $|z|>R$
$$\lim_{z\to \infty}f(z)=L \hspace{1cm}\text{ or }\hspace{1cm} f(z)\to L \text{ as }z\to\infty$$
- The function $f(z)$ is _bounded at infinity_ if there exist positive numbers $\mathcal{K}$ and $R$ such that $|f(z)|<K$ for all $z$ with $|z|>R$


- Sometimes, a limit may apply only if the point is _approached in a particular way_

## Big O notation
- Suppose $f(z)$ and $g(z)$ are functions of $z$

- If $f/g$ is _bounded_ as $z\to z_0$, then $f(z)=O(g(z))$ as $z\to z_0$
- If $f/g\to0$  as $z\to z_0$, then $f(z)=o(g(z))$ as $z\to z_0$
- If $f/g\to 1$ as $z\to z_0$, then $f(z)\sim g(z)$ as $z\to z_0$

- Also applies when $z\to\infty$
- $f(z)=O(1)$ means the function is _bounded_
- Either $f(z)=o(g(z))$ or $f(z)\sim g(z)$ implies $f(z)=O(g(z))$
- Only $f\sim g$ is a _symmetric relation_ (Not equivalent to $f\to g$)
- If $f\sim g$, they are _asymptotically equal_

# Taylor's theorem for functions of a continuous variable
- Let $f(x)$ be a _real or complex_ function for _real $x$_, which is _differentiable at least_ $n$ times in the interval $x_0\leq x \leq x_0+h$, then the _Taylor series_ of $f(x_0+h)$ is given by:
$$f(x_0+h)=f(x_0)+hf'(x_0)+\frac{h^2}{2}f''(x_0)+\dots+\frac{h^{n-1}}{(n-1)!}f^{(n-1)}(x_0)+R_n$$
- The _remainder_ after $n$ terms, $R_n$ can be shown via integration by parts to be:
$$R_n=\int_{x_0}^{x_0+h}\frac{(x_0+h-x)^{n-1}}{(n-1)!}f^{(n)}(x)\,dx$$
- Another form to express the remainder is:
$$R_n=\frac{h^n}{n!}f^{(n)}(\xi)$$
	- where $x_0<\xi<x_0+h$
- It follows that $R_n=O(h^n)$

- If $f(x)$ is smooth, i.e. _infinitely differentiable_, it can be written as an _infinite series_:
$$f(x_0+h)=\sum_{n=0}^\infty \frac{h^n}{n!}f^{(n)}(x_0)$$
- This _power series in $h$_ converges for small $h$

# Analytic functions of a complex variable
- The _complex derivative_ is:
$$f'(z_0)=\lim_{z\to z_0}\frac{f(z)-f(z_0)}{z-z_0}=\lim_{\delta z\to0} \frac{f(z_0+\delta z)-f(z_0)}{\delta z}$$

- The same limit _must be obtained for any sequence of values that tend to $z_0$_
>[!quote]
>"You can get to $z_0$ via a random drunken walk, and you must get the same answer as if you were sober!"
>-Dr. S. J. Cowley, 2022

## The Cauchy-Riemann equations
- Express $f$ and $z$ in terms of their real and imaginary parts:
$$f(z)\equiv f(x+iy)\equiv u(x,y)+iv(x,y)$$
- If $f'(z)$ exists, it can be obtained by taking limits _along the real axis_ ($\delta y=0$), or _along the imaginary axis_ ($\delta x=0$)
- By comparing the real and imaginary parts of doing the derivative both ways:
$$\pd{u}{x}=\pd{v}{y} \hspace{1.5cm} \pd{v}{x}=-\pd{u}{y}$$
- These are the _Cauchy-Riemann equations_
- They are _necessary and sufficient conditions_ for $f(z)$ to be complex differentiable, provided the partial derivatives are _continuous_

## Analytic functions
- If a function $f(z)$ has a complex derivative at _every point_ $z$ in a region $R$ of the complex plane, it is _analytic in $R$_
- To be analytic at a _point_ $z_0$, it must be differentiable throughout some _neighbourhood_ $|z-z_0|<\epsilon$ of that point

- An _entire function_ is a function that is _analytic in the whole complex plane_

- Sums, products, and compositions of analytic functions are _also analytic_
- Rules for differentiation _also apply to complex derivatives of analytic functions_

- Many complex functions are _differentiable everywhere except for isolated points_, and these points are the _singularities_ of the function
- Examples:
	- Rational functions, $f(z)=P(z)/Q(z)$, where $P$ and $Q$ are polynomials
	- $z^c$ at $z=0$ if $c$ is a non-positive constant (it is _multi-valued_)

- Examples of _non-analytic_ functions:
	- $\Re(z)$
	- $z^*$
	- $|z|$ and $|z|^2$

## Consequences of the Cauchy-Riemann equations
- Suppose the _real part of an analytic function is known_, then the imaginary part _up to an additive constant_ can be found via the CR equations
- The real and imaginary parts are _harmonic_:
$$\nabla^2u=\nabla^2v=0$$
- To solve Laplace's equation in 2D, one "just" needs to find an analytic function that satisfies the boundary conditions

- $u$ and $v$ are _conjugate harmonic functions_:
$$\nabla u\cdot \nabla v=0$$
- Curves of _constant $u$_ and curves of _constant $v$_ are _orthogonal_

## Taylor series of analytic functions
- If a function of a complex variable is analytic in the region $R$, it is _differentiable any number of times_ at any point in the region
- Therefore, it can be written as a Taylor series:
$$f(z)=\sum_{n=0}^\infty\frac{(z-z_0)^n}{n!}f^{(n)}(z_0)$$
- This series should converge within _some neighbourhood of $z_0$_
- An analytic function can be alternatively defined as a function that has a Taylor series _with a non-zero radius of convergence_

# Zeros, poles, and essential singularities

## Zeros and poles
- The _zeros_ of $f(z)$ are points $z_0$ where $f(z_0)=0$
- The _zeros_ of $f(z)$ have _order_ $N$ if:
$$\displaylines{f(z_0)=f'(z_0)=\dots=f^{(N-1)}(z_0)=0 \\ f^{(N)}(z_0)\neq0}$$
- The first non-zero term in the Taylor series is _proportional to_ $(z-z_0)^N$
- A _simple zero_ is a zero of order 1

- Suppose $g(z)$ is analytic and non-zero at $z=z_0$
- Consider $$f(z)=(z-z_0)^{-N}g(z)$$
- $f(z)$ is _NOT analytic_ at $z=z_0$ and is said to have a _pole of order $N$_
- Suppose one can write $g(z)$ as a Taylor series:
$$g(z)=\sum_{n=0}^\infty b_n(z-z_0)^n$$
- $f(z)$ can then be written as:
$$f(z)=\sum_{n=-N}^\infty a_n(z-z_0)^n=\sum_{n=-N}^\infty b_{n+N}(z-z_0)^n$$
- If $f(z)$ has a zero of order $N$, $1/f$ has a _pole_ of order $N$ there
- If $f(z)$ is analytic and $g(z)$ has a zero of order $N$ at $z=z_0$, then $f/g$ has a pole of order $N$

## Laurent series and essential singularities
- Any function that is _analytic and single-valued_ throughout an _annulus_ $\alpha<|z-z_0|<\beta$ centred on $z_0$ has a _unique Laurent series_:
$$f(z)=\sum_{n=-\infty}^\infty a_n(z-z_0)^n$$
- The series converges for all $z$ _within the annulus_

- If $\alpha=0$, the function is analytic _within the disk_ (perhaps except the point $z_0$ itself)
- For $\alpha=0$, there are 3 possibilities:
	- If the _first non-zero term_ has $n\geq 0$, then the function is _analytic_ at $z=z_0$, and the Laurent series is _equivalent to the Taylor series_
	- If the _first non-zero term_ has $n=-N<0$, then $f(z)$ has a _pole of order $N$_ at $z=z_0$
	- If the series has an _infinite number of terms_ for $n<0$, then the function has an _essential singularity_ at $z=z_0$

- _Picard's theorem_ states that in any neighbourhood near an essential singularity, the function takes on _every possible complex value_ (with possibly 1 exception)
	- Example: $e^{1/z}$ is never $0$ near the origin

- The behaviour of a function $f(z)$ _at infinity_ can be examined by defining $\zeta=1/z$ and defining $g(\zeta)=f(z)$
- Then, $z=\infty$ _maps to a single point_ at $\zeta=0$
- If $g(0)$ is a _zero, pole, or essential singularity_, $f(z)$ _has the corresponding property at $z=\infty$_

- All _entire functions_ $f(z)$ have _essential singularities_ at $z=\infty$ _unless they are polynomials_
- All _polynomials_ have _poles_ at $z=\infty$ _unless they are constant_

# Power series of a complex variable

## Convergence of power series
- Let a complex-valued function $f(z)$ have the form:
$$f(z)=\sum_{n=r}^\infty a_r(z-z_0)^r$$
- Here, $a_r\in\mathbb{C}$
- The _Taylor series_ of an _analytic_ function is a power series

- [[#Tests for convergence]] can be extended to complex series
- Hence if $\sum |a_r(z-z_0)^r|$ converges, so does $\sum a_r(z-z_0)^r$

- If the power series _converges_ for $z=z_1$, then it _converges absolutely_ for all $z$ such that $|z-z_0|<|z_1-z_0|$, corresponding to _a circle of radius $|z_1-z_0|$ around $z_0$

- If the sum _diverges_ for $z=z_1$, then it _diverges_ for all $z$ such that $|z-z_0|>|z_1>z_0|$ (i.e. _outside a circle with radius $|z_1-z_0|$ around $z_0$_)

- This implies there must exist some real, non-negative number $R$ such that:
	- $\sum a_r(z-z_0)^r$ _converges_ for all $|z-z_0|<R$
	- $\sum a_r(z-z_0)^r$ _diverges_ for all $|z-z_0|>R$
- $R$ is the _radius of convergence_
- $|z-z_0|=R$ is the _circle of convergence_, where the series _only converges inside_

- The radius can be _zero, positive, or infinite_
- _On_ the circle, the series can either converge or diverge
- The radius of convergence for a _Taylor series_ around $z=z_0$ is _equal to the distance to the nearest singular point_

## Determining radius of convergence
- Without loss of generality, take $z_0$ as $0$ and define $$f(z)=\sum_{r=0}^\infty a_rz^r$$
- Using D'Alembert's _ratio test_:
$$\lim_{r\to\infty} \left|\frac{a_{r+1}}{a_r}\right|=\frac{1}{R}$$
	- Proof: use the [[#Ratio test]] for $a_rz^r$
	- The limit does not necessarily exist (e.g. if other term is 0)

- Using _Cauchy's test_:
$$\lim_{r\to\infty}\left|a_r\right|^{1/r}=\frac{1}{R}$$
