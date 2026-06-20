---
title: Validation of Dynamic Bayesian Optimization for Human-in-the-Loop Optimization of Exoskeleton Control at User-Driven Walking Speed
title_zh: 基于用户驱动步行速度的外骨骼控制人在环路优化中动态贝叶斯优化的验证
authors: "Kim, G., Sergi, F."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731447v1.full.pdf"
tags: ["query:sports-sci"]
score: 6.0
evidence: 验证动态贝叶斯优化用于个性化外骨骼控制以提高步行速度。
tldr: 人在环优化（HILO）为外骨骼个性化控制提供了方法，但人体对辅助的响应往往随时间改变，传统贝叶斯优化（BO）难以建模这种非平稳性。本研究提出动态贝叶斯优化（DBO），通过纳入时间动态来适应响应变化。在16名健康受试者的行走速度提升任务中，利用髋部外骨骼施加双侧扭矩脉冲，对三个扭矩参数进行在线优化。通过设置验证迭代比较DBO和BO，结果显示DBO在四项验证中的三项使行走速度显著提高，后期建模准确度更高，且个体化参数效果优于历史方案。DBO能更有效地应对人体响应非平稳性，为康复外骨骼实时优化提供了新思路。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统HILO假设人体响应平稳，而实际行走中辅助效果随时间变化，需一种能适应非平稳响应的优化方法。
method: 采用动态贝叶斯优化（DBO）对16名健康受试者的髋部外骨骼扭矩三参数进行在线优化，通过设定验证迭代与BO对比。
result: DBO在大多数验证迭代中使行走速度相较于基线提升更高，建模准确度在后期优于BO，且个性化参数变化显著大于历史最优方案。
conclusion: DBO通过适应人体响应非平稳性，在优化行走速度上优于BO，为康复外骨骼的实时自适应控制提供了更优策略。
---

## 摘要
人在环路优化（HILO）是一种用于识别特定受试者最优控制器以增强性能的成熟方法。然而，要使HILO算法在康复中发挥作用，优化算法可能需要考虑人类响应随时间在辅助下的变化情况。

在本研究中，我们测试了一种改进版的贝叶斯优化（BO），即动态贝叶斯优化（DBO），针对一个三参数优化问题，旨在找出针对个体提高步行速度的最优解。与BO不同，DBO考虑了人类响应的非平稳性。16名健康参与者接受了由髋部外骨骼提供的双侧髋部扭矩脉冲。外骨骼扭矩参数通过使用DBO或BO的HILO确定。我们在HILO的不同时间点引入了验证迭代，以客观比较不同优化器的性能。

结果表明，与基线相比，DBO和BO都显著提高了步行速度。在比较DBO和BO的性能时，DBO在效能、建模准确性和个性化方面均优于BO。在四个验证迭代中的三个中，DBO引起的步行速度相对于基线的变化超过了BO引起的变化。DBO在后期验证迭代中的建模准确性优于BO。DBO的个性化所诱导的步行速度变化显著大于先前识别的辅助方案所诱导的变化，而BO则未达到这一点。总体而言，我们的结果表明，由于DBO更能考虑人类响应的非平稳方面，因此其性能优于BO。

## Abstract
Human-in-the-loop optimization (HILO) is an established method for identifying subject-specific optimal controllers for performance augmentation. For HILO algorithms to be useful in rehabilitation, however, the optimization algorithm may need to account for how the human response changes over time in response to assistance.

In this study, we tested a modified version of Bayesian optimization (BO), dynamic Bayesian optimization (DBO), in a three-parameter optimization problem that sought to identify participant-specific optimal solutions for increasing walking speed. As opposed to BO, DBO accounts for the non-stationarity of human responses. Sixteen healthy participants received bilateral hip torque pulses delivered by a hip exoskeleton. The exoskeleton torque parameters were determined using HILO with either DBO or BO. Validation iterations were introduced to objectively compare performance across optimizers at different time points of HILO.

The results showed that both DBO and BO significantly increased walking speed compared to baseline. When comparing performance between DBO and BO, DBO emerged as an improvement over BO both in terms of efficacy, modeling accuracy, and personalization. DBO induced changes in walking speed relative to baseline that exceeded those induced by BO at three of the four validation iterations. DBO outperformed BO in modeling accuracy in later validation iterations. DBO personalization induced changes in walking speed that were significantly greater than those induced by previously identified assistive solutions, while this was not the case of BO. Overall, our results indicate that DBO outperformed BO due to its greater ability to account for non-stationary aspects of the human response.