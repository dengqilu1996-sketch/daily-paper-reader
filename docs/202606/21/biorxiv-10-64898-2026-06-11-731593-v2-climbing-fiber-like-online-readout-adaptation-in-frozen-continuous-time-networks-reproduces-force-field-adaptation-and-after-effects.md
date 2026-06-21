---
title: Climbing-fiber-like online readout adaptation in frozen continuous-time networks reproduces force-field adaptation and after-effects
authors: "Kobayashi, J."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731593v2.full.pdf"
tags: ["query:sports-sci"]
score: 9.0
evidence: 冻结连续时间网络的在线读出适应模拟了小脑型运动学习过程，直接建模运动技能习得
tldr: 现有机器人运动控制利用连续时间网络进行离线训练，缺乏在线重校准能力，难以模拟人类运动学习中对环境变化的快速适应。本文提出冻结CfC核心，仅通过最小均方规则在线适应线性读出层，模拟小脑攀爬纤维驱动的误差学习机制。在平面两连杆伸手任务中成功复现了力场适应和经典后效，表明固定连续时间动力学基上的简单读出可塑性足以产生快速运动适应。该结果为开发在线运动学习模型提供了计算框架，有助于理解运动员在动态环境中调整动作技能的神经机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 冻结连续时间网络的在线读出适应模拟了小脑型运动学习过程，直接建模运动技能习得。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Robotic motor control built on liquid neural networks and related continuous-time models, such as LTC and CfC, is typically trained offline via backpropagation through time and lacks an explicit mechanism for recalibrating online as plant dynamics change. We ask whether a frozen CfC core, whose liquid state spans a fixed continuous-time basis, can support cerebellar-style online adaptation by adapting only its linear readout with a climbing-fiber-like error signal. In a planar two-link reaching simulation with a velocity-dependent curl force field, we adapt the readout online with a feedback-error-learning (FEL) signal under a least-mean-squares (LMS) rule, leaving the core untouched. The frozen-core readout-only controller re-straightens curl-perturbed reaches and, upon field removal, produces a mirror-image after-effect, a behavioral signature consistent with internal-model learning, which a feedback-only controller does not produce. The result generalizes from a dense CfC to a sparse Neural-Circuit-Policy (NCP) wiring when the recurrent state, rather than the projected motor output, is used as the readout basis; it is robust to force-field strength and direction; and a recursive-least-squares variant adapts faster but de-adapts slowly because its covariance collapses, a rigidity that a covariance-reset safe-forgetting rule removes. Within the explored two-link planar simulation range, we did not find a readout-only failure case that required adapting the frozen core in the tested conditions. In this simulation study, adapting only the readout therefore provides a biologically inspired, low-cost online error-adaptation layer for offline-trained continuous-time controllers.