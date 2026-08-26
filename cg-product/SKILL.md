---
name: cg-product
description: Maintain and apply Cheng Good Food's approved product master data. Use for proposals, specifications, sales materials, labels, product comparisons, packaging, storage, preparation, food-safety facts, or any task that mentions 呈冠 products. Do not infer missing product facts or treat internal nicknames as formal product names.
---

# CG-PRODUCT｜呈冠產品資料主檔

Use this skill as the single source of truth for Cheng Good Food product facts.

## Required workflow

1. Read [references/product-master.md](references/product-master.md) before writing or checking any product fact.
2. Use confirmed facts exactly. Keep formal product names separate from business nicknames.
3. Treat every item marked `待公司確認`, `擱置`, or `尚缺資料` as unavailable. Do not infer it from another product, old proposal, photo, label, or similar SKU.
4. If the requested output needs an unavailable fact, state the gap clearly and add it to a consolidated company-confirmation list.
5. In status-coded documents, render confirmed content in black and unavailable content in red. In plain text, label unavailable content explicitly.
6. Before delivery, check names, weights, pack counts, carton totals, storage, shelf life, food-business registration numbers, and confirmation status for consistency.

## Non-negotiable invariants

- Formal name for `冰火山` is `冰火山溏心蛋`; `冰火山` is its business nickname.
- Formal name for `單顆30入` is `溏心蛋`; `單顆30入` is its business/packaging nickname.
- Never use `溏心溫泉蛋` as a product name.
- `溏心蛋` and `帶殼溫泉蛋` are different products.
- Company and factory food-business registration numbers must be shown separately.
- All SKUs/product codes remain suspended until confirmed.
- H-category CAS, SGS, testing, traceability, and recall details remain unconfirmed unless the user supplies a newer approved source.
- User-approved label photos may be published externally and used in proposals, catalogs, or sales materials. Other J-category product photos, logo, and document-governance details remain unconfirmed unless explicitly approved.

## Updating the master

Apply source priority in this order: the user's latest explicit confirmation, a newer approved company source, then the current master. A photo or older document cannot override a newer explicit confirmation. Update this existing master in place; never create a second PRODUCT master. Change only affected facts and statuses, preserve unrelated confirmed data, and report conflicts instead of silently reconciling them.
