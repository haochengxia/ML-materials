# Assigment \#1

> Author: Percy
> Date: 2021/03/22

## 0 简介

关于kNN, SVM, SoftMax, two-layer network。共包含5个问题。

- [x] Q1: k-Nearest Neighbor classifier (20 points)
- [x] Q2: Training a Support Vector Machine (25 points)
- [x] Q3: Implement a Softmax classifier (20 points)
- [x] Q4: Two-Layer Neural Network (25 points)
- [x] Q5: Higher Level Representations: Image Features (10 points)

## 1 k-近邻分类器

熟悉numpy的使用，如argsort、dot、sum等以及broadcast机制。

Standard Deviation，即为标准差。

## 2 训练一个支持向量机

求梯度矩阵$dW$：

$ \nabla_W L_i$ = $\frac{\partial L_i}{\partial W}$

同时结合样本$X_i$的损失函数计算公式如下：

$Li = \sum_{j \neq y_i} max(0, W_j^T \cdot X_i - W_{y_i}^T \cdot X_i + \Delta)$

由此可知其在不同分类方向上的梯度：

1. 在正确分类上的梯度为：
   $$ \nabla_{W_{y_i}} L_i = -$$


 $\partial $

## 3 实现一个Softmax分类器

## 4 双层神经网络

## 5 图像特征