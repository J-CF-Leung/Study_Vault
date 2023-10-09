- Consider an _infinite square network_ formed by resistors of resistance $R_0$
![[Resistor network.png]]
- Let the electrostatic potential _tend to zero at infinity_:
$$\phi(r\to\infty)\to0$$

- Consider the current in the network when _wires_ are plugged into _neighbouring sites_ $1$ and $2$, with current $I$ passing through
- It is a _superposition_ of two distributions, where each site has current $I/4$ flowing through neighbouring resistors to infinity
- Hence, the current $I_{12}$ is simply $I/2$, and there is an _effective resistance_ $R_\text{eff}=R_0/2$

- For the general case, consider some _arbitrary point_ $(x,y)$, and the _conservation of current_ near it:
$$\displaylines{I(x+1,y;x,y)+I(x-1,y;x,y)+I(x,y-1;x,y)+I(x,y+1;x,y)\\=-I\delta(\bm{r}-\bm{r}_s)+I\delta(\bm{r}-\bm{r}_d)}$$
- It is _zero everywhere except for the source and drain_
- $I(P;Q)$ is current flowing _from P to Q_

- Using _Ohm's Law_, writing this out in terms of _potential differences_:
$$\displaylines{\phi(x+1,y)+\phi(x-1,y)+\phi(x,y-1)+\phi(x,y+1)-4\phi(x,y)\\=-IR_0[\delta(\bm{r}-\bm{r}_s)-\delta(\bm{r}-\bm{r}_d)]}$$
- Let there be a _Green's function_ satisfying: