# 个人学习计划

## 学员画像

| 维度 | 自评 |
| --- | --- |
| AI 基础 | 有基础 — 用过聊天界面、调过 API；没系统做过 Agent / RAG / MCP |
| Web3 基础 | 熟悉 — 写过并部署过合约，熟一条链的开发栈 |
| 编程 | 能独立开发 |
| 目标 | **Hackathon 项目**（Week 4 拿出 demo / proposal） |
| 每日时间 | 1–2 小时（周末加量） |
| 输出语言 | 中英混合 |
| **主工具** | **Hermes Agent + Telegram**（已装 Hermes v0.14.0，Day 1 接 TG） |

- **长板**：链上技能（合约、钱包、Dev Stack）
- **短板**：Agent 工程化（state / memory / tool calling / MCP / guardrails）、Vibe Coding 工作流

## Week 1 官方任务（来源：[WCB Learning Tab](https://web3career.build/zh/programs/AI-Web3-School?tab=learning) / [Week 1 Notion](https://ethpanda.notion.site/Week-1-AI-Web3-354bbd63be878198afc4f155b5c3a69f)）

### 模块 A · AI 基础

| # | 任务 | 状态 |
| --- | --- | --- |
| 任务 1 | 搭建 learning agent（任选 Claude Code / Codex / **Hermes Agent**），跑通一次对话式学习任务 | 🟡 Hermes 已装；Day 1 接 TG 后完成 |
| 任务 2 | 创建个人 GitHub repo（README / commit / agent 配置说明 / 一次协助日志） | 🟢 repo + README + commit 已 ✓；待补 SOUL.md 备份 + 协助日志 |
| 任務 3 | 用 agent 生成可交互學習產物 | 🟢 `experiments/agent-decision-flow/` + `tasks/task-3-interactive-artifact.md` |

### 模块 B · Web3 基础

- ⚪ 创建测试钱包，说明地址 / 助记词 / 私钥差异（**不提交真实助记词 / 私钥**）
- ⚪ 切换测试网，领测试币，发一笔测试交易
- ⚪ 在区块浏览器记录 tx hash / 状态 / Gas / 区块高度
- ⚪ 用 Remix / Hardhat / Foundry 部署最小合约 + 一次读 + 一次写
- ⚪ 高级：比较 EOA / 智能账户 / 多签

### 模块 C · 最小交叉实验

- ⚪ 至少完成一条 "AI 生成 → 人工复核 → 钱包确认 → 链上执行 → 浏览器验证" 链路，记录流程、风险边界、人工确认点

### 本周交付（4 条）

1. Learning agent / coding agent 配置记录（模型 / API / repo / README / commit / 截图）
2. 至少一次 agent 协助学习或编码日志
3. 测试网交易哈希、合约地址、读写结果、区块浏览器链接
4. 最小 AI × Web3 交叉实验说明（流程、边界、风险、验证材料）

## 本周排期（1–2 h/天，画像驱动）

> Web3 是长板 → Web3 模块可以加速跑；AI 是短板 + 需要先接通 Hermes/TG，所以前 3 天偏 AI/工具，后 4 天偏 Web3 + 交叉实验。

| Day | 日期 | 重点 | 产出 |
| --- | --- | --- | --- |
| D1 | 05-19 | **Hermes + TG 接通**（任务 1 收尾）+ commit 配置记录 | bot 通 + SOUL.md + `daily/2026-05-19.md` 配置日志 |
| D2 | 05-20 | 用 TG bot 推任务 3：选一个 Week 1 概念做可交互产物 | `experiments/<concept>-demo/` + README |
| D3 | 05-21 | 任务 3 收尾 + 写"agent 协助学习日志" | `tasks/task-3-interactive-artifact.md` |
| D4 | 05-22 | 模块 B：测试钱包 + Sepolia faucet + 测试交易 | wallet 地址 + tx hash + 浏览器截图 |
| D5 | 05-23 | 模块 B：Foundry/Hardhat 部署最小合约 + 读 / 写 | 合约地址 + 调用 tx + README |
| D6 | 05-24（六）| 模块 C：跑通最小交叉实验 | 流程图 + trace 笔记 + 人工确认点标注 |
| D7 | 05-25（日）| 周复盘 + Week 2 选题（Bridge PoC 候选 1 个） | `daily/2026-05-25.md` 含周复盘 |

## Week 2–4

| 阶段 | 日期 | 重点 | 交付 |
| --- | --- | --- | --- |
| **Week 2** | 05-26 → 06-01 | Bridge 主题 PoC（Agent Wallet / Machine Payment / Tool Use 任选 1） | `experiments/<bridge-topic>-poc/`；**周末锁 Hackathon track** |
| **Week 3** | 06-02 → 06-08 | Track 选定 + 1-pager proposal | `hackathon/proposal.md` |
| **Week 4** | 06-09 → 06-15 | Demo 收敛 + 提交 | `submissions/` |

## Hackathon track 候选（Week 2 末锁定）

| Track | 匹配度 | 入口 |
| --- | --- | --- |
| Wallet / Permission ⭐ | 高 — 复用合约 + Agent Wallet | [tracks/wallet-permission](https://aiweb3.school/zh/handbook/tracks/wallet-permission/) |
| Agentic Commerce ⭐ | 高 — Machine Payment / Settlement 延伸 | [tracks/agentic-commerce](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/) |
| AI Security | 中 — 偏研究 | [tracks/ai-security](https://aiweb3.school/zh/handbook/tracks/ai-security/) |
| Dev Tooling | 中 — MCP for chain data | [tracks/dev-tooling](https://aiweb3.school/zh/handbook/tracks/dev-tooling/) |
| Open Track | 兜底 | [tracks/open-track](https://aiweb3.school/zh/handbook/tracks/open-track/) |

## 不懂问题清单

- [ ] `temperature` 与 `max_tokens` 如何影响输出？
- [ ] MCP 协议与普通 Tool Calling 的本质区别？
- [ ] 任务"该用 workflow 还是 agent"如何判断？
- [ ] 如何为 agent 设计有效 guardrails？
- [ ] 交叉实验中"人工确认点"设在哪几步？

## 安全护栏

- 任何写入型操作（部署、转账、提交）人工确认
- **测试网 only**；主网操作单独 review
- 不在 repo 写入 API key / 助记词 / 私钥 / Telegram bot token
- Hermes secrets 放 `~/.hermes/.env`，不进 repo
