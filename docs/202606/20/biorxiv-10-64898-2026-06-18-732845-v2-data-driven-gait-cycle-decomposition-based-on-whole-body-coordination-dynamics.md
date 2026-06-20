---
title: Data-driven gait cycle decomposition based on whole-body coordination dynamics
title_zh: 基于全身协调动力学的数据驱动步态周期分解
authors: "De luca, M., Demuru, M., Gallo, E., ANGIOLELLI, M., Tafuri, D., Sorrentino, G., Mandolesi, L., Sorrentino, P., Troisi Lopez, E."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.732845v2.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 基于全身协调动力学的人体步态运动学分析，适用于运动生物力学
tldr: 人类步态研究传统上依赖分相描述，但可能忽视全身协调的连续动态特性。为此，本文提出数据驱动框架，结合网络理论与非负矩阵分解，从三维运动学数据构建动态联结组，并提取全身协调模式。在60名健康成人中识别出六个对称且稳健的协调模式，揭示了跨越传统相位的主动协调及上肢的动态稳定作用。这项研究丰富了经典步态理论，为运动控制和康复评估提供了整体性新工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统步态周期描述依赖观测分析，可能未充分反映全身协调的连续动态过程。
method: 结合网络理论构建全身协调的动态联结组，用非负矩阵分解提取关节协调模式及其时序激活。
result: 从60名健康者数据获得六个高度一致、对称的全身协调模式，有效表征运动功能子任务，并揭示上肢的稳定性作用。
conclusion: 该数据驱动框架丰富了经典相位描述，为理解运动控制及开发临床生物标志物提供了新视角。
---

## 摘要
长期以来，对人类运动的研究依赖于步态周期的描述性框架，这些框架为步行的功能阶段及其背后的生物力学需求提供了重要见解。尽管这些模型仍然具有很高的信息量，但它们主要基于观察性分析，可能无法完全捕捉到人类运动特征的连续、全局协调。本研究提出了一个研究全身协调的综合框架。该框架将网络理论与非负矩阵分解（NNMF）相结合，将步态视为一个由关节协调相互作用构成的动态系统。利用60名健康受试者的三维运动学数据，我们构建了全身协调随时间的表示，称为动态运动连接组。随后使用NNMF对其分解，提取关节协调的空间模式及其对应的时间激活，从而在保留生理意义的同时实现了对运动组织的可解释性表征。我们的分析在受试者中提取了六个稳健、高度一致且对称的协调模式，有效捕捉了运动的主要功能子任务。这些发现并非挑战经典阶段描述，而是丰富了它们，展示了协调如何作为一个连续的、通常具有前瞻性的过程浮现，该过程可以跨越传统的阶段边界，并系统性地整合上肢以实现动态稳定性。总体而言，本研究提供了关于人类运动的整体性、数据驱动视角，为运动控制的未来研究提供了有前景的基础，并可能有助于开发用于临床和康复应用的敏感生物标志物。

## Abstract
The study of human locomotion has long relied on descriptive frameworks of the gait cycle, which have provided essential insights into the functional phases of walking and their underlying biomechanical demands. While these models remain highly informative, they are largely based on observational analyses and may not fully capture the continuous, global coordination that characterizes human movement. The present study proposes an integrated framework to study whole-body coordination. This framework combines network theory with non-negative matrix factorization (NNMF) to treat gait as a dynamic system of coordinated joint interactions. Using three-dimensional kinematic data from 60 healthy subjects, we constructed a representation of whole-body coordination across time, named dynamic kinectome. It was then decomposed using NNMF to extract spatial patterns of joint coordination and their corresponding temporal activations, allowing for an interpretable characterization of locomotor organization while preserving physiological meaning. Our analysis extracted six robust, highly consistent, and symmetrical coordination patterns across participants, effectively capturing the primary functional subtasks of locomotion. Rather than challenging classical phase descriptions, these findings enrich them by showing how coordination emerges as a continuous, often proactive process that can extend across conventional phase boundaries and systematically integrates the upper limbs for dynamic stability. Overall, this study provides a holistic, data-driven perspective on human locomotion, offering a promising basis for future investigations in motor control and may contribute to the development of sensitive biomarkers for clinical and rehabilitative applications.