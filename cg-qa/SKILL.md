---
name: cg-qa
description: 在呈冠跨 Skill 交付或發布前執行可追溯性、資料、邏輯、格式與敏感資訊驗收。輸出 PASS、FAIL 或 BLOCKED 並指派責任 Skill；不擁有或代改領域主資料。
---

# CG-QA｜跨 Skill 最終驗收

以可定位證據判斷交付是否可發布，不替責任 Skill 靜默重寫內容。

## 核心流程

1. 確認交付物、驗收範圍、版本、來源清單與適用責任 Skill。
2. 依 [references/workflow.md](references/workflow.md) 檢查結構、資料來源、邏輯一致性、品牌／語氣、格式、敏感資訊與交付完整性。
3. 產品事實追溯 `cg-product`；客戶事實追溯 `cg-customer`；FIT 追溯 `cg-fb-fit`；方案邊界追溯 `cg-proposal`；正式文件追溯 `cg-word`。
4. 依 [references/schemas.md](references/schemas.md) 對每項問題提供位置、證據、嚴重度、責任 Skill 與修正條件。
5. 依整體閘門輸出 `PASS`、`FAIL` 或 `BLOCKED`。`FAIL`／`BLOCKED` 時退回責任 Skill，不直接更改其主資料或結論。

權責與停止條件見 [references/boundaries.md](references/boundaries.md)。
