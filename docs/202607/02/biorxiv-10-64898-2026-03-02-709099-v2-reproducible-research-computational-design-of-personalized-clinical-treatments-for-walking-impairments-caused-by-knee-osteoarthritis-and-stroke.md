---
title: "Reproducible Research: Computational Design of Personalized Clinical Treatments for Walking Impairments Caused by Knee Osteoarthritis and Stroke"
title_zh: 可重复研究：针对膝骨关节炎和卒中引起的行走障碍的个性化临床治疗的计算设计
authors: "Salati, R. M., Li, G., Williams, S. T., Fregly, B. J."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.02.709099v2.full.pdf"
tags: ["query:sb"]
score: 7.0
evidence: 个性化神经肌肉骨骼模型用于运动优化
tldr: 个性化神经肌肉骨骼模型能优化运动障碍治疗，但现有工具需编程经验且缺乏可重复性。本文通过NMSM Pipeline详细教程，演示模型个性化与治疗优化：针对膝骨关节炎设计步态调整和截骨术，针对中风设计基于协同的功能电刺激。生成的模型与优化紧密复现实验数据，设计优化成功将双膝内收力矩降至目标或平衡双腿推进制动冲量，为个性化治疗提供端到端可重复流程。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有神经肌肉骨骼建模工具使用门槛高，研究可重复性差，尤其缺乏针对真实临床问题的端到端教程。
method: 利用NMSM Pipeline开发教程，针对膝骨关节炎步态调整与截骨术、中风协同功能电刺激进行模型个性化与治疗优化，并设为课程项目。
result: 生成的个性化模型和跟踪优化准确复现受试者行走的实验数据，设计优化成功将膝内收力矩降至目标或平衡推进制动冲量。
conclusion: 首次提供覆盖模型个性化到个性化治疗设计全流程的分步教程，可用于NMSM Pipeline入门和神经肌肉骨骼建模课程教学。
---

## 摘要
背景 个性化计算神经肌肉骨骼模型在优化运动障碍临床治疗方案设计方面具有巨大潜力。尽管许多软件工具针对模型个性化和治疗优化过程的特定部分，但它们通常需要相当的编程经验才能使用，并且未涵盖这两个过程的全部范围。此外，已发表的神经肌肉骨骼建模研究通常不提供他人重复工作所需的所有方法细节。因此，由于缺乏详细的培训材料来展示使用真实受试者运动数据解决真实临床问题的两个过程，寻求发展模型个性化和治疗优化过程技能的研究人员面临陡峭的学习曲线。

方法 本文介绍了使用两个真实临床问题和神经肌肉骨骼建模（NMSM）流水线进行模型个性化和治疗优化过程的详细培训教程。第一个临床问题涉及为双侧膝关节内侧骨关节炎患者设计个性化步态调整和高位胫骨截骨手术，目标是将双膝的峰值内收力矩降低到指定目标水平。第二个临床问题涉及为卒中后行走功能受损的患者设计基于协同功能电刺激处方，目标是使两条腿的推进冲量和制动冲量相等。这两个教程都是作为本科生/研究生机械工程课程中给新手用户的课程项目实施的。

结果 两个教程都生成了个性化神经肌肉骨骼模型和相关的动力学一致的追踪优化，这些优化密切再现了走路时测量的受试者特定的实验关节角度、关节力矩、地面反作用力和力矩以及（如果适用）肌肉激活。随后的设计优化预测了达到目标峰值膝内收力矩或推进和制动冲量的个性化治疗。

结论 本文提供的详细逐步教程首次引导用户完成创建个性化神经肌肉骨骼模型然后使用它们为两个患有不同临床问题的受试者设计个性化治疗的整个过程。这些教程可用于向新用户介绍NMSM流水线，并作为神经肌肉骨骼建模课程的项目。

## Abstract
BackgroundPersonalized computational neuromusculoskeletal models have great potential for optimizing the design of clinical treatments for movement impairments. While many software tools address specific parts of the model personalization and treatment optimization processes, they typically require significant programming experience to use and do not cover the full breadth of these two processes. Furthermore, published neuromusculoskeletal modeling studies typically do not provide all the methodological details needed for others to reproduce the work. Consequently, researchers seeking to develop skills in the model personalization and treatment optimization processes face a steep learning curve due to the lack of detailed training materials that demonstrate both processes for real-life clinical problems using real-life subject movement data.

MethodsThis article presents detailed training tutorials for the model personalization and treatment optimization processes using two real-life clinical problems and the Neuromusculoskeletal Modeling (NMSM) Pipeline. The first clinical problem involves the design of personalized gait modifications and high tibial osteotomy surgery for an individual with bilateral medial knee osteoarthritis, where the goal is to reduce the peak adduction moment in both knees to a specified target level. The second clinical problem involves the design of a synergy-based functional electrical stimulation prescription for an individual post-stroke with impaired walking function, where the goal is to equalize the propulsive and braking impulses between the two legs. Both tutorials were implemented as course projects given to novice users in a combined undergraduate/graduate mechanical engineering course.

ResultsBoth tutorials produced personalized neuromusculoskeletal models and associated dynamically consistent tracking optimizations that closely reproduced subject-specific experimental joint angles, joint moments, ground reaction forces and moments, and (if applicable) muscle activations measured during walking. Subsequent design optimizations predicted personalized treatments that achieved target values of peak knee adduction moments or propulsive and braking impulses.

ConclusionsThe detailed step-by-step tutorials presented with this article are the first to walk users through the entire process of creating personalized neuromusculoskeletal models and then using them to design personalized treatments for two subjects with two different clinical problems. These tutorials can be used to introduce new users to the NMSM Pipeline and as projects in neuromusculoskeletal modeling courses.