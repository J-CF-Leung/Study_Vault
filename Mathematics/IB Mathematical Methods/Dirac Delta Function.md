>[!quote]
>"This shouldn't work, but amazingly it does, it's basically alchemy"
>-Dr. S.J. Cowley, 2022
- The definition of the Delta function:
$$\int_{-\infty}^\infty \delta(x-a)f(x)\,dx=f(a)$$
	- Continuous version of the Kronecker Delta
- Technically it is not a function, and should only be used as a linear operator according to the equation above
	- But that's just to satisfy mathematicians

- The Delta function can be pictured as:
$$\delta(x)= \begin{cases} 0 &x\neq 0 \\ \infty &x=0\end{cases}$$
- It must also satisfy:
$$\int_{-\infty}^\infty \delta(x) \,dx=1$$


- The Delta function as a limit:
$$\delta_\epsilon(x)=\begin{cases}0 & x<-\epsilon \\
\frac{1}{2\epsilon} &-\epsilon<x<\epsilon \\
0 & x>\epsilon\end{cases}$$
- The Delta function can then be written as:
$$\delta(x)=\lim_{\epsilon\to0}\delta_\epsilon(x)$$
- It can also be understood as the Fourier transform of a pure sinusoidal wave:
$$\delta(x-a)=\frac{1}{2\pi}\int_{-\infty}^\infty e^{-ik(x-a)}\,dk$$



## Properties of the Dirac Delta
- The function is _symmetric_:
$$\delta(x)=\delta(-x)$$
- The function is _real_:
$$\delta^*(x)=\delta(-x)=\delta(x)$$

## The Heaviside Step function
- The Heaviside Step function is defined as:
$$H(x) = \begin{cases}0 & x<0 \\ 1 & x>0 \end{cases}$$
- From the definition of the Delta function, one can derive:
$$H(x)=\int_{-\infty}^x\delta(x')\,dx' $$
- This suggests:
$$H'(x)=\delta(x)$$

## Derivative of the Delta function
- By using integral by parts:
$$\int_{-\infty}^\infty \delta'(x-\xi)f(x)\,dx =\left[\delta(x-\xi)f(\xi)\right]_{-\infty}^\infty-\int_{-\infty}^\infty \delta(x-\xi) f'(x)\,dx =-f'(\xi)$$
- The derivative of the Delta function is an _odd function_

## Higher dimension Delta functions
- A Delta function in $n$ dimensions is equivalent to:
$$\delta^n(\bm{x}-\bm{x}')=\delta(x_1-x_1')\delta(x_2-x_2')\dots\delta(x_n-x_n')$$
- Consequently, the action on functions is:
$$\int \delta^n(\bm{x}-\bm{x}')f(\bm{x}-\bm{x}')\,d^n\bm{r}=f(\bm{x}')$$
- The _three-dimensional Delta function_ can be defined using the _Divergence Theorem_
- Consider the function:
$$\displaylines{f(\bm{r})=\frac{\hat{\bm{r}}}{r^2} \\ \iiint_V \nabla\cdot\left(\frac{\hat{\bm{r}}}{r^2}\right)\,d^3\bm{r}=\iint_{\partial V} \hat{\bm{r}}\cdot d\bm{S}=4\pi}$$
- The definition of the divergence _diverges at $r=0$_
- Hence:
$$\nabla\cdot\left(\frac{\hat{\bm{r}}}{r^2}\right)=4\pi\delta^3(\bm{r})$$
