---
title: "Reach-and-hold at a musculoskeletal arm posture is an unstable-equilibrium stabilization problem: the limits of fixed equilibrium-point and impedance controllers"
title_zh: 肌肉骨骼手臂姿势的到达并保持是一个不稳定平衡的镇定问题：固定平衡点和阻抗控制器的局限性
authors: "Kobayashi, J."
date: 2026-06-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732510v1.full.pdf"
tags: ["query:sports-sci"]
score: 7.0
evidence: 评估肌骨姿态固定的控制器，为体育相关的运动控制建模提供参考。
tldr: 肌骨手臂到达并保持固定姿态是运动控制的基本问题，但固定生物启发控制器能否实现尚未明确。本研究在MyoSuite myoArm模型上，按照冻结协议评估了多种固定非学习控制器（包括平衡点/参考λ反射、阻抗控制、重力补偿等）。结果表明，无一控制器能实现稳定近任务保持；平衡点反射可达近目标但维持极限环，阻抗控制则收敛于伪平衡点；系统加速-位置雅可比矩阵具有正实特征值，指示局部不稳定。这揭示了到达保持本质上是不稳定平衡稳定问题，固定平衡点控制器虽能设置近目标平衡点但无法稳定，因此需要学习型阻抗与预测控制来分离平衡点设定与稳定过程。
source: biorxiv
selection_source: fresh_fetch
motivation: 明确固定λ反射、阻抗控制等固定生物启发控制器在肌骨手臂到达保持任务中的可行性及其局限。
method: 在MyoSuite myoArm模型上，使用冻结标准协议评估了多种固定非学习控制器，包括平衡点反射、阻抗控制、重力补偿等。
result: 所有固定控制器均未实现稳定近任务保持；平衡点反射可达近目标但存在极限环，阻抗控制收敛于伪平衡点，系统雅可比矩阵正实特征值表明局部不稳定。
conclusion: 到达保持为不稳定动态稳定问题；固定平衡点控制器可设置近目标平衡点但无法稳定，需学习型阻抗与预测控制分离平衡点设定与稳定。
---

## 摘要
将冗余肢体保持在指定姿势以对抗重力是肌肉骨骼运动控制的一个基本问题。固定的、基于生物学的控制器能否实现这一点仍不清楚。我们在 MyoSuite myoArm 模型上，采用冻结标准、哈希来源的协议，评估了固定的非学习控制器：一个平衡点/参考（lambda）反射、一个带有共收缩的反射、一个末端笛卡尔阻抗控制器、一个重力补偿前馈以及一个精确的逆静力学重力平衡命令。无一能够实现稳定的近任务保持。受测的参考反射能够将平衡置于目标附近（在最低目标处最佳为 0.048 m），但维持了一个结构性极限环，速度阻尼未能消除；末端阻抗稳定在远离目标的假平衡点；精确的重力平衡激活虽可存在，但在实际部署时偏离。在 34 肌和 63 肌模型中评估姿势匹配的目标时，缩减的加速度-位置雅可比矩阵具有正实特征值，表明局部不稳定的二阶模态。在 34 肌模型中，完整的固定控制器网格同样未能产生稳定的近任务保持。在 63 肌模型中，测量的末端刚度在共收缩扫描中跨越人类尺度的幅度，并呈现类似人类的椭圆轴比，因此失败不能归因于模型过于松软或非生物特性。我们得出结论：到达并保持是一个不稳定动力学的镇定问题；受测的固定平衡点/参考控制器能够建立近目标的平衡，但无法稳定它。这些结果促使我们将学习型选择性阻抗和预测/内部模型控制作为下一类机制，从而将平衡的建立与镇定相分离。

## Abstract
Holding a redundant limb at a commanded posture against gravity is a basic problem in musculoskeletal motor control. Whether fixed, biologically grounded controllers can achieve it remains unclear. Using the MyoSuite myoArm under a frozen-criterion, hash-provenanced protocol, we evaluate fixed, non-learning controllers: an equilibrium-point/referent (lambda) reflex, a reflex with co-contraction, an endpoint Cartesian impedance controller, a gravity-compensation feedforward, and an exact inverse-statics gravity-balancing command. None achieves a stable near-task hold. The tested referent reflex placed a near-target equilibrium (best 0.048 m at the lowest target), but sustained a structural limit cycle that velocity damping did not cure; endpoint impedance settled at far false equilibria; and an exact gravity-balancing activation can exist while deployment falls away. At posture-matched targets evaluated in both the 34- and 63-muscle models, the reduced acceleration-position Jacobian has positive real eigenvalues, indicating locally unstable second-order modes. In the 34-muscle model, the full fixed-controller grid also fails to produce a stable near-task hold. In the 63-muscle model, measured endpoint stiffness spans human-scale magnitudes and human-like ellipse axis ratios across a co-contraction sweep, so the failure is not explained by a limp or non-biological plant. We conclude that reach-and-hold is an unstable-dynamics stabilization problem: the tested fixed equilibrium-point/referent controller can place a near-target equilibrium, but does not stabilize it. These results motivate learned selective impedance and predictive/internal-model control as the next class of mechanisms, separating equilibrium placement from stabilization.