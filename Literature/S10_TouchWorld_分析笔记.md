# TouchWorld — 全文分析

> 来源：https://arxiv.org/abs/2607.07287  
> 本地全文：`Papers/S10_TouchWorld.pdf` / `.txt`

## 核心设计

采用多时间尺度层级：高层子任务规划与 tactile world-model 预测，中层 visuo-tactile goal-conditioned action chunk，低层高频 tactile residual refinement；在 Wuji 平台六个长时域任务和人工扰动条件下评估。

## 结果与限制

报告 clean 平均成功率 65.0%，人工扰动 53.7%。全文讨论未来需要 uncertainty-aware tactile goal prediction，并指出跨传感器/手型迁移仍需要适配；因此它覆盖预测+反应，却没有解决跨 embodiment 的统一风险评估。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
analysis_id: AP-S10
source_ids: [S10]
source_identity_and_version: TouchWorld, arXiv 2607.07287
research_question: 多时间尺度的预测触觉目标与高频残差是否能提升长时域灵巧操控？
study_type_and_context: Wuji灵巧手真实机器人，六任务、干净/人工扰动
results_with_uncertainty: 65.0% clean、53.7% human perturbation；100次真实评估rollouts；完整区间待复核
candidate_P: [P-S10]
candidate_F: [F-S10]
evidence_index: [PDF Sec. 3–5, Table 1, Limitations]
limitations: 传感器布局绑定；未来工作才提出 uncertainty-aware goal prediction 与更广泛手型迁移
evidence_status: verified
missing_evidence: 源码、跨手型原始数据、概率校准实验
next_skill: deep-read Mode C
```
