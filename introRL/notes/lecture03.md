## Lecture 03 Model-free Prediction and Control

> Links: [视频](https://space.bilibili.com/511221970/channel/detail?cid=105354) [课件](https://github.com/zhoubolei/introRL/blob/master/lecture3.pdf)

Model-free prediction: estimate value function of an unknown MDP
Model-free control: optimize value function of an unknown MDP

Known MDP: $R$ and $P$ are exposed. ($R$ is the reward function, $P$ is the transition matrix)

### 1 Model-free prediction

#### 1.1 基于Monte Carlo

采样轨迹，根据实际收益估计价值。 → Incremental MC

和DP的区别：DP用bootstraping的思想，对DP来说，用Bellman exception backup，对每种可能的状态转移带来的收益进行加和，然后对policy下每种可能的action进行加和，而蒙特卡洛得到的是实际决定的轨迹，对轨迹上的状态进行更新。

#### 1.2 Temporal Difference Learning

1. model free
2. incomplete episode

$$TD(0):\ v(s_t) = v(s_t) + \alpha(R_{t+1} + \gamma v(s_{t+1}) - v(s_t))$$

根据做一个决策后的reward和实际到达下一个状态的价值来更新估计当前状态的价值。

相比于MC有以下特征
a. support online learning
b. support incomplete sequences
c. support continuing environment
d. utilize Markov property

##### 1.2.1 n-step TD

往前走n步，然后bootstraping。

### 2 Model-free Control

#### 2.1 MC with $\epsilon$ Greedy Exploration

通过Monte Carlo进行随机探索，Greedy方法更新policy，循环。也可以把TD加入进去。

#### 2.2 SARSA

直接去估计Q table。

$$Q(s_t, a_t) \leftarrow Q(s_t, a_t) + \alpha [R_{t+1} + \gamma Q(s_{t+1}, a_{t+1}) - Q(s_t, a_t)]$$

更新了Q table后可以用Greedy生成策略。

Sarsa在更新Q table的时候，需要先采一个action，然后进入到下一状态，而且在进入到下一状态的时候要再根据$\epsilon$ greedy再采一个动作。

可以推广到n-step Sarsa。

Sarsa是on-policy TD control。

#### 2.3 Q-Learning

Q-learning是off-policy TD control。存在behavior policy和learning (target) policy，是互相之间独立的。

$$Q(s_t, a_t) \leftarrow Q(s_t, a_t) + \alpha [R_{t+1} + \gamma \max_{a} Q(s_{t+1}, a) - Q(s_t, a_t)]$$

Q-Learning会比较激进。

