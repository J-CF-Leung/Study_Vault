# One dimension
- The [[Fundamentals of quantum mechanics#Time-independent Hamiltonians and stationary states|time-independent Schrödinger equation]] solves for the eigenkets of the Hamiltonian:
$$\Ham\ket{E}=E\ket{E}$$
- The resultant [[Fundamentals of quantum mechanics#The time-evolution operator|time-evolution operator]] and wave function become:
$$\teo = \sum_n\ket{E_n}\bra{E_n}\exp(-iE_nt/\hbar)=\int\ket{E}\bra{E}\exp(-iEt/\hbar)\,dE$$
$$\ket{\Psi(t)} =\sum_n\ket{E_n}\braket{E_n|\Psi_0}\exp(-iE_nt/\hbar) =\int \ket{E}\braket{E|\Psi_0}\exp(-iEt/\hbar)\,dE$$


## Useful theorems
- The energy $E$ has to be real, and larger than minimum of $V(x)$ for $\wv$ to be normalisable
- If $V(x)$ is an even function, then $\braket{x|\Psi}$ can always be taken to be even or odd
- The eigenfunctions of $\hat{\Ham}$ can always be taken to be real

## Continuity
- Consider the 1D time-independent Schrödinger equation in the position basis:
 $$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V\psi=E\psi$$
 $$\frac{d^2\psi}{dx^2}=-\frac{2m(E-V)}{\hbar^2}\psi$$
	- If there is an abrupt but finite jump in $V$ (and therefore $\psi''$), $\psi'$ will still be continuous
	- If the jump is infinitely large (e.g. Dirac delta), $\psi'$ is discountinuous but $\psi$ is still continuous


## The free particle
- The Hamiltonian and time-independent Schrödinger equation for a free particle is:
$$\Ham=\frac{P^2}{2m}$$
$$\Ham\ket{E} = \frac{P^2}{2m}\ket{E}=E\ket{E}$$
- Any eigenvector of $P$ is also an eigenvector of $\Ham$, therefore allowed values of momentum are:
$$p=\pm\sqrt{2mE}$$
- Difference with classical case: degeneracy of energy leads to a subspace of eigenvectors
$$\ket{E} = \beta\Ket{p=+\sqrt{2mE}}+\gamma\Ket{p=-\sqrt{2mE}}$$
	- One particle with energy $E$ can be observed to be moving left or right
- Due to the degeneracy, it is more appropriate to label states and construct $\teo$ using $p$:
$$\begin{aligned} \teo(t) &= \int_{-\infty}^\infty \ket{p}\bra{p}\exp(-ip^2t/2m\hbar)\,dp \\ &= \sum_{\alpha=\pm} \int_0^{\infty} \frac{m}{\sqrt{2mE}} \ket{E,\alpha}\bra{E,\alpha} \,\exp(-iEt/\hbar)\, dE \end{aligned}$$
- As the $x$-space momentum eigenfunction is $\exp(ipx/\hbar)/\sqrt{2\pi\hbar}$, the energy eigenfunction is:
$$\braket{x|E} = \beta\frac{\exp(i\sqrt{2mE}x/\hbar)}{\sqrt{2\pi\hbar}} +\gamma\frac{\exp(-i\sqrt{2mE}x/\hbar)}{\sqrt{2\pi\hbar}}$$
- The stationary state in the position space is:
$$\braket{x|\Psi_E(t)}=\beta\frac{\exp[ik(x-\hbar kt/2m)]}{\sqrt{2\pi\hbar}}+ \gamma\frac{\exp[(-ik(x+\hbar kt/2m)]}{\sqrt{2\pi\hbar}}$$
	- $p=\hbar k$
	- The _phase velocity_ of a point on the wave is $\hbar k/2m$, or half of the classical velocity
- As for the [[Path integrals in quantum mechanics#The propagator|propagator]], it can be constructed from $\teo$:
$$K(x,t,x',t_0)=\braket{x|\teo(t,t_0)|x'}=\sqrt{\frac{m}{2\pi i\hbar t}} \exp\left[\frac{im(x-x')^2}{2\hbar t}\right]$$
### Wave packets and the group velocity
- The stationary states are non-normalisable, and cannot represent physical particles
- Instead, a linear combination of the stationary states has to be used:
$$\begin{aligned}\braket{x|\Psi(t)}&=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty\phi(p) \exp\left[\frac{ip}{\hbar}x-\frac{ip^2}{2m\hbar}t\right]\,dp \\ &= \int_{-\infty}^\infty \braket{x|p}\braket{p|\Psi(0)}\exp\left(-\frac{ip^2}{2m\hbar}t\right)\,dp\end{aligned}$$
- This _wave packet_ has a range of energies and phase velocities, and can represent a particle, as long as it is normalisable
- - The velocity of the particle represented by the wave packet is the [[Waves#Group velocity|group velocity]]:
$$v_g=\frac{d\omega}{dk}=\frac{\hbar k}{m}=v_{clas}$$
- The momentum-space wave function can be found with transforming $\braket{x|\Psi(0)}$:
$$\braket{p|\Psi(0)}=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty \exp(-ipx/\hbar)\braket{x|\Psi(0)}\,dx$$

### The Gaussian wave packet
>[!quote]
>There is an unwritten law which says that the derivation of the free-particle propagator be followed by its application to the Gaussian packet. Let us follow this tradition.
>-Ramamurti Shankar

- Consider the initial wave function in position space:
$$\braket{x|\Psi(0)}=\frac{1}{(\pi\Delta^2)^{1/4}}\exp\left(ip_0x/\hbar\right) \exp\left(-\frac{x^2}{2\Delta^2}\right)$$
- The time evolution of the position-space wave function is:
$$\braket{x|\Psi(t)}=\left[\sqrt{\pi}\left(\Delta+\frac{i\hbar t}{m\Delta}\right)\right]^{-1/2}\exp\left[-\frac{(x-p_0t/m)^2}{2\Delta^2(1+i\hbar t/m\Delta^2)}+\frac{ip_0}{\hbar}\left(x-\frac{p_0t}{2m}\right)\right]$$

- The corresponding position probability density is:
$$|\braket{x|\Psi}|^2=\frac{1}{\sqrt{\pi}(\Delta^2+\hbar^2t^2/m^2\Delta^2)^{1/2}} \exp\left[-\frac{(x-p_0t/m)^2}{\Delta^2+\hbar^2t^2/m^2\Delta^2}\right]$$

- The mean position and the width become:
$$\displaylines{\braket{X}=\frac{p_0t}{m}=\frac{\braket{P}t}{m} \\ \Delta X(t)=\frac{\Delta}{\sqrt{2}}\left(1+\frac{\hbar^2t^2}{m^2\Delta^4}\right)^{1/2}}$$

- The mean momentum is constant, with $\braket{P}=p_0$ and $\Delta P=\hbar/(\sqrt{2}\Delta)$
	- A small spread in position indicates a large spread in momentum

- The wave packet spreads, but maintains its group velocity

## Particle in a box
- The Hamiltonian for a particle in a "box", or an infinite potential well is:
$$V(x)=\begin{cases}
\infty &x<0 \\
0 &0\leq x\leq a \\
\infty &x>a
\end{cases}$$
- It is easy to see that $\psi(x)=0$ outside the well
- Solving the eigenvalue equation for $x<a$ with the boundary conditions $\psi(0)=\psi(a)=0$:
$$\psi(x)=\sqrt{\frac{2}{L}}\sin\left(k_nx\right)\hspace{1.5cm}k_n= \frac{n\pi}{a}$$
- Applying the Hamiltonian, the allowed energy levels can be found:
$$E_n=\frac{\hbar^2k_n^2}{2m}=\frac{\hbar^2n^2\pi^2}{2ma^2}$$
- One can estimate the lower bound in energy based on the uncertainty principle:
	- Consider a stationary state, where all expectation values are constant
	- For $x\leq a$, $\braket{P}=0$ as the wave cannot escape
	- $\braket{\Ham}=\braket{P}^2/(2m)=(\Delta P)^2/(2m)$
	- Using the uncertainty principle with $\Delta X=L/2$, a lower bound for $E=\braket{\Ham}$ can be found

## Bound states
- The particle in a box is the prime example of a _bound state_, where a particle cannot escape to infinity, in other words:
$$\lim_{x\to\infty}\psi(x)=0$$
- Bound states satisfy:
$$V(\pm\infty)>E$$
- The energy of bound states is always quantised, as the existence of a classically forbidden region applies constraints to the parameters of $\psi$, which can't always be fulfilled



## Single step potential
$$V(x)=\begin{cases}
0 &x<0 \\
V_0 &x\geq 0
\end{cases}$$


## The finite well
$$V(x)=\begin{cases}
V_0 &x<0 \\
0 &0\leq x\leq a \\
V_0 &x>a
\end{cases}$$


## The Delta Function Potential
$$V(x)=-\alpha\delta(x)$$

## The Quantum Harmonic Oscillator
$$V(x)=\frac{1}{2}m\omega^2x^2$$
- Details: [[Quantum Harmonic Oscillator]]

# The 3D time-independent Hamiltonian
- In 3 dimensions, the Hamiltonian bcomes:
$$\Ham=\frac{P^2}{2m}+V=\frac{1}{2m}(P_x^2+P_y^2+P_z^2)+V$$
- In the position basis, the Hamiltonian is:
$$\Ham=-\frac{\hbar^2}{2m}\nabla^2+V$$

- The equation can be rewritten in terms of the [[Angular momentum in quantum mechanics|angular momentum operators]]:
$$\frac{1}{2mr^2}\left[-\hbar^2\pd{}{r}\left(r^2\pd{}{r}\right) +\hat{L}^2 \right]\psi+V\psi=E\psi$$

## Central potentials
- For many systems, the potential only depends on distance from the origin:
$$V(\bm{r})=V(r)$$
- In this case, the 3-dimensional time-independent Schrodinger equation in the position basis becomes separable:
$$\psi(r,\theta,\phi)=R(r)\,Y(\theta,\phi)$$
- Then, one obtains two equations (with arbitrary separation constant) for $R$ and $Y$:
$$\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)-\frac{2mr^2}{\hbar^2}\left[V(r)-E\right]=l(l+1)$$
$$\frac{1}{Y}\left\{\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\pd{Y}{\theta}\right)+\frac{1}{\sin^2\theta}\frac{\partial^2Y}{\partial\phi^2}\right\}=-l(l+1)$$

- The normalisation criteria for the radial and angular parts of the wave function are:
$$\int_0^\infty r^2|R|^2\,dr=1\hspace{1.5cm}\int_0^\pi\int_0^{2\pi}|Y|^2\sin\theta\,d\theta\,d\phi=1$$


### The angular equation
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

### The radial equation
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

