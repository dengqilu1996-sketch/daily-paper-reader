---
title: Synergy-based Feedforward with Minimal Feedback Control Predicts Walking Over Multiple Cycles
title_zh: 基于协同的前馈与最小反馈控制预测多周期行走
authors: "Williams, S. T., Li, G., Fregly, B. J."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.02.709098v2.full.pdf"
tags: ["query:sb"]
score: 9.0
evidence: 开发个性化协同前馈-反馈控制模型用于行走模拟，直接贡献于肌骨建模与仿真。
tldr: "神经反馈在运动控制中至关重要，许多神经系统疾病伴随其异常，但现有的计算模型很少基于真实患者个体化数据，难以临床转化。本研究构建了中风后患者的个性化行走模型，提出基于肌肉协同的前馈与最小反馈组合控制。通过预测模拟，只有前馈占比75%以上的模型能复现近周期步态，且100%前馈最准确。这表明实际人体行走预测需要大量前馈控制，为患者特异性治疗设计奠定了基础。"
source: biorxiv
selection_source: fresh_fetch
motivation: 目前神经肌肉骨骼模型很少代表真实患者，难以临床应用，需开发个性化模型探索神经控制机制。
method: 利用中风患者实验数据，创建个性化三维行走模型，设计基于肌肉协同的前馈与最小反馈控制器，缩放前馈贡献并拟合反馈。
result: "75%及以上前馈模型能预测近周期行走，100%模型最准确；低于75%则需偏离实验初始条件才可行。"
conclusion: 个性化行走预测依赖于充足的前馈控制，提示在神经损伤后步态康复中应重视前馈机制的作用。
---

## 摘要
神经反馈对于运动控制至关重要，多种神经系统疾病（如中风、脑瘫、帕金森病、不完全性脊髓损伤）的特征是神经反馈发生改变。研究人员已创建了大量由模拟神经反馈机制控制的神经肌肉骨骼计算模型，但这些模型很少代表实际人类受试者，因此未找到实际临床应用。作为为神经系统疾病患者设计个性化治疗方案的一步，本研究使用神经肌肉骨骼建模流程，基于一名实际中风后人类受试者的个性化三维神经肌肉骨骼行走模型，开发并评估了一种新颖的基于协同的前馈（FF）+反馈（FB）控制模型。从该受试者收集的实验行走数据被用于创建该受试者的个性化行走模型。然后，针对5个校准行走周期，创建了个性化的基于协同的FF+FB控制模型。首先，使用个性化模型估计与该受试者的肌电图、关节运动和关节力矩数据一致的下肢肌肉激活。其次，计算出每条腿的五个协同激活及其相关协同向量，这些接近地同时重建了受试者的肌肉激活和关节力矩。第三，通过对每条腿的协同激活进行平均，计算名义FF协同激活控制。第四，将名义FF协同控制按0%、25%、50%、75%、100%和125%进行缩放，通过将FB协同激活控制拟合为关节位置、速度和力矩的函数（作为肌肉长度、肌肉速度和肌腱力的替代），填补再现受试者肌肉激活的缺口。接下来，针对3个测试行走周期，使用六种基于协同的FF+FB模型在预测性仿真中控制受试者的个性化行走模型。100% FF模型（仍具有最小反馈）最接近地再现了测试行走周期，并且只有75%、100%和125% FF模型使用与实验值一致的初始条件预测出了近似周期性的行走运动。0%、25%和50% FF模型只有在允许初始条件与实验值有较大偏离时，才能生成近似周期性的行走运动。我们的发现表明，在对实际人类受试者建模时，行走的预测性仿真可能需要大量的前馈控制。

## Abstract
Neural feedback is important for the control of movement, and multiple neurological disorders (e.g., stroke, cerebral palsy, Parkinson's disease, incomplete spinal cord injury) are characterized by altered neural feedback. Researchers have created numerous computational neuromusculoskeletal models controlled by simulated neural feedback mechanisms, but these models rarely represent actual human subjects and thus have not found practical clinical application. As a step toward designing patient-specific treatments for individuals with neurological disorders, this study used the Neuromusculoskeletal Modeling Pipeline to develop and evaluate a novel synergy-based feedforward (FF)+feedback (FB) control model using a personalized three-dimensional neuromusculoskeletal walking model of an actual human subject post-stroke. Experimental walking data collected from the subject were used to create the subject's personalized walking model. Then for 5 calibration walking cycles, personalized synergy-based FF+FB control models were created. First, the personalized model was used to estimate lower body muscle activations consistent with the subject's electromyographic, joint motion, and joint moment data. Second, five synergy activations per leg with associated synergy vectors were calculated that closely reconstructed the subject's muscle activations and joint moments simultaneously. Third, nominal FF synergy activation controls were calculated by averaging the synergy activations for each leg. Fourth, the nominal FF synergy controls were scaled by 0, 25, 50, 75, 100, and 125%, and the gap in reproducing the subject's muscle activations was filled by fitting FB synergy activation controls as a function of joint positions, velocities, and moments as surrogates for muscle lengths, muscle velocities, and tendon forces. Next, for 3 testing walking cycles, the six synergy-based FF+FB models were used to control the subject's personalized walking model in predictive simulations. The 100% FF model (which still had minimal FB) reproduced the testing walking cycles the most closely, and only the 75%, 100%, and 125% FF models predicted near-periodic walking motions using initial conditions consistent with experimental values. The 0, 25, and 50% FF models could generate near-periodic walking motions only when the initial conditions were allowed to diverge substantially from experimental values. Our findings suggest that predictive simulations of walking may require substantial feedforward control when modeling an actual human subject.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将使用中文，以 Markdown 格式对提供的论文进行结构化、深入且客观的总结。

### 1. 论文的核心问题与整体含义 (研究动机和背景)
*   **核心问题**: 在模拟真实人类个体行走时，神经控制中前馈控制和反馈控制各自需要多少贡献？特别是，仅靠反馈控制是否足够，还是需要大量的前馈控制？
*   **研究动机**: 神经反馈对运动控制至关重要，其功能障碍是中风、脑瘫等多种神经疾病的特征。现有的神经肌肉骨骼计算模型虽然模拟了反馈机制（如牵张反射），但它们大多未基于真实患者数据个性化，因此难以在临床上应用，为患者设计特异性治疗方案。
*   **整体含义**: 本研究作为一个关键的中间步骤，旨在开发和评估一种能复现真实个体行走的个性化神经控制模型，并探究前馈与反馈控制的相对贡献，最终目标是促进针对神经损伤后运动障碍的个性化治疗方案设计。

### 2. 论文提出的方法论 (核心思想、关键技术细节、公式或算法流程)
*   **核心思想**: 提出一种新颖的、基于肌肉协同的“前馈+反馈”分层控制模型。前馈部分提供基线命令，反馈部分则根据感官信息进行在线修正，两者都作用于肌肉协同层面，而非单个肌肉层面。
*   **关键技术流程**:
    1.  **模型个性化**: 使用`Neuromusculoskeletal Modeling (NMSM) Pipeline`，基于一名中风后受试者的实验数据，分步构建其高度个性化的三维神经肌肉骨骼行走模型。这包括骨骼几何、关节、足地接触、肌肉-肌腱参数和神经控制模型的个性化。
    2.  **肌肉协同分解**: 从估算出的时变肌肉激活模式中，使用非负矩阵分解等方法提取出**5个肌肉协同及其激活系数**。协同向量在双腿间共享，从而使受试者的不对称控制体现在协同激活上。
    3.  **构建协同控制器**:
        *   **前馈(FF)控制**: 校准用步态周期的平均协同激活，作为名义前馈协同激活控制。
        *   **反馈(FB)控制**: 将名义FF控制按比例缩放（0%, 25%, 50%, 75%, 100%, 125%），并将剩余的“协同激活缺口”拟合为**关节角度、角速度和关节力矩**的线性函数，以此作为简化的神经反馈模型。
        *   **反馈拟合公式**: $[1, q, \dot{q}, M] \times [K_c, K_q, K_{\dot{q}}, K_M]^T = s$，其中 $s$ 是协同激活缺口，$q, \dot{q}, M$ 等为关节级感觉信号，$K$ 为待拟合的反馈增益。
        *   为使病态方程组可解，在MATLAB中使用`lsqnonlin`求解时加入了正则化项以惩罚过大的反馈增益。
    4.  **预测性仿真**: 将组合好的FF+FB控制器应用于个性化模型，使用直接配置法进行预测性仿真，复现测试步态周期。

### 3. 实验设计 (数据集/场景、基准和方法对比)
*   **数据集**: 已发表的一名79岁男性中风幸存者（右侧偏瘫）的数据集。数据包括在跑步机上以0.5 m/s自选速度行走时的运动捕捉、地面反作用力和16块下肢肌肉的肌电图数据。
*   **训练/测试划分**: 从30秒的行走数据中，选取了8个干净的步态周期，其中**5个用于模型校准**（训练集），**3个用于评估预测能力**（测试集）。
*   **基准**: 预测性仿真的准确性通过**均方根误差**来量化，比较对象是经过扭矩驱动追踪优化处理后得到的、动态一致的参考关节角度、关节力矩和地面反作用力。
*   **方法对比**: 核心实验对比了在**6个不同的前馈控制缩放水平**（0%, 25%, 50%, 75%, 100%, 125%）下，FF+FB模型的仿真结果。同时也进行了消融实验，对比了100%纯FF（无FB）和75%纯FF（无FB）的性能。

### 4. 资源与算力
*   文中**未明确提及**使用的具体GPU型号、数量或总体训练时长。
*   仅定性地提到，追踪优化问题在满足约束的前提下，能在**“几个小时内”**收敛。这表明其计算需求对于现代工作站是可接受的，但需数小时的计算时间。

### 5. 实验数量与充分性
*   **实验数量**: 主要包括以下几个层面的实验：
    *   **主要实验**: 6组不同FF缩放水平的仿真（每组预测3个测试周期），这是研究的核心分析。
    *   **条件变更实验**: 对不成功的低FF模型（0%, 25%, 50%），进行了放宽初始条件约束的重复实验。
    *   **消融实验**: 进行了2次额外的关键消融实验——100% FF无FB，以及75% FF无FB的预测仿真。
*   **充分性评估**: 实验设计相对充分且目标明确。通过梯度缩放FF占比，系统地研究了核心问题。通过放宽初始条件和无FB消融实验，深化了对模型行为的理解。实验对比了多个量化指标（关节角度、力矩、地面反力误差，以及R²），较为客观。然而，实验**仅基于单一受试者单一速度的行走数据**，这在一定程度上限制了结论的普适性。

### 6. 论文的主要结论与发现
*   **需要大量前馈控制**: 预测性模拟结果显示，只有当前馈控制占比达到或超过75%（特别是100%）时，模型才能在使用与实验值一致的初始条件下，成功预测出近周期性的行走运动。
*   **100%前馈控制表现最优**: 在所有成功案例中，100%前馈结合最小反馈的模型最准确地复现了测试步态周期中的关节运动、力矩和地面反力。
*   **低前馈控制的替代行为**: 在0%-50%的前馈比例下，模型只有在初始条件允许大幅偏离实验值时才能产生周期性行走，但其步态模式（如步宽更大、步幅更短）与真实步态存在显著视觉差异。
*   **反馈贡献量化**: 若从控制信号的实际数值中分离计算，最成功的100% FF模型的反馈控制贡献仅为**约2-5%**，非常微小。
*   **临床意义启示**: 研究结果表明，对于真实的人体行走，脊髓和脑干水平的反馈控制可能不足以完全补偿前馈下行命令的缺失，这为卒中后等行走障碍的康复治疗重点提供了新的见解。

### 7. 优点 (方法或实验设计上的亮点)
*   **高保真度与个性化**: 构建了从骨骼到肌肉再到足地接触的全方位、高度个性化的三维神经肌肉骨骼模型，这是区别于以往使用简化或通用模型的同类研究的一大进步。
*   **基于真实患者数据**: 整个建模流程，包括前馈和反馈控制器的参数，都源自于一位实际中风患者测量的运动学、动力学和肌电数据，增强了临床相关性。
*   **模型实用性与简化**: 采用关节级感觉信号和肌肉协同作为反馈与控制单元，形成了生理上可解释且数学上更为简洁的双重简化，这为未来更复杂反馈模型的构建提供了可行的中间步骤和对比基准。
*   **方法透明与可复现**: 所有代码、数据和结果均开放获取，并详细描述了优化问题的公式与设置，提高了研究的透明度和可复现性。
*   **严格的动态一致性**: 通过追踪优化和预测仿真的约束，保证了生成的运动是动态一致的，避免了纯运动学复现的物理不可行性。

### 8. 不足与局限 (实验覆盖、偏差风险、应用限制等)
*   **反馈模型过度简化**: 使用关节层面的信号作为反馈输入，忽略了肌肉特异性反馈（如肌梭、高尔基腱器），而后者被认为是关键的生理机制。
*   **缺乏时间延迟**: 反馈模型是瞬时的，未包含已知的神经信号传导和处理延迟，这可能影响其对动态变化的预测能力。
*   **肌腱模型刚性**: 肌肉模型采用刚性肌腱，未考虑肌腱的柔顺性和肌肉的短程刚度，这可能降低在冲击或快速运动下的仿真精度。
*   **样本量与外推性局限**: 研究仅基于**单一名受试者的单一慢速行走数据**。所得结论（如需要大量FF）和具体拟合的模型参数能否推广到其他个体、其他速度或任务均有待验证。
*   **控制自由度缺失**: 模型未能完全控制或准确模拟某些关键自由度，如髋关节内旋/外旋，导致该自由度在仿真中可能不切实际，反映出模型在力矩臂或肌肉强度参数上可能仍存在误差。
*   **模型校准与测试**: 反馈模型是在几乎完美拟合的校准数据上训练的，但研究发现这种完美拟合反而不利于泛化到新的测试周期，这揭示了过拟合的风险和变异性训练数据的重要性。

（完）
