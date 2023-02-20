>[!quote]
>Ludwig Boltzmann, who spent much of his life studying statistical mechanics, died in 1906, by his own hand. Paul Ehrenfest, carrying on the work, died similarly in 1933. Now it is our turn to study statistical mechanics.
>
>Perhaps it will be wise to approach the subject cautiously.
>
>-David L. Goodstein


# The classical statistics of particles
- For a macroscopic body with a very large number of degrees of freedom, solving for the motion of all of its particles becomes impossible
- A state where all degrees of freedom have a specified value is a _microstate_
- Instead, _statistical laws_ emerge, which adequately describe the behaviour of the system at a whole, and are only applicable to large systems
- Assume all particles obey classical mechanics
- Given a system with $s$ degrees of freedom, a certain state can be denoted by a _phase point_ $(q_1,q_2,...,q_s,p_1,p_2,...,p_s)$ in a $2s-$dimensional [[Analytical classical mechanics#Phase space|phase space]] 

## The statistical distribution function
- Inside a closed system with many particles, consider a subsystem of some particles that freely interacts with the rest
- _Ergodic hypothesis_ - After a sufficiently long time $T$, the subsystem will have been in every possible state, i.e. its phase points will have covered all of the subsystem's phase space
- Let $\Delta t$ be the amount of time it spent in the phase volume $\Delta p \Delta q$, the probability the subsystem is in that volume is $w=\Delta t/T$
- Upon taking the limit of an infinitesimal volume $dp\,dq=dq_1\,dq_2\,...dq_s\,dp_1\,dp_2\,...\,dp_s$ , the probability $dw$ of the subsystem being in the phase interval $(q,p)$ to $(q+dq,p+dp)$ is:
$$dw = \rho(q_1...q_s,p_1...p_s)\,dq\,dp$$
- $\rho(p,q)$ is the _statistical distribution function_, and is (obviously) normalised:
$$\int \rho(p,q)\,dp\,dq=1$$
- The statistical distribution _does not depend on the initial conditions_ of the system, as after a sufficiently long time, it has been through every point in phase space, any of which can be the initial state

## Average values
- The statistical distribution allows us to evaluate the distribution and mean of any variable $f(p,q)$ related to the system as a whole, with the mean being:
$$\overline{f}=\left<f\right>=\int f(p,q)\,\rho(p,q)\,dp\,dq$$
- With the definition of $dw$, it can be seen that this is identical to time averaging
- Statistical mechanics is inherently probabilistic as the initial conditions are not used\
- As macroscopic bodies are observed, all quantities are practically constant and equal to their mean (extremely sharp peak at $f=\bar{f}$)
- A system with physical quantities equal (to a very high accuracy) to the mean value is in a state of _statistical/thermodynamic/thermal equilibrium_
- The time it takes for a perturbed system to equilibriate is the _relaxation time_
- The study of how a system equilibriates is _kinetics_, i.e. **not statistical mechanics**

## Statistical independence and fluctuations

### Statistical independence of multiple subsystems
- Consider the interaction of a subsystem with its surroundings
	- It interacts via particles on the surface
	- The proportion of the subsystem that interacts with the rest decreases with size
	- A large subsystem (still small compared to the rest) can be considered _quasi-closed_ for a short period of time
- Different quasi-closed subsystems within the same closed system can be considered statistically independent
- Let there be 2 subsystems, with volume elements $dp^{(1)}\,dq^{(1)}$ and $dp^{(2)}\,dq^{(2)}$
- If regarded as a composite subsystem $(12)$, as the subsystems are statistically independent:
$$\displaylines{\rho_{12}\,dp^{(12)}\,dq^{(12)} = \rho_1\,dp^{(1)}\,dq^{(1)} \rho_2\,dp^{(2)}\,dq^{(2)} \\ \rho_{12}=\rho_1\rho_2}$$
- Converse: if the above is true for any 2 subsystems, they are statistically independent
- Can hold for any number of small subsystems
- Given a physical quantity $f$, the product of the subsystem means is:
$$\overline{f_1f_2}=\bar{f_1}\bar{f_2}$$
### Fluctuations
- Over time, a macroscopic quantity $f$ will fluctuate around the mean $\bar{f}$
- As it varies in both directions, $\mean{\Delta f}=\mean{f-\bar{f}}=0$
- Instead, the _root-mean-square fluctuation_ $\sqrt{\mean{(\Delta f)^2}}$ is used
$$\mean{(\Delta f)^2}=\overline{f^2}-(\bar{f})^2$$
- The _relative fluctuation_ of a quantity $f$ is $\sqrt{\mean{(\Delta f)^2}}/\bar{f}$ 
- To obtain $f$ for a closed system, one can simply add up the $\bar{f_i}$ for many quasi-closed subsystems:
$$\bar{f} = \sum_{i=1}^N\bar{f_i}$$
- The RMS fluctuation is:
$$\mean{(\Delta f)^2} = \mean{\left(\sum\Delta f_i\right)^2}=\sum \mean{(\Delta f_i)^2} \propto N$$
	- Due to statistical independence, $\mean{\Delta f_i\Delta f_k} = 0$
- As $\bar{f}$ is also proportional to $N$, the relative fluctuation is proportional to $1/\sqrt{N}$
- For a large enough system, the value of $f$ is always close to $\bar{f}$


## Phase space flow and Liouville's theorem
>[!INFO] Liouville's Theorem
For a small, closed region of phase space, its shape will change over time, but the total volume will not
In other words, the distribution function along a phase space trajectory is constant in time
- Consider a _statistical ensemble_ of identical subsystems, represented by a "neighbourhood" of phase points in $2s-$dimensional phase space
- As time progresses, the ensemble of points will still be distributed according to $\rho(q,p)$ at $t=0$
- Proof of unchanging volume: [[Analytical classical mechanics#Liouville's Theorem]]
- Liouville's equation:
$$\pd{\rho}{t}=-\PB{\rho}{\Ham}$$
- Liouville's theorem is valid for any _quasi-closed_ system

## The equal probabilities postulate
- One assumption of statistical thermodynamics is that all microstates are equally likely
- It relies on:
	- The fact that the systems under discussion are in equilibrium
	- The ergodic hypothesis
	- (QM) the principle of detailed balance/ (CM) Liouville's theorem
- Ergodic hypothesis: quantum mechanically, there is some way, direct or indirect, to get from any state to any other
	- "Once the quantum apple has been bitten, the loss of innocence is permanent" - R. Shankar
- Detailed balance: probability of any transition is equal to probability of reverse transition
	- Given states of equal energy $a$ and $b$, the probabilities per unit time $P$ are equal:
	$$P(a\rightarrow b)=P(b\rightarrow a)$$
- The classical proof:
	- In equilibrium, all probabilities are independent of time
	- Only a uniform distribution of points in phase space is consistent with equilibrium and Liouville's theorem

- The quantum mechanical proof:
	- Let each microstate $a$ have a probability $w_a$
	- The rate of change of $w_a$ is:
	$$\dot{w}_a=\sum_bw_bP(b\rightarrow a)-w_a\sum_bP(a\rightarrow b)$$
	- At equilibrium, $w_a$ is constant, and using the principle of detailed balance:
	$$\sum_bP(a\rightarrow b)(w_b-w_a)=0$$
	- The only non-trivial solution is that $w_b=w_a$ for all $a$ and $b$

## Importance of energy in statistical mechanics
- From Liouville's theorem, it is clear that $\rho(q,p)$ is a _constant of motion_ for a quasi-closed subsystem
- For two quasi-closed subsystems, $\rho_{12}=\rho_1\rho_2$
- It follows that $\ln{\rho}$ is an _additive constant of motion_ ($\ln{\rho_{12}}=\ln{\rho_1}+\ln{\rho_2}$)
- In mechanics, the independent additive constants of motion are energy $E$, momentum $\bm{P}$, and angular momentum $\bm{L}$, therefore $\ln{\rho}$ can be expressed as:
	$$\ln{\rho}=\alpha+\beta E(q,p)+\bm{\gamma}\cdot\bm{P}(p)+\bm{\delta}\cdot\bm{L}(q,p)$$
	- $\alpha$ is for normalisation
	- $\beta,\bm{\gamma},\bm{\delta}$ determined from values of $E,\bm{P},\bm{L}$ 
- One can _transform_ into a coordinate system where the total $\bm{P}$ and $\bm{L}$ of the system is zero
- Therefore, $\ln{\rho}$ becomes:
$$\ln{\rho}=\alpha+\beta E(q,p)$$
>[!info] A fundamental principle of statistical mechanics
>The statistical properties of a system can be derived from only the energy (or Hamiltonian)

## The microcanonical ensemble
- The simplest statistical distribution is where $\rho$ is constant for $E=E_0$, and zero everywhere else
- The resulting distribution, known as the _microcanonical ensemble_:
$$\rho=\text{const}\cdot\delta(E-E_0)$$

## Large systems
- Relaxation time increases with the size of the system
- For a large system, small parts of it may attain equilibrium by themselves before the system as a whole
- Each small part can be described by a dsitribution function $\rho$ with their own parameters $(\alpha,\beta,\bm{\gamma},\bm{\delta})$
- Another kind of partial equilibrium may be attained if multiple processes occur at different speeds
	- For a slow chemical reaction, the molecules may reach thermal equilibrium long before chemical equilibrium
- A macrostate describes the mean values of physical quantities, determining a particular partial equilibrium

# The quantum statistics of particles
- Assume all particles _obey quantum mechanics_
- Integrating Schrödinger's equation for every particle is impossible

## The practical non-existence of stationary states
- For macroscopic bodies, the energy eigenvalue spectrum is infinite, and extremely dense
- For a given finite range, the number of energy levels increases exponentially with particle number
- The energy of a system is always "broadened" due to interactions with surroundings, with interaction energy >> gap between levels
- The energy-time uncertainty principle:
	- Let there be an interaction between particles last for time $t$, and the energy of one particle before and after the interaction be $E$ and $E'$ respectively
	- Uncertainties: $|\Delta E-\Delta E'| \geq \hbar/\Delta t$
	- For an uncertainty smaller than the energy level gap, and extremely long $\Delta t$ is needed

## The statistical matrix
- To describe an ensemble of particles in a range of states, one must use the [[Density matrix|density matrix]]
- It allows one to calculate means and probabilities of measuring a certain value
- In statistical mechanics, the density matrix of the energy representation, also known as the _statistical matrix_, is used
- For a statistical matrix $\hat{w}$, the mean of a physical quantity $\Omega$ is:
$$\overline{\braket{\Omega}}=\text{Tr}(\hat{\Omega}\hat{w})$$
- The ensemble is never _in_ one of the states of the statistical matrix, as there is no stationary state, the matrix simply a tool to calculate resultant averages of macroscopic quantities
- The statistical matrix is the quantum analogue of [[Fundamental principles of statistical mechanics#The statistical distribution function|the statistical distribution function]] 
- Theorems applied to the classical case, such as relative fluctuations also apply here
- Comparison
	- Classical: direct probability distribution of the system having position and momenta $(q,p)$
	- Quantum: no indication of coordinates and momenta, only probabilities of certain states
		- Coordinates and momenta cannot have definite values simultaneously
- The probability distribution for the coordinate $q$ and momentum $p$ are computed by:
$$\displaylines{dw_q=\text{Tr}(\mathcal{P}_q\hat{w})\,dq=\sum_iw_{i}|\braket{q|E_i}|^2\,dq \\
dw_p=\text{Tr}(\mathcal{P}_p\hat{w}) \,dq=\sum_i}$$