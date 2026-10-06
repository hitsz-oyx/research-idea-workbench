# DexGrasp Anything — 研究分析笔记

> 来源：https://openaccess.thecvf.com/content/CVPR2025/html/Zhong_DexGrasp_Anything_Towards_Universal_Robotic_Dexterous_Grasping_with_Physics_Awareness_CVPR_2025_paper.html  
> 分析时间：2026-10-06

## 1. 一句话概述

该工作把物理约束放入扩散抓取模型的训练和采样阶段，并发布超过 340 万抓取姿态、覆盖超过 1.5 万对象的数据集，目标是通用灵巧手抓取。

## 2. 可用证据

- 任务：从高自由度手和多样物体中生成可用抓取姿态。
- 方法：物理约束扩散生成，训练与采样同时施加约束。
- 数据：CVPR 页面摘要报告 3.4M+ 姿态、15k+ 对象。
- 边界：静态姿态的物理可行性并不等价于真实执行中的接触稳定；触觉、时间动态和世界模型闭环未由摘要证明。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
package_version: research-pipeline-contract v1.0
analysis_id: AP-S03
package_id: AP-S03
created_at: 2026-10-06
source_ids: [S03]
source_identity_and_version: DexGrasp Anything, CVPR 2025
research_question: 如何在大规模对象分布上生成物理可行的通用灵巧手抓取姿态？
study_type_and_context: 生成模型与多数据集抓取评估
design_units_samples_or_materials: 3.4M+姿态、15k+对象（来源摘要）
intervention_input_or_procedure: 训练和采样阶段的物理约束扩散
measurements_and_analysis: 穿透、成功率、多样性等基准指标（完整数值待核验）
results_with_uncertainty: 来源称多数公开数据集SOTA；完整表格与不确定性待核验
claim_evidence_implementation_map: CVPR官方摘要与PDF可定位，源码链接已给出但未运行
limitations_biases_and_ethics: 静态生成与动态闭环之间存在未验证接口
reproducibility_and_transferability: partial
candidate_P: [P-S03]
candidate_F: [F-S03]
evidence_index: [CVPR2025 official abstract]
unresolved_questions: 静态物理约束能否预测滑移？世界模型能否利用生成姿态作为先验？
evidence_status: partial
missing_evidence: 代码复现、真实硬件协议、动态接触数据
next_skill: deep-read Mode C
```
