- An _adiabatic_ process is one where the _external conditions_ change _gradually_
- In other words, the _timescale_ over which _external_ parameters change is _much longer_ than the timescale of "internal" changes
	- Example: a _pendulum_ with a movable platform, where even a small change in _position of the platform_ takes place over _many cycles_
	- Example: a _Foucault pendulum_

- To analyse motion _during an adiabatic process_, first assume the _external parameters held constant_, then allow the parameters to _vary with time_
	- Example: if the length of a pendulum changes slowly as $L(t)$, then the period is $2\pi\sqrt{L(t)/g}$

- For _molecules_, it is assumed that the _nuclei_ are relatively _stationary compared to electrons_
	- This is known as the [[Molecular quantum mechanics#The Born-Oppenheimer approximation|Born-Oppenheimer approximation]]
	- The _ground state energy_ is solved as a _function of inter-nuclear separation_
	- Thus, one can obtain the _equilibrium separation_ and _frequency of vibration_ around this equilibrium

## The adiabatic theorem
>[!info] Adiabatic theorem
>Suppose a Hamiltonian changes _gradually_ from $\hat{\Ham}(0)$ to $\hat{\Ham}(T)$. If the particle was initially in the $n$th eigenstate of $\hat{\Ham}(0)$, it will be _carried to_ the $n$th eigenstate of $\hat{\Ham}(T)$

- This theorem does not restrict the _phase_ of the wave function
- For a _constant_ Hamiltonian, the phase is simply $-E_nt/\hbar$
- Hence, the _phase factor_ after time $t$ can be generalised:
$$\theta_n(t)=\exp\left(-\frac{i}{\hbar}\int_0^t E_n(t')\,dt'\right)$$
- This is known as the _dynamic phase_

- There may also be a _geometric phase_ $\gamma_n(t)$, such that at time $t$, given final eigenstate $\psi_n$:
$$\Psi_n(t)=\exp[i\theta_n(t)]\exp[i\gamma_n(t)]\psi_n(t)$$
- As the phase of $\psi_n$ is _arbitrary_, $\gamma_n$ is still not well-defined

- If the system is carried in a _closed cycle_:
$$\hat{\Ham}(T)=\hat{\Ham}(0)$$
- Then the _geometric phase_ only depends on the _path taken_
- This is known as _Berry phase_:
$$\gamma_B\equiv\gamma(T)-\gamma(0)$$