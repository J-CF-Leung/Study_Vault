## Functionals
- Consider an _integral involving some function_ $y(x)$:
$$G=\int_{\alpha}^\beta \left[y'(x)^2-y(x)^2\right]\,dx$$
- This integral is _independent of $x$_
- Instead, the value _depends on the function $y$_

- This is denoted a _functional_ $G[y]$

- A real _function takes a set of variables as input_, and gives a _real number as output_
$$f: \{y_k\}\to f(\{y_k\})\in\mathbb{R}$$
- A _functional takes a continuous infinity of variables as input_, and gives a _real number as output_
$$G:y(x)\rightarrow G[y]\in\mathbb{R}$$

- A functional can either _implicitly or explicitly_ depend on $x$
$$G[y]=\int_{\alpha}^\beta f(y,y',y'',\dots,;x)\,dx$$
- There may be _any number of dependent variables_ $\{y_i\}$ and _dependent variables_ $\{x_i\}$
- A typical functional is of the form:
$$G[y]=\int_\alpha^\beta f(y,y';x)\,dx$$