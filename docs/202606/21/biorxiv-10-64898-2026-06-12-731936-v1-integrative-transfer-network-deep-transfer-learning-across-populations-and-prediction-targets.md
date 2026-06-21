---
title: "Integrative Transfer Network: Deep Transfer Learning Across Populations and Prediction Targets"
authors: "Gao, Y., Cui, Y."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.12.731936v1.full.pdf"
tags: ["query:cdm-sports"]
score: 7.0
evidence: 跨群体和多预测目标的深度迁移学习方法，可应用于体育分析
tldr: 针对临床数据中多亚组与多预测目标难以联合建模的问题，本文提出集成迁移网络（ITN），一种同时利用亚组差异与多相关结局的深度神经网络。在生存分析与分类任务上的实验表明，ITN能有效捕获共享与亚组特定信息。该方法可迁移至体育分析领域，例如跨运动员群体或多项表现指标的预测。
source: biorxiv
selection_source: fresh_fetch
motivation: 跨群体和多预测目标的深度迁移学习方法，可应用于体育分析。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Large-scale clinical and biomedical datasets increasingly contain both diverse subgroup attributes (e.g., demographic or clinical subgroups) and multiple prediction targets. Although various machine learning approaches can address subgroup differences or multi-target prediction, they often consider these aspects independently rather than jointly. To more effectively capture the shared and subgroup-specific information in such complex datasets, we propose the Integrative Transfer Network (ITN), a deep neural network designed to leverage data across subgroups and multiple related outcomes simultaneously. In extensive experiments, including time-to-event and classification tasks where demographic subgroups and multiple disease end-points are prevalent, ITN demonstrates consistent improvements in subgroup-specific prediction by borrowing strength from other subgroups and outcomes. We envision ITN as a unified frame-work for learning from heterogeneous datasets where subgroup-specific insights are critical.