---
title: "Reliability-weighted target-position estimation in a musculoskeletal arm model: adaptive priors and learned source weighting under violations of fixed-precision assumptions"
title_zh: 肌肉骨骼手臂模型中的可靠性加权目标位置估计：违反固定精度假设下的自适应先验与学习源加权
authors: "Kobayashi, J."
date: 2026-06-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.08.730995v1.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 在MyoSuite肌骨手臂模型上进行贝叶斯线索整合，与感觉运动建模直接相关
tldr: 在肌肉骨骼模型中，可靠性加权整合在标准条件下足够，但先验或通道假设改变时性能下降。本研究在MyoSuite手臂模型上比较了精度加权与自适应先验及学习加权策略，发现自适应先验能跟踪目标均值漂移，学习的softmax整合器在校准偏差、重尾或相关误差时改进估计。结果定义了计算边界：精度加权在校准条件足够，假设违反时自适应或学习源加权变得有用，但当前证据限目标位置估计。
source: biorxiv
selection_source: carryover_cache
motivation: 明确可靠性加权在多传感器肌肉骨骼模型中的适用条件，特别是固定精度假设被违反时需要何种自适应或学习扩展。
method: 在MyoSuite手臂模型中构建场状架构，结合视觉、前向预测和先验，比较精度加权、自适应先验与学习softmax整合器的目标位置估计性能。
result: 学习的softmax整合器在通道误校准、偏置、重尾或相关误差时优于精度加权；自适应先验能跟踪均值漂移并降低对扩散目标的依赖。
conclusion: 精度加权在传感器校准良好时足够，但假设变化时自适应统计或学习源加权是必要的；该边界仍受限于目标估计，端点传播等问题未解决。
---

## 摘要
可靠性加权整合是线索组合的规范解释，但其在肌肉骨骼模型以及需要自适应或学习扩展条件下的适用范围尚不清楚。我们在MyoSuite手臂模型中，采用表示视觉、本体感觉、前向预测和任务先验的场式架构研究了目标位置估计。目标位置实验通过精度加权组合视觉、前向预测以及在适用时组合任务先验；本体感觉为其他状态场提供信息。在开环状态估计层面，一个可信但错误的先验随着视觉可靠性的降低，对目标估计的偏差增大，而一个错误的视觉线索在低噪声下被追随，在高噪声下被折扣；这两种效应都遵循偏差 ≈ w·偏移的模式。跨试次，自适应先验跟踪目标均值的漂移，而方差跟踪则随着目标散布的增加降低了先验权重。一个学习到的softmax积分器在校准的高斯合成观测通道上达到相对于精度加权的预设相等准则，并且在报告方差未校准或通道误差存在偏差、重尾或相关时改善了估计。在两个留出的MyoSuite rollout种子的目标位置观测上，在离线回放过程中，预测未校准和注入视觉离群值下的改善在种子间方向一致。离群值状态下的MSE收益反映了状态层面的源加权，而非一致的逐试次离群检测。这些结果定义了一个计算边界：在本文测试的校准条件下，精度加权已足够，而当假设改变或失效时，自适应统计或学习源加权变得有用。来自手臂模型的证据仅限于目标位置估计；末端传播仍未解决。

## Abstract
Reliability-weighted integration is a normative account of cue combination, but its scope in musculoskeletal models and conditions requiring adaptive or learned extensions remains unclear. We studied target-position estimation in a MyoSuite arm within a field-wise architecture representing vision, proprioception, forward prediction, and a task prior. Target-position experiments combined vision, forward prediction, and, where applicable, the task prior by precision weighting; proprioception informed other state fields. At the open-loop state-estimate level, a trusted but wrong prior biased the target estimate more as visual reliability decreased, and a false visual cue was followed under low noise and discounted under high noise; both effects followed the bias{approx} w {middle dot} offset pattern. Across trials, an adaptive prior tracked shifts in the target mean, while variance tracking reduced the prior weight as the target spread increased. A learned softmax integrator met the prespecified parity criterion relative to precision weighting for calibrated Gaussian synthetic observation channels and improved estimation when reported variance was miscalibrated, or channel errors were biased, heavy-tailed, or correlated. On target-position observations from two held-out MyoSuite rollout seeds, improvements under prediction miscalibration and injected visual outliers were directionally consistent across seeds during offline replay. The MSE benefit in the outlier regime reflected regime-level source weighting rather than consistent per-trial outlier detection. These results define a computational boundary: precision weighting was sufficient in the calibrated conditions tested here, whereas adaptive statistics or learned source weighting became useful when assumptions changed or failed. Evidence from the arm model is limited to target-position estimates; endpoint propagation remains unresolved.