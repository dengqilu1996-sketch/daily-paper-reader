---
title: A time-dependent mechano-bioenergetics model of muscle contraction
title_zh: 肌肉收缩的时间依赖性力学-生物能量学模型
authors: "Konno, R. N., Lichtwark, G. A., Dick, T. J. M."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.734405v1.full.pdf"
tags: ["query:sport-sci"]
score: 9.0
evidence: 模拟运动过程中肌肉能量消耗
tldr: 现有肌肉能量消耗模型忽视时间依赖性ATP恢复成本，难以准确预测周期性运动如行走时的肌肉能量反应。本研究基于钙运输、横桥循环和ATP再生过程，提出时间依赖性机械-生物能量学模型，参数来自离体肌肉数据。模型成功预测动态、次最大和抽搐收缩下的能量速率，捕捉收缩频率对峰值速率的影响及恢复时间进程。该模型以最少自由参数和低计算成本实现跨肌肉和物种推广，可集成于大规模骨骼肌模拟。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有模型忽略时间依赖性ATP再生恢复成本，无法准确预测周期性运动中的肌肉能量消耗。
method: 整合钙运输、横桥循环和ATP再生，建立时间依赖性模型，参数来自离体肌肉实验，覆盖动态、次最大和抽搐收缩条件。
result: 模型成功预测多种收缩条件下的能量速率，并捕捉收缩频率对峰值速率的影响以及ATP恢复的时间进程。
conclusion: 模型以最少自由参数和低计算成本捕获关键生理过程，可跨肌肉和物种推广，适用于大规模肌肉骨骼模拟。
---

## 摘要
在不同肌肉收缩条件下预测骨骼肌能量消耗对于增进我们对运动的理解至关重要。现有的数学模型虽然捕捉了能量消耗过程的力学依赖性，但忽略了与ATP再生相关的时间依赖性行为和恢复成本。这种时间依赖性对于预测肌肉在重复或周期性任务（如运动，其中肌肉经历多次收缩循环）中的能量反应非常重要。本研究提出了一个新模型，基于生理过程预测能量速率：Ca2+运输成本、横桥循环成本和ATP再生。先前的数学模型包含了Ca2+运输和横桥循环的依赖性，但忽略了收缩后的时间依赖性反应及随后的ATP恢复。模型参数从现有的离体肌肉制剂数据中获得，预测的能量速率在包括动态、次最大和抽搐收缩在内的多种收缩条件下的独立数据集上进行了验证。该时间依赖性模型能够捕捉收缩频率对峰值能量速率的影响以及实验观察到的能量恢复时间过程。该模型捕获了关键的生理过程，同时保持了最少的自由参数和低计算成本。这使得该模型能够跨肌肉和物种推广，并可整合到更大规模的肌肉骨骼模型中。

## Abstract
Predictions of skeletal muscle energy consumption under a diverse range of muscle contractile conditions are critical for improving our understanding of locomotion. Existing mathematical models, while capturing the mechanical dependence of energy consuming processes, neglect the time-dependent behaviour and recovery costs associated with regenerating ATP. This time-dependence is important for predicting the energetic response of muscles during repetitive or cyclical tasks like locomotion, where muscle undergoes many contraction cycles. This study presents a novel model to predict energetic rates based on physiological processes: Ca2+ transport costs, cross-bridge cycling costs, and ATP regeneration. Previous mathematical models include the dependence on Ca2+ transport and cross-bridge cycling, but neglect the time-dependent response and the subsequent recovery of ATP following the contraction. Model parameters were obtained from existing data on isolated muscle preparations, and predicted energetic rates were validated on separate datasets across a range of contractile conditions including dynamic, sub-maximal, and twitch contractions. The time-dependent model was able to capture the influence of contraction frequency on peak energetic rates and the time-course of energetic recovery observed experimentally. The model captures key physiological processes while maintaining a minimal number of free parameters and low computational cost. This enables generalisability across muscles and species, and implementation into larger scale musculoskeletal models.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：骨骼肌能量消耗的准确预测对理解运动（如行走、跑步）至关重要。肌肉在周期性运动中经历反复收缩，能量供应依赖 ATP 的即时消耗与后续再生，但现有模型（如 Konno et al., 2025; Lichtwark & Wilson, 2005）多只关注力学状态对能量消耗的瞬时影响，忽略了与 ATP 再生相关的时间依赖性恢复成本及其热释放。
- **核心问题**：缺乏一个能够同时描述 **Ca²⁺ 运输、横桥循环** 等初始耗能过程，以及 **ATP 再生（氧化磷酸化）** 这一时间依赖恢复过程的统一数学模型，导致无法准确模拟反复收缩或变频收缩下的能量动力学。
- **整体含义**：本研究提出一个 **时间依赖性力学‑生物能量学模型**，将初始耗能与随后的代谢恢复过程耦合，旨在以最少自由参数和低计算成本捕捉肌肉能量使用的时间历程，并可在不同肌肉类型、物种间推广，最终整合进全身肌肉骨骼模型。

### 2. 方法论
模型由四个串联的子模块构成，输入为刺激信号，输出为总能量速率及其组分：

- **兴奋‑激活模型**：用简化的钙动力学方程描述刺激引起的 Ca²⁺ 释放、与肌钙蛋白的结合（激活程度 ∝ [CaTn]）以及刺激结束后的 Ca²⁺ 回收（不受力依赖）。关键方程：
  - 胞质游离 Ca²⁺ 浓度变化率 ˙cca 在刺激期和非刺激期由不同时间常数 τact 和 τdeact 控制。
  - 肌钙蛋白结合 Ca²⁺ 比例 ccatn 通过 Hill 型方程由 cca 计算。
- **力学模型**：采用标准 Hill 型肌肉模型，根据激活量 ˆa ≈ ccatn 计算肌肉应变 εce、应变率 ˙εce 和肌力 ˆFm。力由收缩元主动力‑长度、主动力‑速度关系以及并联弹性元被动张力叠加得到。
- **初始能量学模型**：直接基于 Ca²⁺ 运输和横桥循环的生理过程计算初始热。
  - 等长横桥热速率 ˙qcxb,0 正比于 rcxb · ccatn^scxb，再用力‑长度关系缩放得 ˙qcxb。
  - Ca²⁺ 运输热速率 ˙qcat 仅在 Ca²⁺ 被泵回肌质网时（˙cca < 0）按比例 rcat 产生。
  - 机械热速率 ˙qmech 在缩短时正比于 rshort · ccatn · ˆFce,l(εce) · ˙εce（缩短热），在伸长时等于负的肌肉功速率。
  - 总初始能量速率 ˙Einit = ˙qcxb + ˙qcat + ˙qmech + ˙w。
- **生物能量学模型**：接收 ˙Einit，模拟 ATP 消耗与氧化恢复。
  - ATP 消耗通量 ϕATP = ˙Einit/ΔGATP + krest·catp（ΔGATP ≈ 60 kJ/mol）。
  - 微分方程组描述 ATP、PCr 的动态平衡：˙catp = −ϕATP + ϕox + ϕCK，˙cpcr = −ϕCK，并保证总腺苷酸和总肌酸守恒。
  - 氧化磷酸化通量 ϕox 采用 Hill 型动力学，依赖 ADP 浓度；肌酸激酶通量 ϕCK 采用 Vicini & Kushmerick (2000) 的公式。
  - 恢复过程伴生的热速率 ˙qrec = rrec(ϕox − ϕrest)。

参数通过分步优化获得：兴奋‑激活参数采用文献值；力学参数参考 Dick et al. (2017) 并微调最大缩短速度；初始能量学参数通过最小化包含恒温横桥热比例、Ca²⁺运输热比例、缩短机械依赖以及不同刺激频率下 Ca²⁺ 热比的目标函数获得；生物能量学参数（rrec, nox, ϕox,max）通过对小鼠比目鱼肌循环收缩恢复热数据的拟合确定，并依据温度系数进行校正。

### 3. 实验设计与验证
模型训练和验证均基于已发表的离体肌肉实验数据，未与其他现有模型进行定量对比，而是直接与实验观测值比较。

- **训练数据**：
  - 初始能量学参数：小鼠比目鱼肌（SOL）和趾长伸肌（EDL）在不同缩短速度下的能量速率数据（Barclay et al., 2010）。
  - 生物能量学参数：小鼠 SOL 在 20°C 下反复等长收缩的恢复热时间过程（Barclay et al., 1995）。
- **验证数据（独立于训练）**：
  - **动态循环收缩**：Barclay & Weber (2004)，SOL 和 EDL 在不同频率（0.5‑4 Hz）下的缩短‑舒张实验，比较总能量时间历程、恢复时间常数 τr、初始效率 εinit、总效率 εtot 以及恢复/初始热比 R。
  - **氧耗恢复时间**：Mast & Elzinga (1987)，兔乳头肌在 20°C 下连续抽搐后的氧消耗恢复时间常数（使用 SOL 参数）。
  - **次最大激活**：Lewis & Barclay (2014)，不同刺激频率（40‑160 Hz）下的总能量消耗。
  - **双次抽搐 Ca²⁺ 热**：Barclay (2012)，两次抽搐中第二次抽搐相对于第一次的 Ca²⁺ 运输热百分比。
  - **抽搐恢复热比**：Mast & Elzinga (1988)，兔乳头肌连续抽搐后的恢复/初始热比 R。
- **对比基准**：实验测量的能量速率、效率、恢复时间常数和能量比率。文中虽未直接与其他模型定量对比，但指出其前身模型（Konno et al., 2025）会在变频刺激下给出与实验趋势相反的预测。

### 4. 资源与算力
- **计算资源**：文中未提及任何 GPU、服务器算力或训练时长。模型为常微分方程组，参数优化采用非线性最小二乘法，计算量极小，可在普通 CPU 上快速完成，不需要高性能计算设施。

### 5. 实验数量与充分性
- **实验组别**：
  - 两种纤维类型的参数独立优化（SOL 与 EDL）。
  - 生物能量学参数基于 SOL 优化，直接应用于 EDL。
  - 验证覆盖 5 组独立的实验数据集，涉及 4 种不同的肌肉类型（小鼠 SOL、EDL；兔乳头肌），测试了从抽搐、次最大到强直、从等长到动态缩短的多种收缩模式，以及不同的恢复测量方法（肌热、氧耗）。
  - 进行了必要的温度校正和比例校正，使参数在不同实验条件下合理。
- **充分性与客观性**：实验设计较为系统，使用不同物种、不同实验方案和不同终端测量指标，体现了多角度的交叉验证。但验证集部分实验的温度和测量方式与训练集不同，校正过程依赖文献值，可能引入主观性。缺少对人体或其他大型哺乳动物数据的评估，也缺少与其他能耗模型的直接比较。

### 6. 主要结论与发现
- 模型成功捕捉了不同收缩频率下总能量使用的时间过程，包括收缩期间的初始耗能和收缩后的缓慢恢复热。
- 预测的恢复时间常数（τr）与实验值偏差在 5%–20% 以内；初始效率和总效率的差异方向与实验一致（SOL > EDL）；恢复/初始热比 R 略高于实验值，但趋势正确。
- 模型正确再现了 Ca²⁺ 运输热随刺激间隔缩短而减少的现象，而忽略时间依赖的旧模型无法做到这一点。
- 该模型仅需少量自由参数，计算成本低，有利于在更大规模肌肉骨骼模拟中推广。

### 7. 优点
- **生理真实度高**：首次将 Ca²⁺ 运输热直接与 Ca²⁺ 清除速率挂钩，而非仅依赖激活水平；将 ATP 消耗与氧化再生动态耦合，同时计入再生过程的产热。
- **时间依赖性捕捉**：能准确反映收缩频率对峰值能量速率及恢复时间过程的影响，特别适用于周期性运动模拟。
- **参数简洁且可推广**：参数具有明确的生理含义，可依据纤维类型和物种进行调整，为整合到全身模型提供了可能。
- **验证广泛**：在多个独立数据集、不同收缩形式和测量指标下进行了验证，增强了模型可信度。

### 8. 不足与局限
- **恢复参数的同质性**：生物能量学参数仅使用慢肌（SOL）数据优化，并直接应用于快肌（EDL），可能导致快肌恢复热预测的系统偏差（文中观察到 EDL 总效率略低于实验）。
- **未考虑无氧代谢**：忽略糖酵解及其对 pH 的影响，在短时高强度、缺血或疲劳状态下的适用性受限。
- **恢复热比率高估**：模拟中 R 值常大于 1，高于部分实验值，说明恢复热常数 rrec 可能仍需进一步校准。
- **数据温度依赖性处理**：生物能量学模型训练基于 20°C 数据，后通过温度系数放大至 35°C 应用，恢复时间常数验证的独立性有所降低。
- **缺少与其他模型的量化对比**：只在讨论中与 Konno et al. (2025) 的简单趋势比较，未提供全面定量的基准 benchmark，难以判断相对改进幅度。
- **验证范围**：主要基于小鼠和兔的小肌束实验，尚未在人体或整体运动水平进行验证，应用到临床或运动科学尚需进一步检验。
- **简化假设**：激活‑钙动力学模型简化了肌质网 Ca²⁺ 释放与回收的复杂过程，可能在高频刺激或非稳态下有偏差。

（完）
