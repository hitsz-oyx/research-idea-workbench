# DexTacWAM — 全文分析

> 来源：https://arxiv.org/abs/2609.24976  
> 本地全文：`Papers/S12_DexTacWAM.pdf` / `.txt`

## 核心设计

在 22-DoF 双手平台上逐指编码触觉，用 finger/pose-aware compressor 接入视频世界模型，并将预测的联合视觉—触觉 latent 直接提供给动作专家。六个接触丰富任务平均 70.6，强基线 38.0；约 4 小时触觉编码适配、每任务约 100 个演示。

## 失败现象与限制

附录明确指出训练主要使用成功演示；进入未见失败状态后预测和动作质量会同时恶化。作者将失败/恢复数据作为未来工作，并指出跨传感器、跨 embodiment 预训练仍待研究。这是本轮最直接的“意外现象”来源。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
analysis_id: AP-S12
source_ids: [S12]
source_identity_and_version: DexTacWAM, arXiv 2609.24976v1
research_question: 如何把多指触觉接触演化纳入视频世界动作模型并高效用于控制？
study_type_and_context: 22-DoF双手真实平台，六个接触丰富任务
results_with_uncertainty: 平均70.6 vs 38.0；移除触觉世界建模四任务均值74.7→26.6；约4小时适配
candidate_P: [P-S12]
candidate_F: [F-S12, F-S13]
evidence_index: [PDF abstract, Sec. 1, Sec. 4, Sec. 6, Appendix A.8–A.9]
limitations: 成功演示为主；首次执行错误后滚动预测恶化；无系统 failure/recovery calibration
evidence_status: verified
missing_evidence: 源码、失败轨迹规模、跨手型实验、校准曲线
next_skill: deep-read Mode C
```
