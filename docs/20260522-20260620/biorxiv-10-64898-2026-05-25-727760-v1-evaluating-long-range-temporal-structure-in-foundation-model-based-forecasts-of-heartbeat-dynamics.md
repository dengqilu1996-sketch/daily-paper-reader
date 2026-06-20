---
title: Evaluating Long-Range Temporal Structure in Foundation Model-Based Forecasts of Heartbeat Dynamics
title_zh: 评估基于基础模型的心跳动力学预测中的长程时间结构
authors: "Serapio, A., Ramsundar, B., Subramanian, S."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.727760v1.full.pdf"
tags: ["query:sport-tsa"]
score: 7.0
evidence: 评估心跳动力学预测中的长程时间结构
tldr: 当前时间序列基础模型（TSFMs）在心跳动力学预测中的应用逐渐兴起，但其长期时序结构捕捉能力尚未充分验证。本研究基于MIT-BIH正常窦性心律数据库，评估多种TSFMs的R-R间期预测性能，重点分析预测误差随预测时长的演化规律。实验发现，现有模型均无法准确捕获心跳序列的长程依赖，远期预测误差显著增大。该工作揭示了TSFMs在心电时序预测中的关键局限，为后续模型设计和基准测试提供了开放性平台与代码。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究TSFMs在心跳序列预测中是否准确刻画长程时间依赖，弥补现有评估空白。
method: 在MIT-BIH正常窦性心律数据库上，对多个TSFMs进行R-R间期多步预测，分析预测误差随预测步长增长的变化。
result: 结果表明所有TSFMs均未能准确建模长期依赖，R-R间期预测误差随预测时长显著增长。
conclusion: 揭示了TSFMs在捕捉心跳动力学长期时序结构上的不足，为心电预测基准建立和模型优化提供开源代码。
---

## 摘要
我们利用MIT-BIH正常窦性心律数据库（NSRDB）研究了时间序列基础模型（TSFMs）对心跳动力学预测的长程时间结构。我们的发现表明，这些模型未能充分捕捉长程依赖关系，这体现在更长的预测视野下RR间期预测误差不断增大。代码见https://github.com/SubramanianLab/ecg-tsfm-benchmark。

## Abstract
We examine the long-range temporal structure of forecasts produced by Time-Series Foundation Models (TSFMs) on heartbeat dynamics using the MIT-BIH Normal Sinus Rhythm Database (NSRDB). Our findings indicate that these models do not adequately capture long-range dependencies, as reflected in growing errors in RR-interval predictions over longer forecast horizons. Code is available at https://github.com/SubramanianLab/ecg-tsfm-benchmark.