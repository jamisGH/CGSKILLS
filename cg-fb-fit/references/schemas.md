# FIT 輸出 Schema

需要建立或驗證結構化 FIT 結果時讀取本檔。

```yaml
status: PASS | FAIL | BLOCKED
target:
  name: string
  type: brand | channel | restaurant | prospect | other
scenario: string
evidence:
  - claim: string
    class: confirmed | inferred | to_verify | prohibited_guess
    source: string | missing
    as_of: YYYY-MM-DD | unknown
fit_reasons: [string]
risks: [string]
gaps: [string]
confidence: high | medium | low | insufficient
next_steps: [string]
handoff: cg-proposal | cg-customer | cg-product | cg-qa | none
```

`PASS` 表示證據支持適配；`FAIL` 表示證據支持不適配；`BLOCKED` 表示資料不足或衝突。三者都必須附證據與缺口，不能只給分數。
