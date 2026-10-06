# 灵巧手抓取 × 世界模型：项目索引

更新时间：2026-10-06

## 研究目标

围绕多指灵巧手抓取，验证世界模型是否能通过预测“接触力演化—未来手物状态—抓取结果”，减少视觉遮挡和接触不确定性导致的失败，并支持低成本闭环重规划。

## 当前状态

- 阶段：文献边界复核与单故障动作排序诊断
- 当前证据：`partial`；主要依据为公开论文页面/摘要，尚未复现源码或获取同一硬件数据
- 推荐主线：单一滑移故障下的配对失败数据与触觉动作排序
- 首个动作：在一个仿真手型和一个抓取任务上比较 success-only 与 paired-failure

## 目录

| 路径 | 用途 |
|---|---|
| `ref.txt` | 用户给出的科研流程 |
| `skills/` | 已安装的研究 skills 与交接协议 |
| `Papers/` | 已下载并解析的论文 PDF/TXT（大文件不纳入 Git） |
| `Literature/` | 论文解析笔记与 ANALYSIS_PACKAGE |
| `Analysis/` | Mode C 矩阵、Idea 卡片及分析文档 |
| `Source/` | 外部开源代码、数据和复现材料 |
| `Code/` | 本项目代码 |
| `Code Output/` | 运行日志和生成结果 |
| `Sessions/` | 对话和过程记录 |
| `Analysis实验报告/` | 实验分析报告 |
| `Analysis废弃的/` | 废弃方案，保留历史 |

## 关键文档

- [论文笔记](论文笔记.md)
- [论文素材库](论文素材库.md)
- [已发现的实验现象](已发现的实验现象.md)
- [Paper plan](Paper plan.md)
- [Version evolution](Version evolution.md)
- [Mode C 交叉矩阵](Analysis/MODE_C_001_交叉矩阵.md)
- [首个 Idea 卡片](Analysis/IDEA_001_接触预测闭环抓取.md)
- [第二轮 Mode C 矩阵](Analysis/MODE_C_002_失败恢复与跨手型接触世界模型矩阵.md)
- [推荐 Idea-002](Analysis/IDEA_002_失败感知跨手型接触世界模型.md)
- [当前收缩版 Idea-003](Analysis/IDEA_003_触觉失败后的动作排序.md)
- [公开材料核验记录](Literature/公开材料核验记录.md)
