---
task: module-b-wallet-testnet
source: https://web3career.build/zh/programs/AI-Web3-School
created: 2026-05-21
status: doing
---

# 模塊 B：Web3 基礎 — 測試錢包與測試網交易

## 1. 創建測試錢包

用 Foundry `cast wallet new` 生成一個新 EOA 錢包：

| 欄位 | 值 |
| --- | --- |
| 地址 | `0xF3A203fE12e441d7c6F2Cd8778C841240D6C6159` |
| 網路 | Ethereum Sepolia 測試網 |
| 類型 | EOA（Externally Owned Account） |

### 地址 / 私鑰 / 助記詞 差異

| 名詞 | 是什麼 | 能不能公開 | 類比 |
| --- | --- | --- | --- |
| **地址** | 公鑰的哈希，用來收款和查詢 | ✅ 可以公開分享 | 銀行帳號 |
| **私鑰** | 控制帳戶的密鑰，簽名交易用 | ❌ **絕對不能洩露** | 銀行卡密碼 |
| **助記詞** | 12/24 個單詞，私鑰的人類可讀備份 | ❌ **絕對不能洩露** | 銀行卡密碼的備份 |

> 本次創建的是 EOA（Externally Owned Account）— 由私鑰直接控制。Smart Account（智能帳戶）透過合約邏輯控制，支援多簽、社交恢復等高級功能，是 Hackathon 重點方向。

**安全性注意**：本次私鑰僅用於測試網，不會寫入 repo。
