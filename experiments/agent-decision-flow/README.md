# Agent 决策流程图

> 官方任务 3 · 可交互学习产物 · Week 1
> 来源：[Handbook — 智能体（Agent）](https://aiweb3.school/zh/handbook/ai-basics/agent/)

## 这是什么

一张交互式 **Agent 决策流程图**，把 Handbook Agent 章节的核心概念可视化：

- Agent 执行循环：Goal → Plan → Split → Execute → Reflect → Confirm → Transact → Log → Stop
- 每个节点可点击查看 Handbook 原文解读
- 颜色标注安全边界：🟢 自动执行 / 🟡 需人工确认 / 🔴 停止条件

## 产物

| 文件 | 用途 |
| --- | --- |
| `index.html` | 交互式流程图（浏览器打开即可，零依赖） |

## 打开方式

```bash
open experiments/agent-decision-flow/index.html
```

## 涵盖的 Handbook 概念

- Agent 第一性原理
- Tool Use（只读 vs 写入边界）
- Planning（步骤拆分）
- State（外置状态 + 审计日志）
- Reflection（自我检查 vs 外部验证）
- Multi-Agent（分工协作）
- AI × Web3 架构分层
- 停止条件（目标 / 预算 / 风险 / 中断）

## 设计原则

按下图执行循环构建，每个节点标注：

- 该步骤属于哪个阶段（用户 / Agent 处理 / 自动 / 人工确认 / 停止）
- Handbook 原文引用
- 该步骤的风险边界和人工确认点
