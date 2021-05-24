## Lecture 05 Policy Optimization I

对于Value-based RL来说，学到Q函数后，policy在其中就是确定的，通过greedy来生成。

而Policy-based就是对于一个状态得到不同action的probability然后argmax即可。

### 2 两种策略类型

1. Deterministic

2. Stochastic

例1：比如在石头剪刀布游戏，环境中的反应是随机的，如果是确定性的行为那么很容易输。


$J(\theta)$可不可导区分优化方法。

如果可导的话，为了使其最大化

* Derivative

如果不可导：

$\theta^* = arg \max J(\theta)$

Treat $J(\theta)$ as a black box score function.

**CEM**

**Finite Difference**

给定了policy function $\pi_\theta$

### 3 Policy Gradient

