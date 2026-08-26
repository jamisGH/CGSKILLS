---
name: cg-proposal
description: 將已確認的客戶需求、FIT 結果與呈冠產品資料整理成合作方案、提案架構或銷售內容包。適用提案策劃；不臆測商務條件，也不負責正式 Word/PDF 製作。
---

# CG-PROPOSAL｜合作方案內容

把可追溯的需求、FIT 與產品事實轉為可審核的提案內容，不把建議寫成公司承諾。

## 核心流程

1. 確認客戶需求、FIT 結果、產品事實及其來源與狀態。
2. FIT 未完成或關鍵資料不足時，交回 `cg-fb-fit` 或回傳缺口，不跳過評估。
3. 產品內容使用 `cg-product`；正式客戶資料使用 `cg-customer`。
4. 依 [references/workflow.md](references/workflow.md) 組織目標、洞察、建議方案、依據、風險、待決事項與下一步。
5. 依 [references/schemas.md](references/schemas.md) 分開 `recommended` 與 `approved`，標記每項來源及核准狀態。
6. 需要正式 DOCX/PDF 時，把已確認內容包交給 `cg-word`；發布前交給 `cg-qa`。

詳細禁止事項、停止條件與交接規則見 [references/boundaries.md](references/boundaries.md)。
