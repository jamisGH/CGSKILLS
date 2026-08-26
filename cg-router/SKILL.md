---
name: cg-router
description: 依使用者意圖、資料狀態與交付物，在呈冠的 product、customer、FIT、proposal、Word/PDF 與 QA Skills 間選擇最小充分路由。只負責協調，不擁有或改寫領域事實。
---

# CG-ROUTER｜Skill 路由協調

保留使用者原始意圖與授權邊界，優先派給單一最小充分 Skill；只有任務確實跨領域才串接。

## 主要路由

| 使用者意圖／交付物 | 主要 Skill | 必要時串接 |
|---|---|---|
| 產品規格、包裝、儲存、準備、食安、產品比較 | `cg-product` | 發布前可送 `cg-qa` |
| 品牌、通路、餐飲客戶或陌生開發適配性 | `cg-fb-fit` | `cg-product`、`cg-customer` |
| 合作方案、提案架構或銷售內容 | `cg-proposal` | `cg-fb-fit`、`cg-product`、`cg-customer` |
| 建立、查核、合併或更新客戶資料 | `cg-customer` | 衝突未解決時停止下游 |
| 已確認內容製作正式 Word/PDF | `cg-word` | 內容來源依任務串接，完成後送 `cg-qa` |
| 驗收、發布前或跨 Skill 一致性檢查 | `cg-qa` | 問題退回責任 Skill |

## 決策流程

1. 辨識使用者要解決的問題、預期交付物、已有資料狀態與授權範圍。
2. 依 [references/workflow.md](references/workflow.md) 選擇最小充分路由；不要因可用而把所有 Skill 全部串上。
3. 缺關鍵資訊時指出缺口；能由可信現有資料安全判斷時不重複詢問。
4. 使用 [references/schemas.md](references/schemas.md) 保存每段輸入、狀態、來源與交接。
5. 任何上游結果為 `BLOCKED`，停止依賴該結果的下游步驟，不假裝完成。

Router 不建立或修改產品、客戶、FIT、方案、文件或 QA 主內容。模糊意圖、衝突與停止條件見 [references/boundaries.md](references/boundaries.md)。
