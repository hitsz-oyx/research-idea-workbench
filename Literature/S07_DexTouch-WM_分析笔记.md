# DexTouch-WM — 研究分析笔记

> 来源：https://arxiv.org/abs/2609.20649  
> 提交：2026-09-17，v2：2026-09-18

## 关键结论

DexTouch-WM 已提出动作条件的触觉世界模型，从人类触觉交互扩展到灵巧机器人；使用共享触觉布局、人体到机器人动作 retargeting、视频专家与触觉专家，并在固定 5 小时机器人数据的条件下增加 0–100 小时人类数据，评估未来视觉/几何/接触预测、策略评估和合成轨迹生成。

## 对本项目的影响

这直接覆盖了原 `IDEA-001` 的大部分表述：触觉世界模型、动作条件、人到机器人迁移、策略评估和合成轨迹。因此原 Idea 不能再以“首次组合”作为创新主张。

仍可能保留的差异化问题包括：面向抓取稳定性/滑移释放风险的风险校准、以风险触发动作重规划为终端结果、跨手型 D(R,O) 表示，以及严格的对象留出和接触阶段归因。这些仍需核验。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
package_version: research-pipeline-contract v1.0
analysis_id: AP-S07
package_id: AP-S07
created_at: 2026-10-06
source_ids: [S07]
source_identity_and_version: DexTouch-WM, arXiv 2609.20649v2
research_question: 如何用可扩展的人类触觉数据训练可迁移到灵巧机器人的动作条件世界模型？
study_type_and_context: 人类与真实机器人视触觉交互、世界模型与策略评估
design_units_samples_or_materials: 共享触觉布局的人手与灵巧机器人；固定5小时机器人监督，0–100小时人类交互
intervention_input_or_procedure: anatomy-aware tactile tokens、对齐动作条件、视频专家+触觉专家、动作retargeting
measurements_and_analysis: 机器人域视觉、几何、接触预测；策略评估和合成轨迹生成
results_with_uncertainty: 摘要声称人类数据增加可改善held-out机器人预测；完整数值和区间待复核
claim_evidence_implementation_map: arXiv摘要、PDF、HTML、TeX入口可访问；源码入口未在论文页明确给出
limitations_biases_and_ethics: workshop lightning talk；任务、硬件、传感器和原始数据需进一步核验
reproducibility_and_transferability: partial
candidate_P: [P-S07]
candidate_F: [F-S09]
evidence_index: [arxiv 2609.20649v2 lines 8-18, PDF/HTML/TeX links]
unresolved_questions: 是否报告release/slip风险校准？重规划是否以风险预警为触发？是否使用跨手型表示？
evidence_status: partial
missing_evidence: 完整实验表、源码、原始机器人触觉数据、硬件协议
next_skill: deep-read Mode C
```
