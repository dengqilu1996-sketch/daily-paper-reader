---
title: "TracktorLive: an integrated real-time object tracking and response system"
title_zh: TracktorLive：一个集成的实时目标追踪与响应系统
authors: "Minasandra, P., Sridhar, V. H., Roche, D. G., Planas-Sitja, I."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.12.711471v2.full.pdf"
tags: ["query:cv-sports"]
score: 6.0
evidence: 可用于运动员跟踪的实时对象跟踪系统
tldr: 在运动行为研究中，实时跟踪与自动响应系统可减少偏差、提高可重复性，但现有方案因高硬件要求、计算延迟和陡峭学习曲线而受限。TracktorLive利用传统视觉与并发架构，实现高效实时跟踪与响应，并通过可复用代码片段简化复杂工作流。在鱼类实验中，其计时准确性和一致性优于人类实验员，成功完成刺激传递、条件录制等任务。该开源软件模块化、易用，有望推动神经科学、野生动物管理等领域的实时闭环研究。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有实时跟踪系统硬件要求高、延迟大，缺乏标准化响应实现且学习曲线陡峭，限制闭环实验应用。
method: TracktorLive采用传统视觉与并发架构，将跟踪与响应并行化，并提供可组合的cassettes简化复杂工作流实现。
result: 在鱼类刺激任务中，TracktorLive比人工操作更准确且变异性低；展示多场景应用如条件录制和运动触发。
conclusion: 该开源工具兼具易用性、模块化和计算效率，可推动实时跟踪—响应系统在神经科学及野生动物管理等领域的普及。
---

## 摘要
实时追踪与自动响应系统对于运动和行为研究中的实验标准化、减少观察者偏差、提高可重复性至关重要。然而，现有解决方案面临显著挑战：基于人工智能的追踪系统需要昂贵的硬件并存在计算延迟，给闭环实验带来困难；现有的实时追踪工具缺乏标准化的响应传递实现；并且陡峭的学习曲线限制了没有编程或计算机视觉专业知识用户的访问。在这里，我们介绍TracktorLive，一个开源的Python包，旨在通过并发和模块化、基于卡带的架构来克服这些挑战。TracktorLive利用传统计算机视觉技术执行基于图像的目标检测，无需昂贵的硬件或深度学习。通过将目标追踪和响应传递并行化到分离的、并发的服务器和客户端进程中，该软件最大限度地减少了帧处理时间，实现了快速、实时的分析与响应传递。用户友好的卡带——可复制粘贴到脚本中的便携代码片段——使编程经验有限的用户能够实现复杂的工作流，用于实验和实际应用。我们通过多个应用展示了TracktorLive的实用性，包括用于位置相关操控的基于微控制器的刺激传递；仅在感兴趣事件期间激活的条件性视频录制；利用实时速度计算触发基于运动学的响应；以及结合多种功能的多卡带实验设计。提供了详细的教程，以帮助用户熟悉TracktorLive的操作和功能，并且不断增长的卡带库支持处理实时和预录制视频的多样化应用。我们通过比较其在涉及两种鱼类的刺激传递任务中的响应时间与人类实验者来验证该软件，结果显示TracktorLive始终表现出更高的准确性和更低的变异性，特别是对于快速移动的被试。除实验生物学外，TracktorLive独特的架构和多功能性可以支持从神经科学到野生动物管理等许多不同领域的应用。作为结合了可访问性、模块化和计算效率的开源软件，TracktorLive可以帮助在多个学科中普及实时追踪和自动响应系统。

## Abstract
Real-time tracking and automated response systems are essential for standardising experiments, reducing observer bias, and improving reproducibility in studies of movement and behaviour. However, existing solutions face significant challenges: AI-based tracking systems require expensive hardware and impose computational delays, creating challenges for closed-loop experiments; existing real-time tracking tools lack standardised implementations for response delivery; and steep learning curves limit accessibility for users without programming or computer vision expertise. Here, we introduce TracktorLive, an open-source Python package designed to overcome these challenges through concurrency and a modular,  cassette-based architecture. TracktorLive leverages traditional computer vision techniques to perform image-based object detection without the need for expensive hardware or deep learning. By parallelizing object tracking and response delivery into separate, concurrent server and client processes, the software minimizes frame processing time, enabling rapid, real-time analysis and response delivery. User-friendly  cassettes--portable code snippets that can be copy-pasted into scripts--enable users with minimal programming experience to implement complex workflows for use in experiments and practical applications. We demonstrate TracktorLives utility through several applications, including microcontroller-based stimulus delivery for location-dependent manipulations; conditional video recording that activates only during events of interest; kinematic-based response triggering using real-time velocity computations; and multi-cassette experimental designs combining multiple functionalities. Detailed tutorials are provided to familiarize users with TracktorLives operation and functionality, and a growing library of cassettes supports diverse applications for processing both real-time and pre-recorded video. We validated the software by comparing its response timing to human experimenters in a stimulus delivery task involving two fish species, where TracktorLive demonstrated consistently higher accuracy and lower variability, particularly for fast-moving subjects. Beyond experimental biology, TracktorLives unique architecture and versatility could support many different applications in fields ranging from neuroscience to wildlife management. As an open-source software combining accessibility, modularity, and computational efficiency, TracktorLive can help democratize real-time tracking and automated response systems across disciplines.