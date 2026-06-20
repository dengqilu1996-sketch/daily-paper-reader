---
title: Bi-level inverse optimal control for preoperative prediction of postoperative squat kinematics after total knee replacement
title_zh: 基于双层逆最优控制的全膝关节置换术后下蹲运动学术前预测
authors: "Song, H."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731549v1.full.pdf"
tags: ["query:sb"]
score: 7.0
evidence: 使用双层逆最优控制和肌骨模型模拟运动，可直接用于运动生物力学分析。
tldr: 全膝关节置换术（TKR）后患者常难以完成深蹲等高屈曲动作，当前术前规划基于静止影像，无法关联假体对线与动态功能。为此，该研究提出一种双层逆向最优控制框架，通过分析患者术后下蹲数据逆向学习成本函数，进而从计划假体对线直接预测术后下蹲运动学。个性化预测精准复现实验轨迹（均方根误差5.15°），群体预测无需患者术后数据即保持运动模式，下蹲深度由优化自主确定。该框架有望发展为术前工具，辅助医师选择最佳对线以改善功能预后。
source: biorxiv
selection_source: fresh_fetch
motivation: 当前术前规划依赖静态影像，无法预测不同假体对线对术后动态下蹲功能的影响。
method: 构建患者特异肌骨模型，应用双层逆向最优控制分别识别个体化与组级成本函数，预测术后下蹲运动学。
result: 个体化设置低误差复现实验轨迹（均方根误差5.15°，相关系数0.96），组级设置误差略增但保持运动模式与相位，下蹲深度由优化自发确定。
conclusion: 该框架可连接植入物对线与术后下蹲表现，但需更多样本外验证才能用于术前预测辅助工具。
---

## 摘要
全膝关节置换术可恢复晚期骨关节炎患者的活动能力，但许多患者在执行下蹲等高屈曲动作时仍存在受限。当前的术前规划依赖于静态影像，无法预测不同植入物对线选择将如何影响术后动态功能。本研究开发了一个预测性模拟框架，使用双层逆最优控制将术前植入物对线直接与预期的术后下蹲运动学关联起来。

利用实验下蹲数据，为六名全膝关节置换患者构建了个体化肌骨模型。应用双层逆最优控制分别识别个体化和组水平的目标函数。个体化设置提供了个体特异性精度，而组水平设置则推导出一个单一的组水平目标函数，作为无需术后运动数据即可进行术前使用的初步步骤。

个体化设置以低误差重现了所有关节的实验轨迹（平均顶点差异1.53°，均方根误差5.15°，归一化均方根误差11.15%，皮尔逊相关系数0.96）。组水平设置误差较高但可接受（平均顶点差异5.70°，均方根误差6.75°，归一化均方根误差17.53%，皮尔逊相关系数0.95），同时保留了运动的一般模式和相位。下蹲深度由优化自然产生，而非预先规定。

该框架可为未来定量工具的开发提供基础，用以评估植入物对线选择如何影响术后下蹲表现，从而可能改善全膝关节置换的功能结局。

这些结果表明，所提出的逆最优控制框架能够再现全膝关节置换术后下蹲运动学的关键特征，但在用于术前预测或转化为旨在改善功能结局的工具之前，还需要进一步的样本外验证。

## Abstract
Total knee replacement restores mobility in patients with advanced osteoarthritis, yet many individuals still experience limited ability to perform high-flexion tasks such as squatting. Current preoperative planning relies on static imaging and cannot predict how different implant alignment choices will affect postoperative dynamic function. This study developed a predictive simulation framework that uses bi-level inverse optimal control to link preoperative implant alignment directly to expected postoperative squat kinematics.

Subject-specific musculoskeletal models were constructed for six total knee replacement patients using experimental squat data. Bi-level inverse optimal control was applied to identify both individualised and group-level cost functions. The individualised setting provided subject-specific accuracy, while the group-level setting derived a single group-level cost function as an initial step toward preoperative use without requiring postoperative motion data.

The individualised setting reproduced experimental trajectories with low errors across all joints (mean apex difference 1.53{degrees}, root-mean-square error 5.15{degrees}, normalised root-mean-square error 11.15%, Pearson correlation 0.96). The group-level setting yielded higher but acceptable errors (mean apex difference 5.70{degrees}, root-mean-square error 6.75{degrees}, normalised root-mean-square error 17.53%, Pearson correlation 0.95) while preserving the general pattern and phasing of the motion. Squat depth emerged naturally from the optimisation rather than being prescribed.

This framework may provide a basis for future quantitative tools to evaluate how implant alignment choices influence postoperative squat performance, potentially improving functional outcomes in total knee replacement.

These results suggest that the proposed IOC framework can reproduce key features of post-TKR squat kinematics, but further out-of-sample validation is required before it can be used for preoperative prediction or translated into tools aimed at improving functional outcomes in total knee replacement.