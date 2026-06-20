---
title: Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling
title_zh: 基于高CMRR与EMRMS数学模型的低延迟表面肌电实时校正系统设计
authors: "Lo, H. U., Gao, Z., Loi, H. F., Cheng, S. K."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.724714v1.full.pdf"
tags: ["query:sport-tsa"]
score: 8.0
evidence: 低延迟表面肌电校正系统用于可穿戴生理监测
tldr: "表面肌电信号(sEMG)在假肢和外骨骼中应用广泛，但电源线干扰和数字流水线延迟制约临床采用。本研究提出高共模抑制比(CMRR)模拟前端与指数窗RMS(EMRMS)及递归自适应陷波器的联合设计，实现O(1)计算复杂度与确定性低延迟。在Ninapro数据集上信噪比改善13.9 dB，端到端延迟约30 ms，CPU占用仅1.6%，显著优于基线。该方法为实时肌电控制提供了高效嵌入式解决方案。"
source: biorxiv
selection_source: fresh_fetch
motivation: sEMG因电源线干扰和群延迟问题难以实时可靠应用，需要低延迟高抗干扰校正系统。
method: 提出结合高CMRR前端、EMRMS包络估计和递归单频陷波器的模拟-数字协同设计，实现无抖动定点运算。
result: "在Ninapro DB2上平均SNR改善13.9 dB，包络RMSE 70.0 μV，延迟约30 ms，CPU占空比1.6%，形态保真度ρ=0.993。"
conclusion: 该系统以低计算开销实现实时高精度sEMG去噪，适合微控制器，已开源。
---

## 摘要
表面肌电（sEMG）是肌电假肢、外骨骼和康复系统最实用的非侵入式接口，但电力线干扰（PLI）污染和数字流水线的过长群延迟仍限制其临床应用。本文提出了一种模数协同校正系统，将高共模抑制比（CMRR）前端与指数窗均方根（EMRMS）包络估计器及递归单音PLI消除器相结合。我们给出了一个捕捉电极-皮肤不平衡的闭式CMRR模型，并对最小均方（LMS）消除器进行了完整的稳定性分析。EMRMS估计器在时间和空间复杂度上从O(L)降至严格O(1)。该算法无数据依赖分支，实现了确定性算法执行时间（RTOS环境下零抖动），原生兼容无硬件浮点单元（FPU）的微控制器定点运算。参考实现达到每样本中位延迟8.2微秒，端到端延迟约30毫秒——为机电驱动留出超过90毫秒的充裕预算——同时仅需1.6%的主动CPU占空比，支持长时间的深度休眠。在公开的Ninapro DB2数据集上验证，结果显示平均信噪比提升13.9 dB（12通道平均；单通道对比：9.7 dB，表3），相较于长度为200的矩形基准包络均方根误差为70.0微伏。配对Wilcoxon符号秩检验证实了相较于静态基线的统计显著性（p < 0.001），皮尔逊相关分析（ρ = 0.993 ± 0.0002）确认了严格的形态保真度。完整的开源代码库和基准测试均已公开发布。

## Abstract
Surface electromyography (sEMG) is the most practical non-invasive interface for myoelectric prostheses, exoskeletons, and rehabilitation systems, but power-line interference (PLI) contamination and excessive digital pipeline group delay still limit its clinical adoption. This paper proposes a co-designed analog-digital correction system combining a high-CMRR front-end with an exponentially-windowed RMS (EMRMS) envelope estimator and a recursive single-tone PLI canceller. We present a closed-form CMRR model capturing the electrode-skin imbalance, and provide a complete stability analysis of the LMS canceller. The EMRMS estimator reduces the computational overhead from[O] (L) to strictly[O] (1) in both time and space complexities. Featuring no data-dependent branching, the algorithm achieves deterministic algorithmic execution time (zero jitter under an RTOS environment) and is natively compatible with fixed-point arithmetic on microcontrollers lacking a hardware Floating-Point Unit (FPU). A reference implementation reaches an 8.2 {micro}s median per-sample latency, yielding an end-to-end delay of[~] 30 ms -- leaving a generous >90 ms budget for electromechanical actuation -- while requiring an active CPU duty cycle of merely 1.6%, enabling prolonged deep-sleep intervals. Validation on the public Ninapro DB2 dataset demonstrates a 13.9 dB mean SNR improvement (averaged across 12 channels; single-channel comparison: 9.7 dB, Table 3) and a 70.0 {micro}V envelope RMSE against a length-200 rectangular reference. Paired Wilcoxon signed-rank tests confirm statistical significance (p < 0.001) over static baselines, and Pearson correlation analysis ({rho} = 0.993 {+/-} 0.0002) confirms strict morphological fidelity. The full open-source codebase and benchmarks are publicly released.

O_TBL View this table:
org.highwire.dtl.DTLVardef@72d969org.highwire.dtl.DTLVardef@1fb62corg.highwire.dtl.DTLVardef@1f104d1org.highwire.dtl.DTLVardef@73551corg.highwire.dtl.DTLVardef@1d8aed5_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3:C_FLOATNO O_TABLECAPTIONQuantitative comparison on a common 60 s segment of Ninapro-like synthetic sEMG (single channel) with a 3 mV 50.3 Hz mains tone  slightly drifted from the static notchs design centre at 50.0 Hz, stress-testing the adaptive corrector under a frequency mismatch. The Ninapro multi-channel aggregate (13.9 dB) reported in Section 3.4 uses mains exactly at 50 Hz (matched notch) and so achieves a higher {Delta} SNR. "MAC/sample" excludes the EMRMS square root and the pre-computed LMS sine/cosine.

C_TABLECAPTION C_TBL