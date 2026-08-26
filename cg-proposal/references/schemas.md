# 提案內容包 Schema

需要結構化輸出或跨 Skill 交接時讀取本檔。

```yaml
status: READY | BLOCKED
customer_ref: string
fit_ref: string
objective: string
confirmed_inputs:
  - claim: string
    owner: cg-customer | cg-product | cg-fb-fit | user
    source: string
proposal:
  context: string
  recommended_solution: [string]
  rationale: [string]
  risks: [string]
commercial_terms:
  - item: string
    state: recommended | approved | missing
    approval_source: string | missing
open_items: [string]
handoff:
  target: cg-word | cg-qa | none
  content_version: string
```

`READY` 只代表內容包可送審或製作文件，不代表商務條件已獲核准。
