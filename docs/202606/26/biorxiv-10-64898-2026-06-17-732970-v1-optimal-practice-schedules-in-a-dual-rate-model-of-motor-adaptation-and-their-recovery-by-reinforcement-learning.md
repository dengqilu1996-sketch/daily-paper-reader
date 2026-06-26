---
title: "Optimal Practice Schedules in a Dual-Rate Model of Motor Adaptation, and Their Recovery by Reinforcement Learning"
title_zh: 双速率运动适应模型中的最优练习安排及其通过强化学习的恢复
authors: "Jeter, R., Todorov, D., Molkov, Y."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.732970v1.full.pdf"
tags: ["query:sports-sci"]
score: 10.0
evidence: 利用强化学习优化运动适应的练习安排，基于双速率计算模型
tldr: 训练安排常面临获取与保留的权衡，传统blocked与interleaved无法覆盖所有情况。本文基于双速率记忆模型，计算最优练习调度，发现其随保留权重呈交替、混合及带晚期纠正的blocking三种模式，长会话呈现利用-修复-交错结构。进一步用PPO从观察中学习策略，揭示了获取主导区域的崩溃及亚稳态性，并证实少量行为历史即足够规划。为设计有限时间练习以促进长期保留提供了新框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 超越blocked与interleaved简单二分法，依据学习者内部记忆状态动态优化练习调度以提升长期保留。
method: 采用双速率模型（快速共享与慢速情境特异性成分）计算最优序列，用结构束搜索近似长会话解，并用PPO从交互中学习调度策略。
result: 最优调度呈现三种模式：交替、混合、带晚期纠正的blocking；PPO在获取主导区域陷入纯blocking，揭示策略梯度亚稳态性。
conclusion: 练习调度应权衡获取与保留，动态调整；强化学习教师可部分恢复最优策略，但需克服亚稳态，为教学与康复提供设计原则。
---

## 摘要
临床医生指导中风患者进行45分钟的康复治疗，教练规划一天的训练，老师选择练习题的顺序，他们都面临着同样的问题：“鉴于目前练习的所有内容，下一个试验应该是什么？”运动学习文献提供了两种粗略的答案：集中练习和交错（“随机”）练习，有一个众所周知的分离现象：集中练习能更快获得技能但保留较差，而交错练习则相反。我们认为，这种分离不是练习安排的固有特性，而是一个更丰富结构的影子。特别是，对于记忆具有快速共享成分和较慢的情境特定成分的学习者，最佳安排应是学习者当前内部状态和距离保留测试剩余时间的函数。我们在一个最小的双情境快-慢学习者模型中精确地说明了这一点，对于短时训练，其最优安排可以精确计算，对于较长时间则通过结构化束搜索上界近似。最优安排不是集中练习，也不是交错练习，也不是单一规则；它是一族安排，由保留相对于获得的权重决定。该族有三个区域（交替、混合、带有后期修正的集中练习），对于长时间训练，最优安排具有可解释的结构——利用一种情境，修复被忽视的情境，然后交错练习以锁定保留。然后，我们研究了一位强化学习教师，它只观察学习者的动作和错误，无法访问其内部记忆状态，能否仅从交互中学习这些最优策略。将习得的策略与精确最优解比较，我们表明，一个无模型智能体（PPO）在中间区域恢复了短时程安排和长时程的“集中-修复-交错”模式，但基准测试也揭示了在获得主导区域中的显著失败，其中PPO崩溃为纯粹的集中练习，且遗漏了稀疏的末端修正。热启动诊断显示，这种失败是策略梯度的真实亚稳态，而非调参伪迹，集中加切换和纯集中练习充当相互竞争的吸引子，PPO无法在两者之间稳定。对观察历史的超参数扫描揭示，智能体只需要很少的行为背景就能进行最优规划，表明部分可观测性并非寻找最优练习安排的主要障碍。最后，我们讨论了该框架对运动适应和情境干扰的影响，为教师如何设计有限的练习课程以促进长期保留提供了实践见解。

## Abstract
A clinician guiding a stroke patient through a 45-minute rehabilitation session, a coach planning a training day, a teacher choosing the order of practice problems, they all face the same question: "given everything practiced so far, what should the next trial be?" The motor-learning literature offers two coarse answers, blocked and interleaved ("random") practice, with a well-known dissociation, blocked practice gives faster acquisition but worse retention, while interleaved practice gives the opposite. We argue that this dissociation is not a fixed property of practice schedules but a shadow of a richer structure. In particular, for a learner whose memory has a fast shared component and slower context-specific components, the best schedule should be a function of the learners current internal state and the time remaining before the retention probe. We make this precise in a minimal two-context fast-slow learner model whose optimal schedules can be computed exactly for short sessions and approximated by a structured beam-search upper bound for longer ones. The optimal schedule is not blocked, not interleaved, and not a single rule; it is a family of schedules determined by how much retention is weighted relative to acquisition. The family has three regimes (alternating, mixed, blocked-with-late-correction) and for long sessions, the optimal schedule has an interpretable structure -- exploit one context, repair the neglected one, then interleave to lock in retention. We then investigate whether a reinforcement-learning teacher, observing only the learners actions and errors without access to their internal memory states, can learn these optimal policies from interaction alone. Comparing these learned policies against the exact optima, we show that a model-free agent (PPO) recovers the short-horizon schedules and the long-horizon block-repair-interleave motif in the intermediate regime, but the benchmark also exposes a sharp failure in the acquisition-dominated regime, where PPO collapses to pure blocking and misses a sparse terminal correction. A warm-start diagnostic shows this failure is a genuine metastability of policy gradients rather than a tuning artifact, with blocked-plus-switch and pure-blocked acting as competing attractors that PPO cannot stabilize between. A hyperparameter sweep over observation history reveals that the agent requires very little behavioral context to plan optimally, demonstrating that partial observability is not a major barrier to finding optimal practice schedules. Finally, we discuss the implications of our framework for motor adaptation and contextual interference, offering practical insights on how instructors can design finite practice sessions to favor long-term retention.

---

## 论文详细总结（自动生成）

# 论文深度分析：双速率运动适应模型中的最优练习安排及其通过强化学习的恢复

## 1. 论文核心问题与整体含义

- **研究动机**：在实际的运动技能教学与康复训练中（如教练规划训练、教师安排练习顺序、康复师指导中风患者），均面临一个根本问题：“基于当前已练过的所有内容，下一个试次应安排何种任务？”传统运动学习文献给出的答案往往过于二元：**集中练习（blocked）** 获得快但保留差，**交错练习（interleaved）** 保留好但获得慢。论文认为这种分离并非练习安排的固有属性，而是更深层、更丰富的结构的一种表象。
- **核心论点**：对于内部记忆包含“快速共享成分”与“较慢特定情境成分”的学习者，最优练习安排应是**学习者当前内部状态**和**距离保留测试剩余时间**的函数，而不应被简化为阻塞或交错两种极端。
- **研究目标**：
  1. 在最小双情境快-慢学习者模型中，精确刻画最优练习安排的族谱结构与变化规律。
  2. 探究**仅观察行为错误、无法访问内部记忆状态**的强化学习教师，能否仅从交互中恢复这些最优策略，并揭示其可能失败的情形及原因。
  3. 为实际教学设计提供有限练习时间内促进长期保留的原则性指导。

## 2. 方法论

- **核心模型：双速率状态空间模型**
  - 学习者的记忆被建模为一个具有双时间尺度的动态系统：
    - **快速共享成分**：跨任务泛化快但消退也快。
    - **慢速情境特定成分**：任务特异性强保留持久，但积累缓慢。
  - 模型以微分/差分方程描述内部状态的演化，其参数决定了获取-保留的权衡。
- **最优练习序列的求解**
  - **短会话**：通过精确动态规划或穷举搜索，计算获得最大化最终保留（或带权重的获得+保留目标）的最优任务序列。
  - **长会话**：因状态-动作空间呈指数增长，使用**结构化束搜索（structured beam search）** 方法获得一个上界逼近最优序列。
  - 优化目标函数由“保留”相对于“获得”的权重参数化，形成**一族最优调度**，而非单一种类。
- **强化学习教师的策略学习**
  - **环境设定**：教师（Agent）观察学习者的动作与错误历史（一段行为序列），但无权访问其内部快速/慢速记忆状态。
  - **算法**：采用无模型强化学习方法 **PPO（Proximal Policy Optimization）**，在交互中学习一个策略网络，输出下一试次的任务选择。
  - **对比与诊断**：将PPO所学策略与模型的最优解直接对比，并通过“热启动”诊断探究PPO可能的失败模式（亚稳态性/策略梯度吸引子问题）。
  - **观察历史超参数扫描**：系统改变输入给智能体的历史行为长度，以评估部分可观测性对策略恢复的影响。

## 3. 实验设计

- **任务场景与数据集**：
  - 场景为**双情境运动适应**的简化计算模拟实验，并非基于真实人体运动数据，而是基于快-慢内部模型生成合成交互数据。
  - “数据集”即为在给定学习模型下，按特定策略生成的试次-错误序列。
- **Benchmark（基准）**：
  - 以**模型底层状态完全可观测时的精确最优调度**（短会话为精确解，长会话为束搜索上界）作为“金标准”。
  - 对比对象包括：传统的集中练习、交错练习，以及PPO发现的策略。
- **对比方法**：
  - **精确最优解（Exact/Beam-search Optimal）**：内部状态完全已知。
  - **PPO策略（PPO Learned Policy）**：仅从行为观察中学习。
  - 隐含对比：经典训练安排（阻塞、交错）。
- **分析的区域划分**：
  - 根据“保留 vs 获取”目标权重，将最优调度族划分为三种定性模式：
    1. **交替模式（Alternating）**
    2. **混合模式（Mixed）**
    3. **带有后期修正的集中模式（Blocked-with-late-correction）**
  - 对于长会话，进一步呈现“利用—修复—交错”（exploit–repair–interleave）的可解释结构。

## 4. 资源与算力

- **文中未明确提及**所使用的具体GPU型号、数量或详细的训练时长。论文属于计算建模与算法仿真类别，但未在所提供的摘要和元数据中交代具体的算力配置。可能在正式稿或附录中有说明，此处依据目前信息标注为“未明确说明”。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 短会话最优调度族计算（覆盖不同权重）。
  - 长会话束搜索最优调度。
  - PPO策略学习并进行短/长期任务、不同权重区域的对比。
  - **消融/诊断实验**：
    1. **热启动诊断**：考察PPO的亚稳态性，展示纯阻塞与阻塞加切换作为竞争吸引子。
    2. **观察历史长度超参数扫描**：验证对策略质量的影响。
- **充分性与客观性**：
  - 从模型角度看，实验设计较系统：覆盖了从完全可观测最优到部分可观测强化学习的对比，并深入分析了PPO失败的动力学原因（亚稳态），而非仅报告最终性能。
  - 对比基准清晰，且对失败模式进行了独立诊断，具有一定客观性。
  - 局限在于**所有实验均基于仿真模型**，未涉及真实人类行为数据验证，外部有效性待进一步检验。

## 6. 主要结论与发现

- **最优调度不是单一策略，而是一个依赖于保留权重的族**，呈现三种定性相变：交替、混合、带后期纠正的集中练习。
- **长会话调度具有“利用—修复—交错”的有组织结构**：先利用强记忆的情境，再修复被忽视的另一情境，最后交错练习以巩固长期保留。
- **PPO能在中等权重区域成功恢复最优策略**，包括短时程任务和长时程的“阻塞-修复-交错”模式。
- **PPO在“获得主导”（重获取轻保留）区域出现严重失败**：策略崩溃为纯集中练习，遗漏了稀疏的末端修正。热启动分析表明这是一种**策略梯度的真亚稳态**，集中加切换与纯集中形成两个竞争吸引子，PPO无法在其间稳定。
- **部分可观测性并非主要障碍**：历史长度扫描显示，智能体仅需极少量行为上下文即能实现最优规划，意味着即使无法观测内部状态，行为历史足以提供规划所需信息。

## 7. 优点

- **理论深度与新颖性**：超越传统的“阻塞 vs 交错”二分法，从动态学习和最优控制角度重新定义练习安排问题，提出一套基于状态的、自适应的时间规划框架。
- **方法融合与验证**：将认知计算模型（双速率记忆）与强化学习（PPO）有机结合，并用精确最优解作为基准进行系统性偏差分析，方法论缜密。
- **可解释的结构发现**：“利用—修复—交错”的长会话最优模式具有直观教学设计意义，为实践提供了清晰原则。
- **诊断性分析**：对PPO失败的亚稳态分析具有较强洞察力，揭示了算法级的根本限制，而不仅是参数调优问题。

## 8. 不足与局限

- **模型简化与外部效度**：所有结论基于最小双情境快-慢模型，未在人类真实运动适应数据上进行验证。模型的假设（如具体时间常数、线性/非线性形式）可能与生物学习者有差距。
- **状态与任务空间有限**：仅考虑两个任务情境，现实教学中的任务数量庞大且存在复杂转移关系，可扩展性尚未证明。
- **无感知/认知限制**：模型未考虑学习者的注意力波动、疲劳、元认知等真实因素，这些可能在实际应用中显著影响最优调度。
- **算力细节缺失**：从提供的材料中看不出PPO训练的具体计算预算和超参配置，不利于复现或评估其实操难度。
- **仅覆盖无模型RL**：虽然PPO体现了部分可观测下的学习，但未探索有模型RL或贝叶斯最优实验设计等替代方法，这些方法可能在数据效率或失败模式上有不同表现。

（完）
