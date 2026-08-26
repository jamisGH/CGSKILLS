# QA 結果 Schema

需要記錄、交換或驗證 QA 結果時讀取本檔。

```yaml
status: PASS | FAIL | BLOCKED
artifact:
  id: string
  version: string
  location: string
checks:
  - area: structure | source | logic | brand | format | sensitive_data | completeness
    status: PASS | FAIL | BLOCKED
    location: string
    evidence: string
    severity: critical | major | minor | info
    owner: cg-product | cg-customer | cg-fb-fit | cg-proposal | cg-word | cg-qa
    correction_condition: string
traceability:
  - claim: string
    source: string
    owner: string
release_allowed: true | false
```

`location` 必須足以定位檔案、頁面、段落、欄位或紀錄。沒有證據的「看起來沒問題」不能算 PASS。
