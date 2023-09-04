

[[Einstein notation]] will be used in this note unless specified

>[!quote]
>You're here in Cambridge, and not some other place! You're here because you want to become natural scientists, and not some greedy bankers, yes?!
You're not here to become Chancellor of the Exchequer either.
>
>-Dr. S.J. Cowley, 2022


# Vectors in 3 dimensions
- Orthonormal basis:
$$\bm{e}_i\cdot\bm{e}_j=\delta_{ij}$$
- For a right-handed orthonormal basis:
$$[\bm{e}_1,\bm{e}_2,\bm{e}_3]=\bm{e}_1\cdot(\bm{e}_2\wedge\bm{e}_3)=1$$
- All right-handed, orthonormal bases are related by a rotation
- The Cartesian coordinate system:
 $$\bm{r}=x_1\,\bm{e}_1+x_2\,\bm{e}_2+x_3\,\bm{e}_3$$
	- $\bm{e}_1, \bm{e}_2, \bm{e}_3$ are orthonormal and point along $x,y,z$

# Gradient
- Consider a change in the scalar field $\psi(\bm{r})$ from $\bm{r}$ to $\bm{r}+\delta\bm{r}$:
$$\delta\psi=\pd{\psi}{x_j}\delta x_j\,+\,...=\left(\pd{\psi}{x_j}\bm{e}_j\right)\cdot\delta\bm{r}\,+\,O(\delta\bm{r}^2)$$
- Define the _gradient operator_ $\nabla$:
$$\nabla\equiv\bm{e}_j\pd{}{x_j}$$
$$\delta\psi=\nabla\psi\cdot\delta\bm{r}\,+\,O(\delta\bm{r}^2)$$
- The gradient of some important functions:
$$\nabla\bm{r}=\frac{\bm{r}}{r}=\bm{\hat{r}}$$
$$\nabla f(r)=f'(r)\bm{\hat{r}}$$
## The directional derivative
- Consider the rate of change for a scalar field $\phi$ when moving by $\delta s$ along unit vector $\bm{\hat{l}}$
$$\delta\psi=\psi(\bm{r}+\delta s\bm{\hat{l}})-\psi(\bm{r})=\delta s \frac{d}{ds} \psi(\bm{r}+s\bm{\hat{l}})\Big|_{s=0}$$
- Using the definition of the gradient with displacement $\delta \bm{r} = s\bm{\hat{l}}$:
$$d\psi=ds(\bm{\hat{l}}\cdot\nabla\psi)$$
- Hence:
$$\bm{\hat{l}}\cdot\nabla\psi=\frac{d}{ds}\psi(\bm{r}+s\bm{\hat{l}})\Big|_{s=0}$$
- This is the _directional derivative_ along the direction $\bm{\hat{l}}$

- Consider the value of the scalar $\psi$ along a smooth curve, parametrised by arc length $s$, the directional derivative is $d\psi/ds$ along the curve, with $\bm{\hat{l}}$ being the tangent vector

- If $\nabla\psi\neq0$, but $\bm{\hat{l}}\cdot(\nabla\psi)=0$, $\bm{\hat{l}}$ is orthogonal to $\nabla\psi$, hence $\bm{\hat{l}}$ lies on the tangent plane of $\psi=\text{const.}$

- As $\nabla\psi$ is orthogonal to all tangents, it is _normal_ to the plane $\psi=\text{const.}$

- The directional derivative is maximal when $\bm{\hat{l}}$ is along $\nabla\psi$, hence the _gradient points along the direction of maximal change_

# Div and curl
- Apply the nabla operator to a vector field by dotting and crossing a vector field $\bm{F}(\bm{r})$

- Assume Cartesian coordinates
- The basis vectors are independent of position, and left invariant by the differential operator

- Dotting: divergence, produces a scalar field
- Crossing: curl, produces another vector field

- The divergence is defined as:
$$\nabla\cdot\bm{F}=\pd{}{x_j}F_j$$
- The curl is defined as:
$$\nabla\wedge\bm{F}=\epsilon_{ijk}\bm{e}_i\pd{}{x_j}F_k =\begin{vmatrix}
     \bm{e}_{1} & \bm{e}_{2} & \bm{e}_{3}\\ 
     \partial_{x_1} & \partial_{x_2} & \partial_{x_3}\\
     F_{1} & F_{2} & F_{3} 
\end{vmatrix}
$$
- The divergence and curl of the position vector are:
$$\nabla\cdot\bm{r}=3 \hspace{1.5cm}\nabla\wedge\bm{r}=0$$
# Dotting the operator
- Consider the scalar operator $\bm{F}\cdot\nabla$
$$\bm{F}\cdot\nabla=F_j\pd{}{x_j}$$

- For a scalar field:
$$(\bm{F}\cdot\nabla)\psi=F_j\pd{\psi}{x_j}=\bm{F}(\nabla\psi)$$
- The _left-hand notation is preferred_ due to ambiguities for the vector case

# Vector calculus product rules
$$\begin{aligned} \nabla\cdot(\psi\bm{F})&= \psi\,\nabla\cdot\bm{F}+(\bm{F}\cdot\nabla)\psi \\
\nabla\wedge(\psi\bm{F}) &= \psi(\nabla\wedge \bm{F}) + (\nabla\psi)\wedge\bm{F} \\
\nabla\cdot(\bm{F}\wedge\bm{G}) &= \bm{G}\cdot(\nabla\wedge \bm{F}) -\bm{F}\cdot(\nabla\wedge \bm{G}) \\
\nabla\wedge(\bm{F}\wedge\bm{G}) &= {F}(\nabla\cdot\bm{G})-\bm{G}(\nabla\cdot\bm{F}) + (\bm{G}\cdot\nabla)\bm{F} -(\bm{F}\cdot\nabla)\bm{G} \\
\nabla(\bm{F}\cdot\bm{G}) &= (\bm{F}\cdot\nabla)\bm{G}+ (\bm{G}\cdot\nabla)\bm{F}+\bm{F}\wedge(\nabla\wedge\bm{G})+\bm{G}\wedge(\nabla\wedge\bm{F})
\end{aligned}$$

# Second order vector differential operators

## Second order derivatives equal to zero
- These two second order operators go to zero:
$$\nabla\wedge(\nabla\psi)=\epsilon_{ijk}\partial_i\pd{\psi}{x_j}\bm{e}_k= \epsilon_{ijk}\partial_j\pd{\psi}{x_i}\bm{e}_k=-\epsilon_{jik}\partial_j\pd{\psi}{x_i}\bm{e}_k=0$$
$$\nabla\cdot(\nabla\wedge\bm{F})=\partial_i\left(\epsilon_{ijk}\partial_jF_k\right)=-\epsilon_{jik}\partial_j\partial_iF_k=0$$
- The latter identity can be written as $(\nabla\wedge\nabla)\bm{F}=0$
- Therefore, the identities can be summed up as:
$$\nabla\wedge\nabla=\bm{0}$$
## Conservative and solenoidal vector fields
- For vector fields where $\nabla\wedge\bm{F}=\bm{0}$, it is said to be _irrotational_ or _conservative_
	- The vector field can be written as the gradient of a _scalar potential_ $\phi$
$$\nabla\wedge\bm{F}=\bm{0} \iff \bm{F}=\nabla\phi$$
	- Example: gravity, electric field (in electrostatics)


- For vector fields where $\nabla\cdot\bm{B}=0$, it is said to be _solenoidal_
	- The vector field can be written as the curl of a _vector potential_ $\bm{A}$
$$\nabla\cdot\bm{B}=0 \iff \bm{B}=\nabla\wedge\bm{A}$$
	- Example: magnetic field

- Example of a solenoidal field: $\nabla p\wedge \nabla q$
$$\nabla\cdot(\nabla p\wedge \nabla q)=0$$

- The two potentials are _not unique_

## The Laplacian
- The Laplacian operator $\nabla^2$ for a scalar is defined as the div of grad:
$$\nabla\cdot(\nabla\psi)\equiv(\nabla\cdot\nabla)\psi\equiv\nabla^2\psi=\pd{^2}{x_i^2}\psi$$
- Example: Poisson's equation
$$\nabla^2\psi=\rho$$
- Example: Schrodinger equation
$$-\frac{\hbar^2}{2m}\nabla^2\psi+V\psi=i\hbar\pd{\psi}{t}$$
- Example: Helmholtz equation
$$\nabla^2f+\omega^2f=0$$

## Curl of curl
$$\nabla\wedge(\nabla\wedge\bm{F})=\nabla(\nabla\cdot\bm{F})-\nabla^2\bm{F}$$
- Definition of the vector Laplacian
- Best to use this for curvilinear coordinates

## Some special functions
$$\nabla^2(r^n)\equiv\nabla\cdot(\nabla r^n)=\nabla\cdot(nr^{n-2}\bm{x_i})=n(n+1)r^{n-2}$$
	- Use $\nabla \cdot\bm{r}=\bm{r}/r$

# The fundamental theorems

## Divergence Theorem
- Let $\mathcal{S}$ be a "nice" surface enclosing a volume $\mathcal{V}$ in $\mathbb{R}^3$ with the normal vector $\bm{\hat{n}}$
	- "Nice": Continuous, non-self-intersecting
	- $d\bm{S}$: vector surface element pointing along $\bm{\hat{n}}$
	- $dV$: volume element
$$\iiint_\mathcal{V}\nabla\cdot\bm{u}\,dV=\iint_{\mathcal{S}(\mathcal{V})}\bm{u}\cdot d\bm{S}$$
- Right-hand term: total flux through the surface
- Analagous to the fundamental theorem of calculus
	- Divergence theorem relates a triple integral to a double integral
	- The fundamental theorem relates a single integral to a function

- Setting $\bm{u}=\nabla\wedge\bm{v}$, one gets:
$$0=\iiint_\mathcal{V}\nabla\cdot(\nabla\wedge\bm{v})\,dV=\iint_{\mathcal{S}(\mathcal{V})}(\nabla\wedge\bm{v})\cdot d\bm{S}$$

### Generalisation for a scalar field
- For a scalar field $\psi$ with continuous first-order partial derivatives in $\mathcal{V}$:
$$\iiint_{\mathcal{V}}\nabla\psi\,dV=\iint_{\mathcal{S}(\mathcal{V})}\psi\,d\bm{S} $$
- Proof: set $\bm{u}$ in original Divergence Theorem to $\bm{a}\cdot(\nabla\psi)$, where $\bm{a}$ is an arbitrary constant vector
- Set $\bm{a}$ to $\bm{e}_i$ to obtain:
$$\iiint_\mathcal{V}\,\pd{\psi}{x_i}\,dV=\iint_\mathcal{S}\psi,n_i\,dS$$

### Generalisation for a vector potential
- For a vector potential $\bm{A}$ with continuous first-order partial derivatives in $\mathcal{V}$
$$\iiint_{\mathcal{V}} \nabla\wedge\bm{A}\,dV=\iint_{\mathcal{S}(\mathcal{V})} \bm{\hat{n}}\wedge\bm{A}\,dS$$
- Proof: set $\bm{u}=\bm{a}\wedge\bm{A}$ in the original divergence theorem, where $\bm{a}$ is an arbitrary constant vector

### Interpretation
- Applying the divergence theorem to an infinitesimal volume at $\bm{r_0}$:
$$\nabla\cdot\bm{u}=\lim_{|\mathcal{V}|\to0} \frac{1}{|\mathcal{V}|} \iint \bm{u}\cdot d\bm{S} $$
- The divergence is the _outward_ flux per unit volume

- Positive: source
- Negative: sink

## Stokes' Theorem
- Let $\mathcal{S}$ be a 'nice' open surface bounding a 'nice' closed curve $\mathcal{C}$, and $\bm{u}$ be a 'nice' vector field
$$\iint_\mathcal{S}(\nabla\wedge\bm{u})\cdot d\bm{S}=\oint_{\mathcal{C}} \bm{u}\cdot d\bm{l}$$
- Direction of $d\bm{l}$: defined by right hand rule

- The _flux_ of $\nabla\wedge\bm{u}$  across $\mathcal{S}$ is equal to the _circulation_ of $\bm{u}$ around $\mathcal{C}$

- In two dimensions, reduces to Green's Theorem in the plane:
$$\iint_\mathcal{A} \left(\pd{u_y}{x}-\pd{u_x}{y}\right)\,dx\,dy=\int_C u_x\,dx+u_y\,dy$$

### Interpretation
- Let there be a surface $\mathcal{S}$ with normal vector $\bm{\hat{n}}$, bounding the curve $\mathcal{C}$
- Applying Stokes' Theorem to an infinitesimal surface:
$$\bm{\hat{n}}\cdot(\nabla\wedge\bm{u})=\lim_{|\mathcal{S}|\to0} \frac{1}{|\mathcal{S}|}\oint\bm{u}\cdot d\bm{r}$$
- The curl is a measure of the _local_ rotation of a vector field, quantified by the circulation

- For a velocity field $\bm{v=\omega\wedge r}$, $\nabla\wedge\bm{v}=2\bm{\omega}$

## Gradient theorem
- Let $\phi$ be a vector field without singlarities, and $\mathcal{C}$ be an open path from $A$ to $B$, consider the integral:
$$\int_\mathcal{C}\nabla\phi\cdot d\bm{r}$$
- This integral is _independent_ of the path

- Proof: Form a closed curve, use Stokes' Theorem, use $\nabla\wedge\nabla=\bm{0}$

- Since $\nabla\phi\cdot d\bm{r}=d\phi$,
$$\int_{\mathcal{C}}\nabla\phi\cdot d\bm{r}=\phi(B)-\phi(A)$$


- Notation: $q_i$ for generalised coordinates, $x_i$ for Cartesian coordinates

## Digression in 2 dimensions: Green's theorem
- Consider two functions: $p(x,y)$ and $q(x,y)$
- Consider a _simply connected region_ $R$ with some boundary $C$, taken _counterclockwise_
- In this region, the functions must satisfy _Green's theorem_:
$$\oint_C (P\,dx+Q\,dy)=\iint_R \left(\pd{Q}{x}-\pd{P}y{}\right)\,dx\,dy$$
- Proof: Split the integral on the RHS into two and integrate accordingly

- It is also useful for _multiply connected regions_, where the line integral is _taken over all distinct boundaries_

- This can be considered as _special cases_ of _Stokes theorem_ and the _Divergence Theorem_

# Definition of curvilinear coordinates
- To describe positions in space, define 3 sets of surfaces, each parametrised by a single variable
- Any point has "coordinates" given by the labels for the 3 surfaces which intersect at that point

- The unit vectors are the unit normals to these surfaces
- In general, these coordinate surfaces are _curvilinear_

- Coordinate systems are easiest to deal with when _orthogonal_, i.e. $\bm{e}_i\cdot\bm{e}_j=\delta_{ij}$

- The unit vectors can depend on the position:
$$\bm{e}_i\equiv\bm{e}_i(\bm{r})$$
>[!quote]
>"And that's why life's miserable"
>-Dr. S. J. Cowley, 2022


# Relations between coordinate systems
- For non-Cartesian coordinates $q_i$, they can be expressed as a function of Cartesian ones
$$q_i\equiv q_i(x_i)\hspace{0.2cm}, \hspace{0.3cm} i=1,2,3$$
- $q_i=c_i$ defines 3 independent sets of surfaces, each labelled by $c_i$ 
	- The coordinates $c_i$ are labelled by the 3 surfaces that intersect at that point
- The functions defining $q_i$ can be inverted to express $x,y,z$ as functions of $q_i$

## Incremental changes in length and position
- Let there be a change in position vector $d\bm{r}$, it can be written as:
$$d\bm{r}\equiv dx_i\bm{\hat{x}_i}=\left(\pd{x_i}{q_j}\bm{\hat{x}_i}\right)\,dq_j=\pd{\bm{r}}{q_j}\,dq_j\equiv \bm{h}_j\,dq_j $$
- It is a vector sum of displacements along each of the $q$-axes, as expected
- The vectors $\bm{h}_j$ are defined as (not using summation convention):
$$\bm{h}_j=h_j\bm{e}_j=\left|\pd{\bm{r}}{q_j}\right|\,\bm{e}_j$$
- The $h_j$ are known as the _metric coefficients_, which are dependent on position

- The unit vectors $\bm{e}_j$ are defined as (without summation convention):
$$\bm{e}_j=\frac{1}{h_j}\pd{\bm{r}}{q_j}$$
- The unit vectors are likely to change depending on $\bm{r}$, and hence lie on a curve

## The Jacobian matrix
- Let there be a transformation from $x_i$ to $q_i$, the Jacobian matrix $J$ is:
$$J=\begin{pmatrix} \pd{x_1}{q_1} & \pd{x_1}{q_2} & \pd{x_1}{q_3} \\ \pd{x_2}{q_1} & \pd{x_2}{q_2} & \pd{x_2}{q_3} \\ \pd{x_3}{q_1} & \pd{x_3}{q_2} & \pd{x_3}{q_3} \end{pmatrix}$$
- The Jacobian determinant (or Jacobian) $\mathcal{J}$ is written as:
$$\mathcal{J}=|J|=\pd{(x_1,x_2,x_3)}{(q_1,q_2,q_3)}$$
- Using the definitions of $h_i$ from above:
$$\mathcal{J}=\bm{h}_1\cdot(\bm{h}_2\wedge\bm{h}_3)$$
	- Volume of a parallelepiped spanned by the $\bm{h}$ vectors 

- The volume element $dV$ is then written as:
$$dV=[d\bm{r}_1, d\bm{r}_2, d\bm{r}_3]=\mathcal{J}\,dq_1\,dq_2\,dq_3$$

- Relation to the volume element $dV$ in Cartesian coordinates:
$$dV=dx_1\,dx_2\,dx_3=\pd{(x_1,x_2,x_3)}{(q_1,q_2,q_3)}dq_1\,dq_2\,dq_3=\mathcal{J} dq_1\,dq_2\,dq_3$$

- If $|J|=0$ over a range of variables, the transformation is _singular_ 

- The chain rule: consider 3 sets of coordinates $\alpha_i,\beta_i,\gamma_i$
- Using the chain rule for individual coordinates, the Jacobian between $\alpha_i$ and $\gamma_i$ is:
$$\pd{(\alpha_1,\alpha_2\dots\alpha_n)}{(\gamma_1,\gamma_2\dots\gamma_n)}=\pd{(\alpha_1,\alpha_2\dots\alpha_n)}{(\beta_1,\beta_2\dots\beta_n)}\pd{(\beta_1,\beta_2\dots\beta_n)}{(\gamma_1,\gamma_2\dots\gamma_n)}$$

- Consider the case of $\alpha_i$ and $\gamma_i$ being equivalent, one gets the Jacobian for the inverse transformation:
$$\pd{(\alpha_1,\alpha_2\dots\alpha_n)}{(\beta_1,\beta_2\dots\beta_n)}=\left[\pd{(\beta_1,\beta_2\dots\beta_n)}{(\alpha_1,\alpha_2\dots\alpha_n)}\right]^{-1}$$


# Orthogonality of curvilinear coordinates
- Condition for orthogonality:
$$\bm{e}_i\cdot\bm{e}_j=\delta_{ij}$$
- Right-handedness:
$$[\bm{e}_1,\bm{e}_2,\bm{e}_3]=1$$

- Incremental distance for an orthogonal curvilinear coordinate system:
$$|d\bm{r}|^2=\left(\sum_ih_i\,dq_i\bm{e}_i\right)\cdot\left(\sum_jh_j\,dq_j\bm{e}_j\right)=\sum_i h_i^2(dq_i)^2$$


# Spherical polar coordinates
$$q_1=r, q_2=\theta, q_3=\phi$$
- In terms of Cartesian coordinates:
$$\bm{r}=(r\sin\theta\cos\phi, r\sin\theta\sin\phi, r\cos\theta)$$
- There are singularities at $r=0,\theta=0,\theta=\phi$

- [[#Incremental changes in length and position|Metric coefficients]] $h_i\equiv |\partial\bm{r}/\partial q_i|$:
$$h_r=1 \hspace{1cm} h_\theta=r \hspace{1cm} h_\phi=r\sin\theta$$

- The incremental displacement:
$$d\bm{r}=\sum_ih_i\,dq_i\bm{e}_i=dr\,\bm{\hat{e}}_r+r\,d\theta\,\bm{e}_\theta+r\sin\theta\,d\phi\,\bm{e}_\phi$$


# Cylindrical polar coordinates
$$q_1=\rho, q_2=\phi, q_3=z$$
- In terms of Cartesian coordinates:
$$\bm{r}=(\rho\cos\phi, \rho\sin\phi, z)$$
- There is a singularity at $\rho=0$

- The metric coefficients:
$$h_\rho=1 \hspace{1cm} h_\phi=\rho \hspace{1cm} h_z=1$$

- The incremental displacement:
$$d\bm{r}=d\rho\,\bm{e}_\rho + \rho d\phi\,\bm{e}_\phi+dz\,\bm{e}_z$$

# Volume and surface elements in orthogonal curvilinear coordinates
- From the definition of the volume element:
$$dV=d\bm{r}_1\wedge d\bm{r}_2\cdot d\bm{r}_3=h_1h_2h_3dq_1dq_2dq_3=\mathcal{J}\,dq_1\,dq_2\,dq_3$$
- Spherical polar coordinates:
$$dV=r^2\sin\theta\,drd\theta d\phi$$
- Cylindrical polar coordinates:
$$dV=\rho\,d\rho\,d\theta\,dz$$

- For a surface element, consider the special case $d\bm{S} || \bm{\hat{e}}_3$
$$d\bm{S}=h_1h_2dq_1dq_2\bm{\hat{e}}_3$$
- General case:
$$d\bm{S}=\text{sign}(\bm{\hat{n}}\cdot\bm{e}_1)h_2h_3\,dq_2\,dq_3\bm{e}_1+\text{sign}(\bm{\hat{n}}\cdot\bm{e}_2)h_3h_1\,dq_3\,dq_1\bm{e}_2+\text{sign}(\bm{\hat{n}}\cdot\bm{e}_3)h_1h_2\,dq_1\,dq_2\bm{e}_3$$
	- Special case, plus two terms obtains by cyclic permutations, and signs


# Gradient in orthogonal curvilinear coordinates
- [[Vector calculus in 3-dimensions#Gradient|Definition of gradient operator]]

- From the definitions of $\nabla\psi$ and $d\bm{r}$, and using the chain rule:
$$\displaylines{d\psi=\nabla\psi\cdot d\bm{r}=\sum_i \pd{\psi}{q_i} dq_i \\ \nabla=\bm{e}_i\frac{1}{h_i}\pd{}{q_i}}$$
- As expected, the action of the operator depends on position

- Spherical polar coordinates:
$$\nabla=\pd{}{r}\bm{e}_r+\frac{1}{r}\pd{}{\theta}\bm{e}_\theta+\frac{1}{r\sin\theta}\bm{e}_\phi$$

- Cylindrical polar coordinates:
$$\nabla=\pd{}{\rho}\bm{e}_\rho+\frac{1}{\rho}\pd{}{\phi}\bm{e}_\phi +\pd{}{z}\bm{e}_z$$


# Divergence and curl in orthogonal curvilinear coordinates

## Divergence
- For the divergence, consider the definition:
$$\nabla\cdot\bm{F}=\lim_{|\mathcal{V}|\to0} \frac{1}{|\mathcal{V}|} \iint \bm{F}\cdot d\bm{S} $$
- Here, $|\mathcal{V}|$ is the volume element mentioned above
- The three surface elements are $h_ih_j$ for $i\neq j$
- From this, one obtains:
$$\nabla\cdot\bm{F}=\frac{1}{h_1h_2h_3}\left[\pd{}{q_1}(h_2h_3F_1)+ \pd{}{q_2}(h_3h_1F_2)+\pd{}{q_3}(h_1h_2F_3)\right]$$

- Cylindrical polar coordinates:
$$\nabla\cdot\bm{F}=\frac{1}{\rho}\pd{}{\rho}(\rho F_\rho)+\frac{1}{\rho} \pd{F_\phi}{\phi}+\pd{F_z}{z}$$

- Spherical polar coordinates:
$$\nabla\cdot\bm{F}=\frac{1}{r^2}\pd{}{r}(r^2F_r)+\frac{1}{r\sin\theta}\pd{}{\theta}(\sin\theta\,F_\theta)+\frac{1}{r\sin\theta}\pd{F_\phi}{\phi}$$

## Curl
- For the curl, consider the definition:
$$\bm{\hat{n}}\cdot(\nabla\wedge\bm{u})=\lim_{|\mathcal{S}|\to0} \frac{1}{|\mathcal{S}|}\oint\bm{u}\cdot d\bm{r}$$
- Consider each component with $\bm{\hat{n}}=\bm{e}_i$
- This yields the expression:
$$\nabla\wedge\bm{F}=\frac{1}{h_1h_2h_3}\begin{vmatrix} h_1\bm{e}_1 & h_2\bm{e}_2 & h_3\bm{e}_3 \\ \pd{}{q_1} & \pd{}{q_2} & \pd{}{q_3} \\ h_1F_1 & h_2F_2 & h_3F_3 \end{vmatrix}$$


# Laplacian in orthogonal curvilinear coordinates
- Using the above definitions for the divergence and gradient:
$$\nabla^2\equiv\nabla\cdot\nabla=\frac{1}{h_1h_2h_3}\left(\pd{}{q_1}\left(\frac{h_2h_3}{h_1}\pd{}{q_1}\right)+\pd{}{q_2}\left(\frac{h_3h_1}{h_2}\pd{}{q_2}\right)+\pd{}{q_3}\left(\frac{h_1h_2}{h_3}\pd{}{q_3}\right)\right)$$

- Spherical polar coordinates:
$$\nabla^2\psi=\frac{1}{r^2}\pd{}{r}\left(r^2\pd{\psi}{r}\right) + \frac{1}{r^2\sin\theta}\pd{}{\theta}\left(\sin\theta\pd{\psi}{\theta} \right) + \frac{1}{r^2\sin^2\theta}\pd{^2\psi}{\phi^2}$$

- Cylindrical polar coordinates:
$$\nabla^2\psi=\frac{1}{\rho}\pd{}{\rho}\left(\rho\pd{\psi}{\rho}\right) +\frac{1}{\rho^2}\pd{^2\psi}{\phi^2}+\pd{^2\psi}{z^2}$$

- As for the Laplacian of a vector field, there are two ways:
$$\nabla^2\bm{F}=\nabla(\nabla\cdot\bm{F})-\nabla\wedge(\nabla\wedge\bm{F})$$
$$\nabla^2\bm{F}=\nabla^2(F_1\bm{e}_1+F_2\bm{e}_2+F_3\bm{e}_3)$$
- For the latter, the unit vectors are also acted on as they are functions of position