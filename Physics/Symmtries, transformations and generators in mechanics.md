- A symmetry is an operation that does not change the functional form of the [[Analytical classical mechanics|Lagrangian or Hamiltonian]]

## Symmetries in Lagrangian mechanics

### Noether's theorem
- Let there be a one-parameter transformation $q_i(t) \rightarrow Q_i(s,t)$, $Q_i(0,t)=q_i(t)$
- Symmetry: $\Lagr$ is invariant in first order of $s$
$$\frac{\partial}{\partial s}\Lagr(Q_i(s,t),\dot{Q}_i(s,t),t)=0$$
>[!info] Noether's Theorem
>For every symmetry of the action of a system, there is a corresponding conserved quantity

- In the case of the one-parameter transformation, the conserved quantity is:
$$\pd{\Lagr}{s}\Bigg{|}_{s=0}=\frac{d}{dt}\left(\sum_i\pd{\Lagr}{Q_i}\pd{Q_i}{s}\Bigg|_{s=0}\right)=0$$
#### Example: Translations, homogeneity of space
- Consider a system of $i$ particles, at positions $\bm{r}_i$ translated by vector $\bm{n}$
$$\bm{r}_i(t) \rightarrow \bm{r}_i(t)+s \,\bm{n}$$
- Invariance of $\Lagr$ after translation:
$$\pd{\Lagr}{s}=\frac{d}{dt}\left(\sum_i\bm{p}_i\cdot\bm{n} \right)=0$$
- Total momentum along direction $\bm{n}$ is conserved
- The conservation holds for all $\bm{n}$, therefore total momentum is conserved
	- Example: Two-body system
	- Applying Noether's theorem for all directions --> $\dot{p}_i=0$  $\forall\; i$
#### Isotropy of space and rotational invariance
- $\bm{r}_i \rightarrow \bm{r}_i +\alpha\hat{\bm{n}}\times\bm{r}_i$
- Conserved quantity: $\hat{\bm{n}}\cdot \bm{L}$
- $\hat{\bm{n}}$: arbitrary axis, therefore $\bm{L}$ is conserved
#### Homogeneity of time
- Time-translation invariance
- Moving the system in time does not affect its evolution
- Lagrangian cannot explicitly depend on time
- Total change in value of Lagrangian:
$$\frac{d\Lagr}{dt}=\frac{d}{dt}\left(\sum_i\pd{\Lagr}{\dot{q}_i}\dot{q}_i\right)+\pd{\Lagr}{t}$$
- Introduce the Hamiltonian:
$$\Ham=\sum_i\left(\pd{\Lagr}{\dot{q}_i}\dot{q}_i\right)-\Lagr$$
$$\frac{d\Ham}{dt}=-\pd{\Lagr}{t}$$
- The Hamiltonian only changes when the Lagrangian depends explicitly on time
- When $\Lagr=T-V$, $\Ham=T+V=E$
- Energy is conserved when Lagrangian does not depend explicitly on time
	- Example: Magnetic field that varies with time

## Canonical transformations
- By transforming to another coordinate system, while the _values_ of $\Lagr$ and $\Ham$ do not change, their _functional forms_ will 
### Point transformations
- A point transformation relies on the original coordinates:
$$q_i(t) \rightarrow \bar{q}_i(q,t)$$
- As long as the transformation is invertible, if the EL equations hold for all $q_i$, they also hold for all $\bar{q}_i$:
$$\frac{d}{dt}\pd{\Lagr}{\dot{\bar{q}_i}}-\pd{\Lagr}{\bar{q}_i} = 
\sum_j \pd{q_j}{\bar{q}_i}\left(\frac{d}{dt}\pd{\Lagr}{\dot{q}_i}-\pd{\Lagr}{q_i}\right)$$
- The new conjugate momenta are:
$$\bar{p}_i = \pd{\Lagr}{\dot{\bar{q}}_i} = \sum_j p_j\pd{q_j}{\bar{q}_i}$$
- The Hamiltonian can be defined as a function of $(\bar{q},\bar{p})$:
$$\Ham = \sum_i\dot{\bar{q}}_i\bar{p_i}-\Lagr$$
$$\dot{\bar{q}}_i = \pd{\Ham}{\bar{p}_i}\;\;,\;\;\dot{\bar{p}}_i=-\pd{\Ham}{\bar{q}_i}$$


## Generators
