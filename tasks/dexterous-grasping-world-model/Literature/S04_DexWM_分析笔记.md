# DexWM — 研究分析笔记

> 来源：https://arxiv.org/abs/2512.13644  
> 分析时间：2026-10-06

## 1. 一句话概述

DexWM 学习由灵巧动作条件化的潜变量未来状态，并用超过 900 小时的人类和非灵巧机器人视频缓解灵巧操作数据稀缺；作者加入手部一致性损失，报告了在 Allegro gripper 上的零样本迁移。

## 2. 关键证据与限制

- F-S04：仅预测视觉特征不足以保留细粒度灵巧性，手部一致性损失有助于未来状态预测（SC）。
- F-S05：人类/非灵巧机器人视频可支持跨 embodiment 的零样本迁移（SC，部署细节待核验）。
- 结果：来源摘要声称在抓取、放置、到达任务上平均优于 Diffusion Policy 50% 以上；数值和统计口径需复核。
- 限制：摘要没有证明触觉、真实多指手闭环或滑移预测；不能直接把“零样本”推广到本项目。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
package_version: research-pipeline-contract v1.0
analysis_id: AP-S04
package_id: AP-S04
created_at: 2026-10-06
source_ids: [S04]
source_identity_and_version: DexWM, arXiv 2512.13644
research_question: 如何从大规模人类/机器人视频学习可用于灵巧操控的动作条件世界模型？
study_type_and_context: 视频潜变量预测与机器人零样本部署
design_units_samples_or_materials: 900小时以上视频；Allegro gripper部署（摘要）
intervention_input_or_procedure: 历史状态+灵巧动作预测下一潜变量状态，加入手一致性损失
measurements_and_analysis: 未来状态预测、抓取/放置/到达成功率（完整协议待核验）
results_with_uncertainty: 摘要报告相对Diffusion Policy的50%+平均优势；不确定性 unknown
claim_evidence_implementation_map: arXiv摘要可访问；代码与完整实验未核验
limitations_biases_and_ethics: 触觉与真实多指动态尚不清楚；零样本边界 unknown
reproducibility_and_transferability: partial
candidate_P: [P-S04]
candidate_F: [F-S04, F-S05]
evidence_index: [arxiv abstract lines 3-5]
unresolved_questions: 手一致性与接触力预测是否互补？视觉模型在哪些接触阶段失效？
evidence_status: partial
missing_evidence: 完整论文、代码、数据配方、部署日志
next_skill: deep-read Mode C
```
