---
title: Unified comparison of spinal locomotion control architectures in neuromechanical simulations
title_zh: 神经力学模拟中脊髓运动控制架构的统一比较
authors: "Ton, V., Song, S."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731213v1.full.pdf"
tags: ["query:sb"]
score: 9.0
evidence: 在神经力学仿真中统一比较人体运动控制器
tldr: 现有神经力学模拟中的脊髓运动控制架构因模型差异难以直接比较。本研究在统一仿真框架中实现并对比了反射基础、CPG-反射基础、肌肉协同基础及CPG-反射-协同基础四种架构。结果显示，反射基础与CPG-反射-协同架构最能复现人类步态特征，后者在速度-坡度条件下步态适应范围最广。研究强调了整合脊髓上控制对拓展步态多样性的必要性，并公开框架以促进后续探索。
source: biorxiv
selection_source: fresh_fetch
motivation: 以往脊髓运动控制模型因仿真环境、优化方法等差异难以直接比较，需统一评估。
method: 在同一神经力学框架内实现四种代表性控制架构，在共享生物力学条件下对比其步态逼真度与跨速度-坡度适应性。
result: 反射基础与CPG-反射-协同控制器最似人，后者步态稳定范围最广，反射基础紧随其后。
conclusion: 综合架构表现较优，但纯脊髓模型在非典型步态下适应性有限，需引入脊髓上调制，并公开仿真工具。
---

## 摘要
神经力学模拟为研究神经控制架构如何产生和调节人体运动提供了强大框架。已提出的仿生运动控制器包括基于反射、基于中枢模式发生器（CPG）、基于肌肉协同等模型。然而，由于肌肉骨骼模型、优化方法和评估协议的差异，各研究间的直接比较仍然困难。在此，我们在统一的神经力学模拟框架中实现了四种代表性运动控制架构——基于反射、CPG-反射、肌肉协同、以及CPG-反射-协同控制器，以便在共享的生物力学和计算条件下进行受控比较。性能评估根据：(1) 与实验观测步态特征（包括运动学、动力学、肌肉激活以及不同速度和坡度下的生物力学趋势）的一致性，以及 (2) 在不同速度-坡度条件下的运动多样性。基于反射和CPG-反射-协同控制器最接近地再现了实验观测步态特征，而CPG-反射-协同控制器在速度和坡度条件下实现了最广泛的稳定行走行为范围，基于反射控制器紧随其后。这些发现应被解读为对特定模型实现的比较，而非对底层生物学假设的确定性评估。此外，由于所研究的控制器主要关注于名义稳态运动的脊髓层面机制，部分模型在更广泛的速度和坡度条件下表现出的有限多样性表明，在对超出名义稳态步态的运动进行建模时，整合脊髓运动机制与脊髓上调制的重要性。为促进进一步研究，我们公开分享了模拟框架和控制器实现。

要点
• 现有的神经力学运动控制器因模拟框架不同而难以直接比较。
• 我们在统一的模拟框架中实现了四种代表性脊髓运动控制模型（基于反射、基于中枢模式发生器（CPG）-反射、基于肌肉协同、以及CPG-反射-协同），并比较了它们的人体相似性和多样性。
• 基于反射和CPG-反射-协同控制器最佳地再现了类人步态特征，而CPG-反射-协同控制器在速度-坡度条件下展现了最大的运动多样性，基于反射控制器紧随其后。
• 由于所研究的控制器主要模拟与稳态运动相关的脊髓层面机制，它们在更广泛的速度和坡度条件下适应性降低，这凸显了在对名义步态之外的运动进行建模时纳入脊髓上调制的重要性。
• 我们公开分享模拟框架和控制器实现，以支持对人体运动控制的进一步研究。

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

## 1. 研究动机与核心问题

- **背景**：神经力学模拟是探索人体运动神经控制机制的关键途径，已提出多种仿生脊髓运动控制器，如基于反射、基于中枢模式发生器（CPG）、基于肌肉协同等。
- **核心问题**：已有研究因采用的肌肉骨骼模型、优化方法与评估方案各不相同，难以对这些控制器进行直接、公平的比较，从而无法判断何种架构在复现人类步态方面更具优势。
- **整体含义**：亟需一个统一的框架，在共享的生物力学与计算条件下，对代表性控制架构进行受控对比，以识别各自的仿生能力与局限性。

## 2. 方法论

- **核心思想**：在同一神经力学模拟环境中实现并比较四种代表性的脊髓运动控制架构，避免因外部条件差异引起的不可比性。
- **关键技术细节**：
  - **统一仿真框架**：固定肌肉骨骼模型、物理环境、求解器与评估协议。
  - **四种控制架构**：
    1. **反射基础控制器**（reflex-based）：仅依靠感觉反馈驱动的反射环路产生运动。
    2. **CPG-反射基础控制器**（CPG-reflex-based）：在反射基础上引入中枢模式发生器作为节律性节拍。
    3. **肌肉协同基础控制器**（muscle synergy-based）：使用少量肌肉协同基底（synergies）驱动肌肉激活。
    4. **CPG-反射-协同基础控制器**（CPG-reflex-synergy-based）：综合CPG、反射与肌肉协同的复合架构。
  - **算法/流程**（文字描述）：对于每个控制器，先在名义条件下进行参数优化，使其产生稳定的类人步态；随后在不同速度和坡度组合下进行前向动力学模拟，检验步态稳定性与适应性。评估不依赖特定训练数据集，而是通过与实验步态特征（关节运动学、地面反作用力、肌肉激活模式及其随条件的趋势）的吻合度进行定量比较。
  - 所有控制器聚焦于脊髓层面的稳态运动机制，未引入高级中枢的在线调制。

## 3. 实验设计

- **实验场景与Benchmark**：
  - 以**人体正常行走实验数据**作为参考标准，涵盖不同行走速度（如慢速、正常、快速）和不同坡度（如平路、上坡、下坡）下的运动学、动力学及肌电信号特征。
  - 性能基准包括：（1）与实测步态特征（关节角度、关节力矩、肌肉激活时序等）的一致性；（2）在速度-坡度组合空间中的运动多样性（即能够稳定行走的条件范围）。
- **对比方法**：在同一生物力学模型上实现的四种架构之间互相比较，同时与实验基准对比。无外部其他控制器作为竞争者，研究本身即为四种假说之间的横向对比。

## 4. 资源与算力

- **未明确说明**：摘录内容及元数据中均未提及所用 GPU 型号、数量、训练或仿真时长等计算资源信息。考虑到该研究基于神经力学模拟，可能主要消耗 CPU 资源用于运动学动力学求解与优化，但论文本身未在已提供文本中给出具体硬件配置与计算开销。

## 5. 实验数量与充分性

- **实验类型与数量**（基于文本推断）：
  - 四种控制架构各自需在名义条件下进行参数优化，获得稳定步态。
  - 随后在**多种速度与坡度组合**（具体组合数未说明，但强调“跨速度-坡度条件”）下进行步态模拟，评估稳定范围。
  - 每个可行条件下均提取运动学、动力学与肌肉激活，并与实验趋势对比。
- **充分性与公平性**：所有控制器共享同一生物力学模型、同一虚拟环境与同一评估标准，消除了模型差异带来的干扰。对比设计客观，但具体条件数量未知，可能不足以覆盖极端步行场景。研究明确声明仅比较特定模型实现，不做生物学假设的最终裁决，表明了对结论泛化性的谨慎态度。整体实验设计能够支撑核心结论，但细节是否足够丰富（如消融研究、灵敏度分析）未在摘要中体现。

## 6. 主要结论与发现

- **类人步态复现度**：反射基础控制器与 CPG-反射-协同基础控制器最接近实测人类步态特征。
- **运动多样性**：CPG-反射-协同控制器实现了最宽泛的稳定行走条件范围（速度和坡度），反射基础控制器紧随其后。
- **脊髓控制的局限**：四种控制器均主要模拟脊髓层面的稳态步态机制，导致在超出名义步态的条件（极端速度/坡度）下适应性普遍下降。
- **脊髓上调制的重要性**：结果预示，若要对非稳态、大范围变化的运动进行建模，必须整合脊髓上中枢的调制信号。
- **研究性质申明**：上述结论是对特定实现方式的比较，不应等同于对底层生物学控制假说的最终评判。

## 7. 优点

- **统一比较平台**：首次在严格控制的条件下系统对比多种脊髓运动控制架构，解决了领域内长期存在的不可比性问题。
- **综合评估指标**：同时从步态逼真度（与实验吻合度）和运动多样性两个维度进行评价，避免了单一标准的偏颇。
- **公开共享资源**：承诺公开模拟框架与控制器实现，极具促进复现与后续研究的意义。
- **研究审视的诚实性**：明确区分“模型实现比较”与“生物学假说正确性验证”，减少了过度解读的风险。

## 8. 不足与局限

- **模型覆盖范围**：仅选取了四种代表性控制器，其他可能的混合或新型控制结构未纳入比较。
- **条件边界未探究**：摘要未说明具体测试了多少步态速度和坡度条件，可能未系统覆盖跌倒边界或特殊地形（如不平路面、转向）。
- **无脊髓上控制**：研究主动将比较限定在脊髓层面，这既是聚焦也是局限——无法量化脊髓上输入对提高适应性的具体贡献。
- **缺乏训练算力与优化细节**：未报告优化过程中的计算开销、收敛性分析及参数敏感性，复现时可能遇到实施模糊性。
- **效度考量**：仅限于人体正常行走的比较，对于跑步、特殊步态或病理步态的适用性尚不清楚。

（完）
