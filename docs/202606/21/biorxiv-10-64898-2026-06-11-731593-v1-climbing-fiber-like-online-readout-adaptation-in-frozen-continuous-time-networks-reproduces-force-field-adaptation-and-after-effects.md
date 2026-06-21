---
title: Climbing-fiber-like online readout adaptation in frozen continuous-time networks reproduces force-field adaptation and after-effects
authors: "Kobayashi, J."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731593v1.full.pdf"
tags: ["query:sports-sci"]
score: 7.0
evidence: 连续时间神经网络中的在线读出适应模仿力场运动适应，与计算运动学习相关
tldr: 该研究在冻结的连续时间网络核心上，仅通过线性读出的在线适应，模拟小脑式误差驱动学习，成功再现了平面二连杆触碰任务中速度依赖的卷曲力场适应和后效应。结果为机器人运动控制中的快速重校准提供了生物学合理的局部更新机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 连续时间神经网络中的在线读出适应模仿力场运动适应，与计算运动学习相关。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Robotic motor control built on liquid neural networks and related continuous-time models, such as LTC and CfC, is typically trained offline via backpropagation through time and lacks an explicit mechanism for recalibrating online as plant dynamics change. We ask whether a frozen CfC core, whose liquid state spans a fixed continuous-time basis, can support cerebellar-style online adaptation by adapting only its linear readout with a climbing-fiber-like error signal. In a planar two-link reaching simulation with a velocity-dependent curl force field, we adapt the readout online with a feedback-error-learning (FEL) signal under a least-mean-squares (LMS) rule, leaving the core untouched. The frozen-core readout-only controller re-straightens curl-perturbed reaches and, upon field removal, produces a mirror-image after-effect, a behavioral signature consistent with internal-model learning, which a feedback-only controller does not produce. The result generalizes from a dense CfC to a sparse Neural-Circuit-Policy (NCP) wiring when the recurrent state, rather than the projected motor output, is used as the readout basis; it is robust to force-field strength and direction; and a recursive-least-squares variant adapts faster but de-adapts slowly because its covariance collapses, a rigidity that a covariance-reset safe-forgetting rule removes. Within the explored two-link planar simulation range, we did not find a readout-only failure case that required adapting the frozen core in the tested conditions. In this simulation study, adapting only the readout therefore provides a biologically inspired, low-cost online error-adaptation layer for offline-trained continuous-time controllers.