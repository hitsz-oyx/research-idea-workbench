# FeelWorld — 全文分析

> 来源：https://arxiv.org/abs/2607.24267  
> 本地全文：`Papers/S09_FeelWorld.pdf` / `.txt`

## 核心设计

层级预测 contact state、3D tactile latent 与 slip state，通过 contact-gated asymmetric attention 融合视觉/触觉，在 CEM 中只于接触后加入触觉和滑移代价，并用多步 rollout/context noise 缓解累积误差。

## 结果与边界

在 Imeta-Y1、三 RGB 相机和 DM tactile sensors 上做 chip grasping、fruit grasping、USB insertion；报告 contact F1 98.1%、slip F1 83.4%、平均 zero-shot planning success 81.7%。全文指出 slip 正样本约 0.93%，因此 raw accuracy 不可靠；系统是单平台、单传感器协议，未展示跨手型或失败后恢复校准。

## 候选 P/F

- P-S09：预测 slip 并用于 CEM 已有直接先例，但长时域分布外失败和风险校准仍未解决。
- F-S09：接触门控和层级 tactile state 能改善长 rollout 与规划，但结果依赖极度稀疏的 slip 标签。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
analysis_id: AP-S09
source_ids: [S09]
source_identity_and_version: FeelWorld, arXiv 2607.24267v1
research_question: 层级接触/触觉/滑移状态能否改善视觉世界模型规划？
study_type_and_context: 单机器人平台真实接触任务与CEM规划
results_with_uncertainty: contact F1 98.1%、slip F1 83.4%、平均成功率81.7%；滑移正样本0.93%
candidate_P: [P-S09]
candidate_F: [F-S09]
evidence_index: [PDF abstract, Sec. III-E, Sec. IV, Table III–IV]
limitations: 单平台；未报告跨手型、失败恢复或概率校准；slip严重类别不平衡
evidence_status: verified
missing_evidence: 源码运行、跨 embodiment 数据、校准曲线
next_skill: deep-read Mode C
```
