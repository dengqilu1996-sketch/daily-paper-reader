---
title: Precision-Controlled Active Inference Accounts for Sensory Reweighting in Quiet Standing
title_zh: 精确控制下的主动推理模型解释静态站立中的感觉重加权现象
authors: "Kobayashi, J."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.23.733972v2.full.pdf"
tags: ["query:sb"]
score: 6.0
evidence: 主动推理模型模拟安静站立中的感觉重加权，是一种人体运动模拟的优化方法
tldr: "人类安静站立依赖前庭、本体感觉和视觉信息的情境重加权，但感觉可靠性变化如何从状态估计传导至姿势动作的生成模型机制仍不明确。本研究采用一个连续时间主动推理的一连杆倒立摆模型，通过通道特异性预测误差精度控制实现感觉重加权，模型接收多感官观测，基于广义坐标变分自由能估计姿态并选择踝力矩以维持直立目标。关键结果：当视觉或本体感觉通道可靠性降低时，降低对应通道的精度使扰动诱发的姿势偏移减少约82%，自动微分分析显示重加权发生在感知更新中；线性精度定律单调控制感觉贡献，而全局精度降低不产生重加权效应。这些发现表明姿势感觉重加权可理解为相对、上下文选择性的精度控制，为主动推理框架在姿势控制中的解释提供了生成性说明。"
source: biorxiv
selection_source: fresh_fetch
motivation: 安静站立的感觉重加权现象缺乏从状态估计到动作控制的生成模型机制。
method: 构建连续时间主动推理倒立摆模型，通过通道特异性预测误差精度控制实现感觉重加权，利用广义坐标变分自由能优化姿态估计与踝力矩选择。
result: "降低不可靠视觉或本体感觉通道精度使姿势偏移减少约82%，重加权定位于感知更新；线性精度定律控制感觉贡献，全局精度降低不产生重加权。"
conclusion: 姿势感觉重加权是上下文选择性的相对精度控制，支持主动推理框架对感觉运动整合的解释。
---

## 摘要
人类静态站立依赖于前庭觉、本体感觉和视觉信息在特定情境下的重加权。姿势描记术已经凭经验表征了这一现象，但关于感觉可靠性变化如何从状态估计传播到姿势动作的最小生成控制模型仍然不完整。本文中，我们测试了一个最小连续时间主动推理模型用于静态站立。在该模型中，感觉重加权被实现为对预测误差的通道特异性精度控制。一个单链倒立摆接收前庭觉、本体感觉和视觉观察，使用广义坐标变分自由能目标估计姿势，并在一个直立广义感觉目标下通过最小化同一目标选择踝关节力矩。情境变化改变了感觉通道的相对精度，而不改变系统模型、动作优化器或目标动力学。在受控的感觉扰动中，降低不可靠视觉或本体感觉通道的精度使扰动驱动的姿势偏移减少了约82%。基于自动微分的状态更新梯度贡献与此减少量紧密匹配，从而在感知更新中确定了重加权的机制位点。线性可靠性-精度定律 λ(c) = 1 + 7c 单调地控制了感觉贡献，固定精度消融实验表明全局精度降低并不产生重加权：除非在不同通道间选择性地改变精度，否则行为偏差始终与等精度条件相当。这些结果支持以下主张：姿势感觉重加权可以理解为连续主动推理循环中相对的、情境选择性的精度控制。

## Abstract
Human quiet standing depends on the context-dependent reweighting of vestibular, proprio-ceptive, and visual information. Posturography has empirically characterized this phenomenon, but a minimal generative-control account of how changes in sensory reliability propagate from state estimation to postural action remains incomplete. Here, we test a minimal continuous-time active inference model of quiet standing. In this model, sensory reweighting is implemented as channel-specific precision control over prediction errors. A one-link inverted pendulum receives vestibular, proprioceptive, and visual observations, estimates posture using a generalized-coordinate variational free-energy objective, and selects ankle torque by minimizing the same objective under an upright generalized sensory goal. Context changes alter the relative precision of sensory channels, without changing the plant, action optimizer, or goal dynamics. Across controlled sensory perturbations, reducing the precision of an unreliable visual or proprioceptive channel reduced perturbation-driven postural shifts by approximately 82%. An automatic-differentiation-based state-update gradient contribution closely matched the reduction, identifying the mechanistic locus of reweighting in the perceptual update. A linear reliability-to-precision law,{lambda} (c) = 1 + 7c, monotonically controlled sensory contribution, and a fixed-precision ablation showed that global precision reduction did not produce reweighting: the behavioral bias remained comparable to the equal-precision condition unless precision was changed selectively across channels. These results support the claim that postural sensory reweighting can be understood as relative, context-selective precision control in a continuous active inference loop.