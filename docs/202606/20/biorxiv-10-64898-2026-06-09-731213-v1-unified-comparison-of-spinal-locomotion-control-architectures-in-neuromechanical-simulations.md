---
title: Unified comparison of spinal locomotion control architectures in neuromechanical simulations
title_zh: 神经力学仿真中脊髓运动控制架构的统一比较
authors: "Ton, V., Song, S."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731213v1.full.pdf"
tags: ["query:sb"]
score: 9.0
evidence: 在统一神经力学仿真框架内实现并比较多种运动控制架构
tldr: 神经力学模拟对揭示人体运动控制机制至关重要，但反射、中枢模式发生器（CPG）、肌协同等脊柱控制器因仿真框架各异而缺乏系统比较。本文在一个统一神经力学框架中实现了四种代表性脊髓控制架构，在共享生物力学与计算条件下对比其再现人类步态实验数据的能力和跨速度-坡度行走的多功能性。结果表明，反射型控制器和融合CPG、反射与协同的混合控制器最符合人类步态特征，且后者在速度-坡度适应范围最广，反射型次之。该工作揭示了单纯脊髓模型在非稳态运动中的局限性，强调集成脊髓上调制的重要性，并公开了框架与实现以助未来研究。
source: biorxiv
selection_source: fresh_fetch
motivation: 由于仿真框架差异，现有脊髓运动控制器难以直接对比，阻碍了对人步态控制机制的理解。
method: 在统一神经力学框架中实现反射型、CPG-反射型、肌协同型及CPG-反射-协同型四种控制器，进行系统比较。
result: 反射型和CPG-反射-协同型控制器最符合实验步态，后者在速度和坡度条件下展现最广多功能性。
conclusion: 脊髓机制足以解释稳态步态，但非稳态运动需脊髓上调制；公开框架和代码促进未来研究。
---

## 摘要
神经力学仿真为研究神经控制架构如何产生和调节人类运动提供了强大的框架。已经提出了许多受生物启发的运动控制器，包括基于反射的、基于中枢模式发生器（CPG）的和基于肌肉协同的模型。然而，由于肌肉骨骼模型、优化方法和评估协议的不同，跨研究的直接比较仍然困难。在此，我们在统一的神经力学仿真框架内实现了四种代表性的运动控制架构，即基于反射的、CPG-反射结合的、基于肌肉协同的以及CPG-反射-协同结合的控制器，以便在共享的生物力学和计算条件下进行有控制的比较。性能评估依据（1）与实验观察到的步态特征的一致性，包括运动学、动力学、肌肉激活以及随速度和坡度变化的生物力学趋势，以及（2）在不同速度-坡度条件下的运动多样性。基于反射和CPG-反射-协同结合的控制器最准确地再现了实验观察到的步态特征，而CPG-反射-协同控制器在速度和坡度范围内实现了最广泛的稳定行走行为，紧随其后的是基于反射的控制器。这些发现应被解释为特定模型实现之间的比较，而非对潜在生物学假设的最终评价。此外，由于所研究的控制器主要关注名义稳态运动中的脊髓层面机制，某些模型在更广泛的速度和坡度条件下观察到的有限多样性表明，在建模超出名义稳态步态的运动时，将脊髓运动机制与脊髓上调控相结合的重要性。为了促进进一步研究，我们公开分享了该仿真框架和控制器实现。

关键点
• 现有的神经力学运动控制器由于仿真框架的差异难以直接比较。
• 我们在统一仿真框架内实现了四种代表性的脊髓运动控制模型（基于反射的、基于中枢模式发生器（CPG）-反射的、基于肌肉协同的以及CPG-反射-协同的），并比较了它们的类人性和多样性。
• 基于反射和CPG-反射-协同的控制器最准确地再现了类人步态特征，而CPG-反射-协同控制器在速度-坡度条件下表现出最大的运动多样性，紧随其后的是基于反射的控制器。
• 由于所研究的控制器主要建模了与稳态运动相关的脊髓层面机制，它们在更广泛的速度和坡度条件下适应性降低，这凸显了在建模超出名义步态的运动时纳入脊髓上调控的重要性。
• 我们公开分享仿真框架和控制器实现，以支持人类运动控制的进一步研究。

## Abstract
Neuromechanical simulations provide a powerful framework for investigating how neural control architectures generate and regulate human locomotion. Numerous biologically inspired locomotion controllers have been proposed, including reflex-based, central pattern generator (CPG)-based, and muscle synergy-based models. However, direct comparison across studies remains difficult because of differences in musculoskeletal models, optimization methods, and evaluation protocols. Here, we implemented four representative locomotion control architectures, reflex-based, CPG-reflex-based, muscle synergy-based, and CPG-reflex-synergy-based controllers, within a unified neuromechanical simulation framework to enable controlled comparisons under shared biomechanical and computational conditions. Performance was assessed in terms of (1) agreement with experimentally observed gait characteristics, including kinematics, kinetics, muscle activations, and biomechanical trends across speeds and slopes, and (2) locomotor versatility across speed-slope conditions. The reflex-based and CPG-reflex-synergy-based controllers most closely reproduced experimentally observed gait characteristics, while the CPG-reflex-synergy controller achieved the broadest range of stable walking behaviors across speeds and slopes, followed closely by the reflex-based controller. These findings should be interpreted as comparisons of specific model implementations rather than definitive evaluations of the underlying biological hypotheses. Moreover, because the investigated controllers primarily focused on spinal-level mechanisms for nominal steady-state locomotion, the limited versatility observed in some of the models across broader speed and slope conditions suggests the importance of integrating spinal locomotor mechanisms with supraspinal modulation when modeling locomotion beyond nominal steady gait. To facilitate further investigation, we publicly share the simulation framework and controller implementations.

Key pointsO_LIExisting neuromechanical locomotion controllers have been difficult to compare directly because of differences in simulation frameworks.
C_LIO_LIWe implemented four representative spinal locomotion control models (reflex-based, central pattern generator (CPG)-reflex-based, muscle synergy-based, and CPG-reflex-synergy-based) within a unified simulation framework and compared their human-likeness and versatility.
C_LIO_LIThe reflex-based and CPG-reflex-synergy-based controllers best reproduced human-like gait characteristics, while the CPG-reflex-synergy-based controller demonstrated the greatest locomotor versatility across speed-slope conditions, followed closely by the reflex-based controller.
C_LIO_LIBecause the investigated controllers primarily modeled spinal-level mechanisms associated with steady-state locomotion, their reduced adaptability across broader speed and slope conditions highlights the importance of incorporating supraspinal modulation when modeling locomotion beyond nominal gait.
C_LIO_LIWe publicly share the simulation framework and controller implementations to support further investigation of human locomotion control.
C_LI

---

## 论文详细总结（自动生成）

好的，我将基于提供的论文内容，生成一份结构化的中文总结。

### 1. 论文的核心问题与整体含义

*   **核心问题**：现有的生物启发式神经力学运动控制器（如基于反射、中枢模式发生器CPG、肌肉协同等模型）难以直接比较，因为各项研究使用的肌肉骨骼模型、参数优化方法和评估标准各不相同。这种差异阻碍了对人类运动控制机制的理解。
*   **整体含义**：本研究通过在统一的仿真框架内实现并比较四种代表性的脊髓层面运动控制架构，旨在隔离控制策略本身对模拟步态行为的影响，从而为评估不同生物学假说提供一个更客观、更受控的测试平台。

### 2. 论文提出的方法论

*   **核心思想**：在共享的生物力学模型（统一的2D矢状面神经肌肉骨骼模型）、标准化优化程序（CMA-ES算法和相同的多阶段目标函数）和评估协议下，测试四种代表性控制模型的表现。
*   **关键技术细节**：
    *   **统一模拟框架**：使用MATLAB/Simulink（Simscape Multibody）构建一个7环节、9块肌肉（每条腿）的2D矢状面人体模型，包含希尔型肌肉-肌腱单元、生理传输延迟和兴奋-收缩耦合。
    *   **被比较的四种控制器**:
        1.  **基于反射**（Reflex-based）： 采用Song & Geyer (2015a)模型，完全由本体感受器、前庭和皮肤等感觉反馈通路驱动，无显式CPG。
        2.  **基于CPG-反射**（CPG-reflex-based）： 采用Ogihara & Yamazaki (2001)模型，使用Matsuoka神经振荡器产生节律驱动，并结合简化的肌梭和高尔基腱器官反馈。
        3.  **基于肌肉协同**（Muscle synergy-based）： 采用Aoi et al. (2019)模型，通过预设的肌肉协同模块和可调节的时序激活脉冲产生运动，并辅以简单的姿势与速度反馈调节器。原模型的方波脉冲被修改为平滑的钟形曲线。
        4.  **基于CPG-反射-协同**（CPG-reflex-synergy-based）： 采用Di Russo et al. (2023)模型，集成了相位重置CPG、参数化肌肉协同和Ia、Ib等脊髓反射通路。
    *   **优化流程**：所有控制器均使用协方差矩阵自适应进化策略（CMA-ES）进行参数优化，采用一个多阶段目标函数（罚函数法），依次要求：(a) 不摔倒并前进；(b) 达到周期稳定行走；(c) 达到目标速度；(d) 最小化关节极限违反和肌肉努力程度。
*   **公式或算法流程**：
    *   **多阶段目标函数 `J`**：优化过程首先确保步态稳定，然后匹配目标速度，最后才优化能量消耗。
        ```text
        J = 3C0 – Cxdist  (如果摔倒)
        J = 2C0 + CSS     (如果不稳定)
        J = C0 + CV       (如果未达到目标速度)
        J = CP + CE       (其他情况，即稳定且速度合适)
        ```
        其中，`C0 = 10^4` 是一个大常数，`Cxdist` 是前进距离，`CSS` 是步态稳定性指标，`CV` 是速度偏差，`CP` 是关节限制惩罚，`CE` 是距离归一化的肌肉激活平方积分。

### 3. 实验设计

*   **数据集/场景**：
    *   **模拟场景**：标准条件为在平地上以1.2 m/s的速度行走。为测试多功能性，速度范围从0.4 m/s逐步增加/减少，坡度范围从-35°到+21°不等。
*   **基准（Benchmark）**：
    *   **类人性**：与已发表的实验参考数据进行对比，包括：
        *   关节运动学（Rose & Gamble, 2006）。
        *   关节动力学和地面反作用力（Camargo et al., 2021）。
        *   肌肉激活模式（Perry & Burnfield, 2010）。
        *   步幅长度和能量消耗趋势（Hirasaki et al., 1999; Browning et al., 2006; Franz et al., 2012; Lankford et al., 2020）。
    *   **多功能性**：评估每种控制器能生成稳定行走的速度-坡度条件范围。
*   **对比的方法**：对上述四种控制架构（基于反射、CPG-反射、肌肉协同、CPG-反射-协同）进行头对头比较。

### 4. 资源与算力

*   文中未明确提及GPU型号或数量。
*   计算是在本地多核工作站和大学的高性能计算集群（Northeastern University's Explorer）上进行的。
*   典型的优化运行时间为本地3–10小时，集群上6–15小时，具体取决于控制器。

### 5. 实验数量与充分性

*   **实验数量**：
    1.  **名义步态对比**：4个控制器在标准条件（1.2 m/s，平地）下的步态数据对比。
    2.  **速度和坡度趋势扫描**：对成功优化的控制器进行跨速度和坡度的详尽扫描，生成步幅长度和能量消耗趋势曲线，并确定最佳步行速度和坡度。
    3.  **多功能性图谱**：系统性地探索了所有4个控制器在速度-坡度网格上的表现，绘制出成功/失败的稳定行走区域图。
*   **充分性与客观性**：
    *   **公平性措施**：通过共享模型、优化器和评估协议，确保了比较的公平性。
    *   **充分性**：实验设计系统且全面，从单点对比扩展到趋势分析再到全域扫描，层次清晰。为克服高度非凸优化中的局部最小值问题，重复了多次优化尝试。最终评估的画布（速度-坡度条件范围）比原模型各自报告的范围更广，表明统一框架充分挖掘了各模型的潜力。
    *   **潜在偏差**：作者承认，所用仿真框架改编自基于反射模型的研究，这可能引入偏差，尽管已采取措施（如修改被动膝关节力矩、调整跟腱顺应性）来减少框架特异性。

### 6. 论文的主要结论与发现

1.  **最佳类人性与多功能性**：基于CPG-反射-协同的控制器综合表现最强，既最准确地再现了人类的步态特征（与反射模型相当），又在速度和坡度适应性上实现了最广泛的范围（0.4–2.8 m/s， -30° to +21°）。
2.  **反射模型表现强劲**：基于反射的控制器紧随其后，在类人性上表现卓越，且多功能性极佳，但参数数量远少于最强的混合模型，展现出高效率。
3.  **控制结构决定行为**：表现出色的两个模型（反射、CPG-反射-协同）的共同特点是对身体机械状态和环境交互的持续、显式感官锚定（通过连续反馈或事件触发的相位重置），而表现欠佳的模型更依赖内部时序生成。
4.  **机械模型细节的重要性**：性能较弱的控制器（CPG-反射、肌肉协同）的原型开发时缺少一些关键的神经力学特征（如顺应性肌腱、传输延迟），强调了建模细节在评估控制架构时的重要性。
5.  **脊髓控制的局限性**：本研究比较的是脊髓层面的机制。部分模型在更广泛条件下的适应性有限，这表明，对于超出稳态名义步态的运动，整合脊髓上中枢的调控作用是必不可少的。

### 7. 优点

*   **高度受控的比较**：这是本研究的核心亮点，通过统一框架成功隔离了控制架构这一变量，使比较结果更有说服力。
*   **系统化与多层次评估**：评估不仅限于名义步态的静态比较，还纳入了跨速度、坡度的趋势分析和全域多功能性图谱绘制，提供了多维度、深入的性能洞察。
*   **透明度与可复现性**：作者公开分享了完整的仿真框架和所有控制器实现代码，并提供视频演示，极大促进了未来的验证、复现和扩展研究。
*   **清晰解释发现**：明确指出结果是对特定模型实现的比较，而非对生物学假说的最终裁定，避免了过度解读，且客观分析了各模型的优缺点来源。

### 8. 不足与局限

*   **模型与假设的局限性**：
    *   **2D简化**：仿真仅限于矢状面，忽略了3D运动（如髋内收/外展）和侧向平衡控制。
    *   **简化的身体模型**：上肢被建模为单一刚体，缺少足趾环节，肌肉数量有限。
    *   **单一优化目标**：最终阶段的优化主要基于肌肉努力程度最小化，若采用其他目标（如直接最小化代谢能）可能会产生不同结果。
*   **优化与泛化风险**：
    *   **局部最小值**：尽管进行了多次尝试，高度非凸的优化过程仍可能陷入局部最优，尤其是在斜坡条件下（表现为不规律的趋势曲线），难以保证找到全局最优解。
    *   **偏差风险**：尽管做了调整，框架源自反射模型研究，可能自带偏向。其中，对肌协同模型脉冲函数的修改，虽旨在提升性能，但也使其偏离了原始实现。
*   **应用限制**：研究主要针对稳态、周期性的步行模式，排除了跑步步态，未考察控制器对外部干扰的鲁棒性、步态转换等更复杂的动态行为。

（完）
