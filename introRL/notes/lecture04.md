## Lecture 03 Value Function Approximation

> Links: [视频](https://space.bilibili.com/511221970/channel/detail?cid=105354) [课件](https://github.com/zhoubolei/introRL/blob/master/lecture4.pdf)

前面讨论的问题，状态数量都很少。但是对于大规模状态下的强化学习，价值函数不适合再用一个lookup table来实现。

Solution: 用带参数$w$的函数来进行近似，把见过的状态泛化到覆盖没见过的状态，通过插值的办法估计。

$w$ 可以使用 MC 或 TD 来近似估计。

### 1 Function Approximators

#### 1.1 Linear feature representations

用特征向量来表征一个状态。

a. 用当前状态各特征量的线性叠加来表示value function

Montain car 问题

可能会crash

function
approximation

bootstraping

off-policy learning


#### 1.2 Neural Network


### Deep Q learning

用非线性的模型来拟合价值函数。线性模型需要设定好的特征才能够效果比较好。

experience replay

fixed target

---

## Question

1. Loss组成部分的推导