---
title: Validation of a multiscale Hill-type actuator against comprehensive benchmarks of motor unit and muscle force measurements
title_zh: 多尺度希尔型执行器在运动单位和肌肉力测量综合基准上的验证
authors: "Sgarzi, A., Caillet, A. H., Millard, M., Weidner, S., Haralabidis, N., Meranger, T., Bolsterlee, B., Farina, D., Lovell, N. H., Modenese, L."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732276v1.full.pdf"
tags: ["query:sb"]
score: 8.0
evidence: 验证了多尺度Hill型肌肉执行器，用于肌肉骨骼建模
tldr: "现有Hill型肌肉模型因简化兴奋-激活动力学并忽略纤维类型差异，缺乏跨生理尺度和收缩模式的系统验证，制约了模型普适性。本研究开发了多尺度纤维类型特异的Hill型神经肌肉作动器，融入机制性兴奋-激活动力学、激活-长度依赖力-速度关系、弹性肌腱及yielding和sag等效应。在涵盖运动单位和整块肌肉、慢快纤维及等长与动态条件的四项基准测试中，模型平均绝对误差一般低于15%最大等长力，次最大刺激下误差升高。该工作首次实现对单一Hill型作动器的多尺度系统验证，为后续神经肌肉建模提供基准框架。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有Hill型模型简化兴奋-激活动力学，忽略快慢纤维差异，且未在多尺度和动态条件下进行系统验证。
method: 开发多尺度纤维特异Hill型作动器，融入机制性兴奋-激活动力学、激活-长度依赖力-速度关系及纤维特异的yielding与sag，并基于四项实验基准进行系统验证。
result: "模型在等长与动态条件下再现实测力，平均绝对误差一般低于15%最大等长力，但次最大和动态试验误差较大；含yielding与sag的动力学改善了次最大性能。"
conclusion: 首次实现单一多尺度Hill型作动器在运动单位和肌肉力数据上的系统验证，为未来模型评估提供了基准框架。
---

## 摘要
计算希尔型肌肉模型因其高效性和生理可解释性而被广泛用于模拟肌肉力量产生。然而，其公式依赖于限制性假设，包括有争议的多尺度简化、简化的兴奋-激活动力学以及无法捕捉快慢纤维。此外，现有的希尔型模型在生理尺度、纤维类型和收缩模式方面仍未得到充分验证。我们通过开发一种具有机制性兴奋-激活动力学的多尺度纤维类型特异性希尔型神经肌肉执行器，并系统地根据全面的实验基准对其进行验证，解决了这些局限性。该模型建立在一个先前提出的由运动神经元驱动的执行器之上，该执行器整合了基于钙动力学的激活动力学。进一步精炼了兴奋-激活公式以加强其生理基础，同时通过纳入激活和长度依赖的力-速度关系、弹性肌腱、被动弹性元件以及屈服和松弛的纤维类型特异性效应，扩展了收缩动力学。验证针对四个基准数据集进行，这些数据集涵盖运动单位和整个肌肉尺度，包括等长和动态条件下的慢速和快速纤维。实验力量轨迹取自大鼠和猫的六块肌肉，使用广泛的刺激频率、肌肉长度和施加的长度变化，将先前的文献数据集与本项研究专门进行的实验相结合。总体而言，该模型在所有基准条件下复现了力量，平均绝对误差通常低于最大等长力的15%，尽管在某些次最大和动态试验中观察到较大误差。纳入基于生理的兴奋-激活动力学，以及屈服和松弛，改善了模型在次最大激活条件下的性能。本研究首次对单个多尺度希尔型神经肌肉执行器进行了系统验证，使用了全面的实验运动单位和肌肉力量数据，为未来模型的开发和评估提供了一个基准框架。

## Abstract
Computational Hill-type muscle models are widely used to simulate muscle force production because of their efficiency and physiological interpretability. However, their formulation relies on limiting assumptions, including debated multiscale simplifications, a simplified excitation-activation dynamics and an inability to capture slow and fast fibres. Moreover, existing Hill-type models remain insufficiently validated across physiological scales, fibre types, and contraction modes. We addressed these limitations by developing a multiscale fibre-type specific Hill-type neuromuscular actuator with mechanistic excitation-activation dynamics and systematically validated it against comprehensive experimental benchmarks. The model built upon a previously proposed motoneuron-driven actuator incorporating calcium-kinetics-based activation dynamics. The excitation-activation formulation was further refined to strengthen its physiological basis, while the contraction dynamics was extended by including an activation- and length-dependent force-velocity relationship, elastic tendon, passive elastic element, and the fibre-type-specific effects of yielding and sag. Validation was performed against four benchmark datasets spanning motor-unit and whole-muscle scales, including slow and fast fibres under both isometric and dynamic conditions. Experimental force traces were obtained from six muscles of rats and cats using a broad range of stimulation frequencies, muscle lengths, and imposed length changes, combining previous literature datasets with experiments performed ad hoc for this study. Overall, the model reproduced forces across all benchmark conditions, with mean absolute errors typically below 15% of the maximum isometric force, although larger errors were observed in specific submaximal and dynamic trials. The inclusion of physiologically based excitation-activation dynamics, together with yielding and sag, improved model performance under submaximal activation conditions. This study presents the first systematic validation of a single multiscale Hill-type neuromuscular actuator against comprehensive experimental motor unit and muscle force data, providing a benchmark framework for the development and assessment of future models.

---

## 论文详细总结（自动生成）

# 论文总结：多尺度希尔型执行器在运动单位和肌肉力测量综合基准上的验证

## 1. 研究问题与动机
- **核心问题**：现有计算希尔型肌肉模型被广泛用于肌肉骨骼模拟，但存在三大不足：
  - 依赖过度简化的兴奋-激活动力学，对底层生理机制（如钙动力学）表达不足。
  - 无法区分快肌纤维与慢肌纤维的力学特性差异。
  - 缺乏跨生理尺度（运动单位 ↔ 整块肌肉）、跨纤维类型、跨收缩模式（等长与动态）的系统实验验证，模型普适性存疑。
- **整体动机**：构建一个生理基础更扎实、能体现快慢纤维差异的多尺度神经-肌肉执行器，并首次用涵盖运动单位和整块肌肉的多基准实验数据对其进行系统验证，为领域提供可参照的基准框架。

## 2. 方法论
- **模型基础**：沿用先前提出的、由运动神经元驱动的执行器框架，其激活动力学基于细胞内钙浓度变化（钙动力学）。
- **关键改进与扩展**：
  - **兴奋-激活动力学优化**：重构兴奋到激活的映射公式，加强其与神经生理过程的对应关系。
  - **收缩动力学强化**：
    - 引入**激活-长度依赖的力-速度关系**，替代经典Hill模型中常数的力-速度特性。
    - 添加**弹性肌腱**与**被动弹性元件**，使肌腱-肌纤维串联结构更符合解剖实际。
    - 针对快、慢纤维分别模型化**yielding（屈服）**与**sag（衰减）**效应，捕捉次最大刺激时的特征性力学响应。
- **多尺度特性**：模型能从运动神经元放电到单运动单位激发，再聚合至整块肌肉力量输出，实现一致的多尺度描述。

## 3. 实验设计与基准
- **数据来源**：四个基准数据集，包含大鼠和猫的**六块不同肌肉**（具体肌肉名称摘要未详列）。
- **实验条件覆盖**：
  - **生理尺度**：运动单位水平与整块肌肉水平。
  - **纤维类型**：慢肌（S型）与快肌（FF/FR型）单位/肌肉。
  - **收缩模式**：等长收缩（不同长度与刺激频率）和动态收缩（施加长度变化）。
- **刺激协议**：广泛频率范围、多肌肉长度、多长度变化轨迹。
- **对比方法**：模型输出与**实测力轨迹**进行直接比对，未提及与其他模型变体的A/B消融对比，但通过激活动力学、yielding/sag的有无探讨内部模块贡献。

## 4. 资源与算力
- 原文摘要未提及GPU型号、数量、训练时长等算力信息。该工作属于生物力学建模与参数拟合/仿真验证，其计算负载可能来自单个模型求解和参数优化，大概率不依赖大规模深度学习训练。因此，**算力需求未明确说明**，推断为普通科学计算设备即可完成。

## 5. 实验数量与充分性
- **实验组数**：
  - 覆盖 4 个基准数据集。
  - 来自 6 块肌肉（不同物种）。
  - 涵盖多频率、多长度、等长与动态多种条件。
- **充分性评价**：
  - 多层次（运动单位→整块肌肉）、多类型（快/慢）、多模式（等长/动态）的交叉验证，在希尔型模型研究领域属于较为全面的实验设计。
  - 不足之处：仅动物数据（大鼠、猫），缺乏人体在体实验的直接验证；未明确列出与其他已有模型的横向对比，公平性仅体现在与实测数据的吻合度上。
- **客观性**：采用统一的平均绝对误差（%MIF）作为量化指标，客观可比较。

## 6. 主要结论与发现
- 模型能在**全部基准条件下重现力输出**，平均绝对误差通常低于最大等长力的15%，显示良好的整体预测能力。
- **次最大和动态试验中误差较大**，提示模型在低激活水平或长度快速变化的复杂条件下仍有改进空间。
- **生理性兴奋-激活动力学与 yielding、sag 效应的纳入**显著提升了模型在次最大激活条件下的性能，验证了这些细节机制对提升普适性至关重要。
- 本文是**首个**针对单一希尔型神经肌肉执行器进行多尺度（运动单位→整块肌肉）、跨纤维类型、跨收缩模式的系统验证研究。

## 7. 论文优点
- **整合度高**：将钙动力学、纤维类型特异力学（yielding、sag）、激活依赖的力-速度关系等多项改进集成于统一执行器，生理基础扎实。
- **验证尺度全**：跨运动单位与整块肌肉，覆盖慢快纤维，兼顾等长与动态，提供难得的多基准验证框架。
- **误差报告透明**：不仅给出整体优良性，也明确指出次最大与动态条件下的局限，增强结果可信度。
- **为领域提供基准**：整理并可能公开部分自测数据与验证流程，有利于未来模型横向对比。

## 8. 不足与局限
- **物种局限**：仅使用大鼠和猫的肌肉数据，未在人类肌肉上验证，向人体运动模拟的转化风险未知。
- **模型未与其他变体横向对比**：仅基于实验力对比，缺少与经典Hill模型或近期竞争模型的直接性能比较，难以衡量改进幅度。
- **动力学复杂性可能引入过拟合风险**：新增参数较多（钙动力学、力-速度依赖系数、yielding/sag参数等），文中未详细讨论参数可辨识性和鲁棒性。
- **应用场景侧重**：验证集中于分离的肌肉与运动单位，尚未在完整多关节运动任务中检验模型交互效应。
- **误差分布细节缺失**：摘要未提供不同条件下误差的具体分布或最大误差值，难以评估极端偏差情况。

（完）
