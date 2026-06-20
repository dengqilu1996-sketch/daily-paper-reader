---
title: Optimization of Functional Electric Stimulation for Foot Drop Patients using Inertial Measurement Unit.
title_zh: 基于惯性测量单元的功能性电刺激优化足下垂患者步态
authors: "Shahzaib, M., Shaikh, U., Shakil, S., Jangsher, S."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732030v1.full.pdf"
tags: ["query:sport-tsa"]
score: 7.0
evidence: 基于IMU的步态阶段检测优化FES以纠正病理步态
tldr: 足下垂患者因腓肠肌无力导致步态异常，需功能性电刺激(FES)辅助行走，但刺激强度难以个性化优化。本文设计基于惯性测量单元(IMU)的闭环反馈控制系统，通过采集8名健康人的步态数据构建参考模板，在线识别步态相并实时调整FES强度。仿真实验证实，该方法能可靠地纠正模拟患者的病理步态，使之接近正常模板。该研究提出了一种数据驱动的FES优化策略，为足下垂康复治疗提供了新思路。
source: biorxiv
selection_source: fresh_fetch
motivation: 足下垂患者步态异常，现有FES刺激强度难以个性化调节，影响康复效果。
method: 设计基于IMU的闭环反馈系统，采集健康人步态构建模板，在线识别步态相并调整FES强度。
result: 仿真实验表明，系统能纠正模拟足下垂患者的步态轨迹，使其接近正常参考模板。
conclusion: 提出数据驱动的FES优化方法，有望实现个性化实时调控，改善足下垂患者步态。
---

## 摘要
许多足下垂综合征患者在行走时面临困难，导致病理性步态。这种综合征通过一种称为功能性电刺激器的外部人工刺激进行治疗。本文设计了一种在线反馈控制系统，优化施加于麻痹肌肉的功能性电刺激强度，使患者的病理性步态在可接受范围内得到纠正。利用安装在脚上的惯性测量单元作为反馈传感器，识别步态的不同阶段。从8名健康受试者收集数据，并使用数据平均值作为参考模板。由于患者不可得，模拟了足下垂患者的不同轨迹，并根据参考模板进行校正。

## Abstract
Many people which are affected by drop foot syndrome, have to face difficulty while walking which leads to pathological gait. This type of syndrome is treated by means of an external artificial stimulation known as functional electric stimulator (FES). In this paper we are designing an online feedback control system which optimize the strength of a FES given to paretic muscle which results in correction of pathological gait of the patient in a tolerable domain. Different phases of gait are identified using inertial measurement unit (IMU) as a feedback sensor mounted on the foot. Data is collected form 8 different healthy subjects and average of collected data is used as a reference template. Different trajectories of drop foot patients are simulated (due to unavailability of patients) and corrected according to the reference template.