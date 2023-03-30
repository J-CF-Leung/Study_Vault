- In 3 dimensions, the Hamiltonian bcomes:
$$\Ham=\frac{P^2}{2m}+V=\frac{1}{2m}(P_x^2+P_y^2+P_z^2)+V$$
- In the position basis, the Hamiltonian is:
$$\Ham=-\frac{\hbar^2}{2m}\nabla^2+V$$

- The equation can be rewritten in terms of the [[Angular momentum in quantum mechanics|angular momentum operators]]:
$$\frac{1}{2mr^2}\left[-\hbar^2\pd{}{r}\left(r^2\pd{}{r}\right) +\hat{L}^2 \right]\psi+V\psi=E\psi$$

# Central potentials
- For many systems, the potential _only depends on distance from the origin_:
$$V(\bm{r})=V(r)$$
- In this case, the 3-dimensional time-independent Schrodinger equation in the position basis becomes _separable_:
$$\psi(r,\theta,\phi)=R(r)\,Y(\theta,\phi)$$
- Then, one obtains two equations (with arbitrary separation constant) for $R$ and $Y$:
$$\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)-\frac{2mr^2}{\hbar^2}\left[V(r)-E\right]=l(l+1)$$
$$\frac{1}{Y}\left\{\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\pd{Y}{\theta}\right)+\frac{1}{\sin^2\theta}\frac{\partial^2Y}{\partial\phi^2}\right\}=-l(l+1)$$

- The normalisation criteria for the radial and angular parts of the wave function are:
$$\int_0^\infty r^2|R|^2\,dr=1\hspace{1.5cm}\int_0^\pi\int_0^{2\pi}|Y|^2\sin\theta\,d\theta\,d\phi=1$$


## The angular equation
- $Y$ can be further separated into functions of $\theta$ and $\phi$, with separation constant $m$
- As $\hat{\Ham}$, $\hat{L}^2$ and $\hat{L}_z$ commute, the problem can be rewritten as constructing _simultaneous eigenfunctions_ of three operators:
$$\hat{\Ham}\psi=E\psi \hspace{1cm} \hat{L}^2\psi=\hbar^2l(l+1)\psi \hspace{1cm} \hat{L}_z\psi=\hbar m\psi$$

- The solutions to the angular equation are the [[Special functions and orthogonal relations#Spherical harmonics|spherical harmonics]]:
$$Y^m_l(\theta,\phi)=\sqrt{\frac{(2l+1)}{4\pi}\frac{(l-m)!}{(l+m)!}}\exp(im\phi)P^m_l(\cos\theta)$$
- The spherical harmonics are mutually orthogonal:
$$\int_0^\pi\int_0^{2\pi}\left[Y^m_l(\theta,\phi)\right]^*\left[Y^{m'}_{l'} (\theta,\phi)\right]\sin\theta\,d\theta\,d\phi=\delta_{ll'}\delta_{mm'}$$
- $P_l^m(x)$ are the _associated Legendre functions_, defined using the _Legendre polynomials_ $P_l(x)$
$$P_l^m(x)\equiv (-1)^m\left(1-x^2\right)^{m/2}\left(\frac{d}{dx}\right)^mP_l(x)$$
	- $P^{-m}_l(x)=(-1)^m[(l-m)!/(l+m)!]P^m_l(x)$ 
$$P_l(x)\equiv\frac{1}{2^ll!}\left(\frac{d}{dx}\right)^l\left(x^2-1\right)^l$$
- These are the eigenfunctions of [[Angular momentum in quantum mechanics|angular momentum]]


## Radial equation and the radial distribution function
- To solve the equation, change variables:
$$u(r)\equiv rR(r)$$
- The normalisation condition becomes:
$$\int_0^\infty |u|^2\,dr=1$$
- The radial equation then becomes:
$$-\frac{\hbar^2}{2m}\frac{d^2u}{dr^2}+\left[V+\frac{\hbar^2}{2m}\frac{l(l+1)}{r^2}\right]u=Eu$$
- There is an _effective potential_
$$V_{eff}=V+\frac{\hbar^2}{2m}\frac{l(l+1)}{r^2}=V+\frac{\mean{L^2}}{2mr^2}$$
- The second term is a _centrifugal term_ that tends to throw the particle outwards

- $|u|^2$ can be interpreted as a _probability density_:
$$P(r)\,dr=|u|^2\,dr=|R|^2r^2\,dr$$
- This gives the _probability of finding the particle in a spherical shell_ between $r$ and $r+dr$
- Therefore, $|u|^2$ is known as the _radial distribution function_

## The infinite cubical well

## The infinite spherical well

## The hydrogen-like atom
- Consider the _bound states_ of a single electron in an atom
- For an _electron_ in a _hydrogen-like_ atom with atomic charge $Z$, the potential is:
$$V(r)=-\frac{1}{4\pi\epsilon_0}\frac{Ze^2}{r}$$

### Finding energies
- From this, the radial equation becomes:
$$-\frac{\hbar^2}{2m_e}\frac{d^2u}{dr^2}+\left[\frac{l(l+1)\hbar^2}{2m_e
r^2}-\frac{Ze^2}{4\pi\epsilon_0r}\right]u=Eu$$
- To simplify this equation, define:
$$\displaylines{\kappa^2=-\frac{2m_eE}{\hbar^2} \\ A=\frac{2m}{\hbar^2}\frac{Ze^2}{4\pi\epsilon_0}}$$
- This gives the equation:
$$\frac{d^2u}{dr^2}-\left[\frac{l(l+1)}{r^2}-\frac{A}{r}+\kappa^2\right]u=0$$
- Considering _large_ $r$, $u(r)$ behaves like $\exp(-\kappa r)$
- Considering _small_ $r$. $u(r)$ behaves like $r^{l+1}$
- From this:
$$u(r)=G(r)r^{l+1}\exp(-\kappa r)$$
- This then becomes the _associated Laguerre equation_:
$$r\frac{d^2G}{dr^2}+2(l+1-\kappa r)\frac{dG}{dr}+[A-2\kappa(l+1)]G=0$$
- Using a _power series solution_, and requiring that it _terminates_:
$$\displaylines{G(r)=\sum_{j=0}^\infty c_jr^j \\ c_{j+1}=\frac{2\kappa(j+l+1)-A}{(j+1)[j+2(l+1)]}c_j \\ j_\text{max}+l+1-\frac{A}{2\kappa}=0}$$
- Hence, one can define the _principal quantum number_ $n$:
$$\displaylines{n=\frac{A}{2\kappa}\geq1 \\ l\leq n-1}$$
- This gives the quantised energies as:
$$E_n=-\frac{Z^2e^4m_e}{2(4\pi\epsilon_0)^2\hbar^2}\frac{1}{n^2}=-\frac{\hbar^2}{2m_e}\frac{Z^2}{a_0^2}\frac{1}{n^2}$$
- Here, $a_0$ is the _Bohr radius_:
$$a_0=\frac{4\pi\epsilon_0\hbar^2}{m_ee^2}=0.53\times10^{-10}\,\text{m}$$
- This gives energy as:
$$E_n=-\frac{13.6Z^2}{n^2}\,\text{eV}$$
- This is exactly the _same result as the Bohr model_

- For a _hydrogen-like_ atom, the energy _only depends on_ $n$

### Energy eigenstates
- From the above results, the eigenfunctions feature the [[Special functions and orthogonal relations#Associated Laguerre polynomials|associated Lagueere polynomials]]

- The eigenstates are determined by _three quantum numbers_, as the eigenstate is a _simultaneous eigenstate of three commuting operators_
- $n$ determines the _energy_ of the eigenstate
- $l$ determines the _orbital angular momentum_
- $m_l$ determines the _angular momentum along the $z$ direction_
- The allowed ranges are:
$$\begin{aligned}n&\geq1 \\ l&=0,1,2,\dots,n-1 \\ m_l&=-l,-l+1,\dots-1,0,1,\dots,l-1,l\end{aligned}$$

- The _degeneracy_ of each state is:
$$g_n=2\sum_{l=0}^{n-1}(2l+1)=2n^2$$
- The factor of two is due to [[Angular momentum in quantum mechanics#Spin angular momentum|spin]]

- As it is a central potential, there is an _angular part_, given by the _spherical harmonics_
- The formula for the eigenstates is (after normalisation):
$$\psi_{nlm}=\sqrt{\left(\frac{2}{na_0}\right)^3\frac{(n-l+1)!}{2n(n+l)!}}\exp\left(-\frac{r}{na}\right)\left(\frac{2r}{na}\right)^l\left[L^{2l+1}_{n-l-1}\left(\frac{2r}{na}\right)\right]Y_l^m(\theta,\phi)$$

### Radial distribution function
- To visualise the radial probability density, one can use the [[#The radial equation|radial distribution function]]:
$$P(r)=r^2|R_{nl}(r)|^2$$
![[Hydrogen radial distribution function.png]]