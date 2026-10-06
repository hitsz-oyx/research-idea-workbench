# Scaling Cross-Embodiment World Models for Dexterous Manipulation — 全文分析

> 来源：https://arxiv.org/abs/2511.01177  
> 本地全文：`Papers/S08_Scaling-Cross-Embodiment-WM.pdf` / `.txt`

## 核心设计

将人手和机器人手表示为 3D particle 集合，将动作表示为末端粒子位移场，用图网络世界模型预测交互动态，并在粒子空间做 MPC。训练包含多种仿真手和真实人手数据；真实部署覆盖 6-DoF PSYONIC Ability Hand 与 12-DoF Robot Era XHand。

## 结果与限制

全文报告跨 embodiment 的真实塑形实验，并指出粒子图密度会影响不同手型的表现。该工作没有触觉状态建模，重点是几何/动作空间统一；因此不能回答隐蔽接触、滑移风险和失败后的预测校准问题。

## 候选 P/F

- P-S08：跨手型世界模型需要同时处理形态、动作空间和接触图密度差异。
- F-S08：粒子空间可支持不同手型的统一 MPC，但训练手型多样性和图密度影响泛化。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
analysis_id: AP-S08
source_ids: [S08]
source_identity_and_version: Scaling Cross-Embodiment World Models, arXiv 2511.01177v3
research_question: 哪种状态/动作表示可让世界模型跨人手和不同机器人手迁移？
study_type_and_context: 仿真多手型 + 两种真实机器人手，粒子图世界模型与MPC
results_with_uncertainty: 真实实验报告 Ability Hand 18/20、XHand 17/20（co-training）；完整统计已在PDF，尚未复现
candidate_P: [P-S08]
candidate_F: [F-S08]
evidence_index: [PDF abstract, Sec. III–V, Table I, Fig. 4]
limitations: 无触觉预测；未覆盖滑移/失败恢复与触觉跨传感器校准
evidence_status: verified
missing_evidence: 源码运行、完整原始轨迹、触觉扩展
next_skill: deep-read Mode C
```
