---
name: cg-fb-fit
description: 評估食品飲料品牌、通路、餐飲或潛在客戶與呈冠產品及能力的適配性。用於 FIT、陌生開發與合作適配判斷；不撰寫正式提案、維護客戶主檔或製作 Word/PDF。
---

# CG-FB-FIT｜品牌與客戶適配評估

把可追溯的對象資料與呈冠已確認能力轉成 FIT 評估，不把未知資訊寫成事實。

## 核心流程

1. 確認評估對象、通路或使用情境、目標與資料來源。
2. 需要產品名稱、規格、包裝、保存、製備或食品安全事實時，先使用 `cg-product`；不得從印象、舊提案或相似產品補值。
3. 依 [references/workflow.md](references/workflow.md) 區分已確認事實、合理推論、待查證資訊與禁止猜測項目，再評估適配理由、風險與缺口。
4. 依 [references/schemas.md](references/schemas.md) 輸出評估對象、情境、證據、信心等級、風險、缺口與下一步。
5. 資訊不足時列出待補資料；不足以支持結論時回傳 `BLOCKED`，不得硬判適合或不適合。

## 邊界與交接

- 不撰寫正式合作提案；需要提案內容時，將 FIT 結果交給 `cg-proposal`。
- 不建立或更新客戶主檔；需要可信客戶事實時交給 `cg-customer`。
- 不製作 Word/PDF；已確認內容交給 `cg-word`。
- 不做最終跨 Skill 驗收；交付前由 `cg-qa` 檢查。
- 詳細停止條件與禁止事項見 [references/boundaries.md](references/boundaries.md)。
