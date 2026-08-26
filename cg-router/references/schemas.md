# Router 交接 Schema

需要記錄跨 Skill 路由或交接狀態時讀取本檔。

```yaml
intent: string
deliverable: string
authorization: string
primary_skill: cg-product | cg-customer | cg-fb-fit | cg-proposal | cg-word | cg-qa
route:
  - skill: string
    purpose: string
    inputs: [string]
    status: PENDING | READY | PASS | FAIL | BLOCKED
    outputs: [string]
    sources: [string]
gaps: [string]
stop_reason: string | none
```

每個下游只能使用上游明確提供的輸出與狀態。Router 可傳遞內容，不得自行把 `missing`、`unverified`、`conflicting` 或 `BLOCKED` 升級為已確認。
