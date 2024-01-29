- Typically, in _insulators_, electronic energy levels are of the order $\text{eV}$, corresponding to a _temperature_ of $\sim 10,000\text{ K}$
- Hence, _electronic specific heat_ is only significant in very high temperatures

- In _metals_, one can have _low energy excitations_ for a _small fraction of electrons_
- Conduction electrons form a [[Advanced statistical mechanics#The Fermi gas|degenerate Fermi gas]]
- A _fraction_ $\sim k_{B}T/E_{F}$ are close enough to $\mu$ to contribute to _heat capacity_

- For electrons on the _Fermi surface_, most travel at _very high speeds_
- Without external field, the _drift velocity_ $\left<v\right>$ is $0$

# Free electron gas and the Fermi sphere
- The _free electron gas_:
$$-\frac{\hbar^{2}}{2m}\nabla^{2}\psi(\boldsymbol{r})=E\psi(\boldsymbol{r})$$
- Introduce _eigenstates_
$$\psi(\boldsymbol{r})$$

- With _periodic boundary conditions_, the _allowed values_ of $\boldsymbol{k}$ are _discrete_:
$$\boldsymbol{k}=$$
- $n_i$ are _positive or negative integers_

- At _zero temperature_, the _Fermi sphere_ is filled up to Fermi energy $E_{F}$
- Each _triplet_ of $n_{i}$ corresponds to _2 states_ due to _spin degeneracy_
- The _volume_ of a $\boldsymbol{k}-$state is $(2\pi/L)^{3}$

- Writing out the _volume_ of the Fermi sphere in terms of $k_{F}$, one gets:
$$N=2 \left( \frac{4}{3}\pi k_{F}^{3} \right)\left( \frac{2\pi}{L} \right)^{-3}\implies k_{F}=(3\pi^{2}n)^{1/3}$$
- One then gets $E_{F}\propto n^{2/3}$

- Define a _density of states_ w.r.t. $E_{F}$:
$$g(E_{F})\equiv \frac{dn}{dE_{F}}=\frac{3}{2} \frac{n}{E_{F}}$$
- The _density of states_ w.r.t. energy:
$$g(E)\,dE=\frac{2(4\pi k^{2}\,dk)}{8\pi^{3}/V}$$
- It is _proportional to volume_
- One can define $g(E)$ as _number of states per energy per unit volume_ to remove the normalisation factor $V$

# Thermodynamic properties
- The [[Advanced statistical mechanics#The Fermi gas|Fermi distribution]]:
$$f(E)=\frac{1}{\exp[(E-\mu)/k_{B}T]+1}$$
- At _zero temperature_, the _chemical potential_ $\mu=E_{F}$
	- The distribution is a _step function_
- At finite temperature, there is some _smearing_ $\sim k_{B}T$
- At _room temperature_, $k_{B}T\approx 26 \text{ meV}$
- For _metals_, $E_{F}\approx 1-10\,\text{eV}\gg k_{B}T_\text{room}$

- The _number density_:
$$n=\frac{1}{V}\sum_\text{states} f(E_{i})=\int  g(E)f(E) \, dE $$
- The _internal energy density_:
$$u=\frac{U}{V}=\int E\,g(E)\,f(E) \, dE $$
- The _heat capacity at constant volume_:
$$c_{V}=\frac{\partial u}{\partial T}\Bigg|_{V}=\int E \,g(E)\,\frac{\partial f(E)}{\partial T} \, dE $$
- The derivative is _sharply peaked_ at the _chemical potential_ $\mu$
- Hence, the _contributions_ are mainly from states _around_ $k_{B}T$ of $\mu$
- Each state has specific heat $\sim k_{B}$, giving total specific heat:
$$c_{V}\approx n \frac{k_{B}T}{E_{F}}k_{B}$$
- One gets a more exact answer from the [[Advanced statistical mechanics#Away from absolute zero|Sommerfeld expansion]]:
	- It is a _leading order term_ from the expansion of $\mu$ in powers of $(k_{B}T/E_{F})^{2}$
$$c_{V}=\frac{\pi^{2}}{3}k_{B}^{2}Tg(E_{F})$$
- Defining the _Fermi temperature_ $T_{F}=E_{F}/k_{B}$
$$c_{V}=\frac{\pi^{2}}{2}\frac{T}{T_{F}}nk_{B}$$

- Typically in _solids_, this is much smaller than the _lattice specific heat_ due to [[Phonons]]
- It is more achieveable with a _mixture_ of $\ce{ ^{3}He }$ and $\ce{ ^{4}He }$ (Fermi gas of atoms)

# Screening and the Thomas-Fermi approximation
- Consider adding some _positive charge_ to a solid
- In a _metal_, _classically_, electrons can _move freely_, and _screen_ the positive charge, _cancelling out_ the electric field
	- In a _dielectric_, the potential is _reduced_ by the dielectric constant $\epsilon$

- _Quantum mechanically_, electrons are _waves_ and hence the electrons _cannot be aribitrarily close to the charge_
	- Electrons _minimise_ the _potential and kinetic energies_
- There is a _length scale_ over which the electron is _screened_

- The _charge density response_ of a free-electron gas to some _perturbing potential_ $V_{0}(\boldsymbol{r})$
$$\nabla^{2}V_{0}(\boldsymbol{r})=-\frac{\rho_{0}(\boldsymbol{r})}{\epsilon_{0}}$$

- Jellium

- In the presence of a _perturbing potential_ $V_\text{ext}(\boldsymbol{r})$, the _charge density redistributes_ to $\rho(\boldsymbol{r})=\rho_{0}(\boldsymbol{r})+\delta \rho(\boldsymbol{r})$
- This then _changes the potential_ to

- Assume the perturbing potential is _slowly varying_, and only shifts _free electron energy levels_