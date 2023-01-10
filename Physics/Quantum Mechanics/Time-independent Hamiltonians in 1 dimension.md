# The time-independent Schrödinger equation
- Applicable for problems with a time-independent Hamiltonian
- The [[Fundamentals of quantum mechanics#Time-independent Hamiltonians and stationary states|time-independent Schrödinger equation]] solves for the eigenkets of the Hamiltonian:
$$\Ham\ket{E}=E\ket{E}$$
- The resultant [[Fundamentals of quantum mechanics#The time-evolution operator|time-evolution operator]] and wave function become:
$$\teo = \sum_n\ket{E_n}\bra{E_n}\exp(-iE_nt/\hbar)=\int\ket{E}\bra{E}\exp(-iEt/\hbar)\,dE$$
$$\ket{\Psi(t)} =\sum_n\ket{E_n}\braket{E_n|\Psi_0}\exp(-iE_nt/\hbar) =\int \ket{E}\braket{E|\Psi_0}\exp(-iEt/\hbar)\,dE$$


# Useful theorems
- The energy $E$ has to be real, and larger than minimum of $V(x)$ for $\wv$ to be normalisable
- If $V(x)$ is an even function, then $\braket{x|\Psi}$ can always be taken to be even or odd
- The eigenfunctions of $\hat{\Ham}$ can always be taken to be real

## Continuity
- Consider the 1D time-independent Schrödinger equation in the position basis:
 $$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V\psi=E\psi$$
 $$\frac{d^2\psi}{dx^2}=-\frac{2m(E-V)}{\hbar^2}\psi$$
	- If there is an abrupt but finite jump in $V$ (and therefore $\psi''$), $\psi'$ will still be continuous
	- If the jump is infinitely large (e.g. Dirac delta), $\psi'$ is discountinuous but $\psi$ is still continuous


# The free particle
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
## Wave packets and the group velocity
- The stationary states are non-normalisable, and cannot represent physical particles
- Instead, a linear combination of the stationary states has to be used:
$$\begin{aligned}\braket{x|\Psi(t)}&=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty\phi(p) \exp\left[\frac{ip}{\hbar}x-\frac{ip^2}{2m\hbar}t\right]\,dp \\ &= \int_{-\infty}^\infty \braket{x|p}\braket{p|\Psi(0)}\exp\left(-\frac{ip^2}{2m\hbar}t\right)\,dp\end{aligned}$$
- This _wave packet_ has a range of energies and phase velocities, and can represent a particle, as long as it is normalisable
- - The velocity of the particle represented by the wave packet is the [[Waves#Group velocity|group velocity]]:
$$v_g=\frac{d\omega}{dk}=\frac{\hbar k}{m}=v_{clas}$$
- The momentum-space wave function can be found with transforming $\braket{x|\Psi(0)}$:
$$\braket{p|\Psi(0)}=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty \exp(-ipx/\hbar)\braket{x|\Psi(0)}\,dx$$

## The Gaussian wave packet
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

# Particle in a box
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

# Bound states
- The particle in a box is the prime example of a _bound state_, where a particle cannot escape to infinity, in other words:
$$\lim_{x\to\infty}\psi(x)=0$$
- Bound states satisfy:
$$V(\pm\infty)>E$$
- The energy of bound states is always quantised, as the existence of a classically forbidden region applies constraints to the parameters of $\psi$, which can't always be fulfilled



# Single step potential
$$V(x)=\begin{cases}
0 &x<0 \\
V_0 &x\geq 0
\end{cases}$$


# The finite well
$$V(x)=\begin{cases}
V_0 &x<0 \\
0 &0\leq x\leq a \\
V_0 &x>a
\end{cases}$$


# The Delta Function Potential
$$V(x)=-\alpha\delta(x)$$

# The Quantum Harmonic Oscillator
$$V(x)=\frac{1}{2}m\omega^2x^2$$
- Details: [[Quantum Harmonic Oscillator]]
