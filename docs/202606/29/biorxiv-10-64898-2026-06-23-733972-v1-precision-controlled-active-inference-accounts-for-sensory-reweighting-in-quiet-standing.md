---
title: Precision-Controlled Active Inference Accounts for Sensory Reweighting in Quiet Standing
title_zh: 精确控制的主动推理模型解释安静站立中的感觉重加权现象
authors: "Kobayashi, J."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.23.733972v1.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 单连杆倒立摆模型动态模拟安静站立，属于肌骨系统动力学仿真
tldr: "静立平衡依赖前庭、本体和视觉信息的上下文重加权，行为学已表征该现象，但从状态估计到姿势控制的生成机制仍不明确。本研究提出一个最小连续时间主动推理模型，采用通道特异精度控制预测误差来实现感觉重加权，在单链倒立摆上接收多通道观测。结果表明，在感觉扰动下，降低不可靠通道的精度可使姿势偏移减少约82%，且重加权源于感知更新梯度的变化，而非全局精度调整。该发现支持将姿势感觉重加权视为主动推理循环内上下文选择的相对精度控制，为量化感觉整合提供了计算框架。"
source: biorxiv
selection_source: fresh_fetch
motivation: 针对静立平衡中感觉重加权的生成控制机制仍不明确的问题，本研究旨在构建计算模型。
method: 基于单链倒立摆的连续时间主动推理模型，通过通道特异性精度调节预测误差，并采用自动微分定位重加权机制。
result: "降低不可靠视觉或本体感觉通道精度减少姿势偏移约82%，重加权位点在感知更新，且需选择性精度调整。"
conclusion: 姿势感觉重加权本质上是主动推理循环中上下文依赖的相对精度控制，全局精度变化不足以产生重加权效应。
---

## 摘要
人类安静站立依赖于对前庭、本体感觉和视觉信息的情境依赖性重加权。姿势描记术已从经验上表征了这一现象，但关于感觉可靠性变化如何从状态估计传递到姿势动作的简洁生成控制解释仍不完整。在此，我们测试了一个安静站立的最小连续时间主动推理模型。该模型中，感觉重加权被实现为对预测误差的通道特异性精确控制。一个单连杆倒立摆接收前庭、本体感觉和视觉观测，利用广义坐标变分自由能目标估计姿势，并通过在恢复性广义感觉目标下最小化同一目标来选择踝关节力矩。情境变化改变了感觉通道的相对精确性，而不改变被控对象、动作优化器或目标动力学。在受控的感觉扰动中，降低不可靠视觉或本体感觉通道的精确性，使扰动驱动的姿势偏移减少了约82%。基于自动微分的状态更新梯度贡献与减少量密切匹配，确定了重加权在感知更新中的机制位置。一个线性可靠性-精确性法则，λ(c)=1+7c，单调地控制了感觉贡献，固定精确性的消融实验表明，全局精确性降低不会产生重加权：除非跨通道选择性地改变精确性，否则行为偏差仍然完全存在。这些结果支持了一个主张，即姿势感觉重加权可以理解为连续主动推理循环中的相对、情境选择性精确性控制。

## Abstract
Human quiet standing depends on the context-dependent reweighting of vestibular, proprioceptive, and visual information. Posturography has empirically characterized this phenomenon, but a compact generative-control account of how changes in sensory reliability propagate from state estimation to postural action remains incomplete. Here, we test a minimal continuous-time active inference model of quiet standing. In this model, sensory reweighting is implemented as channel-specific precision control over prediction errors. A one-link inverted pendulum receives vestibular, proprioceptive, and visual observations, estimates posture using a generalized-coordinate variational free-energy objective, and selects ankle torque by minimizing the same objective under a restorative generalized sensory goal. Context changes alter the relative precision of sensory channels, without changing the plant, action optimizer, or goal dynamics. Across controlled sensory perturbations, reducing the precision of an unreliable visual or proprioceptive channel reduced perturbation-driven postural shifts by approximately 82%. An automatic-differentiation-based state-update gradient contribution closely matched the reduction, identifying the mechanistic locus of reweighting in the perceptual update. A linear reliability-to-precision law, lambda(c)=1+7c, monotonically controlled sensory contribution, and a fixed-precision ablation showed that global precision reduction did not produce reweighting: the behavioral bias remained full unless precision was changed selectively across channels. These results support the claim that postural sensory reweighting can be understood as relative, context-selective precision control in a continuous active inference loop.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义
- **研究动机**：人类安静站立时，中枢神经系统会依据情境对前庭、本体感觉和视觉信息进行动态重加权（reweighting），即根据各感觉通道的可靠性调整其贡献度。这一现象已在姿势描记术（posturography）中被大量行为实验证实，但**感觉可靠性变化如何从状态估计传导至姿势动作的生成控制机制仍不清楚**。
- **整体含义**：论文旨在为感觉重加权提供一个紧凑的生成式控制解释，验证“重加权本质上是连续主动推理循环中情境选择性的相对精度控制”这一假说，并构建可量化的计算框架。

### 2. 方法论
- **核心思想**：将安静站立建模为一个**连续时间主动推理**过程，把感觉重加权实现为对**预测误差的通道特异性精度（precision）控制**。系统通过最小化同一变分自由能目标同时完成姿势估计（感知）和踝关节力矩选择（动作），而上下文变化仅改变各感觉通道的相对精度，不改变被控对象、动作优化器或目标动力学。
- **关键技术细节**：
  - **被控对象**：单连杆倒立摆（one-link inverted pendulum），接受前庭、本体感觉和视觉三种通道的观测。
  - **状态估计与动作选择**：使用**广义坐标下的变分自由能**作为统一目标函数。感知更新通过梯度下降最小化自由能；动作（踝力矩）在“恢复性广义感觉目标”下同样通过最小化自由能产生。
  - **精度控制律**：采用线性映射`λ(c) = 1 + 7c`，其中`c`为情境依赖的可靠性系数，`λ`为对应通道的精度。通过增减某一通道的`c`，即选择性地提高或降低该通道预测误差的精度。
  - **机制定位工具**：利用**自动微分**计算状态更新梯度中各感觉通道的贡献度，据此确定重加权的机制作用位点是否在感知更新阶段。
  - **消融条件**：将所有通道精度全局降低（固定精度）而不进行通道特异性调整，对比重加权效应的存在性。

### 3. 实验设计
- **实验场景**：感觉扰动下的安静站立仿真，扰动类型可控（视觉或本体感觉不可靠）。
- **基准与对比**：
  - **基准**：无感觉扰动或全通道高可靠性的正常站立行为。
  - **主要对比**：① 对不可靠通道特异性降低精度；② 全局均匀降低精度（消融实验）；③ 通过梯度贡献分析对比重加权效应的来源。
- **评价指标**：扰动驱动的姿势偏移量减少幅度（约82%），以及梯度贡献与行为偏移减少量之间的匹配程度。

### 4. 资源与算力
- 论文摘要及提供的文本中**未提及任何算力信息**，如GPU型号、数量、训练时长或仿真时长。从模型性质看（单连杆倒立摆、常微分方程仿真），该研究对算力需求极低，可能在普通个人计算机上完成。

### 5. 实验数量与充分性
- **实验规模**：文中明确报告了至少三类实验：
  1. 受控感觉扰动下，选择性降低不可靠通道精度观察姿势偏移减少（定量结果：减少约82%）。
  2. 基于自动微分的梯度贡献分析，定位重加权的机制位置（感知更新）。
  3. 固定精度消融实验，证明全局精度降低不产生重加权效应。
- **充分性评价**：
  - 作为一台计算模型的验证，实验设计**目标明确、逻辑简洁**，通过选择性调控与非选择性调控的对冲，有效支撑了核心假说。
  - 对比对象主要为**模型自身的变体**，而非其他独立模型，适合理论验证但缺乏与现有主流感觉整合模型（如卡尔曼滤波加权模型）的直接性能或机制比较。
  - 扰动类型和参数范围未详细列出，可能仅覆盖有限的条件组合，但摘要中的“约82%”等量化结果仍提供了可检验的预测。

### 6. 主要结论与发现
- **重加权的效果**：在感觉扰动下，只降低不可靠通道的精度，可减少扰动驱动的姿势偏移约82%。
- **重加权的位点**：状态更新梯度的贡献度与行为减少量高度一致，表明重加权机制位于**感知更新**环节，而不是动作选择环节。
- **选择性是关键**：全局精度下降**不会**产生重加权；必须跨通道**选择性地改变精度**才能消除行为偏差。
- **概念归结**：姿势感觉重加权在本质上是一种**上下文依赖的、相对的精度控制**，属于连续主动推理循环的内在机制。

### 7. 优点
- **理论基础坚实**：将感觉重加权嵌入主动推理框架，统一了解释姿势控制中感知与动作的生成过程。
- **机制解释清晰**：通过梯度贡献分析将重加权的计算位点精确定位在感知更新，超越单纯的行为描述。
- **模型最小化**：单连杆倒立摆、少数感觉通道、简洁的精度映射律，使得核心机制不会被无关复杂性遮蔽。
- **可检验性强**：提出的线性可靠性-精度律和消融对立预测，易于在人类实验或进一步仿真中验证。

### 8. 不足与局限
- **建模简化**：将人体简化为单关节倒立摆，忽略了多节段协调、肌肉-肌腱动力学和神经传导延迟等因素，可能限制向真实多感官姿势控制的推广。
- **缺乏真实数据校准**：结论完全基于仿真，未使用人类姿势描记数据校准或检验模型预测的准确性。
- **比较基线有限**：仅与自身全局精度消融条件对比，没有与最优感觉整合模型（如基于贝叶斯或卡尔曼滤波的模型）进行比较，难以彰显其独特优势或等效性。
- **干扰参数与鲁棒性未知**：扰动强度、精度调节参数（如`λ(c)`的系数7）的敏感性分析未见描述，模型在更剧烈或更复杂的噪声环境下的表现需要进一步考察。
- **应用边界不明**：研究仅覆盖安静站立，未涉及动态站立或行走等更复杂的姿势任务，泛化性待验证。

（完）
