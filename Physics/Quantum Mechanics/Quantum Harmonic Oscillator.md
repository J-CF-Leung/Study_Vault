# In 1 dimension
- The Hamiltonian:
$$\hat{\Ham}=\frac{\hat{p}^2}{2m}+\frac{1}{2}m\omega^2\hat{x}^2$$
- System always vibrates at $\omega$, an energy eigenstate gives an indication of "average" amplitude and momentum

## Power series method
- What to solve: The time-independent Schrodinger equation in the coordinate basis
$$-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}\psi+\frac{1}{2}m\omega^2x^2\psi=E\psi$$
- Consider the dimensionless variables:
$$\displaylines{\xi=\sqrt{\frac{m\omega}{\hbar}}x \\ K=\frac{2E}{\hbar\omega}}$$
- The Schrodinger equation becomes:
$$\frac{d^2\psi}{d\xi^2}=(\xi^2-K)\psi$$
- In the limit of _large $\xi$_, the solution tends to $\psi\approx\exp(-\xi^2/2)$

- Then, let $\psi$ be:
$$\displaylines{\psi=h(\xi)\exp(-\xi^2/2) \\ h(\xi)=\sum_{n=0}^\infty a_n\xi^n}$$
- Using a power series, one gets that only certain values of $K$ makes the function _square-integrable_:
$$K=2n+1\rightarrow E=\left(n+\frac{1}{2}\right)\hbar\omega$$
- Continuing the process, one can find the wave functions to be:
$$\psi_n(x)=\left(\frac{m\omega}{2^{2n}\pi\hbar(n!)^2}\right)^{1/4} H_n(\xi)\exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$
- $H_n$ are the _Hermite polynomials_, defined [[Special functions and orthogonal relations#Hermite polynomials|here]]


## Ladder operators
- Looking at the eigenvalue equation:
$$\left(\frac{\hat{p}^2}{2m}+\frac{1}{2}m\omega^2\hat{x}^2\right)\ket{E} =E\ket{E}$$
- Introduce the _ladder operators_:
$$\hat{a}_+\equiv\sqrt{\frac{1}{2m\omega\hbar}}(m\omega \hat{x}-i\hat{p})$$
$$\hat{a}_-\equiv\sqrt{\frac{1}{2m\omega\hbar}}(m\omega \hat{x}+i\hat{p})$$
	- Hermitian conjugates of each other

- Using the commutation relation of $[\hat{x},\hat{p}]$:
$$[\hat{a}_-,\hat{a}_+]=1$$
- Rewrite the Hamiltonian:
$$\hat{\Ham}=\hbar\omega\left(\hat{a}_\pm\hat{a}_\mp\pm\frac{1}{2}\right)$$
- Given one eigenstate of the Hamiltonian, these operators can produce more, with different energies:
$$\displaylines{\hat{\Ham}\ket{E}=E\ket{E} \\ \hat{\Ham}(\hat{a}_+\ket{E})=(E+\hbar\omega)\ket{E} \\ \hat{\Ham}(\hat{a}_-\ket{E})=(E-\hbar\omega)\ket{E}}$$
- As the minimum of the potential energy is zero, energy cannot be lowered infinitely
- Therefore, there must be a _ground state_ $\ket{E_0}$ where:
$$\hat{a}_-\ket{E_0}=\ket{0}$$

- Solving the equation, one gets the normalised ground state and its energy to be:
$$\braket{x|E_0}=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}\exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$
$$E_0=\frac{1}{2}\hbar\omega$$
- Comparing the equation for the Hamiltonian and the energies, one sees:
$$\hat{a}_+\hat{a}_-=n$$
	- This is also known as the _counting operator_
	- From the commutation relation, $\hat{a}_-\hat{a}_+=n+1$

- From applying $\hat{a}_\pm$ to $\ket{E_n}$, one gets a ket _proportional_ to $\ket{E_{n\pm 1}}$
- By examining $\braket{E_{n\pm1}|E_{n\pm1}}$, the proportionality constants are found to be:
$$\displaylines{\hat{a}_+\ket{E_n}=\sqrt{(n+1)}\ket{E_{n+1}} \\\hat{a}_-\ket{E_n}=\sqrt{n}\ket{E_{n-1}}}$$

- Combining these, one gets the general wave functions to be:
$$\braket{x|E_n}=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}\frac{1}{\sqrt{n!}}(\hat{a}_+)^n\exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$

## General features of the eigenfunctions
- The energy levels are quantised, but the gap is negligible compared to the energy of a clasically oscillating object
- At high energy levels, the behaviour of the particle becomes more classical
- There is a zero-point energy reflecting the uncertainty principle

### Average values

### Uncertainty