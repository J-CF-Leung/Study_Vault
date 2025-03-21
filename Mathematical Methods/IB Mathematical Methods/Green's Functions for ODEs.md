
# Second order linear ODEs
- Second order linear ODEs are of the form:
$$y''+p(x)y'+q(x)y=f(x)$$
- Or:
$$\displaylines{Ly(x)=f(x) \\ L\equiv\frac{d^2}{dx^2}+p(x)\frac{d}{dx}+q(x)}$$
- $f(x)=0$: Homogeneous (unforced)
- $f(x)\neq 0$: Inhomogeneous (forced)

## Homogeneous second order linear ODEs
- Let $y_1$ and $y_2$ be solutions to:
$$y''+py'+qy=0$$
- Then $\alpha y_1+\beta y_2$ is also a solution to the equation
- If the two solutions are linearly independent, it is the _general solution_ to the equation
- $y_1$ and $y_2$ are known as _complementary functions_
- $\alpha$ and $\beta$ are the two integration constants

## Inhomogeneous second order linear ODEs
- Suppose $y_0$ is any solution to:
$$Ly_0=f$$
- The _general solution_ to the ODE is:
$$y(x)=y_0+\alpha y_1+\beta y_2$$
- $y_0$ is known as the _particular integral_

## The Wronskian
- If $y_1$ and $y_2$ are linearly dependent, so are $y_1'$ and $y_2'$ 
- Linear dependence of the complementary functions can be expressed by:
$$\begin{pmatrix}y_1 & y_2 \\ y_1' & y_2'\end{pmatrix} \begin{pmatrix} \alpha \\ \beta\end{pmatrix}= \begin{pmatrix} 0 \\ 0 \end{pmatrix}$$
- Linearly dependent: $\alpha$ and $\beta$ can be non-zero

- The condition for linear dependence can be expressed via the _Wronskian_:
$$W=\begin{vmatrix}y_1 & y_2 \\ y_1' & y_2'\end{vmatrix}=y_1y_2'-y_2y_1'$$
- Linearly independent iff $W\neq0$

## Boundary conditions (BCs)
- To fully determine the solution of a second-order ODE, 2 BCs must be specified
- A boundary condition relates $y$ and $y'$ at one point
	- Higher derivatives can be expressed via $y$ and $y'$ using the ODE

- The general form of a _linear_ BC is:
$$Ay(a)+By'(a)=E$$
- $A,B,E$: constants, $A$ and $B$ are not both zero
- $E=0$: homogeneous BC

- _Initial value problem_: both $y$ and $y'$ specified at one point
- _Boundary value problem_: BCs are specified at different points
# Green's functions
## For two-point homogeneous boundary value problems
- Problem: the differential equation with the operator $L$
$$Ly(x)=f(x)$$
$$L=\frac{d^2}{dx^2}+p(x)\frac{d}{dx}+q(x)$$
- Let the solution satisfy a two-point _homogeneous_ boundary condition:
$$\displaylines{Ay(a)+By'(a)=0 \\ Cy(b)+Dy'(b)=0}$$
	- $A$ and $B$, and $C$ and $D$ are not both zero

- Let there be a function $G(x,\zeta)$ that is the _reponse to forcing_ at the point $\zeta$
$$\Lagr G(x,\zeta)=\delta(x-\zeta)$$
- Here, $\delta(x-\zeta)$ is the [[Dirac Delta Function]] 
- When $x\neq\zeta$, $G$ satisfies the homogeneous equation $\Lagr G=0$

- $G$ _has to be subject to_ the boundary conditions:
$$\displaylines{AG(a,\zeta)+BG_x(a,\zeta)=0 \\ CG(b,\zeta)+DG_x(b,\zeta)=0}$$
- Notation:
$$\displaylines{\Lagr=\pd{^2}{x^2}+p(x)\pd{}{x}+q(x) \\ G_x(x,\zeta)=\pd{G}{x}}$$
- The solution to the original problem is:
$$y(x)=\int_a^b G(x,\zeta)f(\zeta)\,d\zeta$$
- Reasons:
	- By _substituting the above into the BCs_, one can see that they are satisfied
	- By _applying $\Lagr$ to both sides_, one regains the original ODE
- This is equivalent to _adding all impulse responses_ at points $\zeta$, _weighted_ by $f(\zeta)$, to form the _general solution_
	- Example: adding _potentials_ from different _charges_ ([[Poisson and Laplace's equations]])

- $G(x,\zeta)$ is called the _Green's function_ of $\Lagr$ for the given homogeneous boundary conditions 

>[!quote]
>"We solve the equation in two regions with a discontinuity in between, then we superglue them together!"
>-Dr. S.J. Cowley, 2022


## Properties of Green's functions
- Integrate $\Lagr G=\delta(x-\zeta)$ from $\zeta-\epsilon$ to $\zeta+\epsilon$:
$$1=\lim_{\epsilon\to 0}\int_{\zeta-\epsilon}^{\zeta+\epsilon} \left(\pd{^2G}{x^2} +p(x)\pd{G}{x}+q(x)\right)\,dx$$
- Through some rearrangement, one gets:
$$1=\lim_{\epsilon\to 0}\left[\pd{G}{x}+pG\right]_{\zeta-\epsilon}^{\zeta+\epsilon}-\lim_{\epsilon\to 0} \int_{\zeta-\epsilon}^{\zeta+\epsilon} \left(\frac{dp}{dx}-q\right)G\,dx $$

- Suppose that $G$ is continuous, this requires:
$$\lim_{\epsilon\to 0}\Big[G(x,\zeta)\Big]_{\zeta-\epsilon}^{\zeta+\epsilon}=0$$
- Since $p$ and $q$ are continuous, this requires:
$$\lim_{\epsilon\to 0} \left[\pd{G}{x}\right]_{\zeta-\epsilon}^{\zeta+\epsilon}=1$$

## Building a Green's function
- From the definition of $G$, it _obeys the homogeneous ODE for $x\neq\zeta$_
- The solutions to the _homogeneous_ ODE are $y_1(x)$ and $y_2(x)$
- Due to the jump, it should be separated into 2 regions:
$$G(x,\zeta)= \begin{cases} \alpha_-(\zeta)\,y_1(x) +\beta_-(\zeta)\, y_2(x) &a\leq x\leq \zeta \\ \alpha_+(\zeta)\,y_1(x) +\beta_+(\zeta)\, y_2(x) &\zeta\leq x\leq b\end{cases}$$

- By substituting in the continuity/discontinuity conditions above:
$$\begin{pmatrix} y_1 & y_2 \\ y_1' & y_2' \end{pmatrix} \begin{pmatrix} \alpha_+-\alpha_- \\ \beta_+-\beta_- \end{pmatrix}=\begin{pmatrix} 0 \\ 1 \end{pmatrix}$$

- A solution to this exists if the [[#The Wronskian|Wronskian]] is non-zero

- The solutions to this are:
$$\alpha_+-\alpha_-=-\frac{y_2(\zeta)}{W(\zeta)} \hspace{1cm} \beta_+-\beta_-=\frac{y_1(\zeta)}{W(\zeta)}$$
- Two equations of four that are needed

- Then, substitute these into boundary conditions at $x=a$ and $x=b$ for two more equations
- Solve for $\alpha_+$, $\alpha_-$, $\beta_+$, $\beta_-$

- The boundary conditions:
$$\displaylines{AG(a,\zeta)+BG_x(a,\zeta)=0 \\ CG(b,\zeta)+DG_x(b,\zeta)=0}$$
- For simplicity, construct _complementary functions_ such that:
$$Ay_1(a)+By_1'(a)=0 \hspace{1cm} Cy_2(b)+Dy_2'(b)=0$$
- Then, substituting this into the boundary conditions for the Green's function:
$$\alpha_+=\beta_-=0$$
- Using all of the above equations:
$$G(x,\zeta)= \begin{cases}\frac{y_1(x)y_2(\zeta)}{W(\zeta)} &a\leq x < \zeta \\ \frac{y_1(\zeta)y_2(x)}{W(\zeta)} &\zeta\leq z\leq b \end{cases}$$

- When $W(\zeta)$ vanishes, as $y_2=cy_1$, the complementary function _satisfies both boundary conditions at once_, and the solution may not exist, or be unique

## Homogeneous initial value problems
- Let there be a hompgeneous boundary condition at $x=a$:
$$y(a)=y'(a)=0$$
- Require that the Green's function satisfy:
$$G(a,\zeta)=\pd{G}{x}(a,\zeta)=0$$
- Choose the complementary functions such that:
$$y_1(a)=0 \hspace{1cm} y_2'(a)=0$$
- This requires:
$$\alpha_-=\beta_-=0$$
- The conditions become:
$$\begin{pmatrix} y_1(\zeta) & y_2(\zeta) \\ y_1'(\zeta) & y_2'(\zeta) \end{pmatrix} \begin{pmatrix} \alpha_+(\zeta) \\ \beta_+(\zeta) \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$
- The Green's function therefore becomes:
$$G(x,\zeta) = \begin{cases} 0 &a\leq x<\zeta \\ \frac{y_1(\zeta)y_2(x)-y_1(x)y_2(\zeta)}{W(\zeta)} &\zeta\leq x<b \end{cases}$$
## Inhomogeneous boundary conditions
- Solution for inhomogeneous equation for homogeneous BCs is $y_\text{hbc}$

- Solve homogeneous equation for inhomogeneous BCs, solution is $y_\text{ibc}$

- Solution: $y_\text{ibc}+y_\text{hbc}$

## As an eigenfunction expansion
- From [[Sturm-Liouville Theory]], given that the Sturm-Lioville operator $\Lagr$ has _orthonormal eigenfunctions_ $\{y_n\}$, with _eigenvalues_ $\lambda_n$, the Green's function can take the form:
	- Normalisation: _delta function_
$$G(x,x')=\sum_{n=1}^\infty \frac{1}{\lambda_n} y_n(x)y_n^*(x')$$
- The _solution_ is then:
$$y(x)=\sum_{n=1}^\infty y_n\frac{1}{\lambda_n}\int_{\alpha}^\beta y_n^*(x')f(x')\,dx'=\sum_{n=1}^\infty y_n(x)\frac{\braket{y_n|f}}{\lambda_n}$$
