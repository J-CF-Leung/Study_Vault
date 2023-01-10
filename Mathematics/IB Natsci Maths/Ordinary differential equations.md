#IB_Natsci 

# Classification
- The _general first-order_ ordinary differential equation is:
$$y'+p(x)y=f(x)$$
- This can be solved using an _integrating factor_:
$$\displaylines{g=\exp\int p(x)\,dx \\ y=\frac{1}{g}\int fg\,dx}$$
- The _general second order_ ordinary differential equation is:
$$F(y'',y',y,x)=0$$
- The _linear second order_ ODE is:
$$\displaylines{Ly(x)=g(x) \\ Ly(x)=a(x)y''+b(x)y'+c(x)y}$$
- If $f(x)=0$, it is _homogeneous_
- Since it's linear, the _principle of superposition_ applies

- One can recover the equation in _standard form_:
$$y''+p(x)y'+q(x)y=f(x)$$

# Homogeneous linear second order ODEs and the Wronskian
- Given two solutions $y_1(x)$ and $y_2(x)$ to the equation _in standard form_
- Let their _linear combination_ be
$$y(x)=\alpha y_1(x)+\beta y_2(x)$$
- If $y=0$ implies $\alpha=\beta=0$, then they are _linearly independent_
- If they are linearly independent, $y(x)$ is the _general solution_

- The [[Second order linear ODEs and Green's Functions#The Wronskian|Wronskian]] $W(x)=y_1y_2'-y_2y_1'$ is _non-zero if they are linearly independent_

- One can find the _derivative of the Wronskian_ to be:
$$W'=\frac{dW}{dx}=y_1y_2''-y_2y_1''=-pW$$
- The solution to this is:
$$W=\kappa\exp\left(\int^xp(\zeta)\,d\zeta\right)$$
- The _lower limit is absorbed into $\kappa$_
- It can be shown that up to a multiplicative constant, _the Wronskian is an intrinsic property of the ODE_
- If $W\neq0$ for one value of $x$, _it is non-zero for all $x$_, hence $y_1$ and $y_2$ are _linearly independent for all $x$_

- Given a solution to the equation, $y_1(x)$
- The other solution, $y_2$ can be _found via the Wronskian_
- From the definition of the Wronskian:
$$y_2(x)=y_1(x)\int^x\frac{W(\eta)}{y_1^2(\eta)}\,d\eta=y_1(x)\int^x\frac{\kappa}{y_1^2(\eta)}\,\exp\left(-\int^\eta p(\zeta)\,d\zeta\right)\,d\eta$$
- The indefnite integral _involves an arbitrary additive constant_
- $W$ is determined up to a multiplicative constant, since $y_2$ _can be multiplied by any constant_
- From this, _the integral gives the general solution_


# Series solutions
- Generalise the homogeneous ODE to _complex function_ $y$ of _complex variable_ $z$:
$$y''(z)+p(z)y'(z)+q(z)y(z)=0$$
- If $p(z)$ and $q(z)$ _are both analytic_ at a point $z=z_0$, then it is an _ordinary point_ of the ODE
- If _either are [[Elementary Analysis#Zeros, poles, and essential singularities|singular]]_ at $z=z_0$, it is a _singular point_

- A singular point $z=z_0$ is _regular if both_ $(z-z_0)p(z)$ and $(z-z_0)^2q(z)$ are _analytic_ at $z_0$
	- Example: Legendre's equation has _regular singular_ points at $z=\pm1$

## Solution at ordinary points
- If $z=z_0$ is ordinary point, then $y(z)$ is anaytic at that point
- Let there be a non-zero radius of convergence $R$
- Inside the region of convergence, there are _two linearly independent solutions_ of the form:
$$y=\sum_{n=0}^\infty a_n(z-z_0)^n$$
- Find $a_n$ by _substituting into the differential equation_
- $R$ is the _distance to the nearest singular point_
- Without loss of generality, let $z_0=0$
- The derivatives are:
$$\displaylines{y=\sum_{n=0}^\infty a_nz^n\equiv \sum_{m=0}^\infty a_mz^m \\ y'=\sum_{n=1}^\infty na_nz^{n-1}=\sum_{m=0}^\infty (m+1) a_{m+1}z^m\\y''=\sum_{n=2}^\infty n(n-1)a_nz^{n-2}=\sum_{r=0}^\infty (r+2)(r+1)a_{r+2}z^{r}}$$

- At the ordinary points:
$$p(z)=\sum_{n=0}^\infty p_nz^n \hspace{1cm} q(z)=\sum_{n=0}^\infty q_nz^n$$
- Redefine $r=n+m$, and rewrite multiplication of sums:
$$\sum_{n=0}^\infty A_nz^n\sum_{m=0}^\infty B_nz^n=\sum_{r=0}^\infty\left( \sum_{m=0}^r A_{r-m}B_m\right)z^r$$
	- Constant $r$: integer diagonal entries in $n,m$ plane

- From this, terms in the ODE can be rewritten:
$$\displaylines{p(z)y'(z)=\sum_{r=0}^\infty\left(\sum_{m=0}^r p_{r-m}(m+1)a_{m+1}\right)z^r \\ q(z)y(z)=\sum_{r=0}^\infty \left(\sum_{m=0}^r q_{r-m}a_m\right)z^r}$$
- Substitute these into the ODE and _group powers of $z$_:
$$\sum_{r=0}^\infty\left((r+2)(r+1)a_{r+2}+\sum_{m=0}^r\Big( (m+1)p_{r-m}a_{m+1}+q_{r-m}a_m\Big)\right)z^r=0$$
- Because this _must be true for all $|z|<r$_, each coefficient of $z^r$ must be zero, hence one obtains a _recurrence relation_:
$$a_{r+2}=-\frac{1}{(r+1)(r+2)}\sum_{m=0}^r\Big( (m+1)p_{r-m}a_{m+1}+q_{r-m}a_m\Big)$$
- If $a_0$ and $a_1$ are known, then _all other coefficients are known_
- $a_0$ and $a_1$ are the _integration constants of the second-order ODE_
- There should be _two different solutions_ for $a_r$ 

- This is the _general solution_, but _simpler forms can often be obtained by not using the standard form_, and only substituting the power series

## Solution at regular singular points
- Let $z=z_0$ be a _regular singular point_
- Without loss of generality, let $z_0=0$
- Define:
$$p(z)=\frac{1}{z}s(z)\hspace{1.5cm}q(z)=\frac{1}{z^2}t(z)$$
- The ODE then becomes:
$$z^2y''+zs(z)y'+t(z)y=0$$
- Since $s$ and $t$ are finite, define $s(z=0)\equiv s_0$ and $t(z=0)\equiv t_0$

### Indicial equation
- If $z=0$ is a regular singular point, _Fuchs's theorem_ states that there is always _at least one solution_ to the equation with the form:
$$y(z)=z^\sigma\sum_{n=0}^\infty a_nz^n \hspace{1cm}\text{ with }a_0\neq0 \hspace{0.1cm}\text{ and } \sigma\in\mathbb{C}$$
- There may be one or two solutions of this form
- $a_0\neq0$ is _required to determine the solution uniquely_
- _Substitute the solution_ into the ODE, then divide by $z^\sigma$:
$$\sum_{n=0}^\infty\Big((\sigma+n)(\sigma+n-1)+(\sigma+n)s(z)+t(z)\Big)a_nz^n=0$$
- Evaluate at $z=0$ to obtain the _indicial equation_:
$$\sigma(\sigma-1)+\sigma s_0+t_0=0$$
- The roots $\sigma_1$, $\sigma_2$ are the _indices_ of the regular singular point

### Frobenius' method
- If $\sigma_1-\sigma_2\notin \mathbb{Z}$, we can find _both_ linearly independent solutions
- If $\sigma_1-\sigma_2\in\mathbb{Z}$:
	- If $\sigma_1=\sigma_2$, we can always _only find one solution_ with the given ansatz
	- If they differ by an _integer_, it _fails (in general) to give both solutions_, with some exceptions

- Method: substitute power series into ODE
	- Separate sums based on power of $z$
	- Different values of $n$ may yield indicial equation or recursion relation

### Example: Bessel's equation
- _Bessel's equation_ of order $\nu$ is:
$$y''+\frac{1}{z}y'+\left(1-\frac{\nu^2}{z^2}\right)y=0$$
- In this case, the relevant functions are:
$$s(z)=1 \hspace{1cm} t(z)=z^2-\nu^2$$
- Substituting the power series into the equation:
$$\displaylines{\sum_{n=0}^\infty \left[(\sigma+n)(\sigma+n-1)+(\sigma+n)-\nu^2\right]a_nz^n+\sum_{n=0}^\infty a_nz^{n+2}=0 \\ \sum_{n=0}^\infty\left[(\sigma+n)^2-\nu^2\right]a_nz^n+\sum_{n=2}^\infty a_{n-2}z^n=0}$$
- For $n=0$, $n=1$, and $n\geq2$:
$$\displaylines{\sigma^2-\nu^2=0 \\ ((\sigma+1)^2-\nu^2)a_1=0 \\ ((\sigma+n)^2-\nu^2)a_n+a_{n-2}=0}$$
- From these equations, both the _indicial equation_ and _recurrence relation_ are found:
$$\displaylines{\sigma=\pm\nu \\ (1\pm2\nu)a_1=0 \\ n(n\pm2\nu)a_n=-a_{n-2} \text{ for }n\geq2}$$
- Using the recurrence relation to find the _radius of convergence_, one finds that the solutions are _convergent everywhere_
- If $\sigma=+\nu$, the recurrence relations _always_ work fine

- When $\nu\notin\mathbb{Z}$, the recurrence relations work fine, and _two linearly independent_ solutions are found
- When $2\nu=2m+1$, $m\in\mathbb{N}$, since $\sigma_1$ and $\sigma_2$ differ by an _odd_ integer, it works
- When $2\nu=1$, $a_1$ _must be zero_
- When $\nu=0$, then $\sigma_1=\sigma_2$ and there is _only one solution_
- When $\nu=m\in\mathbb{N}$, _only one solution_ can be found with $\sigma=+\nu$, otherwise $a_{2m}$ would be _infinite_

### Non-power series solutions for Bessel's equation

## Irregular singular points
- If an equation has _irregular singular points_, the solutions will probably also show singular behaviour

# Method of Variation of Parameters