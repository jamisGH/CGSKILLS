# CG-FB-FIT

呈冠品牌、通路、餐飲與潛在客戶適配評估 Skill。

- 輸入：評估對象、使用情境、目標、可追溯來源，以及 `cg-product`／`cg-customer` 提供的已確認事實。
- 輸出：證據分級的 FIT 結論、信心、風險、缺口與下一步。
- 相依：產品事實由 `cg-product` 提供；客戶正式資料由 `cg-customer` 提供。
- 交接：正式方案交給 `cg-proposal`，文件交給 `cg-word`，最終驗收交給 `cg-qa`。

範例：`使用 $cg-fb-fit 評估某連鎖早餐品牌導入呈冠產品的適配性；未知資料請列為待查證。`

版本採語意化版本，初版見 `VERSION`；規則入口為 `SKILL.md`。
