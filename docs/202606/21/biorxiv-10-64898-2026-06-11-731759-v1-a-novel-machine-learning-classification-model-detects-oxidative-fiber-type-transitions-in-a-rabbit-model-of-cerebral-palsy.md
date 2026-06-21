---
title: A novel machine-learning classification model detects oxidative fiber type transitions in a rabbit model of cerebral palsy
authors: "Kramer, C. A., Reedich, E. J., McCann, H., Drouin, S., Sanders, D., Gonzalez, E., Ung, T., Mukisa, A., Mena Avila, E., Moline, B. C., Genry, L. T., Glennon, J. E., Quiroga, C., Dowaliby, L., DiDonato, C. J., Quinlan, K. A., Manuel, M."
date: 2026-06-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731759v1.full.pdf"
tags: ["query:sports-sci"]
score: 9.0
evidence: 用于肌纤维分类的XGBoost模型，适用于运动生理学。
tldr: 针对肌纤维类型高通量分析的需求，提出了一种基于XGBoost的新型机器学习分类模型，能够准确检测脑瘫兔模型中的氧化纤维类型转换，平衡准确率和F1值均为0.89，为肌肉生理学研究提供了有力工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 用于肌纤维分类的XGBoost模型，适用于运动生理学。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
The distribution of slow-and fast-twitch fiber types in a skeletal muscle heavily influences its physiology. Muscle biopsy studies indicate atypical fiber type composition and fiber size variation in children with cerebral palsy (CP), but subjects have variable treatment history and a variety of muscles affected, so uncertainties remain. In this study, we developed a novel machine-learning classification model to perform high-throughput fiber typing of complete transverse muscle sections. Our XGBoost algorithm-based prediction model yielded a balanced accuracy score of 0.89 and a macro F1-score of 0.89, reflecting its ability to robustly predict muscle fiber type from myosin heavy chain (MyHC) isoform immunofluorescence intensities and morphological descriptors. This is the first reported fiber type classifier to consider hybrid fibers, which is a major advance, considering at least 20% of myofibers are hybrid yet they are routinely overlooked due to difficulty in their detection. We used this classification model to define fiber types of more than 7 million myofibers from flexor-extensor muscle pairs in rabbits that experienced hypoxia-ischemia (HI) injury in utero (modeling CP), and typically developing sham rabbits. We observed an oxidative fiber type shift in flexor muscles (biceps brachii and tibialis anterior) of HI rabbits at postnatal day (P)14-20 and P30-32 (weaning age). This altered fiber type composition imparts reduced contractile force and is amenable to sustained muscle activity; it may reflect chronic low-frequency motor unit activation. This work supports prior clinical reports that developmental trajectories of muscle fibers are disrupted in CP.