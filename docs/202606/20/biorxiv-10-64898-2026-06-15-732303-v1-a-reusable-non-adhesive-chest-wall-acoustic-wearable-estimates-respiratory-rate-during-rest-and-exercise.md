---
title: A Reusable Non-Adhesive Chest-Wall Acoustic Wearable Estimates Respiratory Rate During Rest and Exercise
title_zh: 一种可重复使用的非粘性胸壁声学可穿戴设备在静息和运动期间估算呼吸率
authors: "Haxel, L., Schroff, A., Fennell, C., Dickinson, J. W."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732303v1.full.pdf"
tags: ["query:sport-tsa"]
score: 9.0
evidence: 评估可穿戴声学胸部传感器在静息和运动中监测呼吸率
tldr: "呼吸率是重要的生理信号，但现有可穿戴设备在非安静状态下难以连续直接监测，常依赖间接替代指标或皮肤粘附。本研究评估了Alveos One磁力纺织可穿戴设备，通过胸壁声学和惯性传感直接捕捉呼吸运动。在20名健康成人中，休息及控制呼吸任务下94.6%的窗口估计误差小于2次/分钟，运动任务下为79.3%，偏差仅为0.24和-1.07次/分钟。结果支持非粘附、可重复使用的胸壁声学传感作为纵向呼吸率监测的可行方案，并揭示了运动强度与通气需求是主要限制。"
source: biorxiv
selection_source: fresh_fetch
motivation: 呼吸率连续监测对临床与行为评估至关重要，但缺少摆脱皮肤粘附且适用于日常活动的直接胸壁传感手段。
method: 采用Alveos One磁力通过纺织品的胸壁可穿戴设备，结合声学与惯性传感，在20名健康受试者的休息、控制呼吸及运动中，与光电容积描记、肺量计等参考同步记录。
result: "在休息和控制呼吸下94.6%有效窗口的呼吸率估计误差在2次/分钟内，运动下为79.3%；Bland–Altman偏差分别为0.24和-1.07次/分钟。"
conclusion: 非粘附胸壁声学传感可支撑长期呼吸率监测，但高强度运动和高通气需求限制了报告的自信度。
---

## 摘要
呼吸率是一种具有临床和行为信息价值的信号，但在安静休息之外的连续监测仍很困难。可穿戴系统通常通过心血管或运动替代指标间接推断呼吸，而直接的胸壁感知通常依赖于皮肤粘附或受控实验室条件。我们评估了Alveos One，一种体耦合声学和惯性胸壁可穿戴设备，以测试一种通过织物磁吸的可重复使用形态是否能在静息、受控呼吸、运动任务和分级运动期间估算呼吸率。在单次会话方案中，我们分析了20名健康成年人的记录，以结构光体积描记法、逐次呼吸肺活量测定法和节拍呼吸目标作为参考。在静息和受控呼吸期间，94.6%的有效窗口内估算值在参考值的2次呼吸/分钟以内，运动期间为79.3%；静息和受控呼吸期间的Bland-Altman偏倚为0.24次呼吸/分钟，运动期间为-1.07次呼吸/分钟。二次分析比较了磁吸配置与皮肤粘附贴片，并评估了气道模式分类和运动相关操作限制。这些发现支持可重复使用的非粘性胸壁声学感知作为纵向呼吸率监测的实用途径，并指出增加的运动强度和高通气需求是可靠报告的主要限制。

## Abstract
Respiratory rate is a clinically and behaviourally informative signal, yet continuous monitoring outside quiet rest remains difficult. Wearable systems often infer breathing indirectly from cardiovascular or motion surrogates, while direct chest-wall sensing has typically depended on skin adhesion or controlled laboratory conditions. We evaluated Alveos One, a body-coupled acoustic and inertial chest-wall wearable, to test whether a reusable magnet-through-textile form factor can estimate respiratory rate across rest, controlled breathing, motion tasks, and graded exercise. In a single-session protocol, we analysed recordings from 20 healthy adults referenced to structured light plethysmography, breath-by-breath spirometry, and paced-breathing targets. Estimates fell within 2 breaths/min of the reference for 94.6% of valid windows during rest and controlled breathing and 79.3% during exercise; Bland--Altman bias was 0.24 breaths/min during rest and controlled breathing and -1.07 breaths/min during exercise. Secondary analyses compared the magnet configuration with a skin-adhered patch and assessed airway-mode classification and motion-related operating limits. These findings support reusable, non-adhesive chest-wall acoustic sensing as a practical route to longitudinal respiratory-rate monitoring, and identify rising motion intensity and high ventilatory demand as the principal limits on confident reporting.

---

## 论文详细总结（自动生成）

# 论文总结：一种可重复使用的非粘性胸壁声学可穿戴设备在静息和运动期间估算呼吸率

## 1. 核心问题与整体含义
- **研究动机**：呼吸率是一个具有重要临床和行为评估价值的生理信号，但现有可穿戴技术在安静休息以外的日常活动中难以进行可靠的连续、直接监测。
- **现存痛点**：多数系统依赖心血管信号或运动信号的间接推断，无法直接感知胸壁的运动；而能直接感知胸壁的方案又通常需要皮肤粘附或受控实验室条件，不适合长期、自然状态下的纵向监测。
- **整体含义**：该研究旨在验证一种摆脱粘附、可重复使用、能“穿在衣服外”直接捕捉胸壁运动的声学‑惯性传感方案，为日常连续呼吸监测提供一个实用化路线。

## 2. 方法论
- **核心思想**：将微型声学传感器与惯性传感器集成于可穿戴设备（Alveos One），通过织物上的磁吸方式固定在胸壁位置，直接拾取呼吸运动引起的胸廓振动和运动信号，进而从中估算呼吸率。
- **关键技术细节**：
  - **传感原理**：融合身体耦合声学信号（胸壁振动声音）与惯性运动信号，捕捉与呼吸节律相关的幅度与频率特征。
  - **形态与穿戴方式**：传感器模块采用磁力吸附，通过日常衣物（无需直接接触皮肤）与胸壁耦合，实现可重复使用和非粘性佩戴。
  - **信号处理与估算流程**（摘要未详细展开，据方法描述推断）：对声学/惯性信号进行窗口化处理，提取与呼吸相关的周期性成分，经滤波、峰值检测或频谱分析后输出实时呼吸率估计值，并与参考设备同步对比验证。
- **无显式公式说明**：文中未给出具体数学公式或算法流程图，仅概括为利用声学和惯性数据进行呼吸率估计。

## 3. 实验设计
- **受试者与数据来源**：20名健康成年人，单次实验会话中采集数据。
- **测试场景**：覆盖四种状态——静息、受控节拍呼吸、特定运动任务、分级递增运动。
- **参考标准（Benchmark）**：
  - 结构光体积描记法 (structured light plethysmography)
  - 逐次呼吸肺活量测定法 (breath‑by‑breath spirometry)
  - 节拍呼吸目标 (paced‑breathing targets)
- **对比方法**：并未与多个不同设备或算法直接对比，但进行了**二次分析**，比较了磁吸通过织物的配置与皮肤粘胶贴片配置的性能差异，同时评估了气道模式分类能力及运动相关的操作极限。

## 4. 资源与算力
- **文中未提及**任何关于 GPU 型号、数量、训练时长或计算资源使用的描述。因此无法提供算力总结。

## 5. 实验数量与充分性
- **实验组别**：在单次会话内划分了静息/受控呼吸与运动两大类条件，并进一步细分了不同运动强度和通气需求水平，同时做了磁吸配置与贴片的对比。可视为约3‑4类条件组合。
- **充分性评估**：
  - 样本量20人偏小，但涵盖多种呼吸模式和运动强度，条件设置较为全面。
  - 与临床金标准（肺量计）和光学参考装置同步比对，标准选择合理、客观。
  - 缺少长期纵向测试、多日重复穿戴的稳定性数据，也未见与其他商用可穿戴呼吸率产品的直接横向对比。
  - 总体而言，在证明概念可行性的层面实验设计尚可，但就普适性和鲁棒性验证而言仍不足。

## 6. 主要结论与发现
- **准确率**：
  - 静息与受控呼吸期间：94.6%的有效窗口中呼吸率估计误差在±2次/分钟以内。
  - 运动期间：79.3%的有效窗口满足相同误差阈值。
- **偏差**：
  - 静息/受控呼吸阶段的 Bland‑Altman 偏差为 0.24 次/分钟。
  - 运动阶段的偏差为 -1.07 次/分钟。
- **可行性确认**：可重复使用的非粘性胸壁声学传感被证明是纵向监测呼吸率的实用途径。
- **适用范围与限制**：运动强度增大和高通气需求是影响估算信心和可靠性的主要限制因素。气道模式分类可行，但性能受运动干扰影响。

## 7. 优点
- **摆脱皮肤粘附**：通过磁吸织物实现非粘性、可重复使用的穿戴，大幅提升长期佩戴的用户体验和卫生性。
- **直接胸壁感知**：不同于基于 ECG/PPG 的间接呼吸率估计算法，可从呼吸运动源头获取信号，避免心血管‑呼吸耦合误差和动作伪影。
- **多场景验证**：实验覆盖静息、控制呼吸、日常运动及递增负荷运动，比多数仅验证静态条件的可穿戴研究更贴近真实应用。
- **与金标准比对**：使用肺量计和结构光体积描记的高精度参考，增强了结论的可信度。
- **磁吸对比贴片分析**：提供了配置形态对性能影响的证据，为产品化设计提供参考。

## 8. 不足与局限
- **样本量小且人群单一**：仅20名健康成年人，未涉及不同年龄、性别、体型、肺部疾病患者，外推性有限。
- **运动强度下的性能衰减明显**：高强度运动和高通气时准确率下降（79.3% vs 94.6%），偏差也增大，尚未达到临床监测的黄金标准。
- **缺乏长期佩戴评估**：单次会话无法考察设备在长时间、多日连续穿戴中的稳定性、漂移、皮肤刺激或移位影响。
- **未与其他可穿戴设备直接对比**：不能体现相对市场上已有间接法设备的优势程度。
- **气道模式分类等附加功能描述简略**：其具体性能指标未充分报告，难以评估实际可用性。
- **算法细节未公开**：信号处理和呼吸率估计算法的透明度不够，无法判断是否存在过拟合或信号选择偏倚风险。

（完）
