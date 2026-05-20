---
task: task-3-interactive-artifact
source: https://aiweb3.school/zh/handbook/ai-basics/agent/
created: 2026-05-21
status: done
---

# 任務 3：用 Agent 生成可交互學習產物 — Agent 決策流程圖

## 目標

選 Week 1 的一個核心概念（智能體 Agent），用 Hermes Agent 輔助生成可交互學習產物，讓自己在動手過程中真正理解概念，成品也能當作學習證明。

## 完成定義（DoD）

- [x] 選定 Agent 執行循環作為可視化主題
- [x] 生成零依賴交互式 HTML 流程圖
- [x] 每個節點可點擊查看 Handbook 原文解讀
- [x] 顏色標註安全邊界（🟢 自動 / 🟡 需確認 / 🔴 停止）
- [x] 產物放 `experiments/agent-decision-flow/`
- [x] 撰寫此 Agent 協助學習日誌

## Proof-of-work

- Commit：`29d3ecf` → https://github.com/june-in-exile/AI-Web3-Colearning/commit/29d3ecf
- 文件：
  - `experiments/agent-decision-flow/index.html` — 交互式流程圖
  - `experiments/agent-decision-flow/README.md` — 產物說明
  - `daily/2026-05-20.md` — Day 2 日誌
  - `daily/2026-05-21.md` — Day 3 日誌

## 流程紀實

### 第 1 步：讀 Handbook，選概念

從 Handbook Agent 章節提取 5 個核心概念：
| 概念 | 一句話 |
| --- | --- |
| Tool Use | 只讀 vs 寫入工具的風險等級完全不同 |
| Planning | Agent 需要能拆步驟、暴露每一步的工具和權限需求 |
| State | 狀態必須外置、可查、可審計 |
| Reflection | 自我檢查是輔助，不能替代外部驗證 |
| Stop Conditions | 沒 break 的循環 = 超時或失控 |

**選題判斷**：Agent Decision Flow 把這些概念串成一個執行循環，比單獨做概念卡片更能理解它們怎麼協作。同時直接通到 Hackathon 賽道（Agent Wallet / Agentic Commerce 都需要精確的確認流程圖）。

### 第 2 步：用 Hermes 生成交互產物

直接讓 Hermes Agent 讀取 Handbook 內容 + 上述概念提取，生成：

1. **SVG 流程圖**：Goal → Plan → Split → (Auto Read / Policy Check) → Reflection/Sim → Confirm → Execute → Log → Stop
2. **點擊面板**：每個節點綁定 JS 點擊事件，顯示 Handbook 原文解讀和安全邊界說明
3. **圖例 + 知識卡片**：顏色說明 + 4 張核心要點卡

全過程 Hermes 完成 HTML/CSS/JS/svg 生成，人工做的只有：
- 提供 Handbook 概念提取方向
- 調整流程圖佈局（左右分支的平衡）
- 確認資訊面板的文字準確性

### 第 3 步：人工審查與微調

審查發現的問題：
- 部分節點解讀文字偏抽象，補充了實際例子
- 確認標籤顏色語義一致
- 補上 footer 連結

## Agent 協助學習的價值

| 維度 | 人工做 | Hermes 協助 |
| --- | --- | --- |
| 概念提取 | 讀 Handbook → 自己歸納 | 幫忙從原文提取核心概念和逐層拆解 |
| 可視化 | 需要手畫流程圖或學前端 | 直接生成 SVG + 交互 JS，零依賴 HTML |
| 解讀面板 | 要自己查原文來回切換 | 把原文關鍵段落直接嵌入節點點擊事件 |
| 迭代 | 改一次要改圖 + 文字多處 | 告訴修改方向，批量更新 |
| 產出速度 | ~半天（含學習） | ~1-2h（含學習 + 審查） |

**結論**：Agent 最強的不是代替思考，而是把「理解 → 表達 → 驗證」的循環加速。概念我來吸收，輸出形式 Hermes 幫我生成，我專注在審查準確性和補充細節。

## 筆記 / 坑

- **SVG 座標是手工勞動** — Hermes 第一次生成的節點位置偏擠（左右分支重疊），只能手調 x/y。下次可以考慮用 `excalidraw` skill 做草圖再轉 SVG 來規避座標微調問題。
- **零依賴是正確決定** — 純 HTML/SVG 可以 `open` 直接看，不需要 npm install / 啟動 server，降低分享門檻。
- **中文 vs 英文內容混用** — Handbook 部分原文是英文，產物輸出中英混合，但要確保關鍵詞統一（e.g. Reflection 不翻成「反思」以免偏離原術語）。

## 復盤

- **哪裡 Work**
  - 先讀 Handbook 再讓 Agent 生成，比直接讓 Agent 「做個流程圖」效果好很多 — 因為我有概念框架來判斷生成品質
  - 零依賴 HTML 是正確的形式 — 打開即用，適合學習產物分享
  - 交互式（點擊看解讀）比靜態圖多一層學習價值

- **哪裡不 Work**
  - SVG 座標花了不少時間來回調整
  - 第一次生成的「人工確認點」描述太模糊，需要人工補具體場景
  - 過程中 API balance 用完了，斷了一次 — 中間結果沒存，恢復後要重新引導

- **下次改什麼**
  - 如果主題偏佈局/圖形，優先試 `excalidraw` skill
  - 時間分配：60% 學習概念 → 30% 生成產品 → 10% 審查，這次學習比例偏低
  - 學習產物完成後應立刻寫此日誌，避免間隔太久遺忘細節
