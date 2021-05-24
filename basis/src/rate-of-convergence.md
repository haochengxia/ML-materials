# Rate of Convergence

收敛数列的收敛顺序(convergence order)和收敛速率(convergence rate)是表示数列接近其极限的速度的量。

一个收敛到$x^*$的数列，具有收敛顺序$q$和收敛速率$\mu$，如果：

$$
\lim _{n \rightarrow \infty} \frac{\left|x_{n+1}-x^{*}\right|}{\left|x_{n}-x^{*}\right|^{q}}=\mu
$$

而在离散化方法中，收敛速度的表示方法为，

$$
\begin{array}{l}
\left|x_{n}-L\right|<C n^{-q} \text { for all } n\\
\end{array}
$$

即，$\left|x_{n}-L\right|=\mathcal{O}\left(n^{-q}\right)$。

接下来用一个例子了解离散方法中收敛速度的计算。蒙特卡洛方法的收敛速率是$O\left(\frac{1}{\sqrt{N}}\right)$，数列均值为$\mu$，方差为$\sigma ^ 2$。

$$
\mathbb{E}\left[ | \frac{1}{N} \sum_{i=1}^{n} X_{i}-\mu | \right] \rightarrow O\left(\frac{1}{\sqrt{N}}\right)
$$


**证明:**

使用中心极限定理可以得到，
$$
\mathbb{E}\left[\left(\frac{1}{N} \sum_{i=1}^{n} X_{i}-\mu\right)^{2}\right]=\frac{\sigma^{2}}{N}
$$

同时由于对于任何的随机变量来说，$\mathbb{E}[|Z|]^{2} \leq \mathbb{E}\left[Z^{2}\right]$，

$$
\begin{aligned}
\mathbb{E}\left[\left|\bar{X}_{N}-\mu\right|\right]^{2} &=\mathbb{E}\left[\left|\bar{X}_{N}-\mathbb{E}\left[\bar{X}_{N}\right]\right|\right]^{2} \leq \mathbb{E}\left[\left(\bar{X}_{N}-\mathbb{E}\left[\bar{X}_{N}\right]\right)^{2}\right] \\
&=\operatorname{Var}\left(\bar{X}_{N}\right)=\frac{1}{N^{2}} \sum_{i=1}^{N} \operatorname{Var}\left(X_{i}\right)=\frac{\sigma^{2}}{N}
\end{aligned}
$$

综上所述，

$$
\mathbb{E}\left[ | \frac{1}{N} \sum_{i=1}^{N} X_{i}-\mu | \right] \leq \frac{\sigma}{\sqrt{N}}
$$

所以收敛速率是$O\left(\frac{1}{\sqrt{N}}\right)$。



## Reference

[1] [Rate of convergence - WIKI](https://en.wikipedia.org/wiki/Rate_of_convergence)

[2] [CLT - StackExchange](https://math.stackexchange.com/questions/3382341/central-limit-theorem-mathbbe-left-frac1n-sum-i-1n-x-i-mu-ri?rq=1)