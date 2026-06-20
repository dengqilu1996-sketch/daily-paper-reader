---
title: "ANNet: A first-principles neural network for forward and inverse dynamics"
title_zh: ANNet：一个用于正向和逆向动力学的第一性原理神经网络
authors: "Bahdasariants, S., Parola, L., Kacker, K., Feldman, A. K., Zdobinski, Z., Kang, I., Weber, D. J."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729998v1.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 用于前向和逆向动力学的物理信息神经网络
tldr: 运动控制需同时解决逆动力学与正向动力学，但传统方法将两者分开建模，忽略内在联系。本文提出ANNet，基于Appell加速度能量学习单一标量函数，通过微分与优化分别实现逆、正向动力学。在双摆任务中，网络无需重训练即可实时准确地进行前向与逆向仿真，为预测与控制提供了一体化表示。
source: biorxiv
selection_source: carryover_cache
motivation: 逆动力学与正向动力学通常分开估计或建模，但它们共享运动方程约束，需要统一框架以利用内在结构。
method: ANNet学习Appell加速度能量，逆动力学由其导数得到，正向动力学通过最小化目标函数实现，无需重训练。
result: 在未见过的双摆轨迹上测试，逆动力学和优化基正向仿真均达到实时精度。
conclusion: ANNet为预测和控制提供统一的物理信息表示，在神经科学与机器人中具有应用前景。
---

## 摘要
生物系统和机器人系统为完成运动必须解决两个相关的计算问题：逆向动力学，即确定产生期望运动所需的力或力矩；正向动力学，即将施加的力映射为运动。尽管这些计算通过相同的运动方程耦合在一起，但在基于模型和数据驱动的公式中，它们通常被估计或实现为独立的逆向映射和正向映射。这种分离可能掩盖约束这两个问题的共享结构。本文提出了ANNet，一个物理信息神经网络，它通过从经典力学中学习单个标量——阿佩尔加速能量——将两种计算置于一个共同的学习表示之上。该网络将运动学状态和候选加速度映射到这个标量函数，并通过将学习的能量函数对加速度求导来得到关节力矩，从而获得逆向动力学。然后，无需重新训练，通过将相同的学习能量景观嵌入到优化目标中来计算正向动力学，该目标的无约束最小值满足吉布斯-阿佩尔方程。由此产生的加速度在时间上进行前向积分。我们在双摆范式上评估ANNet。在网络训练期间未见过的试验中，逆向和基于优化的前向模拟具有实时准确性。我们的结果提供了一条第一性原理路径，使用单一的学习表示来支持预测和控制。

显著性机器人和动物必须解决两个运动问题：计算期望运动所需的力或力矩（逆向动力学）和确定施加力产生的运动（正向动力学），这两个问题通常被分开建模。我们展示了这两个问题都可以用经典力学中的一个标量函数——阿佩尔加速能量来表示。训练一个神经网络，使这个学习函数的导数与参考关节力矩相匹配，从而执行逆向动力学。然后，同一个网络通过最小化基于学习的能量景观构建的目标来计算正向动力学，无需重新训练。该框架为神经科学和机器人学中的预测和控制提供了一个统一的表示。

## Abstract
Biological and robotic systems must solve two related computations to move: inverse dynamics, which determines the forces or torques needed to produce a desired movement, and forward dynamics, which maps applied forces to motion. Although these computations are coupled by the same equations of motion, they are usually estimated or implemented as distinct inverse and forward mappings, in both model-based and data-driven formulations. This separation can obscure the shared structure that constrains both problems. Here, we present ANNet, a physics-informed neural network that places both computations on a common learned representation by learning a single scalar quantity from classical mechanics--Appell acceleration energy. The network maps kinematic state and candidate accelerations to this scalar function, and inverse dynamics is obtained by differentiating the learned energy function with respect to acceleration to recover joint torques. Forward dynamics is then calculated without retraining by embedding the same learned energy landscape in an optimization objective whose unconstrained minimum satisfies the Gibbs- Appell equation. The resulting accelerations are integrated forward in time. We evaluate ANNet on a double pendulum paradigm. In trials unseen by the network during training, inverse and optimization-based forward simulations are real-time accurate. Our results provide a first-principles route for using a single learned representation to support both prediction and control.

SignificanceRobots and animals must solve two problems to move: computing the forces or torques needed for a desired motion (inverse dynamics) and determining the motion produced by applied forces (forward dynamics), which are usually modeled separately. We show that both problems can be expressed using a single scalar function from classical mechanics, Appell acceleration energy. A neural network trained so that the derivative of this learned function matches reference joint torques performs inverse dynamics. The same network then computes forward dynamics by minimizing an objective built from the learned energy landscape, without retraining. This framework provides a unified representation for prediction and control in both neuroscience and robotics.