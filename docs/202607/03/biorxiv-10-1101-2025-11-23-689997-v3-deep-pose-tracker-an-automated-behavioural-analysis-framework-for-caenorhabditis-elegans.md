---
title: "Deep-Pose-Tracker: an automated behavioural analysis framework for Caenorhabditis elegans"
title_zh: Deep-Pose-Tracker：一种秀丽隐杆线虫自动化行为分析框架
authors: "Saha, D., Chaudhary, S., Vyas, D., Ghosh-Roy, A., Sharma, R."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.23.689997v3.full.pdf"
tags: ["query:cv-sports"]
score: 6.0
evidence: 基于YOLO的自动姿态检测用于线虫，可迁移至人体姿态估计
tldr: 在秀丽隐杆线虫等模式生物的行为研究中，手动追踪分析耗时且易出错，自动化需求迫切。Deep-Pose-Tracker(DPT)基于YOLO实现自动姿态检测，集成下游分析算法量化速度、方向、复杂弯曲等特征，并采用特征虫分解降维表征姿态动态。该工具在测试中表现可靠且高速，为多实验刺激下的线虫行为自动量化提供了高效实用的框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有线虫行为分析依赖人工追踪，效率低且易出错，亟需自动化工具以加速研究。
method: 提出Deep-Pose-Tracker，基于YOLO实现线虫自动姿态检测，并集成速度、方向、复杂弯曲等行为量化及特征虫分解降维分析。
result: 在验证和测试数据集上，DPT表现出高准确度与快速推理，能可靠检测姿态并有效量化多种行为特征。
conclusion: DPT为用户友好的自动化行为量化框架，适用于多种实验刺激下的C. elegans研究，有望加速行为神经科学发现。
---

## 摘要
追踪和分析动物行为是神经科学和发育生物学等领域的关键步骤。例如，对线虫秀丽隐杆线虫的行为研究有助于理解生物体如何对外部线索作出反应，以及特定的生理反应如何与即时或习得行为相关联。虽然通过运动模式与体态动力学追踪行为是常规操作，但手动进行时变得费时费力。因此，该过程的自动化对于准确、快速的检测和分析至关重要。为此，我们开发了Deep-Pose-Tracker (DPT)，一个基于YOLO (You Only Look Once) 的模型，用于从视频和图像中自动化检测秀丽隐杆线虫的体态。该模块进一步用于多种下游分析算法，以量化关键行为特征，包括运动速度、方向、前进或后退运动，以及复杂的身体弯曲（如欧米茄转弯）。此外，它还包括特征蠕虫分解，将复杂的体态动力学表示为低维空间。该模型在验证和测试数据集上表现出可靠的性能，具有高推理速度，并且用户友好。因此，DPT可以成为在不同实验刺激下对秀丽隐杆线虫进行自动化行为量化的宝贵工具包。

## Abstract
Tracking and analyzing animal behaviour is a crucial step in fields such as neuroscience and developmental biology. Behavioural studies in the nematode C. elegans, for example, help in understanding how organisms respond to external cues and how the specific physiological responses link to either instantaneous or learned behaviours. Although tracking behaviour through locomotion patterns and postural dynamics is routine, it becomes laborious and time-consuming when performed manually. Automation of this process is therefore crucial for accurate and fast detection and analysis. To this end, we report Deep-Pose-Tracker (DPT), a YOLO (You Only Look Once)-based model for automated pose detection of C. elegans from videos and images. The module is further utilized for several downstream analysis algorithms to quantify essential behavioural features, including locomotion speed, orientation, forward or reverse locomotion, and complex body bends such as omega turns. In addition, it includes eigenworms decomposition to represent complex posture dynamics in a low-dimensional space. The model shows reliable performance on the validation and test datasets, with high inference speed, while being user-friendly. DPT, therefore, can be a valuable toolkit for automated behavioural quantification of C. elegans under varying experimental stimuli.