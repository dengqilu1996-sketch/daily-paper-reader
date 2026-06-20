---
title: An end-to-end platform for pose estimation and real-time edge-AI deployment
title_zh: 一个用于姿态估计和实时边缘AI部署的端到端平台
authors: "Haggerty, D. L., Darden, C. B., Lovinger, D. M."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.24.700912v2.full.pdf"
tags: ["query:cv-sports"]
score: 6.0
evidence: 姿态估计与边缘AI部署的端到端平台
tldr: 针对现有姿势估计工具依赖工作站GPU、难以实时边缘部署的问题，研发了SqueakPose Studio软件套件和SqueakView、MouseHouse边缘硬件平台。平台采用现代目标检测架构实现端到端训练，无需分块后处理，在嵌入式设备上支持实时姿势估计。该统一平台覆盖数据集创建、模型训练、离线分析与实时实验全流程，降低了对高端硬件的依赖。该平台无缝连接离线分析和实时部署，无需外部中间件或工作站GPU，为行为定量分析提供了低门槛、高灵活性的完整方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有深度学习姿势估计工具依赖工作站GPU和离线工作流，难以在嵌入式设备上实现实时部署。
method: 提出SqueakPose Studio与SqueakView、MouseHouse软硬件平台，采用现代目标检测架构实现端到端训练，覆盖数据创建至边缘部署。
result: 在嵌入式设备上实现实时姿势估计，无需工作站GPU或外部中间件，且支持CPU、GPU和Apple Silicon。
conclusion: SqueakPose平台实现了从离线分析到边缘实时部署的无缝衔接，摆脱了对高端硬件的依赖，为行为定量分析提供了高效、灵活的解决方案。
---

## 摘要
准确姿态估计是行为定量分析的基础，但许多基于深度学习的跟踪工具仍优化为离线工作流程，依赖于碎片化的软件管道、工作站级GPU或外部中间件以实现实时部署。本文介绍了一个集成的软硬件生态系统，用于姿态估计，涵盖数据集创建、模型训练、离线分析以及在嵌入式边缘计算设备上的实时部署。SqueakPose Studio提供了一个基于全帧深度学习的姿态估计软件套件，统一了数据集创建、手动和模型辅助标注、模型训练、验证和大规模离线推理。该系统利用现代目标检测架构，实现高效的端到端训练和推理，无需基于补丁的采样或多阶段后处理，并支持在CPU、GPU和Apple Silicon上执行。对于需要连续记录和同步数据采集的实验设置，SqueakView可在嵌入式边缘计算硬件上实现实时模型部署、视频捕获和传感器记录，而MouseHouse则提供了一个紧凑的模块化外壳，专为基于家笼的实验设计，集成了嵌入式GPU计算、基于微控制器的时序和外设I/O。共享的数据格式和确定性时序架构确保了离线分析和实时部署之间的一致性。总之，SqueakPose Studio、SqueakView和MouseHouse提供了一个统一的姿态估计平台，支持传统的离线分析和嵌入式实时实验，无需依赖工作站级硬件或外部中间件。

## Abstract
Accurate pose estimation underpins quantitative analysis of behavior, yet many deep learning-based tracking tools remain optimized for offline workflows that rely on fragmented software pipelines, workstation-grade GPUs, or external middleware to enable real-time deployment. Here we present an integrated software-hardware ecosystem for pose estimation that spans dataset creation, model training, offline analysis, and real-time deployment on embedded edge-computing devices. SqueakPose Studio provides a software suite for whole-frame, deep learning-based pose estimation that unifies dataset creation, manual and model-assisted labeling, model training, validation, and large-scale offline inference. The system leverages modern object-detection architectures to enable efficient end-to-end training and inference without patch-based sampling or multi-stage postprocessing, and supports execution on CPUs, GPUs, and Apple Silicon. For experimental settings requiring continuous recording and synchronized data acquisition, SqueakView enables real-time model deployment, video capture, and sensor logging on embedded edge-computing hardware, while MouseHouse provides a compact, modular enclosure designed for home cage-based experiments that integrates embedded GPU compute, microcontroller-based timing, and peripheral I/O. A shared data format and deterministic timing architecture ensure consistency across offline analysis and real-time deployment. Together, SqueakPose Studio, SqueakView, and MouseHouse provide a unified platform for pose estimation that supports both conventional offline analysis and embedded, real-time experimentation, without reliance on workstation-grade hardware or external middleware.