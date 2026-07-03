---
title: Automated behavioral segmentation and markerless pose tracking of mice during spaceflight
title_zh: 太空飞行中小鼠的自动化行为分割与无标记姿态追踪
authors: "Kiffer, F. C., Scott, R. T., Martens, M. T., Mayo, A., Li, Y., Mendoza, M., Gautam, S., Huang, J., Bathwal, M., Jaikumar, S., Mahajan, A., Sanders, L. M., Eisch, A. J., Pereira, T. D."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.30.721950v2.full.pdf"
tags: ["query:cv-sports"]
score: 6.0
evidence: 应用无标记姿态估计追踪动物行为，技术可迁移至人体姿态估计
tldr: 在国际空间站上，啮齿动物行为研究对于理解太空适应至关重要，但长期视频分析依赖繁重的人工标注。本研究利用SLEAP进行标记点姿态估计，DeepEthogram进行行为分割，处理NASA Rodent Research-1任务的存档视频。即使面对镜头逐渐污损、网格遮挡和光学像差，姿态追踪精度仍与人类标注者间差异相当；对八类行为分类精度达到0.86-0.90，显示小鼠在微重力下出现渐进行为适应；通过圈转运动重建，估算出小鼠周期性产生的向心加速度接近地球重力水平。首次验证了深度学习工具在太空环境啮齿动物行为自动分析中的可行性，为未来空间站自动化监测系统奠定基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 太空啮齿动物行为研究依赖耗费人力的手动视频标注，难以扩展，亟需自动化方法以应对长期飞行任务。
method: 应用SLEAP姿态估计与DeepEthogram行为分割于国际空间站小鼠视频，应对镜头污损、遮挡等挑战性成像条件。
result: 姿态追踪精度媲美人类标注间差异，八类行为分类准确率达0.86-0.90，并发现圈转运动产生接近1g的向心加速度。
conclusion: 首次验证深度学习在太空动物行为自动分析中的有效性，为未来长期飞行监测建立基准。
---

## 摘要
国际空间站上的NASA啮齿动物栖息舱实现了对太空飞行行为反应的长期研究，但基于视频的行为分析一直依赖于耗时的人工标注。尚无研究检验深度学习工具在轨道动物实验室的苛刻成像条件下能否实现该分析的自动化。我们将姿态估计（SLEAP）和行为分割（DeepEthogram）应用于来自Rodent Research-1任务的存档影像。九名标注员在2,063个帧上标注了3,249个姿态标签，三名行为学家在66段视频上标注了411,194个帧。尽管存在渐进式镜头污染、网格遮挡和球面像差，姿态追踪准确度仍接近人类标注者间的差异。八类行为分类的准确度达到0.86–0.90，并提示了对微重力的渐进行为适应。转圈运动的重建运动学估计出周期性接近1g的向心加速度。这是首次将基于深度学习的姿态估计和行为分割应用于太空飞行中的啮齿动物，为未来的监测系统确立了基准。

## Abstract
The NASA Rodent Habitat aboard the International Space Station enabled long-duration studies of behavioral responses to spaceflight, but video-based behavioral analysis has relied on laborious manual annotation. No study has tested whether deep learning tools can automate this analysis under the demanding imaging conditions of orbital vivaria. We applied pose estimation (SLEAP) and behavioral segmentation (DeepEthogram) to archival footage from the Rodent Research-1 mission. Nine labelers annotated 3,249 pose labels across 2,063 frames, and three behaviorists labeled 411,194 frames across 66 videos. Pose tracking accuracy approximated human inter-annotator variability despite progressive lens soiling, grid occlusions, and spherical aberration. Behavioral classification across eight categories achieved accuracy of 0.86-0.90 and suggests progressive behavioral adaptations to microgravity. Kinematic reconstruction of circling estimated centripetal accelerations periodically approaching 1g. This is the first application of deep learning-based pose estimation and behavioral segmentation to rodents in spaceflight, establishing benchmarks for future monitoring systems.