---
title: Predicting Drosophila Body Orientation from a Translational Trajectory using an Artificial Neural Network
title_zh: 使用人工神经网络从平移轨迹预测果蝇身体朝向
authors: "Mangat, N., May, C. E., van Breugel, F."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.30.715335v2.full.pdf"
tags: ["query:sport-tsa"]
score: 7.0
evidence: 利用ANN从平动轨迹数据预测身体偏航方向，类似于从GPS轨迹估计运动员朝向
tldr: 在果蝇等昆虫飞行行为分析中，身体偏航朝向是理解导航策略的关键，但现有测量方法局限于小体积专用硬件，难以应用于大规模轨迹研究。本文训练全连接前馈人工神经网络，以轨迹的时延嵌入向量（包含地面速度、空速和推断推力）作为输入，直接估计身体偏航角。在2340条自由飞行轨迹上的测试显示，中位绝对角度误差仅约5°，可准确恢复−π到π全范围朝向。该数据驱动方法为仅记录质心运动的历史轨迹数据提供了朝向恢复工具，极大拓展了可分析的昆虫行为数据，推动计算神经行为学研究。
source: biorxiv
selection_source: fresh_fetch
motivation: 测量果蝇飞行身体偏航朝向通常需要专用硬件，限制了大规模轨迹数据分析。
method: 训练全连接前馈人工神经网络，以轨迹时延嵌入的地面速度、空速和推断推力向量预测偏航角。
result: "在2340条自由飞行轨迹上，中位绝对角度误差约5°，可覆盖整个[−π,π)范围。"
conclusion: 该估计器能为仅有质心运动轨迹的历史数据恢复身体朝向，扩展了昆虫导航行为分析的数据利用。
---

## 摘要
身体朝向是分析昆虫飞行行为的关键变量，但在大多数实验设置中，仍难以在轨迹全程进行测量。尽管现代追踪系统能可靠地捕捉质心的位置和速度，但解析身体偏航朝向通常需要专用的硬件，且局限于小型专门构建的空间，不适用于大规模或长时程研究。在此，我们开发了一种数据驱动的估计器，直接从平移飞行轨迹数据预测身体偏航朝向。我们在自由飞行的黑腹果蝇中同时记录了飞行轨迹和身体朝向的数据集上，训练了一个全连接前馈人工神经网络，使用地速、空速和推断推力向量的时延嵌入作为输入特征。在2,340条轨迹上训练后，该ANN预测器实现了约5°的中位绝对角度误差，并在整个[−π, π)范围内准确恢复朝向。该估计器为从仅记录质心运动的现有轨迹数据集中恢复身体朝向信息提供了一种实用工具，将昆虫导航的行为和计算分析扩展到之前无法获取的数据。

## Abstract
Body orientation is a key variable in the analysis of insect flight behavior, yet it remains difficult to measure across the full extent of a trajectory in most experimental settings. Although modern tracking systems reliably capture the position and velocity of the center of mass, resolving body yaw orientation typically requires dedicated hardware confined to a small, purpose-built volume, and is impractical for large-scale or long-duration studies. Here, we develop a data-driven estimator that predicts body yaw orientation directly from translational flight trajectory data. We trained a fully connected feedforward artificial neural network (ANN) on a dataset in which both flight trajectory and body orientation were recorded simultaneously in freely flying \textit{Drosophila}, using a time-delay embedding of ground velocity, air velocity, and inferred thrust vectors as input features. Trained on 2,340 trajectories, the ANN predictor achieved a median absolute angular error of approximately 5$^{\circ}$, with accurate heading recovery across the full $[-\pi,\pi)$ range. The estimator provides a practical tool for recovering body orientation information from existing trajectory datasets in which only center-of-mass motion was recorded, extending the behavioral and computational analysis of insect navigation to previously inaccessible data.