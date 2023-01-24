- The study of _eigenvalue problems_ for _Sturm-Liouville operators_

- Let $\Lagr$ be a _linear differential operator_ such that:
$$\displaylines{\Lagr y(x)=f(x) \\ \Lagr=p(x)\frac{d^2}{dx^2}+r(x)\frac{d}{dx}+s(x)}$$
- There are also _boundary conditions_ on $y$, at $x=\alpha$ and $x=\beta$

- Since $\Lagr$ is _linear_, solutions can be expressed in terms of a _superposition_ of a set of _basis functions_
	- Common choices: power series, trigonometric functions

- The usual choice for the _basis_ is the _set of eigenfunctions_ $y_i$ of $\Lagr$, which _satisfy the boundary conditions_, and:
$$\Lagr y_i(x)=\lambda_iy_i(x)$$
- Example: the eigenfunctions for $\Lagr=-d^2/dx^2$, with conditions $y(0)=y(\pi)=0$, are $\sin(nx)$ for $n\in\mathbb{N}$

## Inner Products of functions
- [[Vectors and matrices#Scalar product/inner product|Definition of the inner product between vectors]]

- Matrices are _analagous to linear differential operators_
- The operator acts on _functions in an infinite dimensional space of functions_, transfprming from one to the other

- _Complex functions and eigenvalues_ are permitted
- The _inner product of functions_ $u$ and $v$, defined for $\alpha\leq x\leq\beta$:
$$\braket{u|v}=\int_\alpha^\beta u^*(x)\,v(x)\,dx$$
- This fits _all definitions_ of an inner product

- The _norm_ of a function is:
$$||u||^2=\braket{u|u}=\int_\alpha^\beta|u(x)|^2\,dx$$
- The norm is _real_ and $\geq0$
- If it is zero, that implies $u=0$ for _well-behaved functions_
- A _normalised eigenfunction_ $y_i$ is one that satisfies $||y_i||^2=1$
	- Example: for the first example with $\Lagr=-d^2/dx^2$, the normalised eigenfunction is:
	$$y_n(x)=\sqrt{\frac{2}{\pi}}\sin(nx)$$

- Functions $u$ and $v$ are _orthogonal_ if $\braket{u|v}=0$

## Adjoint and self-adjoint operators
- For _any operator_ $\Lagr$, the _adjoint_ of the operator, $\Lagr^\dagger$, is defined by:
$$\begin{aligned}\braket{u|\Lagr v}=\int_\alpha^\beta u\left(\Lagr v\right)\,dx&=\int_\alpha^\beta\left(\Lagr^\dagger u^* \right)v\,dx+\text{boundary terms} \\ &=\braket{\Lagr^\dagger u|v} +\text{boundary terms}\end{aligned}$$
	- Second equality obtained by multiple _integrations by parts_

- If the _boundary terms are zero_, and $\Lagr=\Lagr^\dagger$, then $\Lagr$ is _self-adjoint_:
$$\braket{u|\Lagr v}=\braket{\Lagr u|v}$$
- They are _analagous to Hermitian operators_

- A _Sturm-Liouville operator_ is a second order differential operator, defined in the range $\alpha\leq x\leq \beta$, that can be expressed in the form:
$$\Lagr=-\frac{d}{dx}\left(\rho(x)\frac{d}{dx}\right)+\sigma(x)$$
- Here, $\rho(x)>0$, and $\sigma,\rho$ are _real_ over the range over which $\Lagr$ is defined

- By considering arbitrary functions $u$ and $v$, it can be proven that _all Sturm-Liouville operators are self-adjoint if and only if_ the boundary conditions satisfy:
$$\left[\rho(vu^*{'}-u^*v{'})\right]_\alpha^\beta=0$$
## Weight functions and converting to Sturm-Liouville form
- Consider a _weight function_ $w(x)$, which is _real_ and _positive_ for $\alpha<x<\beta$
- The _generalised inner product_ is then:
$$\braket{u|v}_w=\int_\alpha^\beta u^*(x)v(x)w(x)\,dx$$

- _Not all_ second-order linear operators can be put into Sturm-Liouville form
- For such an operator $\tilde{\Lagr}$, there is _always a weight function_ $w$ such that $\Lagr=w\tilde{\Lagr}$ is in Sturm-Liouville form

- Let the general second-order operator be:
$$\displaylines{\tilde{\Lagr}=p\frac{d^2}{dx^2}+r\frac{d}{dx}+s=-\frac{d}{dx}\left(a(x)\frac{d}{dx}\right)-b(x)\frac{d}{dx}-c(x) \\ p=-a \\ r=-(b+a') \\ s=-c}$$
- Multiplying the operator by $w(x)$, subject to the constraints mentioned above:
$$w\tilde{\Lagr}=-\frac{d}{dx}\left(aw\frac{d}{dx}\right)+(aw'-bw)\frac{d}{dx}-wc$$
- _Choose_ $w(x)$ such that $aw'=bw$
$$w(x)=C\exp\left[\int^x \frac{b(x')}{a(x')}\,dx'\right]$$
- This gives an operator _in Sturm-Liouville form_:
$$\displaylines{\Lagr=w\tilde{\Lagr}=-\frac{d}{dx}\left(aw\frac{d}{dx}\right)-wc=-\frac{d}{dx}\left(\rho\frac{d}{dx}\right)+\sigma \\ \rho=aw \\ \sigma=-wc }$$
- Then, with the appropriate _boundary conditions_ being satisfied, $\Lagr=w\tilde{\Lagr}$ is _self-adjoint_:
$$\braket{u|\Lagr v}=\int_\alpha^\beta u^*\Lagr v\,dx=\braket{\Lagr u|v}$$
- Since $w$ is real, this can be rewritten as:
$$\displaylines{\int_\alpha^\beta wu^*\tilde{\Lagr} v\,dx=\int_\alpha^\beta w(\tilde{\Lagr}u)^*v^*\,dx \\ \braket{u|\tilde{\Lagr}v}_w=\braket{\tilde{\Lagr}u|v}_w}$$
- Hence, $\tilde{\Lagr}$ is _self-adjoint with respect to an inner product with weight function $w$_
- As long as the _boundary condition_ is satisfied:
$$\left[aw(vu^*{'}-u^*v')\right]_\alpha^\beta=0$$

- So, if $y(x)$ satisfies the eigenvalue equation for $\tilde{\Lagr}$:
$$\tilde{\Lagr}y=\lambda y$$
- Then, multiplying both sides by $w$, $y(x)$ satisfies a _generalised eigenvalue equation_ for $\Lagr$ with weight function $w$:
$$\Lagr y=\lambda w(x)y$$
- Example: 
	- In _Hermite's equation_, the operator _is not in Sturm-Liouville form_
	- However, it can be converted by using the _weight function_ $\exp(-x^2)$

## Eigenvalues and eigenfunctions of self-adjoint operators
- Analagous to the [[Vectors and matrices#Special properties of matrices|eigenvalues and eigenvectors of Hermitian matrices]]

- Let $\tilde{\Lagr}$ be _self-adjoint_ w.r.t. the weight function $w$, and let $u$ be a _non-zero eigenfunction_:
$$\lambda||u||_w^2=\lambda\braket{u|u}_w=\braket{u|\lambda u}_w=\braket{u|\tilde{\Lagr}u}_w=\braket{\tilde{\Lagr}u|u}_w=\braket{\lambda u|u}_w=\lambda^*\braket{u|u}_w=\lambda^*||u||_w^2$$
- Hence, $\lambda$ _must be real_

- Considering _two non-zero eigenfunctions_ $u_1$ and $u_2$, with _different eigenvalues_ $\lambda_1$ and $\lambda_2$
$$\displaylines{\lambda_1\braket{u_2|u_1}_w=\braket{u_2|\lambda_1u_1}_w=\braket{u_2|\tilde{\Lagr}u_1}_w}=\braket{\lambda_2u_2|u_1}_w=\lambda_2^*\braket{u_2|u_1}_w$$
- Since the _eigenvalues are real_, and $\lambda_1\neq\lambda_2$, the _eigenfunctions must be orthogonal_

