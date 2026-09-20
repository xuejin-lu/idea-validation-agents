# Sample Deliverable Spec

所有示例必須使用 synthetic/demo data，不得複製真實客戶檔案、統編、姓名、地址、帳號或可回推的交易資料。

## 1. Cover and scope

- Demo company: `DEMO-001`。
- Period: `2026-08`。
- Sources: `DEMO_SHOP_A`, `DEMO_GATEWAY`, `DEMO_BANK`。
- Scope: order total、settled amount、refund/allowance、invoice reference 的資料整理與差異標記。
- Explicitly not a bookkeeping entry, tax filing or professional sign-off。

## 2. Normalized table

建議欄位：

| 欄位 | 說明 |
|---|---|
| record_id | demo 內部識別碼，不使用真實訂單號 |
| period | 交易/入帳月份 |
| channel | 平台或來源代號 |
| order_ref_masked | 遮蔽後參考碼 |
| transaction_date | 日期或日期區間 |
| gross_amount | 原始金額 |
| fee_amount | 平台/金流費用，如來源有提供 |
| refund_amount | 退款/折讓金額，如來源有提供 |
| net_expected | 依事先約定規則計算的 expected 值，標明規則版本 |
| settlement_amount | 來源提供的實際入帳/結算值 |
| invoice_ref_masked | 遮蔽後發票參考碼 |
| source_file | 原始檔案代號 |
| source_row_or_page | 原始列號或頁碼 |
| reconciliation_status | matched / difference / missing / needs_review |
| notes | 不確定事項與限制 |

不得把 demo 的 `net_expected` 寫成會計認定金額；它只是依輸入欄位的機械核對結果。

## 3. Exception list

每一筆差異至少包含：

- exception_id；
- 差異類型：missing settlement、refund mismatch、invoice reference missing、fee mismatch、duplicate candidate、other；
- affected source/channel；
- 金額或數量區間；
- source/evidence link：指向 demo 檔案與列號/頁碼；
- current status：open / buyer_to_confirm / accountant_to_review / closed；
- unresolved_items：尚未知道的欄位、需要誰確認、截止日；
- no conclusion beyond data observed。

## 4. Source/evidence index

建立一張 index，把每個 normalized 欄位連回：

- source_file ID；
- source row/page；
- import date；
- transformation rule ID；
- redaction note；
- any manual adjustment and reason。

## 5. Accountant-handoff checklist

- [ ] 所有來源檔案與月份確認。
- [ ] 缺少的來源/列/頁已列在 exception list。
- [ ] 退款/折讓項目已標記待確認，未自行做稅務判斷。
- [ ] 發票參考欄位已標記 missing/needs_review。
- [ ] 原始檔案與整理表的筆數/加總已做機械比對。
- [ ] 買方的記帳士/會計師已知道哪些欄位尚待專業判斷。
- [ ] 交付物附上 scope、limitations 和產出版本。

## 6. Professional review flags

以下任何事項都必須標記 `accountant_review_required`，不可由本包下結論：

- 是否應認列收入、費用、折讓或稅額；
- 發票作廢、退回或折讓證明的法定處理；
- 稅務申報期間、申報方式或罰則；
- 正式傳票/帳簿處理、簽證或對外報表；
- 任何法律責任或合規保證。

## 7. Demo-only disclaimer

Sample deliverable 的首頁與檔名都要寫：`DEMO / SYNTHETIC DATA — NOT FOR ACCOUNTING OR TAX FILING`。未經買方與合格專業人士審閱，不得拿 demo 代替正式帳務文件。
