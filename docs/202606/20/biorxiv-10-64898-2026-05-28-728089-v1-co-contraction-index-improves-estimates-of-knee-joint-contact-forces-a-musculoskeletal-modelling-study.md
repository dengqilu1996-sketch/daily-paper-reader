---
title: "Co-contraction index improves estimates of knee joint contact forces: A musculoskeletal modelling study"
title_zh: 共收缩指数改善膝关节接触力估计：一项肌肉骨骼建模研究
authors: "Hoermann, S., Tumer, N., Zadpoor, A. A., Seth, A."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.728089v1.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 结合共收缩指数的肌骨建模改进膝关节接触力估计
tldr: "在肌肉骨骼建模中，最小肌肉激活假设可能无法准确估计病理状态下肌肉协调改变后的膝关节接触力。本研究以共收缩指数修正目标函数，融合肌电测量，同步最小化肌肉激活和共收缩水平误差。结果将膝接触力估计的均方根误差降至0.31倍体重，较最小激活法改善7%体重，且对共收缩水平变化更不敏感。该发现表明，纳入共收缩信息对于准确捕捉个体特异性肌肉协调适应至关重要。"
source: biorxiv
selection_source: carryover_cache
motivation: 传统最小激活假设未考虑病理肌肉协调改变，影响膝接触力估计准确性。
method: 修订肌肉冗余求解器目标函数，利用肌电测量信息最小化肌肉激活与共收缩水平误差。
result: "膝接触力均方根误差降至0.31倍体重，改善7%体重，且对共收缩水平敏感性低。"
conclusion: 表明最小激活假设不足，纳入共收缩信息对准确估计个体化膝力至关重要。
---

## 摘要
健康个体被认为采取最小化能量消耗的肌肉协调策略。然而，在病理条件下，这些模式经常改变，因为患者采用替代策略以增强稳定性。在肌肉骨骼建模中，当估计内部量如膝关节接触力时，这种肌肉协调的变化通常未被考虑。为了解决这个问题，我们调整了肌肉冗余求解器的目标函数，利用肌电图测量来指导肌肉激活，同时最小化肌肉激活和共收缩水平的误差。结果得到的膝关节接触力估计值与三种活动中的体内测量值进行了比较。在所有受试者和活动中平均，基于共收缩指数的方法实现了最低的均方根误差，为0.31倍体重，相较于最小激活求解器结果改善了7%体重。值得注意的是，使用最小激活方法时，均方根误差随共收缩水平增加而增加（β=1.55，95%置信区间[0.79, 2.30]），而基于共收缩指数的方法对此敏感度较低（β=0.78，95%置信区间[0.14, 1.43]）。这些发现表明，基于最小肌肉激活的目标函数可能不足以准确估计肌肉协调改变者的膝关节力。因此，纳入共收缩信息对于捕捉个体特异性适应至关重要。

## Abstract
Healthy individuals are hypothesized to adopt muscle coordination strategies that minimize energy expenditure. However, under pathological conditions, these patterns often change, as patients adopt alternative strategies to enhance stability. In musculoskeletal modeling, such changes in muscle coordination are often not accounted for when estimating internal quantities such as knee joint contact forces. To address this, we adapted the objective function of a muscle redundancy solver to inform muscle activations from electromyography measurements, minimizing errors in both muscle activations and co-contraction levels. The resulting estimates of knee joint contact force were compared with in vivo measurements across three activities. The co-contraction index-informed approach achieved the lowest root-mean-square-error of 0.31 body weight, averaged across all subjects and activities, improving the results of the minimum activation solver by 7% body weight. Notably, root-mean-squared-error increased with the level of co-contraction with the minimum activation approach ({beta} = 1.55, 95% confidence interval [0.79, 2.30]), whereas the co-contraction index-informed approach remained less sensitive ({beta} = 0.78, 95% confidence interval [0.14, 1.43]). These findings suggest that objective functions based on minimum muscle activation may be insufficient to accurately estimate knee joint forces in individuals with altered muscle coordination. Incorporating co-contraction information is therefore essential to capture subject-specific adaptations.

---

## 论文详细总结（自动生成）

## 一、论文核心问题与整体含义

- **研究动机**：膝骨关节炎（KOA）患者因疼痛或关节不稳定常改变肌肉协调策略，表现为下肢肌肉共收缩增加。传统的肌肉骨骼建模在求解肌肉冗余时常采用最小化肌肉激活平方和的目标函数（假设健康人追求代谢经济性），但这可能无法准确反映病理人群因稳定性需求而增加的共收缩，从而导致膝关节接触力（KCF）估计的系统性偏差。
- **整体含义**：本研究提出一种基于共收缩指数（CCI）的肌肉冗余求解方法，通过融合少量表面肌电（EMG）信息来修正目标函数，以更真实地体现个体肌肉协调策略，从而提高KCF估计精度，为运动康复和步态干预提供更可靠的关节负荷监测手段。

## 二、论文提出的方法论

- **核心思想**：在已有的快速肌肉冗余求解器（RMR）框架中，除最小化肌肉激活平方和外，额外引入一项最小化模拟与实测共收缩指数（CCI）之间误差的损失项，迫使肌肉激活模式匹配受试者实际的主缩肌‑拮抗肌共激活水平。
- **关键技术细节**：
  - 基础RMR求解器目标函数包含肌肉激活平方和与理想储备致动器惩罚项，并加入被动肌肉力以提升生理合理性。
  - EMG‑informed 目标函数增加测量肌肉的激活偏差平方和，权重为肌肉权重的两倍，需8块主要下肢肌肉的EMG。
  - **CCI‑informed 目标函数**：仅增加一对肌肉（股外侧肌与腓肠肌内侧头）的CCI误差平方项（权重亦为两倍），其中CCI定义为：
    \[
    CCI = \frac{EMG_S}{EMG_L} \cdot (EMG_S + EMG_L)
    \]
    其中EMG\_S和EMG\_L分别为较小和较大的肌电线性包络值，使CCI归一化在0–2范围，且对最大自主收缩（MVC）归一化偏差不敏感。
  - 求解仍为逐帧的静态优化，不引入模型校准步骤，计算效率较高。

## 三、实验设计

- **数据集**：CAMS公开数据集，6名接受全膝关节置换且植入器械化胫骨托的受试者（1女5男，年龄68±5岁，体重88±12 kg，身高173±4 cm），提供体内实测的三维膝关节力和力矩作为金标准。实验采集包含运动捕捉、地面反力、8通道下肢EMG。
- **测试场景**：三种活动——平地行走、斜坡下降、楼梯下降。平地行走每人8次试验，斜坡和楼梯下降各4次试验（其中K3R斜坡下降因地面反力无效被排除）。
- **对比方法**：共比较了四种肌肉冗余求解器：
  1. **静态优化（SO）**：经典最小化肌肉激活平方和，不考虑被动肌肉力。
  2. **最小激活（RMR）**：在SO基础上加入被动肌肉力和储备致动器惩罚，目标仍为最小化激活平方和。
  3. **EMG‑informed**：在RMR基础上增加8块肌肉的EMG跟踪误差项。
  4. **CCI‑informed（本文重点）**：在RMR基础上增加VL‑MG共收缩指数误差项。
- **评价指标**：均方根误差（RMSE，单位体重BW）、决定系数R²、第二峰值力误差（站立相40‑60%最大压缩力），并考察RMSE与CCI的线性回归关系（聚类稳健标准误）。

## 四、资源与算力

- 文中未明确说明计算资源（如GPU类型、数量或具体训练时长）。本研究主要使用OpenSim 4.5和Python环境进行肌肉骨骼建模和优化求解，属于传统数值优化而非深度学习，算力需求相对较低，未报告并行计算或专用硬件使用情况。工作流管理采用Snakemake，但未提供执行时间细节。

## 五、实验数量与充分性

- **实验规模**：共6名受试者，3种活动，总计约（6×8）+（6×4）+（5×4）= 48+24+20 = 92次独立试验（具体因数据排除略有变化），每个试验分别用4种求解器估计，产生约368组比较。
- **分析方法**：采用配对Wilcoxon符号秩检验（Holm‑Bonferroni校正）比较RMSE差异；用聚类稳健标准误线性回归分析RMSE与CCI关系。同时报告了R²和峰值误差等多维度指标。
- **充分性与公平性**：对比的四种方法均基于同一肌肉骨骼模型、同一运动学数据和相同的优化权重（肌电项和CCI项权重均为肌肉项权重的2倍，储备致动器权重为10倍），未对权重进行任何针对金标准的手动调优，保证了公平性。但受限于仅有6名受试者，统计推断效力较弱，且活动类型不包括坐‑站转换或深蹲等大范围屈膝动作。

## 六、论文的主要结论与发现

- **CCI‑informed方法整体最优**：在所有受试者和活动下平均RMSE为0.31 BW，优于最小激活法（0.38 BW）和EMG‑informed（0.44 BW），改善约7% BW。
- **共收缩水平影响估计误差**：最小激活法下RMSE随CCI升高而显著增大（β=1.55, p<0.05），而CCI‑informed方法的这种依赖性大幅减弱（β=0.78），尤其在平地行走和斜坡下降中几乎消除了CCI‑RMSE的相关性。
- **EMG‑informed方法表现不稳定**：虽在三名受试者中获得最低RMSE，但在其余三人中误差最高，可能因MVC归一化不准确导致过高估计肌肉激活。
- **共收缩信息对准确估计KCF至关重要**：对于共收缩明显增高的个体（如K1L、K2L、K5R、K7L），CCI‑informed方法显著降低RMSE并提高R²，说明最小激活假设不足以捕捉肌肉协调策略的个体性改变。

## 七、优点

- **降低实验复杂性**：仅需一对浅层肌肉（VL和MG）的EMG即可有效校准肌肉协调模式，避免需要全部主要下肢肌肉的繁琐记录，适合可穿戴场景。
- **对MVC误差鲁棒**：CCI为比值指标，对绝对肌电幅值偏差不敏感，无需耗时校准，增强了方法的实用性和外推能力。
- **无需调参**：权重因子固定，不依赖金标准调整，结果具有普适性。
- **保留生理合理性**：基于RMR框架包含被动肌肉力，避免了静态优化因忽略被动力引起的过高共收缩和KCF峰值。
- **统计证据详实**：不仅提供常规误差指标，还通过回归分析揭示了RMSE与CCI的关联模式，强化结论的因果解释。

## 八、不足与局限

- **样本量小**：仅6例老年植入假体受试者，统计推断受集群数少影响（线性回归使用聚类稳健标准误，但混合效应模型常不收敛），结论的泛化到早期KOA或健康人群尚需验证。
- **活动范围有限**：未包含深关节屈曲动作（如坐‑站、下蹲），已有研究表明在此类动作下1自由度膝关节模型因运动学简化会导致较大KCF估计误差，方法可能未在该条件下充分检验。
- **仅验证压缩力**：虽然压缩力为主要负载成分，但未评估其他方向的力（如剪切力）和力矩，无法全面反映关节负荷状态。
- **肌肉配对选择单一**：只基于数据驱动选择了VL‑MG对，未探讨多肌肉对联合CCI或其它共收缩指标，可能未完全捕捉所有受试者不同的协调策略。
- **模型简化约束**：采用1自由度膝关节模型，膝关节的附属运动（内旋、外展）系由被动屈曲关系预设，可能在高屈曲或特殊任务中引入运动学偏差，间接影响力估计。

（完）
