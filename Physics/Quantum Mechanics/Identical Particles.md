- In many systems, one comes across _many identical particles_
	- e.g. any multi-electron atom
# Particle exchange, fermions and bosons
- One can _index_ particles in a Hamiltonian, but they _do not label particular particles_, as they are _fundamentally indistinguishable_
- _Interchanging_ labels should leave a Hamiltonian _unchanged_

## Probability density
- The _probability density_ of finding 2 identical particles $1$ and $2$:
$$|\psi(\bm{r}_1,\bm{r}_2)|^2\,d^3\bm{r}_1\,d^3\bm{r}_2$$
- It should be _equivalent when labels are exchanged_:
$$|\psi(\bm{r}_1,\bm{r}_2)|^2=|\psi(\bm{r}_2,\bm{r}_1)|^2$$

- For a system of $N$ particles:
$$\psi=\ket{1,2,\dots N}$$
- The labels represent _all degrees of freedom for a single particle_

- If two particles $j$ and $k$ are _indistinguishable_, then from the requirement above:
$$\ket{1,2,\dots,j\dots k\dots N}=\exp(i\phi)\ket{1,2,\dots,k\dots j\dots N}$$
- Exchanging _twice_ gives the _same wave-function_:
$$\exp(2i\phi)=1$$
- Therefore:
$$\ket{1,2,\dots,j\dots k\dots N}=\pm\ket{1,2,\dots,k\dots j\dots N}$$

- If the wave-function is _symmetric_ under particle exchange, the particles are _bosons_
	- For large $N$, obey _Bose-Einstein statistics_
- If the wave-function is _antisymmetric_ under exchange, they are _fermions_
	- For large $N$, obey _Fermi-Dirac statistics_

- For fermions:
$$\ket{1,2,\dots,j\dots j\dots N}=0$$
- This is the _Pauli exclusion principle_
>[!info] Pauli Exclusion Principle
>Two _identical fermions_ cannot occupy a state where they have an _identical set of quantum numbers_
- E.g. same _spatial state and spin state_
- Two fermions can occupy the _same position_ if they have _different spin_

## Spin-statistics theorem
- To _identify_ particles as fermions or bosons, use the _spin-statistics theorem_
>[!info] Spin-statistics theorem
>Any particle with an _integer spin_ are _bosons_
>Any particle with a _half-inteer spin_ are _fermions_

- For a _multi-particle system_, by [[Angular momentum in quantum mechanics#Addition of angular momenta|adding angular momenta]]:
	- An _even_ number of _half-integer spins_ always gives _integer total spins_
	- An _odd_ number of _integer spins_ always gives _half-integer total spins_
- One can check symmetry by _exchanging particles one at a time_
- Therefore, the _spin-statistics theorem also holds for composite particles_

# Systems of identical particles
- For a system of $N$ _non-interacting, identical_ particles the Hamiltonian can be expressed as a _sum_ of _identical single-particle Hamiltonians_, each acting on _different particles_
$$\hat{H}(1,2\dots N)=\sum_{i=1}^N\hat{H}_1(i)$$
- Each single-particle Hamiltonian possess _a common set of eigenstates_
$$\hat{H}_1\ket{\alpha_i}=E_i\ket{\alpha_i}$$
- They _only act on their respective particle_

- A wave-function of the form:
$$\ket{}$$
- It satisfies, with total energy:

- However, it is _not symmetric or antisymmetric_ under exchange

## Slater determinants
- For a system consisting of _2 identical fermions_, one can make an antisymmetric state:
$$\ket{\psi}_A=\frac{1}{\sqrt{2}}(\ket{1,\alpha_1}\ket{2,\alpha_2}-\ket{1,\alpha_2}\ket{2,\alpha_1})$$
- This can be written as a _determinant_:
$$\ket{\psi}_A=\frac{1}{\sqrt{2}}\begin{vmatrix}\ket{1,\alpha_1}&\ket{2,\alpha_1} \\ \ket{1,\alpha_2}&\ket{2,\alpha_2}\end{vmatrix}$$

- This can be generalised to the $N-$particle _Slater determinant_:
$$\ket{\psi}_A=\frac{1}{\sqrt{N!}}\begin{vmatrix}\ket{1,\alpha_1}&\ket{2,\alpha_1} &\dots&\ket{N,\alpha_1}\\ \ket{1,\alpha_2}&\ket{2,\alpha_2}&\dots&\ket{N,\alpha_2} \\ \vdots &\vdots &\ddots &\vdots \\ \ket{1,\alpha_N}&\ket{2,\alpha_N}&\dots&\ket{N,\alpha_N}\end{vmatrix}$$

- Similarly, for _bosons_, set _all terms of the Slater deteminant as positive_
- This _sums over all permutations of states_, while _normalising_ with $1/\sqrt{N!}$
$$\ket{\psi}_S=\frac{1}{\sqrt{N!}}\sum_\text{all permutations}\ket{i_1,\alpha_1}\ket{i_2,\alpha_2}\dots\ket{i_N,\alpha_N}$$

# Two-electron systems
- Consider a _two-electron system_ occpying the _same spatial state_ $\ket{a(\bm{r})}$
- There are _two available states_ due to _spin_:
$$\displaylines{\ket{a\uparrow}=\psi_a(\bm{r})\ket{\uparrow}\equiv\ket{a(\bm{r})}\ket{\uparrow}\equiv\ket{a}\ket{\uparrow} \\ \ket{a\downarrow}\equiv\ket{a}\ket{\downarrow}}$$

- If they _occupy the same spin state_, one sees that the _Slater determinant vanishes_

- Therefore, they must occupy _different spin states_:
$$\ket{\psi}=\ket{a}_1\ket{a}_2\otimes\frac{1}{\sqrt{2}}\left(\ket{\uparrow}_1\ket{\downarrow}_2-\ket{\uparrow}_2\ket{\downarrow}_1\right)$$
- Their _total spin_ is then zero
- Manifestation of the _Pauli exclusion principle_ (same spatial state _forces_ different spin states)

- Suppose they are in _distinct spatial states_, $\ket{a(\bm{r})}$ and $\ket{b(\bm{r})}$
- Take states with the _same spin_:
$$\displaylines{\ket{\psi}_{\uparrow\uparrow}=\ket{a\uparrow}\ket{b\uparrow} \\ \ket{\psi}_{\downarrow\downarrow}=\ket{a\downarrow}\ket{b\downarrow}}$$
- These have a _total spin_ of $S=1$, with $m_S=\pm1$

- For states with _different spins_, form _linear combinations_ such that they are _eigenstates_ of [[Angular momentum in quantum mechanics#Addition of angular momenta|total spin]]:
$$\displaylines{\ket{\psi}_-=\frac{1}{\sqrt{2}}\left[\ket{a\uparrow}\ket{b\downarrow}+\ket{a\downarrow}\ket{b\downarrow}\right] \\ \ket{\psi}_+=\frac{1}{\sqrt{2}}\left[\ket{a\uparrow}\ket{b\downarrow}-\ket{a\downarrow}\ket{b\downarrow}\right]}$$
- The upper state has $S=1$, with $m_S=0$
- The lower state has $S=0$, with $m_S=0$

- This gives a set of _triplet states_
	- The _spatial part_ is _antisymmetric_
	- The _spin part_ is _symmetric_
- There is another _singlet state_

- For _two identical bosons_, one can use the same procedure
- For $N>2$, overall states _do not in general factorise into separate spatial and spin components_
	- For large $N$, calculate [[Advanced statistical mechanics#Grand canonical ensemble|probability distribution functions for each state]]

# Exchange forces
- Consider two _non-interacting particles_, each occupying _distinct, orthonormal states_ $\ket{a}$ and $\ket{b}$
- For _distinguishable particles_, there are _two possible states_
$$\psi(x_1,x_2)=\cases{\ket{1,a}\ket{2,b} \\ \ket{2,a}\ket{1.b}}$$
- One can calculate a _mean-square separation_:
$$\mean{(x_1-x_2)^2}\equiv\mean{x_{12}^2}=\mean{x^2}_a+\mean{x^2}_b-2\mean{x}_a\mean{x}_b$$

- For _identical particles_, the _spatial component_ is:
$$\ket{\psi}=\frac{1}{\sqrt{2}}\left(\ket{1,a}\ket{2,b}\pm\ket{2,a}\ket{1,b}\right)$$
- The mean square separation is found to be:
$$\displaylines{\mean{x_{12}^2}=\mean{x^2}_a+\mean{x^2}_b-2\mean{x}_a\mean{x}_b\mp2|x_{ab}|^2 \\ x_{ab}=\braket{a|\hat{x}|b}}$$
- Therefore, _identical, non-interacting particles_ are typically _closer/further apart_ than _distinguishable particles in the same spatial states_

- For example, _triplet states_ are typically _further apart on average_ than the singlet state

- The quantity $x_{ab}$ measures the _spatial overlap_ of each wave-function
- If there is _very little overlap_, then identical particles are _practically indistinguishable_
- If there is _overlap_, then identical particles have a _"force" of attraction/repulsion_ for a _symmetric/antisymmetric_ state