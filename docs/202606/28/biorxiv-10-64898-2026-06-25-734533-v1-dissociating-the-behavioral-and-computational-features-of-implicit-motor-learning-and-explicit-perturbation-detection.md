---
title: Dissociating the behavioral and computational features of implicit motor learning and explicit perturbation detection
title_zh: 分离内隐运动学习与外显扰动检测的行为和计算特征
authors: "Kim, H. E., Darley, J. O., Landy, M. S., Chua, R., Fox, D. J."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.25.734533v1.full.pdf"
tags: ["query:sports-sci"]
score: 10.0
evidence: 通过视觉运动旋转任务中的误差解析研究内隐运动学习，直接为运动技能获取的计算模型提供信息
tldr: 人类感觉运动系统能自动分解运动误差，但对微小扰动的内隐适应与意识检测的分离尚需在同一实验验证。本研究采用被试内设计与计算建模，发现参与者内隐适应仅需1°旋转，而外显报告需约4°阈限。适应行为符合基于本体与视觉线索比较的误差校正模型，检测行为则依赖贝叶斯因果推断。结果表明内隐与外显处理运用截然不同的计算策略，深化了对感知-行动分离机制的理解。
source: biorxiv
selection_source: fresh_fetch
motivation: 之前研究暗示内隐适应与外显检测存在分离，但需跨实验推断，缺少直接证据和计算机制解释。
method: 采用被试内设计，参与者在伪随机旋转下进行伸手任务，一条件额外要求每次伸手后外显报告是否检测到扰动，并结合计算建模分析行为。
result: 内隐适应阈限显著低于外显检测：对1°旋转稳健适应，而可靠检测需约4°。适应模型基于本体与视觉线索比较校正误差，检测模型为贝叶斯因果推断。
conclusion: 内隐适应与外显扰动检测在行为和计算层面均存在分离，感觉运动系统采用不同策略，深化了对感知-行动双通路模型的理解。
---

## 摘要
人类感觉运动系统非常高效地自动将总运动误差解析为其组成部分，即由扰动引起的误差成分（或称外部生成误差（EGE）），与由运动噪声引起的误差成分（或称内部生成误差（IGE））。参与者稳健且内隐地适应以随机视觉运动旋转形式出现的微小（2度）EGE，同时忽略由IGE引起的同等大小的误差。这种误差解析及其相关的知觉过程，与先前的工作直接形成对比，先前工作表明人类必须观察到旋转幅度大于其运动变异标准差的1.5倍，或≥4度，才能外显报告其存在。虽然综合结果表明行动知觉（允许精确且自动的误差解析）与意识检测知觉之间存在分离，但这必须通过使用不同方法的研究来推断。在这里，我们结合了被试内研究设计和计算建模，以阐明内隐适应扰动和外显扰动检测的基本原理。神经典型成年人参与了两个实验，实验包括在伸手触及单个目标时施加伪随机旋转，其中一个实验阶段要求每次伸手后外显报告是否检测到扰动。参与者表现出对内隐扰动响应和外显检测之间的明显分离，对1度EGE有稳健的适应，但直到EGE达到约4度时才能可靠报告其存在。对于适应任务，一个假设参与者比较本体感觉和视觉线索以检测扰动并校正该误差的一部分的模型最能拟合数据。对于信号检测，一个贝叶斯因果推断模型——其中感觉线索与对其原因的先前经验进行最优整合——最能拟合这些数据。这些结果表明，内隐适应与外显扰动检测相分离，且感觉运动系统对这些行为应用了不同的计算策略。

## Abstract
The human sensorimotor system is remarkably effective at automatically parsing total movement error into its constituent parts, the error component due to a perturbation, or externally-generated error (EGE), versus the error component due to motor noise, or internally-generated error (IGE). Participants robustly, and implicitly, adapt to minuscule (2{degrees}) EGEs in the form of randomized visuomotor rotations while ignoring identically-sized errors caused by IGE. This error parsing, and its associated perceptual processes, directly contrasts previous work showing that humans must observe rotations that are >1.5x the standard deviations of their motor variability, or [&ge;]4{degrees}, before explicitly reporting their presence. While the combined results suggest a dissociation between perception for action---which allows for precise and automatic error parsing---and perception for conscious detection, this must be inferred across studies using different methodologies. Here, we combined a within-subjects study design and computational modeling to shed light on the principles underlying implicit adaptation to a perturbation and explicit perturbation detection. Neuro-typical adults participated in two experiments consisting of pseudo-randomized rotations during reaches to a single target, with one session requiring explicit reports after each reach of whether a perturbation was detected. Participants demonstrated a clear dissociation between implicit responses to a perturbation and explicit detection, with robust adaptation to 1{degrees} EGEs, but an inability to reliably report the presence of an EGE until it reached ~4{degrees}. For the adaptation task, a model that assumes the participant compares proprioceptive and visual cues to detect a perturbation and corrects for a proportion of this error best fit the data. For signal-detection, a Bayesian causal-inference model in which sensory cues are optimally integrated with a prior on their cause best fit those data. These results indicate that implicit adaptation is dissociated from explicit perturbation detection and the sensorimotor system applies distinct computational strategies to these behaviors.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义  
- **研究背景**：人类感觉运动系统能自动将运动误差拆解为外部扰动引起的成分（外部生成误差，EGE）和自身运动噪声引起的成分（内部生成误差，IGE）。以往研究发现，人们能内隐地（无意识）适应极小的随机视觉运动旋转（如2°），同时忽略等量级的IGE；但若要求外显报告扰动存在，则需要观察到旋转幅度超过自身运动变异标准差的1.5倍，或≥4°。  
- **核心问题**：内隐运动适应与外显扰动检测之间是否存在行为和计算层面的分离？由于先前证据来自不同研究的方法差异，缺少直接比较和机制解释。  
- **整体含义**：本文通过同一批被试的直接对比和计算建模，试图阐明感觉运动系统对外部误差的内隐学习与意识觉知采用截然不同的计算策略，深化对感知‑行动双通路模型的认知。

### 2. 论文提出的方法论  
- **被试内实验设计**：同一组神经典型成年人参与两种实验条件，消除个体差异干扰。  
- **任务范式**：伸手触达目标任务，施加幅度伪随机变化的视觉运动旋转（即扰动）。一个实验阶段中，每次伸手后额外要求外显判断“是否察觉到扰动”。  
- **计算建模**  
  - **内隐适应模型**：假定参与者通过比较本体感觉线索与视觉线索来检测扰动，并根据检测到的误差按固定比例进行校正。该模型通过拟合适应曲线来解释内隐学习行为。  
  - **外显信号检测模型**：采用贝叶斯因果推断框架，将当前感觉线索与关于扰动原因的先前经验（先验）进行最优整合，给出“有扰动/无扰动”的决策。该模型还原了外显报告的阈限特征。

### 3. 实验设计  
- **数据来源与场景**：实验室条件下的定点伸手运动任务，只有一个目标位置，扰动为视觉‑本体感觉不一致的视觉旋转。  
- **关键对比**：  
  - 内隐适应量（通过伸手方向误差的系统性偏移测量）与外显检测阈限（基于扰动幅度的心理测量曲线）的直接比较。  
  - 对不同旋转幅度（如1°、2°、4°等）的适应与检测敏感性。  
- **Benchmark 与对比方法**：并非在多个模型间竞赛，而是用两种计算模型分别拟合内隐适应和外显检测数据，通过模型拟合优度来推断潜在的计算策略，实质上对比的是“内隐误差校正机制”与“贝叶斯因果推断机制”。

### 4. 资源与算力  
- 论文为行为实验与计算建模，未涉及大规模神经网络训练。文中未提及 GPU 型号、数量或训练时长等算力资源。计算建模仅需在个人计算机上完成参数估计和模型拟合。

### 5. 实验数量与充分性  
- **实验组数**：包含两项主实验（适应任务与外显报告任务），均为被试内设计。  
- **实验充分性**：在同一被试群体内直接比较两种行为，避免了跨研究推断的偏差；结合模型拟合提供了计算层面的解释。但论文未报告具体样本量或交叉验证细节，无法确切评估统计功效和模型泛化性。总体上看，实验设计简洁、针对性较强，能够支撑核心结论。

### 6. 论文的主要结论与发现  
- **行为分离**：内隐适应阈限显著低于外显检测阈限——参与者对约1°的外部生成误差即可表现出稳健的内隐适应，而直到误差达到约4°时才能可靠地外显报告扰动存在。  
- **计算策略分离**：  
  - 内隐适应符合“比较本体与视觉线索以检测扰动，并按比例校正”的误差修正模型。  
  - 外显扰动检测则遵循贝叶斯因果推断，即先验经验与当前感觉信号的最优融合。  
- **理论意义**：感觉运动系统在对扰动做出反应时，并不依赖单一共享的感知通路；内隐运动适应与意识检测在行为和算法层面截然分离，支持感知‑行动双通路假说。

### 7. 优点  
- **直接被试内比较**：首次在同一实验中同时测量内隐适应和外显检测，排除了方法学差异对结论的混淆。  
- **多层面证据**：既从行为阈限上展示分离，又通过计算建模揭示背后的算法原则，增强了结论的深度。  
- **简洁而有力的任务设计**：单一目标、伪随机旋转范式和追加的是否判断，有效分离了内隐和外显过程。  
- **与理论模型衔接**：将经典的感觉运动适应理论与贝叶斯推断框架结合，为理解运动学习中的无意识与意识过程提供了统一解释。

### 8. 不足与局限  
- **样本信息缺失**：未提供被试数量、人口学特征及效应量，无法评估结论的普遍性和统计稳定性。  
- **扰动类型单一**：仅涉及视觉运动旋转，未探讨力场扰动、延迟等其他误差源，模型的可推广性尚待检验。  
- **模型选择范围有限**：虽比较了两种计算策略，但未排除其他可能的适应模型（如基于状态空间模型的误差更新）或信号检测模型变体。  
- **缺乏神经层面证据**：纯行为与建模研究，未结合脑成像或神经调控，难以定位生理机制。  
- **外显报告的敏感性**：外显检测判断可能受反应偏向、认知策略影响，未充分控制这些混杂因素。  
- **应用限制**：实验环境高度受控，结论向真实世界的运动技能学习（如运动康复、体育训练）的转化需进一步验证。

（完）
