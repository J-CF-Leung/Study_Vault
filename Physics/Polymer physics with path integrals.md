#### [[Path integrals in quantum mechanics|Introduction to path integration in the context of quantum mechanics]]

# The statistical mechanics of polymers
- Modelling of polymers usually involves some coarse-graining, such as grouping atoms into "beads"
- For a polymer with $n$ particles, its configurational [[Principles of statistical mechanics|partition function]] is expressed as:
$$Z=\int d\bm{r}^n \exp[-\beta U(\bm{r}^n)]$$

- The flexibility of a chain depends on both short and long range interferences
	- In the short range, the orientation of a bond may be constrained by neighbours
	- In the long range, there can be an excluded volume effect as 2 segments on the polymer cannot occupy the same position

# Ideal random chain
- For an ideal chain, all joints are free to rotate
- Probability density of one rigid segment with length $a$:
$$P_1(\bm{r})=\frac{1}{4\pi a^2}\delta(|\bm{r}|-a)$$
	- Prefactor ensures probability density is normalised
- Probability distribution of the end-to-end displacement $\bm{R}$, with bonds $\bm{r}_i$:
$$P_N(\bm{R})=\prod_{n=1}^N\left[\int d\bm{r}_n \frac{1}{4\pi a^2}\delta(|\bm{r_n}|-a)\right]\delta^3\left(\bm{R}-\sum_{n=1}^N\bm{r}_n \right)$$
- Expressing the Delta function as an integral of $\exp[i\bm{k}\cdot(\bm{R}-\sum \bm{r}_n)]$, one can find the Fourier transform of the probability:
$$P_N(\bm{R}) = \int\frac{d\bm{k}}{(2\pi)^3}\exp(i\bm{k}\cdot\bm{R}) \tilde{P}_N(\bm{k})$$
$$\tilde{P}_N(\bm{k})=\prod_{n=1}^N\left[\int d\bm{r}_n\frac{1}{4\pi a^2}\delta(|\bm{r_n}|-a)\exp(-i\bm{k}\cdot\bm{r}_n)\right]= \left[\tilde{P}_1(\bm{k})\right]^N$$









# Polymer field theory