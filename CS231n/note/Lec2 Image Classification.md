# Lec 2

## Part 1 数据驱动方法

**semantic gap**: 图片的实际含义与计算机所看到的数值含义差距很大。

图像识别任务存在以下挑战：

- view point variation
- illumination
- deformation
- occlusion
- background clutter
- intraclass variation
  
---

使用明确规则（hard specific rules）对图像识别任务来说不适用：

- performance bad
- not scalable

而数据驱动（**data driven**）可以很好规避明确规则无法推广的问题。

---

如何比较两张图片?

Distance Metric to compare images

- L1 distance

---

kNN algo 训练快但是预测慢，而卷积神经网络则相反。

| Period | Time Cost |
| - | - |
| train | O(1) |
| predict | O(N) |


## Part 2 K最近邻算法

Distance Metric:
- L1 (Manhattan) distance: rotate coordinate, the value of L1 distance will change.
- L2 (Euclidean) distance: sensitiveless to the rotation of the coordinate.

Hyperparameters:
 - k
 - distance metric

DO NOT care the fitting of the training data care how performe on the unseen data.

---

**Data Spliting:**

Train Validation Test

Cross Validation (useful for small dataset, but DL consume large computation resource, so it is not used to frequently)

---

KNN NEVER used on images.

1. 向量化的距离函数不太适合度量图片在视觉上的相似度
2. 维度灾难 （curse of dimensionality）

## Part 3 线性分类器

Parametric Approach:

f(x, W) → x is the input

**f(x, W) = Wx + b**, W is parameters or wright, b is bias.

可以理解为Template Matching。

Limitation：每个类别只能够学习一个模板。

1. odd or even
2. multimodal situations