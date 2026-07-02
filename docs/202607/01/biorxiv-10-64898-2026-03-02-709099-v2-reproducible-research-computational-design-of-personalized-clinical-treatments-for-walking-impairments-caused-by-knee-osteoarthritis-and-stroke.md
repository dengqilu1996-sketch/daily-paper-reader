---
title: "Reproducible Research: Computational Design of Personalized Clinical Treatments for Walking Impairments Caused by Knee Osteoarthritis and Stroke"
title_zh: 可重复研究：膝骨关节炎和卒中引起的行走障碍的个性化临床治疗方案的计算设计
authors: "Salati, R. M., Li, G., Williams, S. T., Fregly, B. J."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.02.709099v2.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 用于优化临床治疗设计的个性化计算神经肌骨模型
tldr: 个性化神经肌肉骨骼模型可优化步态障碍治疗，但缺乏完整可复现教程致学习门坎高。本文以膝骨关节炎及中风步态异常为例，详述运用 NMSM Pipeline 进行模型个性化与治疗设计。结果构建出精准复现实验数据的模型，并优化得到达成目标力矩或冲量的治疗。首次提供从建模到治疗的端到端教程，填补教学空白。
source: biorxiv
selection_source: fresh_fetch
motivation: 个性化神经肌肉骨骼模型用于临床治疗优化缺少标准化可复现的完整教程，初学者上手难。
method: 通过膝骨关节炎步态修改/截骨术和中风电刺激两案例，详述NMSM Pipeline的模型个性化与治疗设计流程。
result: 教程成功构建了精确复现实验步态数据的个性化模型，并优化得到满足目标峰值膝内收力矩或推进/制动冲量的治疗方案。
conclusion: 首次提供从个性化建模到治疗设计的端到端教程，填补教学空白，助力NMSM Pipeline推广应用。
---

## 摘要
背景：个性化计算神经肌肉骨骼模型在优化运动障碍临床治疗方案设计方面具有巨大潜力。尽管许多软件工具解决了模型个性化与治疗优化过程的特定部分，但通常需要丰富的编程经验才能使用，并且未能涵盖这两个过程的全部范围。此外，已发表的神经肌肉骨骼建模研究通常未提供他人复现工作所需的所有方法细节。因此，由于缺乏详细的培训材料来展示利用真实受试者运动数据解决真实临床问题的两个过程，寻求发展模型个性化与治疗优化过程技能的研究人员面临着陡峭的学习曲线。方法：本文通过两个真实临床问题和神经肌肉骨骼建模（NMSM）流水线，为模型个性化与治疗优化过程提供了详细的培训教程。第一个临床问题涉及为一名双侧内侧膝骨关节炎患者设计个性化步态调整与高位胫骨截骨术，目标是使双膝的峰值内收力矩降低至指定目标水平。第二个临床问题涉及为一名中风后行走功能受损的患者设计基于协同的功能性电刺激处方，目标是均衡双腿的推进冲量与制动冲量。这两个教程均作为课程项目，在面向初学者的本科与研究生联合机械工程课程中实施。结果：两个教程均生成了个性化神经肌肉骨骼模型及相应的动力学一致跟踪优化，这些优化能够精确再现受试者行走时测量的特异性关节角度、关节力矩、地面反作用力与力矩，以及（如适用）肌肉激活。随后的设计优化预测了个性化治疗方案，达到了峰值膝内收力矩或推进与制动冲量的目标值。结论：本文提供的详细分步教程首次引导用户完成创建个性化神经肌肉骨骼模型的整个过程，并随后使用这些模型为两名具有不同临床问题的受试者设计个性化治疗方案。这些教程可用于向新用户介绍NMSM流水线，并作为神经肌肉骨骼建模课程中的项目。

## Abstract
Background: Personalized computational neuromusculoskeletal models have great potential for optimizing the design of clinical treatments for movement impairments. While many software tools address specific parts of the model personalization and treatment optimization processes, they typically require significant programming experience to use and do not cover the full breadth of these two processes. Furthermore, published neuromusculoskeletal modeling studies typically do not provide all the methodological details needed for others to reproduce the work. Consequently, researchers seeking to develop skills in the model personalization and treatment optimization processes face a steep learning curve due to the lack of detailed training materials that demonstrate both processes for real-life clinical problems using real-life subject movement data. Methods: This article presents detailed training tutorials for the model personalization and treatment optimization processes using two real-life clinical problems and the Neuromusculoskeletal Modeling (NMSM) Pipeline. The first clinical problem involves the design of personalized gait modifications and high tibial osteotomy surgery for an individual with bilateral medial knee osteoarthritis, where the goal is to reduce the peak adduction moment in both knees to a specified target level. The second clinical problem involves the design of a synergy-based functional electrical stimulation prescription for an individual post-stroke with impaired walking function, where the goal is to equalize the propulsive and braking impulses between the two legs. Both tutorials were implemented as course projects given to novice users in a combined undergraduate/graduate mechanical engineering course. Results: Both tutorials produced personalized neuromusculoskeletal models and associated dynamically consistent tracking optimizations that closely reproduced subject-specific experimental joint angles, joint moments, ground reaction forces and moments, and (if applicable) muscle activations measured during walking. Subsequent design optimizations predicted personalized treatments that achieved target values of peak knee adduction moments or propulsive and braking impulses. Conclusions: The detailed step-by-step tutorials presented with this article are the first to walk users through the entire process of creating personalized neuromusculoskeletal models and then using them to design personalized treatments for two subjects with two different clinical problems. These tutorials can be used to introduce new users to the NMSM Pipeline and as projects in neuromusculoskeletal modeling courses.

---

## 论文详细总结（自动生成）

## 1. 研究动机与核心问题
- 个性化神经肌肉骨骼（NMS）模型在运动障碍临床治疗设计中有巨大潜力，但现有工具要么需要大量编程经验，要么只覆盖模型个性化或治疗优化的局部环节，且已发表研究极少提供完整的方法细节，使得新研究者面临陡峭的学习曲线。
- 本文旨在通过两个真实的临床案例——双侧内侧膝骨关节炎（OA）与脑卒中后偏瘫步态——提供一套完整的、可复现的端到端教程，利用刚发布的 **NMSM Pipeline** 软件包，从模型个性化一直走到治疗优化，填补该领域的培训空白。

## 2. 方法论
- **整体框架**：基于 MATLAB 的 NMSM Pipeline（结合 OpenSim 4.5），用户通过编写 XML 设置文件（无需手写代码）即可顺序调用模型个性化工具和治疗优化工具。
- **模型个性化工具**（Model Personalization）：
  - **Joint Model Personalization**：优化关节功能轴、体段缩放因子和标记点位置，使模型运动学尽可能逼近实验标记轨迹。
  - **Ground Contact Model Personalization**：校准足‑地接触模型的刚度、阻尼和摩擦参数，以精确复现地面反力与力矩。
  - **Muscle-tendon Model Personalization**：利用 EMG 驱动方式标定肌肉激活‑力参数，使模型预测的关节力矩贴合实验逆动力学力矩。
  - **Neural Control Model Personalization**：从肌肉激活中提取双侧对称的肌肉协同（synergy），并用其再现关节力矩，形成个性化神经控制模型。
- **治疗优化工具**（Treatment Optimization）：
  - **Tracking Optimization**：以个性化模型为基础，通过直接配点最优控制（GPOPS‑II 求解器）产生动态一致的运动，精确跟踪所有实验变量（关节角、力矩、地面反力、肌肉激活）。
  - **Verification Optimization**：仅跟踪控制量而不直接跟踪运动，验证最优控制问题的合理性和可行性。
  - **Design Optimization**：引入临床目标（如降低膝内收力矩、平衡推进/制动冲量）和治疗设计变量（如截骨矫正角、步态修改、协同缩放因子），预测最优治疗方案。
- **案例一（膝 OA）**：采用纯扭矩驱动模型，通过 Joint Model Personalization + Ground Contact Model Personalization + Tracking/Design Optimization，分别设计 **高位胫骨截骨术（HTO）** 和 **内侧推力步态（MTG）**，使峰值膝内收力矩（KAM）降至 30.3 Nm 的目标。
- **案例二（脑卒中）**：引入肌肉与神经控制，经过 Muscle-tendon + Neural Control Model Personalization，在 Tracking Optimization 中利用肌肉协同驱动运动，最终通过 Design Optimization 调整协同激活幅度和推进/制动冲量目标，生成 **基于协同的功能性电刺激（FES）处方**。

## 3. 实验设计与对比方案
- **数据来源**：
  - 膝 OA 患者：47 岁男性，双侧内侧 OA，自选行走速度 1.2 m/s，采集运动学、地面反力。
  - 脑卒中患者：79 岁男性，右侧偏瘫，最快舒适速度 0.8 m/s，额外采集 16 通道表面与细丝 EMG。
- **基准与对比**：
  - 教程内部比较：Joint Model Personalization 的序贯优化 vs. 同时优化；地面接触模型的库仑摩擦 vs. 粘性摩擦。所有跟踪误差均以 RMSE 量化，并与文献中同类方法对比。
  - 治疗设计比较：HTO 测试 3 种矫正角（3°/6°/9°），MTG 测试三种 KAM 容限（10/15/20 Nm），寻找达到目标的参数；脑卒中 FES 通过不同协同缩放策略使推进/制动冲量对称度趋近零。
  - 可重现性评估：来自课程项目的学生（本科/研究生）作业表明，各模块完全或接近复现结果的比例为 64%–95%，证明教程具有良好的可复现性。

## 4. 资源与算力
- **硬件**：Windows 11 PC 工作站，AMD Ryzen 9 7950X 16 核处理器，32 GB DDR5 RAM。**未使用 GPU**。
- **软件**：NMSM Pipeline v1.4.0（依赖 MATLAB 多个工具包，如优化、并行、统计、信号处理等）；OpenSim 4.5；最优控制求解器 GPOPS‑II（学术年付 $165）。
- **运行时间**：
  - 教程一：模型个性化 <0.6 小时，跟踪优化约 0.2 小时，设计优化 0.12–0.38 小时。
  - 教程二：模型个性化约 0.6 小时，跟踪优化约 6.3 小时（最耗时），设计优化约 1.1 小时。

## 5. 实验数量与充分性
- 实验分为两个完整的教程案例，每个案例包含 4 个模块，共计 **7 种 NMSM Pipeline 工具运行**（教程一 5 种，教程二 7 种，部分为学生直接运行，部分为教师预生成）。
- 每一模块均有细致的误差分析（如关节角 RMSE、力矩 RMSE、标记点误差），并通过多个变体（例如两种接触模型、三种治疗参数）进行对比。
- 可重现性通过 20 余名学生的提交结果得到量化评估，证明流程的稳健性。
- 总体而言，实验覆盖了从数据到治疗决策的全链条，但**未与其他主流工具（如 OpenSim Moco、CEINMS）进行横向比较**，实验性质更偏向教学教程的可行性验证，而非计算方法的优势比较。

## 6. 主要结论与发现
- 教程成功地引导用户通过 NMSM Pipeline 建立了个性化模型，获得的跟踪优化能够以很小的误差（关节角 <3.2° RMSE，力矩 <6.0 Nm）复现实验行走数据，并确保动力学一致性。
- 基于个性化模型的设计优化给出了符合临床目标的治疗方案：HTO 矫正约 6°，MTG 容许 KAM 15 Nm 时可将 KAM 降至 30.3 Nm 以下；脑卒中 FES 通过缩放协同激活使双腿推进/制动冲量对称指数从 ~100% 降至 <2%。
- 首次展示了从原始数据到个性化治疗优化全流程的**完全可重复**范例，并且通过学生项目验证其教学可行性。

## 7. 优点
- **端到端教学**：首次提供覆盖模型个性化与治疗优化的完整教程，新手无需编程基础即可上手。
- **真实临床案例**：使用真实患者数据设计两种不同机理的治疗，具有直接临床参考价值。
- **细节透明**：教程中详细解释了每一步的配置原理、参数选择理由以及常见问题的调试策略，弥补了常规论文中缺失的“隐性知识”。
- **可重现性强**：开源代码、共享数据与设置文件，且通过了学生群体的复现测试。
- **集成化工具链**：NMSM Pipeline 将多个工具统一在同一框架下，减少了工具间的衔接成本。

## 8. 不足与局限
- **代表性有限**：仅包含两名受试者、两种特定病理，所提流程未必能直接迁移至其他临床问题或患者。
- **治疗简化假设**：
  - HTO 仅通过修改膝关节内收角模拟手术，未引入真实的截骨关节模型，且未包含肌肉作用，可能高估运动调整能力。
  - MTG 虽在单例中验证过，但不保证其他患者能实现所预测的步态。
  - 脑卒中 FES 假设双侧协同向量几乎一致，且受试者能自主纠正代偿性协同，实际中枢损伤可能无法达到；PAP 研究通常只能刺激少数肌肉，而教程刺激整个协同，临床可实施性受限。
- **需付费软件**：GPOPS‑II 虽提供学术许可，但仍构成一定成本门槛。
- **未进行横向工具对比**：未与 OpenSim Moco、CEINMS 等成熟工具在处理相同问题时的性能或精度进行比较。
- **实验验证仅限于数值模拟**：预测的治疗效果未经过实际临床试验或前瞻性研究验证，结论停留在计算层面。

（完）
