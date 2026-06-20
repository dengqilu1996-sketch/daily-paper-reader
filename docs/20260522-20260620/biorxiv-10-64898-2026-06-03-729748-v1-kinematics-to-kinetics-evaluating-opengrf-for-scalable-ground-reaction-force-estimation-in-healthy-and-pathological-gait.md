---
title: "Kinematics to Kinetics: Evaluating OpenGRF for Scalable Ground Reaction Force Estimation in Healthy and Pathological Gait"
title_zh: 从运动学到动力学：评估 OpenGRF 在健康与病理步态中可扩展的地面反力估算
authors: "Abdullah, M., Hulleck, A. A., Khalaf, K., El-Rich, M."
date: 2026-06-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729748v1.full.pdf"
tags: ["query:sb"]
score: 10.0
evidence: 利用运动捕捉数据和肌骨模型估计地面反作用力，用于步态分析。
tldr: 地面反力（GRF）是步态分析的关键指标，但测力板测量成本高且受限。OpenGRF是一种基于运动学数据的GRF估计框架，但其在病理步态中的准确性尚不明确。本研究评估了OpenGRF在健康人群和帕金森病、中风、髋骨关节炎等多种病理步态中的表现，发现垂直GRF估计最准确，前后GRF偏差较大。结果表明OpenGRF可作为无法使用测力板时的替代方案，用于动力学步态评估。
source: biorxiv
selection_source: fresh_fetch
motivation: 地面反力对步态评估至关重要，但常规测力板测量方法昂贵且受限，需验证开源估计方法在病理步态中的准确性。
method: 采用OpenGRF框架从运动学数据估计GRF，在健康与帕金森病、中风、髋骨关节炎等多种步态中与测力板测量进行对比验证。
result: 垂直GRF一致性最高(PCC 0.84-0.94)，内外侧误差小，前后GRF准确性较差，PD推进期偏差最大。
conclusion: OpenGRF能合理估计健康及病理步态的GRF，可作为力板不可用时的替代工具，支持临床动力学评估。
---

## 摘要
地面反力是步态损伤与康复的重要标志，但直接使用测力台测量成本高昂且局限于实验室环境。OpenGRF 是一个开源框架，利用肌肉骨骼建模从运动捕捉数据估算地面反力，但其在病理步态中的有效性尚不确定。本研究评估了 OpenGRF 在健康成人以及帕金森病、卒中、髋骨关节炎和全髋关节置换术患者步态中估算三维地面反力的准确性，并检验其再现临床相关地面反力峰值大小与时机的能力。在健康参与者以及帕金森病（停药/服药状态）、卒中和髋骨关节炎患者术前及术后6个月的队列中，将 OpenGRF 估算值与测力台测量值进行了比较。采用均方根误差、归一化均方根误差和皮尔逊相关系数量化准确性。峰值分析考察了前后方向的制动峰与推进峰、第一和第二垂直峰以及主要内外侧峰的偏差，以及步态周期中的时间偏移。采用一维统计参数映射检验波形差异（p = 0.01）。OpenGRF 重现了各组的整体地面反力轮廓。垂直地面反力的一致性最好（皮尔逊相关系数 0.84–0.94；归一化均方根误差 0.14–0.23），而内外侧地面反力显示出较低的绝对误差（均方根误差 1.45–1.95 %BW）和中等至良好的一致性（皮尔逊相关系数 0.70–0.82）。前后方向地面反力准确性最低（皮尔逊相关系数 0.61–0.73），尤其在帕金森病推进阶段（归一化均方根误差高达 0.39）。OpenGRF 能够合理估算健康与病理步态中的地面反力，在无法使用测力台时可支持动力学步态评估。

## Abstract
Ground reaction forces (GRFs) are important markers of gait impairment and rehabilitation, but direct measurement with force plates is expensive and limited to laboratory settings. OpenGRF is an open-source framework that estimates GRFs from motion-capture data using musculoskeletal modeling, yet its validity in pathological gait remains uncertain. This study evaluated the accuracy of OpenGRF for estimating three-dimensional GRFs during gait in healthy adults and in people with Parkinsons disease (PD), stroke, hip osteoarthritis (HOA), and total hip arthroplasty, and assessed its ability to reproduce clinically relevant GRF peak magnitudes and timings. OpenGRF estimates were compared with force-plate measurements in healthy participants and in cohorts with PD (OFF/ON medication), stroke, and HOA before surgery (M0) and 6 months after surgery (M6). Accuracy was quantified using root mean square error (RMSE), normalized RMSE (NRMSE), and Pearson correlation coefficients (PCC). Peak analyses examined biases in anterior-posterior (AP) braking and propulsive peaks, first and second vertical peaks (V1, V2), and the main mediolateral peak, as well as timing shifts across the gait cycle. One-dimensional statistical parametric mapping tested waveform differences (p = 0.01). OpenGRF reproduced overall GRF profiles across groups. Vertical GRF showed the best agreement (PCC 0.84-0.94; NRMSE 0.14-0.23), whereas mediolateral GRF showed low absolute error (RMSE 1.45-1.95 %BW) and moderate-to-good agreement (PCC 0.70-0.82). AP GRF was least accurate (PCC 0.61-0.73), especially during propulsion in PD (NRMSE up to 0.39). OpenGRF can reasonably estimate GRFs in healthy and pathological gait and may support kinetic gait assessment when force plates are unavailable.

---

## 论文详细总结（自动生成）

### 论文结构化总结

#### 1. 核心问题与整体含义
- **研究动机**：地面反作用力是评估步态损伤与康复效果的关键生物力学指标，但传统的测力台测量方法成本高、对实验环境要求严苛，且可能干扰自然步态，限制了其在临床和社区场景中的广泛应用。
- **核心问题**：开源框架 OpenGRF 可利用运动学数据和肌肉骨骼模型估算 GRF，但其在健康人群中的验证较多，在帕金森病（PD）、脑卒中、髋骨关节炎（HOA）等病理步态人群中的准确性和有效性尚不明确。
- **整体含义**：本研究旨在系统评估 OpenGRF 在估算健康与多种病理步态中三维 GRF 的表现，探究其能否作为数字生物标志物开发、客观康复监测和疾病进展评估的可靠工具，从而实现在缺乏测力台条件下的动力学步态评估。

#### 2. 方法论
- **核心思想**：利用受试者特定的肌肉骨骼模型和运动学数据（关节角度），通过 OpenGRF 框架的反向动力学与优化方法，预测足-地接触过程中的三维 GRF，完全摆脱对测力台的依赖。
- **关键技术细节与流程**：
    1.  **运动学数据预处理**：将来自不同数据集的 C3D 文件转换为 OpenSim 兼容的格式（.trc 和 .mot），并进行标准化、单位换算，以及根据足部标记点将测力台数据分配至对应下肢。
    2.  **肌肉骨骼建模**：在 OpenSim 中采用经过修改的 Rajagopal 全身模型（22个身体节段，37个自由度）。通过静态标定数据对通用模型进行缩放，生成受试者特异性模型。随后进行逆向运动学，求解出关节角度。
    3.  **GRF 估计**：将缩放后的模型文件和关节角度文件输入 OpenGRF 工具。该工具通过优化方法估算三维 GRF、地面反作用力矩和压力中心，并输出包含时间序列的 .mot 文件。模拟过程中保留了工具的默认执行器最优力和权重因子。
    4.  **后处理与对比**：
        *   以 20N 的垂直力阈值定义步态周期（足跟触地至足尖离地）。
        *   将估算和实测的力归一化为体重百分比（%BW），并进行时间归一化（0-100% 步态周期）和重采样（101个样本）。
        *   对每个试验、每条肢体计算所有可用周期的中位数波形，以确保偏差估计的稳健性。
        *   采用预定义窗口（如 V1 峰在 5-20% 步态周期）独立识别估算与实测波形中的关键峰值（AP-B, AP-P, V1, V2, ML-P），计算其幅值偏差和时间误差。

#### 3. 实验设计
- **数据集与场景**：
    *   **健康与卒中**：来自 Criekinge 等人的公开数据集。包含 138 名健康成年人和 50 名脑卒中后患者（约 53 天）的 8 摄像头 Vicon 运动捕捉数据（100 Hz）和 4 块测力台数据（1000 Hz）。
    *   **帕金森病（PD）**：来自 Shida 等人的数据集。包含 26 名特发性 PD 患者在停药（OFF）和服药（ON, 约 1 小时后）状态下的 12 摄像头光学数据（150 Hz）和 5 块测力台数据（300 Hz）。
    *   **髋骨关节炎（HOA）及全髋关节置换术**：来自 Bertaux 等人的数据集。包含 106 名（术前）和 92 名（术后 6 个月）单侧 HOA 患者的 8 摄像头 Vicon 数据（100 Hz）和 2 块测力台数据（1000 Hz）。
- **黄金标准（Benchmark）**：同步采集的测力台实测 GRF 数据。
- **对比方法**：
    *   主要对比为 OpenGRF 估算值与测力台实测值。
    *   在讨论部分，将结果与前人研究中的同类方法（如基于 AnyBody 的预测模型、基于 Kinect 的预测模型）的结果进行了横向比较。

#### 4. 资源与算力
- 论文中未明确提及进行 OpenGRF 估算和统计测试时所使用的具体硬件配置、GPU 型号/数量或总运行时长。

#### 5. 实验数量与充分性
- **实验组数量**：实验涵盖了 1 个健康对照组和 3 种不同的临床病理组（其中 PD 组还区分了停药与服药状态，HOA 组分为了术前和术后），共 5 个独立队列，每个队列均分析了左右双侧下肢。
- **分析维度**：
    *   **整体波形精度**：对三维 GRF，分别计算了中位数 RMSE (%BW)、NRMSE 和 PCC。
    *   **波形差异检验**：应用了一维统计参数映射来识别步态周期中统计学显著的差异区间（p=0.01）。
    *   **临床峰值特征**：对 5 个临床关键峰值进行了幅值偏差和计时偏差的单独量化。
- **充分性与客观性**：实验设计较为全面和系统。使用了多个独立的外部公开数据集，覆盖了神经性和骨性两大类步态障碍。评估指标同时包含了整体误差、相关性、波形显著性检验和临床峰值偏差，评估维度丰富。对比均在统一的后处理框架下进行，实验过程相对客观、公平。

#### 6. 主要结论与发现
- **总体结论**：OpenGRF 能够合理估算健康和多种病理步态中的三维 GRF 轮廓，具有替代力板进行动力学评估的潜力，但在不同方向和不同病理条件下的精度表现不一。
- **具体发现**：
    *   **垂直 GRF (vGRF)** 的估算精度最高（PCC: 0.84–0.94, NRMSE: 0.14–0.23），波形形状和峰值再现最为一致。
    *   **内外侧 GRF (ML GRF)** 的绝对误差最低（RMSE: 1.45–1.95 %BW），波形相关性中等至良好（PCC: 0.70–0.82），但峰值时间误差在不同组间变异较大。
    *   **前后向 GRF (AP GRF)** 的估算精度最低，尤其在 PD 人群中（NRMSE 最高达 0.39），主要误差集中于推进阶段，表现为显著的幅值高估（6.57 – 8.93 %BW）和计时延迟（5 – 7% 步态周期）。

#### 7. 优点
- **临床价值高**：系统评估了 OpenGRF 在多种重要病理步态中的有效性，填补了该工具在临床验证方面的空白，推进了其向实际临床应用转化。
- **开源工具验证**：验证了 OpenGRF 这一开源、可访问的工具，这有助于降低动力学步态分析的门槛，促进研究结果的透明性和可复现性。
- **评估体系全面**：不仅评估了整体波形误差，还专门针对临床医生关注的、有诊断价值的 GRF 峰值特征（幅值和出现时机）进行了深入分析。
- **数据利用充分**：有效利用了多个公开数据集，在不进行新实验的情况下完成了对工具的跨疾病、多维度的广泛验证。
- **方法学严谨**：采用中位数波形进行对比以减少异常周期的影响，并使用一维统计参数映射进行波形层面的显著性检验。

#### 8. 不足与局限
- **病理类型覆盖有限**：研究仅局限于 PD、卒中和 HOA 三种疾病，未涉及其它常见步态障碍，如膝骨关节炎、脑瘫或截肢等。
- **样本偏差风险**：PD 队列存在性别比例失衡（女性仅 6/26），且所用 Rajagopal 肌肉骨骼模型基于男性解剖学几何，可能引入对女性受试者的估计偏差。
- **验证维度单一**：研究仅验证了 GRF 的估算准确性，未评估 OpenGRF 输出的其他关键动力学参数，如压力中心、自由力矩，以及基于这些力进行逆动力学计算得出的关节力和力矩。
- **场景局限性**：所有数据均在实验室约束环境下采集，未能评估 OpenGRF 在基于可穿戴传感器（如 IMU）数据或真实世界自由行走场景下的表现。
- **未来改进方向**：论文指出，未来工作应扩展临床人群、改善性别平衡、采用性别特异性模型、验证更多动力学输出指标，并评估在实验室外及可穿戴传感条件下的性能。此外，可以通过改进足-地接触模型、引入受试者特异性鞋类和软组织顺应性参数以及速度依赖性校准来进一步提升估计精度。

（完）
