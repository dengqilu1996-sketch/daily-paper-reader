---
title: Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling
title_zh: 基于高共模抑制比和指数窗均方根数学模型的低延迟表面肌电实时校正系统设计
authors: "Lo, H. U., Gao, Z., Loi, H. F., Cheng, S. K."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.724714v2.full.pdf"
tags: ["query:sports-sci"]
score: 7.0
evidence: 低延迟sEMG校正系统用于假肢和康复，可应用于运动损伤恢复
tldr: "sEMG信号易受电力线干扰和数字延迟制约临床应用。本文提出高CMRR模拟前端结合指数窗口RMS包络与递归单音陷波器，将计算复杂度降至O(1)且零分支抖动，实现确定性实时处理。在Ninapro DB2上验证，每样本延迟8.2μs，端到端30ms，SNR升13.9dB，RMSE 70μV，相关0.993(p<0.001)。为机电执行预留>90ms，CPU占1.6%，适合无FPU单片机，已开源。"
source: biorxiv
selection_source: fresh_fetch
motivation: sEMG信号易受电力线干扰且数字处理延迟大，阻碍临床假肢与外骨骼应用。
method: 融合高CMRR模拟前端、指数窗口RMS估计和递归单音LMS陷波器，实现O(1)复杂度、无分支的实时校正。
result: "在Ninapro DB2上平均SNR提升13.9dB，包络RMSE 70μV，形态相关0.993，延迟仅30ms，CPU占用1.6%。"
conclusion: 该系统在延迟、信噪比和形态保真方面均表现优异，计算资源需求极低，适合单片机实时处理，已开源。
---

## 摘要
表面肌电（sEMG）是用于肌电假肢、外骨骼和康复系统最实用的无创接口，但电力线干扰（PLI）污染和过度的数字流水线群延迟仍然限制其临床应用。本文提出一种联合设计模数校正系统，将高共模抑制比（CMRR）前端与指数窗均方根（EMRMS）包络估计器和递归单频电力线干扰消除器相结合。我们给出一个捕捉电极-皮肤不平衡的闭合形式CMRR模型，并提供对LMS消除器的完整稳定性分析。EMRMS估计器在时间和空间复杂度上将计算开销从O(L)降至严格O(1)。该算法无数据依赖分支，实现确定性的算法执行时间（在RTOS环境下零抖动），并且天然兼容无硬件浮点单元（FPU）微控制器上的定点算术。一个参考实现达到每样本8.2 μs的中位延迟，产生约30 ms的端到端延迟——为机电驱动留下充裕的>90 ms预算——同时仅需1.6%的主动CPU占空比，允许延长的深度睡眠间隔。在公开数据集Ninapro DB2上的验证表明，平均信噪比提高13.9 dB（12通道平均；单通道比较：9.7 dB，见表3），相对于长度为200的矩形窗参考，包络均方根误差为70.0 μV。配对Wilcoxon符号秩检验确认与静态基线相比具有统计显著性（p < 0.001），Pearson相关分析（ρ = 0.993 ± 0.0002）证实严格的形态保真度。完整的开源代码库和基准测试已公开发布。表3：在一段常见的60秒类Ninapro合成sEMG（单通道）上的定量比较，其中叠加了3 mV 50.3 Hz市电频率，略微偏离静态陷波器设计的中心频率50.0 Hz，在频率失配下对自适应校正器进行压力测试。第3.4节报告的Ninapro多通道聚合结果（13.9 dB）采用刚好50 Hz的市电（匹配陷波），因此获得更高的ΔSNR。“MAC/样本”不包括EMRMS的平方根运算和预计算的LMS正弦/余弦值。

## Abstract
Surface electromyography (sEMG) is the most practical non-invasive interface for myoelectric prostheses, exoskeletons, and rehabilitation systems, but power-line interference (PLI) contamination and excessive digital pipeline group delay still limit its clinical adoption. This paper proposes a co-designed analog-digital correction system combining a high-CMRR front-end with an exponentially-windowed RMS (EMRMS) envelope estimator and a recursive single-tone PLI canceller. We present a closed-form CMRR model capturing the electrode-skin imbalance, and provide a complete stability analysis of the LMS canceller. The EMRMS estimator reduces the computational overhead from O(L) to strictly O(1) in both time and space complexities. Featuring no data-dependent branching, the algorithm achieves deterministic algorithmic execution time (zero jitter under an RTOS environment) and is natively compatible with fixed-point arithmetic on microcontrollers lacking a hardware Floating-Point Unit (FPU). A reference implementation reaches an 8.2 {micro}s median per-sample latency, yielding an end-to-end delay of[~] 30 ms -- leaving a generous >90 ms budget for electromechanical actuation -- while requiring an active CPU duty cycle of merely 1.6%, enabling prolonged deep-sleep intervals. Validation on the public Ninapro DB2 dataset demonstrates a 13.9 dB mean SNR improvement (averaged across 12 channels; single-channel comparison: 9.7 dB, Table 3) and a 70.0 {micro}V envelope RMSE against a length-200 rectangular reference. Paired Wilcoxon signed-rank tests confirm statistical significance (p < 0.001) over static baselines, and Pearson correlation analysis ({rho} = 0.993 {+/-} 0.0002) confirms strict morphological fidelity. The full open-source codebase and benchmarks are publicly released.

O_TBL View this table:
org.highwire.dtl.DTLVardef@8e9e6borg.highwire.dtl.DTLVardef@1428c51org.highwire.dtl.DTLVardef@a4384org.highwire.dtl.DTLVardef@1d6c478org.highwire.dtl.DTLVardef@fce0c6_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3:C_FLOATNO O_TABLECAPTIONQuantitative comparison on a common 60 s segment of Ninapro-like synthetic sEMG (single channel) with a 3 mV 50.3 Hz mains tone  slightly drifted from the static notchs design centre at 50.0 Hz, stress-testing the adaptive corrector under a frequency mismatch. The Ninapro multi-channel aggregate (13.9 dB) reported in Section 3.4 uses mains exactly at 50 Hz (matched notch) and so achieves a higher {Delta} SNR. "MAC/sample" excludes the EMRMS square root and the pre-computed LMS sine/cosine.

C_TABLECAPTION C_TBL