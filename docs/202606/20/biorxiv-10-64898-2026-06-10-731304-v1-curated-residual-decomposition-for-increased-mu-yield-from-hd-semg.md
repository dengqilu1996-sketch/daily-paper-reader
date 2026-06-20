---
title: Curated Residual Decomposition for Increased MU Yield from HD-sEMG
title_zh: 通过整理残差分解提高高密度表面肌电图运动单位产量
authors: "Osswald, M., Del Vecchio, A."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731304v1.full.pdf"
tags: ["query:sport-tsa"]
score: 7.0
evidence: 改进高密度表面肌电图的运动单位分解，一种可穿戴生理传感器
tldr: "高密度表面肌电图（HD-sEMG）分解算法通常仅识别部分运动单元（MU），且偏好高振幅单元，低振幅MU大量遗漏。本研究提出策展残差分解（CRD），通过对初始分解残差信号的再分解，额外挖掘低振幅MU。跨多个数据集和肌肉的验证表明，首次CRD迭代使MU产量增加31–142%，信号解释功率显著提升，且经肌内肌电图验证，新增MU识别准确度与原始MU相当（RoA：0.992 vs 0.994）。新增MU振幅更小、募集阈值更低，证实了对低阈值小MU的恢复。CRD为离线分析提供了可靠、可选的步骤，实现更完整的全募集范围MU分解。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有HD-sEMG分解偏好高振幅MU，遗漏低振幅MU，限制神经肌肉系统全面评估。
method: 提出策展残差分解（CRD），对人工编辑的初始分解后残差信号迭代分解，识别先前未检测的低振幅运动单元。
result: "首次CRD迭代使MU产量提高31–142%，新增MU动作电位振幅更小、募集阈值更低，且与原始MU识别准确度相当。"
conclusion: CRD可靠增加MU产量与信号解释功率，恢复低阈值小MU，为离线分析提供更完整的分解结果。
---

## 摘要
高密度表面肌电图（HD-sEMG）分解算法可从无创记录中识别运动单位（MU），但即使是黄金标准方法通常也只能分解所有生理活跃运动单位的一部分，并优先提取幅度较高的运动单位，导致低幅度运动单位代表性不足。我们提出了整理残差分解（CRD）：通过对人工编辑的初始分解后剩余的残差信号进行分解，我们识别出额外的、主要是低幅度的运动单位，这些单位此前因动作电位叠加和优先收敛到较大运动单位而未被检测到。

我们将该方法应用于三个数据集：来自三块肌肉的同步HD-sEMG与HD-iEMG记录，用于双源验证，以及两个公开数据集。在所有数据集中，CRD均显著提高了运动单位产量。在双源验证数据集中，第一次CRD迭代将产量提高了31-50%（FDI：46.9%，TA：49.8%，VL：31.1%），并通过肌内记录验证确认CRD识别准确性与原始运动单位相当（原始RoA：0.994 ± 0.005；CRD RoA：0.992 ± 0.009）。在公开数据集中，第一次迭代使每块肌肉的产量增加35%至142%。相应地，解释信号功率比也增加，且第一次迭代贡献了大部分增益。第二次CRD迭代进一步小幅提高了产量（0-26.7%）。额外识别出的运动单位具有更小的动作电位幅度和更低的募集阈值，表明恢复了更小、更低阈值的运动单位。

CRD在不同的肌肉、数据集和分解实现中均可靠地提高了运动单位产量并解释信号功率。该方法为离线分析中在整个募集范围内获得更完整的分解结果提供了一个可选且经过验证的步骤。

## Abstract
High-density surface electromyography (HD-sEMG) decomposition algorithms identify motor units (MUs) from non-invasive recordings, yet even gold-standard methods typically decompose only a subset of all physiologically active MUs and preferentially extract higher-amplitude units, leaving low-amplitude MUs underrepresented. We propose Curated Residual Decomposition (CRD): Through decomposition of the residual signal remaining from a manually edited initial decomposition, we identify additional, mainly lower amplitude MUs that were previously undetected due to action potential superposition and preferential convergence to larger MUs.

We applied this approach to three datasets: concurrent HD-sEMG and HD-iEMG recordings from three muscles for two-source validation, and two publicly available datasets. Across all datasets, CRD substantially increased MU yield. In the two-source validation dataset, the first CRD iteration increased yield by 31-50% (FDI: 46.9%, TA: 49.8%, VL: 31.1%), with validation via intramuscular recordings confirming comparable identification accuracy of the CRD compared to the original MUs (RoA original: 0.994 {+/-} 0.005; RoA CRD: 0.992 {+/-} 0.009). In public datasets, yield increases ranged from 35-142% per muscle in the first iteration. Correspondingly, the explained signal power ratio increased, with the first iteration accounting for most gains. A second CRD iteration resulted in an additional, yet smaller yield increase (0-26.7%). Additionally identified MUs had smaller action potential amplitudes and lower recruitment thresholds, indicating the recovery of smaller, lower-threshold MUs.

CRD reliably increased MU yield and explained signal power across diverse muscles, datasets, and decomposition implementations. The approach provides an optional, validated step for more complete decomposition results across the full recruitment range in offline analyses.