# IDEA-002 阶段 A 实验记录模板

按 `skills/record-experiment/SKILL.md` 复制为具体实验记录，执行前固定 `plan_version`，不得只保留最佳运行。

```text
package_type: EXPERIMENT_RECORD
package_version: research-pipeline-contract v1.0
experiment_id: EXP-002-A
source_idea_id: IDEA-002
plan_version: IDEA-002-v1
execution_status: planned
research_question: 失败/干预轨迹是否改善首次接触错误后的风险校准和恢复？
hypothesis: success-only世界模型在错误后进入分布外并过度自信；失败增强可降低退化。
planned_vs_actual_design_and_controls: B0/B1/B2/B3/B4，待执行后补充实际配置
actual_configuration: 手型、仿真器、摩擦、延迟、触觉丢帧、模型和seed
samples_materials_or_data_provenance: 轨迹生成脚本、对象集合、数据切分和版本
results_with_uncertainty: 全部运行、ECE/Brier、AUPRC、恢复率、bootstrap区间
all_runs_or_repetitions: 至少3 seeds；保存失败和异常运行
observations_and_deviations: 观察/解释/待复验分栏
evidence_locations: Code、Code Output、数据路径、图表和配置
known_limits_and_missing_evidence: 仿真摩擦、触觉仿真、跨手型覆盖
next_routes: squeeze-experiment
next_skill: squeeze-experiment
```
