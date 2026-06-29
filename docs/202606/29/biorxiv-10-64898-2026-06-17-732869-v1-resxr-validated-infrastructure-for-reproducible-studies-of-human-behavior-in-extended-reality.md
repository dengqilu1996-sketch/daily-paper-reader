---
title: "ResXR: validated infrastructure for reproducible studies of human behavior in Extended Reality"
title_zh: ResXR：用于在扩展现实中可重复研究人类行为的经过验证的基础设施
authors: "Bergstein, Y., Barel, N., Shai Basson, G., Bromberg, O., Schonberg, T."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.732869v1.full.pdf"
tags: ["query:sb"]
score: 7.0
evidence: XR中标准化运动捕捉数据的开源工具包
tldr: 扩展现实（XR）研究兼具实验控制与生态效度，但缺乏共享基础设施，导致数据格式不一、难以复现。ResXR 是一个开源工具包，基于Unity模板采集头、手、眼、面部追踪等同步传感器数据，通过Python管道进行质量验证与标记，并导出标准化的Motion-BIDS数据集。该工具提供了三种开箱即用的行为范式，首次强调消费级头显传感器数据须经实证验证而非仅依赖厂商文档，为可复现XR实验奠定透明、可扩展的基础。
source: biorxiv
selection_source: fresh_fetch
motivation: XR行为研究因缺少共享基础设施，实验构建需专门工程，产生无法跨实验室重分析的定制格式数据。
method: ResXR提供Unity模板与独立Python管道，采集同步传感器数据，验证质量、标记异常区间，并导出标准化Motion-BIDS数据集。
result: 开发出包含三种通用行为范式的开源工具，传感器数据经压力测试验证，生成自含式质量报告。
conclusion: ResXR为可复现XR实验提供透明、可扩展的基础，强调消费级传感器数据的实证验证，推动社区标准化。
---

## 摘要
扩展现实（XR）结合了实验控制与生态效度，然而行为XR研究缺乏共享基础设施：构建沉浸式实验需要专门的工程技能，而自定义工具产生的数据格式各异，其他实验室难以重新分析。我们推出ResXR（使用XR进行研究），一个开源工具包，提供从沉浸式实验到标准化数据集和质量报告的路径，可在独立头戴设备上运行。一个Unity模板记录同步的头部、手部、眼部和面部追踪数据，并附带每个样本的硬件时间戳；一个独立的Python管道验证数据质量，标记有问题的区间，并以Motion-BIDS格式导出原始和衍生数据集，同时包含自包含的质量报告。三个即用型范式涵盖了常见的行为设计。ResXR是XR研究中的一个新理念：消费级头戴设备的传感器数据必须经过实证验证，而非依赖供应商文档，其模式和质量标记基于经过压力测试的传感器行为。其目标是为可重复的XR实验提供一个透明、可由社区扩展的基础。

## Abstract
Extended Reality (XR) combines experimental control and ecological validity, yet behavioral XR research lacks shared infrastructure: building immersive experiments demands specialized engineering, and custom tools yield data in custom formats that other laboratories cannot readily reanalyze. We present ResXR (Research with XR), an open-source toolkit providing a path from immersive experiment to standardized dataset and quality report, running on standalone headsets. A Unity template records synchronized head, hand, eye, and face tracking with per-sample hardware timestamps; an independent Python pipeline validates quality, masks flagged intervals, and exports raw and derivative datasets in Motion-BIDS format with self-contained quality reports. Three ready-to-run paradigms span common behavioral designs. ResXR is an idea new to XR research: sensor data from consumer headsets must be empirically validated rather than taken from vendor documentation, grounding its schema and quality flags in stress-tested sensor behavior. Its aim is a transparent, community-extensible foundation for reproducible XR experimentation.