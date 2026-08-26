# 客戶主檔 Schema

建立、驗證或交換客戶紀錄時讀取本檔。

```yaml
customer_id: string
official_name: {value: string, status: verified | unverified | conflicting | missing}
aliases: [string]
identifiers:
  - type: registration | internal | domain | other
    value: string
    status: verified | unverified | conflicting | missing
contacts:
  - channel: phone | email | address | person | other
    value: string
    status: verified | unverified | conflicting | missing
    sensitivity: public | internal | restricted
sources:
  - id: string
    location: string
    observed_at: YYYY-MM-DD | unknown
verification_status: verified | unverified | conflicting | missing
updated_at: YYYY-MM-DD
handling_notes: [string]
```

每個欄位須能連回 `sources`。`customer_id` 應穩定且不由可變顯示名稱單獨產生；缺少既定編碼規則時回報需求，不自行宣稱正式編碼。
