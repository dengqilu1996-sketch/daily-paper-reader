---
title: Data-driven gait cycle decomposition based on whole-body coordination dynamics
title_zh: 基于全身协调动力学数据驱动的步态周期分解
authors: "De luca, M., Demuru, M., Gallo, E., ANGIOLELLI, M., Tafuri, D., Sorrentino, G., Sorrentino, P., Troisi Lopez, E."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.732845v1.full.pdf"
tags: ["query:sb"]
score: 9.0
evidence: 利用全身运动学数据进行数据驱动步态分解，直接关联人体运动运动学分析
tldr: 传统步态周期描述多基于观察分析，难以全面捕捉人体运动的连续全局协调。本研究提出融合网络理论与非负矩阵分解的分析框架，从全身三维运动学数据中提取协调模式。结果显示，六个稳健且对称的协调模式可有效表征步态功能子任务，揭示了协调的连续性与主动性，并系统纳入上肢贡献。该数据驱动方法深化了对步行协调机制的理解，为运动控制研究与临床评估提供了新工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统步态模型难以刻画全身连续的协调动态，需要数据驱动方法以全局视角解析步行协调机制。
method: 结合网络理论与非负矩阵分解，从60名健康受试者的三维运动数据中构建动态kinectome，提取协调模式的空间与时间特征。
result: 提取出六个稳健、对称且高度一致的协调模式，捕捉了步行主要功能子任务，并显示协调跨相位边界并涉及上肢。
conclusion: 该框架丰富了经典步态描述，揭示了协调的连续性与主动性，有望为运动控制和临床评估提供敏感生物标志物。
---

## 摘要
人类运动研究长期以来依赖步态周期的描述性框架，这些框架为行走的功能阶段及其生物力学需求提供了重要见解。尽管这些模型仍然具有很高的信息量，但它们主要基于观察分析，可能无法完全捕捉表征人类运动的连续、全局协调。本研究提出了一个综合框架来研究全身协调。该框架将网络理论与非负矩阵分解（NNMF）相结合，将步态视为协调关节相互作用的动态系统。利用来自60名健康受试者的三维运动学数据，我们构建了随时间变化的全身协调表示，命名为动态kinectome。然后使用NNMF对其进行分解，以提取关节协调的空间模式及其对应的时间激活，从而在保留生理意义的同时，实现对运动组织的可解释表征。我们的分析提取了六个稳健、高度一致且对称的协调模式，有效捕捉了运动的主要功能性子任务。这些发现并非挑战经典阶段描述，而是通过展示协调如何作为一个连续的、往往具有前瞻性的过程出现，跨越传统阶段边界，并系统性整合上肢以实现动态稳定性，从而丰富了这些描述。总体而言，本研究为人类运动提供了一个整体的、数据驱动的视角，为运动控制的未来研究提供了有希望的基础，并可能有助于为临床和康复应用开发敏感的生物标志物。

## Abstract
The study of human locomotion has long relied on descriptive frameworks of the gait cycle, which have provided essential insights into the functional phases of walking and their underlying biomechanical demands. While these models remain highly informative, they are largely based on observational analyses and may not fully capture the continuous, global coordination that characterizes human movement. The present study proposes an integrated framework to study whole-body coordination. This framework combines network theory with non-negative matrix factorization (NNMF) to treat gait as a dynamic system of coordinated joint interactions. Using three-dimensional kinematic data from 60 healthy subjects, we constructed a representation of whole-body coordination across time, named dynamic kinectome. It was then decomposed using NNMF to extract spatial patterns of joint coordination and their corresponding temporal activations, allowing for an interpretable characterization of locomotor organization while preserving physiological meaning. Our analysis extracted six robust, highly consistent, and symmetrical coordination patterns across participants, effectively capturing the primary functional subtasks of locomotion. Rather than challenging classical phase descriptions, these findings enrich them by showing how coordination emerges as a continuous, often proactive process that can extend across conventional phase boundaries and systematically integrates the upper limbs for dynamic stability. Overall, this study provides a holistic, data-driven perspective on human locomotion, offering a promising basis for future investigations in motor control and may contribute to the development of sensitive biomarkers for clinical and rehabilitative applications.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义
- **研究动机**：传统步态周期描述（如基于观察的相位划分）难以全面捕捉人类行走中全身关节连续、全局的协调动态。现有模型虽能揭示功能阶段与生物力学需求，但对协调的连续性和上肢系统性参与缺乏整体刻画。
- **核心问题**：如何利用数据驱动方法，从全身三维运动学数据中提取可解释的协调模式，以更完整地描述步态周期的功能组织，并为运动控制与临床评估提供新工具。
- **整体含义**：该研究试图将步态看作一个动态协调系统，通过整合网络理论与非负矩阵分解，构建“动态kinectome”并用其分解出协调模式，从而丰富而非挑战经典步态描述，揭示协调的连续性与前瞻性，并为敏感生物标志物的开发奠定基础。

### 论文提出的方法论
- **核心思想**：将步态视为关节协调相互作用的动态系统，使用网络理论表示全身协调关系，再通过非负矩阵分解（NNMF）提取空间协调模式及其时间激活，以保持生理可解释性。
- **关键技术细节**：
  - 从60名健康受试者的三维运动学数据出发，构建随时间变化的全身协调表征，命名为“动态kinectome”（dynamic kinectome）。该表征可能是基于关节角度或位置数据计算得到的关节间协调网络（如互信息、相关性或图模型）。
  - 应用非负矩阵分解（NNMF）对动态kinectome进行分解。NNMF可以将非负矩阵分解为两个非负低秩矩阵的乘积，分别对应空间模式（节点权重）和时间激活系数，从而避免负值导致的生理意义模糊。
- **算法流程**（文字说明）：  
  1. 采集全身标记点三维运动数据，计算各关节的运动学时间序列。  
  2. 通过滑窗或逐点构建功能连接矩阵（如每个时间点的关节间协调强度），形成三维张量或动态矩阵序列，即动态kinectome。  
  3. 将所有受试者的动态kinectome拼接或平均后，进行NNMF，得到若干空间模块（协调模式）和对应的时间激活曲线。  
  4. 分析空间模式的对称性、一致性，以及时间激活与经典步态相位的关系。

### 实验设计
- **数据集**：60名健康受试者的三维运动学数据（很可能在行走任务中采集）。  
- **基准参考**：经典步态周期功能任务描述（如基于观察的相位划分）。没有表明与其他建模方法（如PCA、肌肉协同分析等）的直接定量对比，而是将提取的6个协调模式与现有运动学/功能任务对应，以验证生理意义。  
- **对比方法**：未明确提及与其他分解方法（如PCA、ICA）的系统benchmark，重点在于阐释NNMF提供的非负与可解释优势。  
- **分析角度**：评估模式的空间对称性、被试间一致性、时间激活曲线与经典相位的对应关系以及上肢参与情况。

### 资源与算力
- 论文元数据未提供所用GPU型号、数量或训练时长等算力信息。  
- 由于NNMF是相对低复杂度的矩阵分解，且数据量不算特别庞大（60人、步态周期时长），可能未使用大规模算力，但文中并未说明。

### 实验数量与充分性
- **实验数量**：基于现有摘要，主要实验为：①构建动态kinectome；②应用NNMF提取协调模式；③分析模式的稳健性（跨被试一致性）、对称性及与经典功能子任务的对应关系。可能还包括对模式数量的确定（如通过方差解释曲线）。  
- **充分性评价**：未提及消融实验（如改变网络构建方法、分解秩等）或与其他分解技术的定量对比。仅从60名健康受试者提取并报告了模式特征，样本量合理，但缺乏对异常步态的验证测试。实验在内部一致性和生理可解释性上较为充分，但在方法泛化性与比较方面有所不足。  
- **客观公平性**：研究主要展示所提框架的发现，未刻意与别的方法竞争，因此不涉及公平性问题。但其结论多基于描述性对应，缺乏统计显著性检验细节，可能影响推断强度。

### 论文的主要结论与发现
- 提取出六个稳健、高度一致且对称的协调模式，有效捕捉了步行的主要功能性子任务（如负重接收、单支撑、推进等）。  
- 协调呈现出跨越传统阶段边界的连续性和前瞻性过程，并非严格局限于离散相位。  
- 上肢被系统性地整合进各协调模式中，揭示其在动态稳定性中的主动作用。  
- 该数据驱动框架未推翻经典描述，而是从全局协调视角对其进行了丰富和拓展，为运动控制研究和临床评估提供了潜在的敏感生物标志物。

### 优点
- **方法创新**：将网络理论与NNMF有机结合，应用于全身协调分析，实现了对多维运动学数据的高层次抽象。
- **生理可解释性**：非负约束保证了分解结果的非负性，便于解释为协同收缩或共同激活模式，更贴合神经肌肉控制特性。
- **整体视角**：突破了仅关注下肢或离散相位的传统方法，纳入上肢并揭示连续协调动态。
- **稳健性展示**：在60名被试中得出高度一致且对称的模式，为方法可靠性提供了较强证据。

### 不足与局限
- **样本限制**：仅包含60名健康成人，未涉及病理群体、不同年龄或特殊任务人群，结论普适性待验证。
- **方法对比缺失**：未与PCA、ICA、肌肉协同分析等常规分解方法进行定量比较，无法凸显NNMF的独特增益。
- **网络构建细节模糊**：动态kinectome的具体构建方式（如连接度量、窗口宽度等）未明确，影响可复现性。
- **统计论证不足**：空间对称性、跨被试一致性等缺乏严格的统计检验报告（如对称性指数置信区间），部分结论可能流于描述。
- **应用证据薄弱**：虽提出可作为临床生物标志物，但未提供实际临床验证或区分度分析，应用潜能仍属推测。
- **算力与实现细节未公开**：计算资源、具体参数设置（如NNMF秩选择）未见说明，对复现有所制约。

（完）
