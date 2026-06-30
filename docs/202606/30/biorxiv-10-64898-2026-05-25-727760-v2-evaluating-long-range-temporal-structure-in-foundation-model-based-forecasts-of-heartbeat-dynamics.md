---
title: Evaluating Long-Range Temporal Structure in Foundation Model-Based Forecasts of Heartbeat Dynamics
title_zh: 评估基于基础模型的心跳动力学预测中的长程时序结构
authors: "Serapio, A., Ramsundar, B., Subramanian, S."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.727760v2.full.pdf"
tags: ["query:sport-tsa"]
score: 7.0
evidence: 评估基础模型在预测RR间期心跳动态中的表现
tldr: 时间序列基础模型在生理信号预测任务中日益受到关注，但其能否捕捉心跳动力学的长期依赖结构尚不明确。本研究利用MIT-BIH正常窦性心率数据库，系统评估了TSFM预测的长期时间结构。实验发现，现有模型未能有效建模RR间隔的长程依赖，预测误差随预测视野延长而急剧上升。该发现揭露了基础模型在生理时间序列预测中的关键短板，为未来模型设计与评估提供了重要方向。
source: biorxiv
selection_source: fresh_fetch
motivation: 检验时间序列基础模型在心跳动力学预测中是否具备捕捉长程依赖的能力，评估其临床可靠性。
method: 基于MIT-BIH正常窦性心率数据库，分析TSFM在RR间隔预测中的长期误差增长，评估时间结构捕获能力。
result: TSFM未能有效捕捉RR间隔的长程依赖，预测误差随预测视野延长而显著增大，长期结构建模不足。
conclusion: 现有时间序列基础模型无法充分建模心跳动力学的长程依赖，需改进模型以更好地适应生理时间序列的长期预测需求。
---

## 摘要
我们利用MIT-BIH正常窦性心律数据库（NSRDB），检测了时间序列基础模型（TSFMs）在心跳动力学上生成的预测的长程时序结构。研究结果表明，这些模型未能充分捕捉长程依赖性，表现为在更长预测范围内RR间期预测的误差逐渐增大。

## Abstract
We examine the long-range temporal structure of forecasts produced by Time-Series Foundation Models (TSFMs) on heartbeat dynamics using the MIT-BIH Normal Sinus Rhythm Database (NSRDB). Our findings indicate that these models do not adequately capture long-range dependencies, as reflected in growing errors in RR-interval predictions over longer forecast horizons.