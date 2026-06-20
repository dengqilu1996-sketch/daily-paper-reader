---
title: Effect-oriented automated muscle path modeling via gradient-specified optimization using muscle surface mesh and moment arm
title_zh: 基于肌肉表面网格和力臂的梯度指定优化实现面向效果的自动肌肉路径建模
authors: "Chen, Z., Hu, T., Haddadin, S., Franklin, D. W."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.15.718668v2.full.pdf"
tags: ["query:sb"]
score: 9.0
evidence: 利用优化方法自动进行肌肉路径建模，用于精确的肌骨仿真。
tldr: 传统肌肉路径建模依赖几何对齐，难以精确再现长度-力臂关系。本文提出面向效果的自动化方法，将肌肉路径拟合形式化为多目标最小二乘问题，约束包括穿过横截面椭圆、力臂匹配实验值和功能方向，并采用梯度指定优化。在可视人男性数据集上生成42条路径，兼具解剖真实性与生物力学精度，仅需20.1分钟。该方法比数值梯度更快更准，适用于大规模受试者特异性建模。
source: biorxiv
selection_source: fresh_fetch
motivation: 准确重现肌肉长度-力臂关系对仿真精度至关重要，传统几何对齐方法无法保证。
method: 将路径建模形式化为最小二乘优化，基于肌肉表面网格划分为多个椭圆截面，同时约束力臂与实验值一致及功能方向，采用梯度指定优化加速求解。
result: 在可视人男性数据上生成42条肌肉路径，解剖逼真，力臂精确，仅需20.1分钟，梯度指定法比数值梯度更快更准。
conclusion: 梯度指定优化框架高效准确，适用于大规模特定受试者肌肉骨骼建模，为个性化生物力学仿真提供了可靠高效的工具。
---

## 摘要
肌肉腱路径建模不仅仅是调整缆线以反映肌肉腱单元的几何特征。从仿真精度的角度来看，关键在于复现目标肌肉的长度和力臂-关节角度关系。在本研究中，我们提出了一种面向效果的自动路径建模方法，通过基于肌肉表面网格和力臂的混合校准实现。该任务被表述为一个最小二乘优化问题，其目标有三：使路径（1）穿过代表肌肉横截面的多个椭圆，（2）产生与实验测量相匹配的力臂，以及（3）产生预期功能方向上的力臂。我们利用Visible Human Male的肌肉骨骼表面网格和文献中的力臂数据集，展示了优化框架的性能——在20.1分钟内生成了42条解剖学上真实且生物力学上准确的路径。我们的优化框架采用梯度指定，比使用默认数值梯度更快、更准确，使其适用于大规模的个体化应用。

## Abstract
There is more to musculotendon path modeling than aligning a cable to reflect the geometric features of a musculotendon unit. From the perspective of simulation accuracy, the key is to replicate the length- and moment arm-joint angle relations of the target muscle. In this study, we propose an effect-oriented approach of automated path modeling, via hybrid calibration based on muscle surface mesh and moment arm. The task is formulated as a least-squares optimization problem with a threefold objective for the path to: (1) pass through multiple ellipses representing muscle cross-sections, (2) yield moment arms that match experimental measurements, and (3) yield moment arms in the expected functional directions. We demonstrate the performance of our optimization framework with the musculoskeletal surface mesh from the Visible Human Male and moment arm datasets from literature--producing 42 paths that are anatomically realistic and biomechanically accurate within 20.1 minutes. Our optimization framework is gradient-specified, which is faster and more accurate than using the default numerical gradient, making it applicable for large-scale subject-specific uses.

---

## 论文详细总结（自动生成）

## 1. 论文核心问题与研究背景

- **问题**：肌肉骨骼仿真中，肌肉腱路径（musculotendon path）模型必须准确再现肌肉的**长度–关节角度关系**和**力臂–关节角度关系**，否则动力学分析（正向与逆向）将存在较大偏差。
- **现有方法局限**：
  - **原因导向（cause‑oriented）**：依靠骨骼和周围组织几何形状约束路径，但仅视觉对齐无法保证多关节、大范围运动时的力臂精度。
  - **效果导向（effect‑oriented）**：仅有少量研究直接用实验力臂数据校准路径，但若缺少形态学约束，可能导致路径长度失准或外观不自然；且实验力臂数据往往稀疏、仅覆盖主导自由度。
- **本文动机**：将**肌肉表面网格的形态信息**与**实验力臂数据**相结合，实现一种**混合校准**，生成既解剖真实又生物力学准确的自动肌肉路径。

## 2. 方法核心思想与技术细节

- **问题形式化**：将路径建模表述为多目标最小二乘优化问题，优化参数为路径锚点、中间点（via point）及包裹障碍（可选）的位置。
- **复合目标函数**：
  \[
  J(\mathbf{p}) = J_{\text{SM}}(\mathbf{p}) + J_{\text{vMA}}(\mathbf{p}) + J_{\text{sMA}}(\mathbf{p})
  \]
  其中：
  - **表面网格项 \(J_{\text{SM}}\)**：路径需穿过从肌肉表面网格提取的多个椭圆截面（代表肌腹横截面）。
  - **力臂值匹配项 \(J_{\text{vMA}}\)**：路径在当前关节构型下产生的力臂与文献中实验测量值一致。
  - **力臂符号匹配项 \(J_{\text{sMA}}\)**：保证力臂功能方向（如屈/伸、收/展）与解剖学描述相符，尤其对缺乏数据的小肌肉。
- **网格预处理与椭圆截面**：
  - 在固定姿态下，利用肌肉表面网格计算调和标量场，提取等值线并拟合成椭圆（每个肌肉约4个）。
  - 椭圆用标准二次型表示，路径与椭圆相交条件通过两个标量指标连续化，引入**软ReLU函数**和**软阶梯函数**使布尔交截条件可微，从而可提供解析梯度。
- **力臂校准策略**：
  - 若有力矩测量，使用距离比例函数归一化误差（容差为 \(10\% r_{\text{target}} + 5\) mm）。
  - 若无测量，仅保持力矩符号正确（通过软阶梯函数转换为连续代价）。
- **优化方法**：
  - **梯度指定（gradient‑specified）**：手动推导复合目标函数的解析梯度，替代数值差分，提高收敛速度与精度。
  - 使用MATLAB的`lsqnonlin`（信赖域反射算法），并行生成多个初始点以避免局部极小。
  - 路径结构按复杂度递进尝试：OI → OVI → OV1V2I → OCI → OC1C2I，选达到目标且结构简单的解。

## 3. 实验设计与基准比较

- **数据集**：
  - **骨骼与肌肉表面网格**：来源于Visible Human Male（VHM）的3D分割数据集（Andreassen et al., 2023）。
  - **力臂目标值**：自文献收集的300个髋、膝、踝力臂数据集（陈和Franklin，2025），用于校准值（\(J_{\text{vMA}}\)）。
  - **目标符号**：基于解剖学教科书确定肌肉功能方向，用于\(J_{\text{sMA}}\)。
- **运动学模型**：移植Arnold下肢模型（Arnold et al., 2010）的6自由度关节定义至VHM骨骼，旋转中心手动对齐，对踝关节ever/inversion额外增加一套与测量实验一致的旋转轴。
- **基准方法对比**：
  - 论文在表1中列举了近年自动肌肉路径建模方法：Modenese & Kohout (2020)（基于网格中心线，无显式力臂校准）；Lloyd et al. (2021)（原因导向，计算量极大）；Livet et al. (2022)（使用非梯度指定优化，仅测试简单路径）；Wang et al. (2025)（离散包裹点，无解析力臂）；以及本团队此前工作Chen et al. (2026)（仅力臂校准，无形态约束）。本文方法首次结合表面网格和力臂进行混合自动校准，且采用梯度指定。
- **应用场景**：校准42条下肢肌肉路径，覆盖髋、膝、踝单关节及多关节肌，从直通路到双中间点，无包裹障碍。

## 4. 资源与算力

- **硬件环境**：2.9‑GHz Intel Core i9处理器，64 GB内存，14个CPU核心，使用MATLAB并行工具箱（`parfor`）。
- **计算耗时**：全部42条路径的总校准时间为**20.1分钟**，无GPU参与。
- **未明确说明**：未提及具体内存占用或CPU负载情况，亦无与其他方法的计算时间对比（仅指出梯度指定比数值梯度快）。

## 5. 实验数量与充分性

- **实验规模**：对42条下肢肌肉进行了全面校准，每条肌肉输出最终路径结构、成本和时间。
- **实验类型**：
  - 个体案例解剖和力臂结果可视化（如股四头肌、腘绳肌、比目鱼肌、臀大肌、内收长肌等）。
  - 针对数据稀缺肌肉（如臀小肌、耻骨肌），仅依赖符号和网格约束。
- **实验充分性评估**：
  - **优点**：覆盖肌肉数量多，考虑不同数据条件下的策略（有测量、仅符号、无任何数据），展示了方法对不同输入的自适应。
  - **局限**：
    - 缺乏**系统定量验证**：没有报告力臂在全关节空间内的误差统计（如平均绝对误差、最大误差），仅展示少数代表性图表。
    - 未与表中所列其他自动方法进行**定量对比实验**。
    - 未验证**未校准关节构型**下的力臂准确性（仅通过符号成本约束）。
    - 运动学移植带来的偏差没有量化评估。
  - 总体上看，实验偏向**概念验证与性能展示**，尚未完成严格的系统性基准测试，客观性部分受限。

## 6. 主要结论与发现

- 提出的梯度指定优化框架成功生成了**解剖真实且力臂准确**的42条下肢肌肉路径，总耗时仅约20分钟。
- 对多个自由度肌肉（如臀大肌、比目鱼肌），即便实验数据稀疏，也能通过符号约束和网格约束避免功能逆转。
- 即使在缺少肌腱网格的情况下，力矩校准也能引导路径形成合理走向（如长屈肌、伸肌），弥补纯形态学方法的不足。
- 梯度指定优化在求解该类多目标、多约束问题时，明显优于数值梯度方案，使大规模个性化建模成为可能。

## 7. 方法及实验设计亮点

- **混合校准框架**：首次将肌肉表面网格（约束路径长度和外观）与力臂（值及符号）统一于一个可微优化问题中，兼顾形态与功能。
- **梯度指定与连续化处理**：用软ReLU和软阶梯函数将椭圆交截这一分段条件完全连续化，使得目标函数处处可微并可用解析梯度，大幅提升优化效率与稳定性。
- **自动化程度高**：自动识别肌腹入口/出口点，自动生成椭圆截面，自动尝试多种路径结构并挑选最优。
- **容错设计**：针对力臂数据缺失的肌肉，通过符号成本项保证功能方向，避免显著错误；对肌腱网格缺失的情形，力矩数据提供额外补偿。
- **实用性**：20分钟即可完成整个下肢的路径校准，适用于临床或科研中的快速个体化建模。

## 8. 不足与局限

- **验证不充分**：缺少对路径长度、力臂全范围的定量验证指标，未与其他自动方法进行横向对比，无法客观衡量精度提升幅度。
- **截面椭圆简化假设**：仅有4个椭圆代表整个肌腹，对形态复杂肌肉可能过于简化；未利用非固定姿态下的网格数据，校准仅在单一尸体固定姿态下进行。
- **运动学误差**：关节旋转中心与轴直接移植自Arnold模型，未根据VHM个体作优化，可能引入力矩的基线偏差。
- **数据局限性**：力臂测量来自不同研究、不同受试者群体，与VHM个体解剖不匹配；大量肌肉缺乏覆盖多自由度的力臂数据，无法完全验证三维力矩面。
- **附着点估计**：当肌腱网格缺失时，自动估计的起止点可能偏离解剖标志，需人工后期修正，影响通用化和大规模应用。
- **包裹障碍未实际使用**：所有最终路径均为直连或中间点结构，未出现需要圆柱体包裹的复杂路径，方法对极端的包裹情形未有充分测试。
- **计算环境限制**：虽声称适用于大规模应用，但仅在单个CPU上进行，尚未展示在更大关节自由度或超高精度网格时的可扩展性。

（完）
