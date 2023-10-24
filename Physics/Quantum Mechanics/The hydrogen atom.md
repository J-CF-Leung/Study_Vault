- Considerations:
	- _Electron_ spin
	- _Relativistic_ effects lead to _fine structure_
	- _Proton_ spin leads to _hyperfine structure_

# With electron spin
- The "zeroth-order" Hamiltonian for the hydrogen atom:
$$\hat{H}_0=\frac{\hat{p}^2}{2m_e}+V(r)\hspace{1.5cm} V(r)=-e\phi(r)=-\frac{Ze^2}{4\pi\epsilon_0r}$$
- It _does not include spin_
- The eigenstates are then _direct products_ of spatial and spin eigenstates:
$$\ket{nlm_lsm_s}=\ket{nlm_l}\otimes\ket{sm_s}$$
- The energies depend _only on_ $n$:
$$\hat{H_0}\ket{}=E_n\ket{} \hspace{1.5cm}E_n=-\frac{Z^2}{n^2}R_\infty$$
- The _degeneracy_ of each level is $2n^2$

- In _spherical polars_, the spatial components:
$$\ket{nlm_l}=R_{nl}(r)Y_{lm_l}(\theta,\phi)$$
- [[3D time-independent Hamiltonians#The hydrogen-like atom|Functional forms]]
- The energy eigenstates are _orthonormal_

- One can use the [[Angular momentum in quantum mechanics#Addition of angular momenta|total angular momentum]] as the basis states $\ket{njm_jls}$
$$\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}\hspace{1.5cm}j=l\otimes s=l\pm\frac{1}{2}$$
- They are also _energy eigenstates_ as they only depend on $n$
- They are known as the _coupled_ eigenstates
	- They are simply _linear combinations_ of the uncoupled eigenstates
- One can denote the states using [[Molecular quantum mechanics#Energy levels and term symbols|term symbols]]:
$$n^{2S+1}L_J$$

- The coupled eigenstates can be written as:
$$\ket{njm_jls}=\sum_{m_l+m_s=m_j}\ket{nlm_lsm_s}\braket{lm_lsm_s|jm_j}$$

- Consider that $\hat{\bm{L}}$ and $\hat{\bm{S}}$ _commute_ with each other
- One can prove that:
$$[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{L}}^2]=[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{S}}^2]=0$$
- Therefore:
$$[\hat{\bm{J}}^2,\hat{\bm{L}}^2]==0$$

- One can see that for the Hamiltonian, there are _two mutually commuting sets of operators_, each of which has _its own set of simultaneous eigenstates_:
$$\displaylines{\{\hat{H},\}\Longrightarrow\ket{} \\ \{\hat{H},\}\Longrightarrow\ket{}}$$

# Relativistic effects
- The Schrodinger equation is _Lorentz invariant_
	- It has a _first-order time derivative_ and _second-order space derivatives_

## Zero spin: Klein-Gordon equation
- Applying the operator replacements:
$$\bm{p}\longrightarrow -i\hbar\nabla \hspace{1.5cm} E\longrightarrow i\hbar\pd{}{t}$$
- Using the _relativistic_ relation:
$$E^2=|\bm{p}|^2c^2+m^2c^4$$
- This gives the _Klein-Gordon_ equation:
$$\frac{1}{c^2}\pd{^2\psi}{t^2}-\nabla^2\psi+\frac{m^2c^2}{\hbar^2}\psi=0$$
- This describes _relativistic particles of zero spin_

## Spin-half: Dirac equation
- The _Dirac equation_ can be expressed as:
$$i\hbar\pd{\psi}{t}=\hat{H}\psi \hspace{1.5cm} \hat{H}=c\hat{\bm{\alpha}}\cdot\hat{\bm{p}}+\beta mc^2$$
- One has to describe the wave function via a _spinor_:

- An external field is introduced with the _substitutions_:
$$\bm{p}\to\bm{p}-q\bm{A} \hspace{1.5cm} E\to E+q\phi$$
- This gives the equation:
$$(E'-q\phi)\psi=$$
- $E'$ is the _relativistic kinetic energy_:
$$E'\equiv E-mc^2$$

- The operator $\hat{\bm{S}}$ is the familiar [[Angular momentum in quantum mechanics#Spin angular momentum|spin operator]] for spin$-1/2$ particles
	- It obeys the same _commutation relation_
- The _intrinsic nature_ of spin can be said to be _derived_ from the Dirac equation
- The Hamiltonian includes a term:
$$\hat{H}_B=-\hat{\bm{\mu}}_S\cdot\bm{B} \hspace{1.5cm}\hat{\bm{\mu}}\equiv\frac{q}{m}\hat{\bm{S}}$$
- The [[Charged Particles#Spin precession|magnetic interaction with spin]] is also _derived_ fom the Dirac equation

## Application to the hydrogen atom
- Compute the _leading_ relativistic effects, up to terms of _order_ $v^2/c^2$
- With the _absence_ of an external _magnetic_ field, the Dirac equation becomes:

- This corresponds to applying some _perturbation_ $H'$ given by:

### Terms in the perturbation
- The first term can be understood as the _first-order relativistic correction_ to electron energy

- Spin-orbit term

- The _Darwin term_ is _purely relativistic_ in origin

### Applying perturbation theory
- As the _unperturbed_ energy levels are _degenerate_, one must use [[Approximation Methods#Degenerate perturbation theory|degenerate perturbation theory]]
