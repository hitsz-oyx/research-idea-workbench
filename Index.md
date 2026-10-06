# Research Idea Workbench

这是一个用于寻找、筛选和验证科研 idea 的通用仓库。仓库根目录不绑定某个研究领域；每个具体方向都放在 `tasks/` 下，拥有自己的论文、分析、代码、实验记录和版本演化。

## 当前任务

| Task | 主题 | 状态 | 入口 |
|---|---|---|---|
| `dexterous-grasping-world-model` | 灵巧手抓取 × 触觉世界模型 | 诊断阶段 | [Task Index](tasks/dexterous-grasping-world-model/Index.md) |

后续可以直接在 `tasks/` 下增加新的方向，例如 `vision-language-action`、`robot-learning` 或其他完全不同的研究主题。Task 名称使用小写短横线，不把某个暂时的 idea 写进目录名。

## 通用科研流程

1. 读取 [ref.txt](ref.txt)，明确从论文到 idea、实验和回流分析的流程。
2. 在 `tasks/<task-slug>/Literature/` 保存论文笔记、证据核验和公开材料记录。
3. 在 `tasks/<task-slug>/Analysis/` 保存交叉矩阵、Idea 卡片和实验设计。
4. 在对应 Task 内运行 `record-experiment → squeeze-experiment → deep-read` 的回流流程。
5. 只有经过验证的结论才进入 Task 的主线；过时方案放入该 Task 的 `Analysis废弃的/`。

## 根目录

| 路径 | 用途 |
|---|---|
| `ref.txt` | 通用科研流程和文件约定 |
| `skills/` | 本项目使用的研究 skill 与交接协议 |
| `skills.zip` | skill 安装包归档 |
| `tasks/` | 独立研究方向，每个方向自包含 |
| `P` | 项目根目录标记 |

## 目录原则

- 根目录只放跨任务的流程、规范和任务索引。
- 论文 PDF、源码、实验代码和实验输出必须放入具体 Task，避免不同方向互相污染。
- 一个 Task 可以有多个 IDEA；Task 目录名描述研究方向，Idea 文件名描述具体假设。
- 未验证的假设标记为 `diagnostic`，不要直接写成论文贡献。
