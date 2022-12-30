
### Multipole expansion
- Purpose: approximate the potential of a charge distribution, with each term having a different dependence on $r$
![[Multipole expansion terms.png]]
- Exact potential is given by:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\int \frac{1}{|\bm{r-r'}|}\rho(\bm{r'}) d\tau'$$
- Using the expansion of $|\bm{r-r'}|$ with Legendre polynomials $P_n(\cos\alpha)$, where $\alpha$ is the angle between $\bm{r'}$ and $\bm{r}$:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^\infty \frac{1}{r^{n+1}}\int (r')^n\,P_n(\cos\alpha)\,\rho(\bm{r'})\, d\tau'$$
### The monopole term
- The first term is:
$$V_{mon}(\bm{r})=\frac{1}{4\pi\epsilon_0}\frac{Q}{r}$$
	- where $Q=\int \rho d\tau$, the total charge. For point charges, this is the exact potential
### The dipole term
- The second term of the expansion is:
$$\begin{aligned}
V_{dip}(\bm{r})&=\frac{1}{4\pi\epsilon_0}\frac{1}{r^2}\int r'\cos\alpha\;\rho(\bm{r'})\,d\tau' \\
&= \frac{1}{4\pi\epsilon_0}\frac{1}{r^2}\hat{\bm{r}}\,\cdot\int \bm{r'} \rho(\bm{r'})\, d\tau'
 \\
&= \frac{1}{4\pi\epsilon_0} \frac{\bm{p\cdot \hat{\bm{r}}}}{r^2}
\end{aligned}
$$
- $\bm{p}$ is the dipole moment of the charge configuration, defined by:
$$\bm{p}\equiv\int \bm{r'} \rho(\bm{r'})\, d\tau'=\sum_iq_i\bm{r'_i}$$
