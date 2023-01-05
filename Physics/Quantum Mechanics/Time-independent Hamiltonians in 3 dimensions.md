- Solving the [[Fundamentals of quantum mechanics#Time-independent Hamiltonians and stationary states|time-independent Schrödinger equation]] with a 3-dimensional Hamiltonian

## The 3D time-independent Hamiltonian
- In 3 dimensions, the Hamiltonian bcomes:
$$\Ham=\frac{P^2}{2m}+V=\frac{1}{2m}(P_x^2+P_y^2+P_z^2)+V$$
- In the position basis, the Hamiltonian is:
$$\Ham=-\frac{\hbar^2}{2m}\nabla^2+V$$

- The equation can be rewritten in terms of the [[Angular momentum in quantum mechanics|angular momentum operators]]:
$$\frac{1}{2mr^2}\left[-\hbar^2\pd{}{r}\left(r^2\pd{}{r}\right) +\hat{L}^2 \right]\psi+V\psi=E\psi$$

### Central potentials
- For many systems, the potential only depends on distance from the origin:
$$V(\bm{r})=V(r)$$
- In this case, the 3-dimensional time-independent Schrodinger equation in the position basis becomes separable:
$$\psi(r,\theta,\phi)=R(r)\,Y(\theta,\phi)$$
- Then, one obtains two equations (with arbitrary separation constant) for $R$ and $Y$:
$$\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)-\frac{2mr^2}{\hbar^2}\left[V(r)-E\right]=l(l+1)$$
$$\frac{1}{Y}\left\{\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\pd{Y}{\theta}\right)+\frac{1}{\sin^2\theta}\frac{\partial^2Y}{\partial\phi^2}\right\}=-l(l+1)$$

- The normalisation criteria for the radial and angular parts of the wave function are:
$$\int_0^\infty r^2|R|^2\,dr=1\hspace{1.5cm}\int_0^\pi\int_0^{2\pi}|Y|^2\sin\theta\,d\theta\,d\phi=1$$


#### The angular equation
- $Y$ can be further separated into functions of $\theta$ and $\phi$, with separation constant $m$
- As $\hat{\Ham}$, $\hat{L}^2$ and $\hat{L}_z$ commute, the problem can be rewritten as constructing simultaneous eigenfunctions of three operators:
$$\hat{\Ham}\psi=E\psi \hspace{1cm} \hat{L}^2\psi=\hbar^2l(l+1)\psi \hspace{1cm} \hat{L}_z\psi=\hbar m\psi$$

- The solutions to the angular equation are the [[Special functions and orthogonal relations#Spherical harmonics|spherical harmonics]]:
$$Y^m_l(\theta,\phi)=\sqrt{\frac{(2l+1)}{4\pi}\frac{(l-m)!}{(l+m)!}}\exp(im\phi)P^m_l(\cos\theta)$$
- The spherical harmonics are mutually orthogonal:
$$\int_0^\pi\int_0^{2\pi}\left[Y^m_l(\theta,\phi)\right]^*\left[Y^{m'}_{l'} (\theta,\phi)\right]\sin\theta\,d\theta\,d\phi=\delta_{ll'}\delta_{mm'}$$
- $P_l^m(x)$ are the _associated Legendre functions_, defined using the _Legendre polynomials_ $P_l(x)$
$$P_l^m(x)\equiv (-1)^m\left(1-x^2\right)^{m/2}\left(\frac{d}{dx}\right)^mP_l(x)$$
	- $P^{-m}_l(x)=(-1)^m[(l-m)!/(l+m)!]P^m_l(x)$ 
$$P_l(x)\equiv\frac{1}{2^ll!}\left(\frac{d}{dx}\right)^l\left(x^2-1\right)^l$$
- These are also the eigenfunctions of [[Angular momentum in quantum mechanics|angular momentum]]

#### The radial equation
- To solve the equation, change variables:
$$u(r)\equiv rR(r)$$
- The normalisation condition becomes:
$$\int_0^\infty |u|^2\,dr=1$$
- The radial equation then becomes:
$$-\frac{\hbar^2}{2m}\frac{d^2u}{dr^2}+\left[V+\frac{\hbar^2}{2m}\frac{l(l+1)}{r^2}\right]u=Eu$$
- There is an _effective potential_
$$V_{eff}=V+\frac{\hbar^2}{2m}\frac{l(l+1)}{r^2}$$
- The second term is a _centrifugal term_ that tends to throw the particle outwards

## The infinite cubical well

## The infinite spherical well

## The hydrogen atom

