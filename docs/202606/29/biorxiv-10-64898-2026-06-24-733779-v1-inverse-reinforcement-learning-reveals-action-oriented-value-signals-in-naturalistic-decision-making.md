---
title: Inverse reinforcement learning reveals action-oriented value signals in naturalistic decision making
title_zh: 逆强化学习揭示自然决策中面向行动的价值信号
authors: "Lee, S. H., Chung, C., Oh, M.-h., Ahn, W.-Y."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.733779v1.full.pdf"
tags: ["query:sports-rl"]
score: 6.0
evidence: 逆强化学习从行为推断价值信号，可迁移至体育策略和对手建模
tldr: 自然主义决策中，实时目标导向行为的价值计算是认知神经科学的挑战。传统计算模型成功应用于受控试次范式，但难以推广到自然行为。逆向强化学习（IRL）利用观察到的行为数据逆向求解潜在的奖励函数，然而其推导的奖励轨迹是否映射到大脑价值信号尚未可知。本研究在fMRI实时驾驶任务中，将IRL推导出的逐时奖赏与脑活动关联，发现奖赏轨迹稳健地激活背侧纹状体，同时也涉及认知控制与感觉运动相关脑区。这一结果表明IRL奖赏可捕捉以奖赏回路为核心的分布式神经活动，为自然决策提供了一种基于行为的、时间解析的评价代理，有助于理解真实世界决策的神经计算原理。
source: biorxiv
selection_source: fresh_fetch
motivation: 在自然决策场景，传统计算模型难以推广，逆向强化学习的神经可解释性尚不明确，需要验证其奖励信号是否与大脑价值表征一致。
method: 利用fMRI记录受试者实时驾驶任务中的脑活动，应用逆向强化学习（IRL）从行为推导逐时刻奖赏轨迹，并分析其与全脑活动的关联。
result: IRL导出的奖赏轨迹主要与背侧纹状体活动显著相关，并涉及前额叶等认知控制区和感觉运动皮层，呈现以奖赏回路为中心的模式。
conclusion: 逆向强化学习提供了一种行为驱动、时间解析的评价代理，可捕捉自然决策中面向行动的价值信号，为真实世界决策研究提供了新工具。
---

## 摘要
认知神经科学的一个主要挑战是解释在复杂和自然环境中如何计算目标导向行为的价值。标准决策计算模型在受控的、基于试次的范式中非常成功，但它们往往不适合自然范式中展开的实时行为。逆强化学习（IRL）提供了一种从自然环境中观察到的行为推断潜在评价状态的方法，但其神经可解释性仍然很大程度上未知。在这里，我们研究了在fMRI扫描期间执行的实时驾驶任务中，从IRL推导的即时奖励轨迹是否映射到大脑中的价值信号。IRL衍生的奖励轨迹与背侧纹状体的活动最为密切相关，该区域通常与价值导向的行动选择相关联。它们还显示出与支持其他过程的分布式区域有关联，包括认知控制和感觉运动处理。这种模式表明，IRL奖励捕获了以奖励回路为中心的分布式神经活动，可能反映了估值如何与其他过程相互作用。总之，这些发现表明，IRL奖励为自然决策过程中面向行动的估值提供了一个基于行为的、时间解析的代理。

## Abstract
A major challenge for cognitive neuroscience is to explain how value of a goal-directed behavior is computed in complex and naturalistic environments. Standard computational models of decision making have been highly successful in controlled, trial-based paradigms, but they are often ill-suited to real-time behavior unfolding in naturalistic paradigms. Inverse reinforcement learning (IRL) offers a way to infer latent evaluative state from observed behavior in naturalistic environments, but its neural interpretability remains largely unknown. Here, we investigated whether moment-to-moment reward trajectories derived from IRL map onto value signals in the brain during a real-time driving task performed during fMRI scanning. IRL-derived reward trajectories were most robustly associated with activity in the dorsal striatum, a region often linked to value-guided action selection. They also showed associations with distributed regions supporting additional processes, including cognitive control and sensorimotor processing. This pattern suggests that IRL reward captures distributed neural activity centered on the reward circuitry, potentially reflecting how valuation interacts with other processes. Together, these findings suggest that IRL reward provides a behaviorally grounded, temporally resolved proxy for action-oriented valuation during naturalistic decision making.