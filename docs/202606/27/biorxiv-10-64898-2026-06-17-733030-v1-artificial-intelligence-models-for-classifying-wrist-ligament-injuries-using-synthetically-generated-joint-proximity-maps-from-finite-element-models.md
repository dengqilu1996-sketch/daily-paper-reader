---
title: Artificial Intelligence Models for Classifying Wrist Ligament Injuries Using Synthetically-Generated Joint Proximity Maps from Finite Element Models
title_zh: 利用有限元模型生成的合成关节邻近图进行腕部韧带损伤分类的人工智能模型
authors: "Chen, H.-Y., Camp, J., Trentadue, T. P., Thoreson, A. R., Leng, S., Holmes, D. R., Kakar, S., An, K.-N., Zhao, K. D., Andreassen, T. E."
date: 2026-06-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.733030v1.full.pdf"
tags: ["query:sport-sci"]
score: 7.0
evidence: 利用合成关节接近图AI分类腕部韧带损伤以实现无创诊断
tldr: 腕韧带损伤早期诊断困难，易致骨关节炎。本研究基于两名健康者四维CT数据构建个性化有限元模型，通过蒙特卡洛采样22个韧带参数模拟7500种损伤，生成900万张骨间接近RGB图像，结合17个运动学指标训练CNN。模型对所有损伤类型的平均AUROC为0.757，在临床相关手腕功能角度下提升至0.824；特定韧带识别AUROC最高0.999，灵敏度与特异度超0.99。结果验证了合成数据训练AI的可行性，骨间接近图可作为腕韧带损伤非侵入性生物标志物。
source: biorxiv
selection_source: fresh_fetch
motivation: 腕韧带损伤的非侵入性诊断困难，早期检测对预防骨关节炎至关重要。
method: 从两名健康者四维CT构建个性化手腕有限元模型，蒙特卡洛采样韧带属性模拟7500种损伤生成900万张接近图，训练混合CNN。
result: 模型平均AUROC 0.757，临床角度子集0.824，特定韧带识别AUROC达0.999，灵敏度和特异度超0.99。
conclusion: 合成数据训练AI分类腕韧带损伤可行，骨间接近图有望成为非侵入性生物标志物。
---

## 摘要
背景/目的：诊断腕部韧带损伤具有挑战性；早期发现与治疗对防止骨关节炎进展至关重要。骨间邻近图作为关节间隙的替代指标，可从体积成像数据生成，并可能提供有关腕部健康的重要信息。人工智能可提高基于成像衍生指标的无创诊断准确性。本研究验证了使用有限元模型生成的合成邻近图数据训练人工智能的可行性。

方法：基于四维计算机断层扫描衍生的解剖和运动学数据，为两名无症状受试者构建了个性化腕部有限元模型。通过蒙特卡洛抽样改变22项韧带材料属性，模拟了7500个独特损伤场景，从有限元导出的运动中生成了900万张标记的红绿蓝（RGB）骨间邻近向量场图像。这些图像与17项描述性指标关联，包括整体腕关节角度和骨面配对，并用于开发混合输入卷积神经网络。评估了模型识别特定韧带损伤的性能。

结果：在所有损伤类型和运动学条件下，卷积神经网络的平均受试者工作特征曲线下面积（AUROC）为0.757。在具有临床相关功能角度的子集中，平均AUROC达到0.824。单个韧带的最佳AUROC范围为0.807至0.999。在特定腕关节角度和骨面配对下，某些韧带损伤模拟的灵敏度和特异度超过0.99。

结论：本研究证明了使用有限元模型的合成数据训练人工智能模型以分类腕部韧带损伤的可行性。基于邻近图的RGB图像可能成为韧带损伤的相关生物标志物。

## Abstract
Background/PurposeDiagnosing wrist ligament injuries is challenging; early detection and treatment are important to prevent osteoarthritis progression. Interosseous proximity maps, a proxy measure for joint space, can be generated from volumetric imaging data and may provide important information about wrist health. Artificial intelligence (AI) could enhance accuracy of noninvasive diagnosis based on imaging-derived metrics. This work demonstrates feasibility of AI training using synthetic proximity map data generated from finite element models (FEMs).

MethodsPersonalized wrist FEMs for two asymptomatic participants were created from four-dimensional computed tomography-derived anatomic and kinematic data. Monte Carlo sampling varied 22 ligament material properties and simulated 7,500 unique injury scenarios generating 9,000,000 labeled red, green, and blue (RGB) images of interosseous proximity vector fields from FEM-derived motions. Images were associated with 17 descriptive metrics, including gross wrist angles and bone surface pairs, and used to develop mixed-input convolutional neural networks (CNNs). Model performance was evaluated for identifying specific ligament injuries.

ResultsAverage area under receiver operating characteristic curve (AUROC) for CNNs was 0.757 across all injury types and kinematics. In a subset with clinically-relevant functional angles, the average AUROC was 0.824. Best-performing individual ligament AUROCs ranged from 0.807 to 0.999. Sensitivities and specificities exceeded 0.99 for some ligament injury simulations under specific wrist angles and bone surface pairs.

ConclusionThis study demonstrates the feasibility of using synthetic data from FEMs to train AI models for classifying wrist ligament injuries. Proximity-based RGB images may be a relevant biomarker of ligamentous injury.