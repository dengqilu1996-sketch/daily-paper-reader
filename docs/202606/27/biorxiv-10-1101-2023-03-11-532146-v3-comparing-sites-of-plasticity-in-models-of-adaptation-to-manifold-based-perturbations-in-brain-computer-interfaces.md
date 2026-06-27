---
title: Comparing sites of plasticity in models of adaptation to manifold-based perturbations in brain-computer interfaces
title_zh: 比较脑机接口中基于流形的扰动适应模型中可塑性位点
authors: "Payeur, A., Orsborn, A. L., Lajoie, G."
date: 2026-06-27
pdf: "https://www.biorxiv.org/content/10.1101/2023.03.11.532146v3.full.pdf"
tags: ["query:sports-sci"]
score: 6.0
evidence: 使用线性循环网络的运动适应计算模型模拟与技能学习相关的运动学习
tldr: 运动皮层神经活动处于低维流形上，与流形对齐的扰动在脑机接口中引发快速适应，不对齐的则适应缓慢，这引出了可塑性位点的争论。为比较不同假设，本研究采用在固定点运行的最小线性循环网络，以梯度下降训练。发现所有候选可塑性位点均能产生差异适应，但其强度取决于循环权重方差；Hessian分析揭示不对齐扰动引入损失景观的浅曲率方向，导致梯度下降缓慢。此外还提出了区分不同可塑性位点贡献的实验测试，明确了循环权重方差和可塑性位点作为控制差异适应的关键因素。
source: biorxiv
selection_source: fresh_fetch
motivation: 理解低维流形结构如何约束脑机接口中的适应学习，以及不同可塑性位点假说的有效性。
method: 使用在固定点运行的最小线性循环网络，通过梯度下降训练，比较不同可塑性位点假设，并执行Hessian分析探索损失景观。
result: 所有候选可塑性位点均能产生差异适应，其强度取决于循环权重方差；Hessian分析揭示不对齐扰动引入浅曲率方向，导致学习缓慢。
conclusion: 循环权重方差与可塑性位点共同决定差异适应，所提出的实验测试可区分不同位点贡献，为神经适应机制提供新见解。
---

## 摘要
在训练有素的行为中，运动皮层的神经群体活动位于一个低维流形上。这引出了一个问题：这种结构如何制约后续的学习。在非人灵长类动物的脑机接口实验中，与该子空间对齐的扰动引发了快速适应，而未对齐的扰动则导致了较慢的适应。已有几种理论解释这种差异适应，它们的不同之处在于可塑性的位置。我们使用一个在其不动点运行并通过梯度下降训练的最小线性递归网络来比较这些假说。所有候选可塑性位点都能产生一定程度的差异适应，其强度取决于递归权重的方差，并且不同位点的敏感性不同。海森分析揭示了未对齐的扰动如何通过引入浅曲率方向重塑损失景观，梯度下降沿这些方向进展缓慢。我们进一步提出了一个实验测试，以帮助区分适应过程中不同可塑性位点的贡献。总之，我们的结果指出，递归权重的方差是调控差异适应的一个关键控制参数，此外还有可塑性位点。

## Abstract
During well-trained behaviors, neural population activity in motor cortex lies on a low-dimensional manifold. This raises the question of how such structure constrains subsequent learning. In brain-computer interface experiments in nonhuman primates, perturbations aligned with this subspace induced rapid adaptation, whereas misaligned perturbations induced slower adaptation. Several theoretical accounts have been proposed to explain this differential adaptation, differing in the locus of plasticity. We compare these hypotheses using a minimal linear recurrent network operating at its fixed point and trained by gradient descent. All candidate plasticity sites are able to produce some degree of differential adaptation, whose strength depends on the variance of recurrent weights, with different sensitivities across sites. Hessian analysis reveals how misaligned perturbations reshape the loss landscape by introducing directions of shallow curvature along which gradient descent proceeds slowly. We further propose an experimental test to help distinguish the contributions of different plasticity sites during adaptation. Overall, our results identify the variance of recurrent weights as a key control parameter governing differential adaptation, alongside the site of plasticity.