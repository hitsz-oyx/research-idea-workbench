# TacForeSight — 全文分析

> 来源：https://arxiv.org/abs/2606.11184  
> 本地全文：`Papers/S11_TacForeSight.pdf` / `.txt`

## 核心设计

用高频腕部力/力矩预测短时 tactile latent dynamics，再用预测 latent 作为 anticipatory contact prior，并通过 gating 融合视觉/触觉；在 xArm7 + Robotiq 2F-85 上做五类任务和三类扰动。

## 边界

这是强的 force-conditioned tactile foresight 基线，但硬件是二指夹爪而非多指灵巧手；它证明实时短时预测有用，却没有回答多指 contact allocation、跨手型迁移或长时域失败后校准。

## ANALYSIS_PACKAGE

```text
package_type: ANALYSIS_PACKAGE
analysis_id: AP-S11
source_ids: [S11]
source_identity_and_version: TacForeSight, arXiv 2606.11184
research_question: 高频腕部力/力矩能否提前预测局部触觉演化并改善扰动下控制？
study_type_and_context: xArm7 + Robotiq 2F-85真实机器人，五任务、三种扰动
results_with_uncertainty: 真实任务报告优于基线；具体数值见PDF表格，尚未复现
candidate_P: [P-S11]
candidate_F: [F-S11]
evidence_index: [PDF abstract, Sec. III–IV]
limitations: 二指夹爪；短时 latent；无多指跨 embodiment 和失败恢复
evidence_status: verified
missing_evidence: 源码/数据运行、多指扩展、概率校准
next_skill: deep-read Mode C
```
