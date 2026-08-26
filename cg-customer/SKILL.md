---
name: cg-customer
description: 建立、查核、正規化或維護呈冠客戶主檔，處理唯一識別、別名、來源、驗證狀態、重複與衝突。適用可信客戶資料管理；不做 FIT、提案、產品主檔或文件排版。
---

# CG-CUSTOMER｜客戶主檔

維護可追溯且最小揭露的客戶資料，讓其他 Skill 能安全引用。

## 核心流程

1. 確認操作目的、授權範圍、資料來源與更新日期。
2. 依 [references/schemas.md](references/schemas.md) 正規化唯一識別、正式名稱、別名、聯絡資訊、來源、驗證狀態、敏感度與時間戳。
3. 依 [references/workflow.md](references/workflow.md) 查核來源；使用 `verified`、`unverified`、`conflicting`、`missing` 標示欄位狀態。
4. 合併或判定重複前列出證據；名稱相似不足以合併。無法排除不同實體時停止合併。
5. 對其他 Skill 回傳欄位值、狀態、來源與更新日期；只揭露任務必要資訊。

個資、商務敏感資訊、外傳限制與停止條件見 [references/boundaries.md](references/boundaries.md)。不做 FIT、方案創作、產品主資料維護或文件排版。
