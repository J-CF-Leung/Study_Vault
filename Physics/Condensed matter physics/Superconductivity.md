![[Superconducting periodic table.png|500]]
# Phenomenology
- A _drop_ in _resistivity_ $\rho$ to _zero_ at _low temperatures_

- This leads to _dissipation-less currents_

- One consequence is that for a _ring geometry_, it _freezes_ the flux inside the ring
	- The flux takes an _infinite time_ to decay
	- The flux frozen must also be an _integer multiple_ of the _flux quantum_
$$\frac{\partial B}{\partial t}=-\nabla\times \boldsymbol{E}=\rho \nabla\times \boldsymbol{J}=0$$
- If one tries to _switch on_ a field below superconducting temperature, it _will not penetrate_ into the material
- Meanwhile, if one _keeps the magnetic field while cooling_, the material will _expel_ the magnetic field
	- The _Meissner-Ochsenfeld effect_
![[Meissner effect.png|200]]

- Above a certain _critical field_, superconductivity will be _destroyed_
	- Type I: complete breakdown of superconducting state
	- Type II: _partial_ penetration
![[Critical field for superconducting.png|400]]

## London equations
- From _Drude theory_:
$$\left( \frac{\partial}{\partial t}+\frac{1}{\tau} \right)\boldsymbol{j}=\left( \frac{\partial}{\partial t}+\frac{1}{\tau} \right)\left( \frac{ne^{2}}{m} \right)\boldsymbol{E}$$
- For perfect conductivity, $\tau\to \infty$
	- $\Lambda=(ne^{2}/m)^{-1}$
$$\Lambda \frac{\partial}{\partial t}\boldsymbol{j}=\boldsymbol{E}$$
- One can have a _constant current without any electric field_

- Then from Maxwell's equations:
$$\displaylines{\frac{\partial \boldsymbol{B}}{\partial t}=-\nabla\times \boldsymbol{E}=-\Lambda \nabla\times \frac{\partial}{\partial t}\boldsymbol{j} \\ \boldsymbol{B}=-\Lambda \nabla\times \boldsymbol{j}}$$
- This gives _flux expulsion_

- Using $\nabla\times \boldsymbol{B}=\mu_{0}\boldsymbol{j}$, this gives:
$$-\nabla^{2}\boldsymbol{B}=-\frac{\mu_{0}}{\Lambda}\boldsymbol{B}$$
- The magnetic field must _decay_ with some _penetration depth_:
$$B\propto \exp\left( -\frac{x}{\lambda} \right)\qquad \lambda^{2}=\frac{\Lambda}{\mu_{0}}=\left( \frac{c}{\omega_{p}} \right)^{2}$$
- Typical depth is $\sim 40\,\text{nm}$

- The London equations imply that for the _vector potential_:
$$\boldsymbol{A}=-\Lambda \boldsymbol{j}$$
- The _London gauge_:
$$\nabla\cdot \boldsymbol{A}=0$$
- Meanwhile, $\boldsymbol{A}=0$ in the _bulk_, and $\boldsymbol{A}_{\perp}=0$ on the _surface_

### Atomic diamagnetism analogy
- Decompose an atomic wavefunction:
$$\psi=|\psi|\exp(i\phi)$$
- From _single-valuedness_, the _phase change_ upon circling the nucleus is $2\pi n$ regardless of field
- There is then _quantised wavelengths_ $\lambda=2\pi r/n$
- The _semiclassical_ momentum, taking the _vector potential_ into account:
$$p=mv+qA=\frac{h}{\lambda}$$

- When one _changes_ $\boldsymbol{A}$, there is some _screening current_
$$j=nqv=-\frac{nq^{2}}{m}A$$
- Same as the London eq.
## Ginzburg-Landau Theory
