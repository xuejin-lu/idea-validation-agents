# DEMO／SYNTHETIC DATA

這個目錄全部是虛構示範資料，僅用來展示「來源可追溯、差異可列出、未決事項可交接」的輸出格式。不得拿來作為記帳、報稅、發票、收入認列、法律或合規依據。

## 檔案

- `normalized_demo.csv`：含一筆 matched item，以及手續費、退款／折讓、缺少入帳的例外。
- `exceptions_demo.csv`：每個例外連回 record、source file 與 source row。
- `accountant_handoff_demo.md`：示範如何把未決事項交給買方既有的合格專業人士。

## 追溯規則

`normalized_demo.csv` 的 `source_file_id` 與 `source_row_ref` 是虛構來源索引；正式案件必須改用買方提供且已去識別化的實際檔案，不得把 demo ID 當作真實證據。

## 專業邊界

本 demo 不作稅務、會計或法律判斷；`expected_net` 只是機械比對欄位。任何收入、費用、退款／折讓、發票或申報處理，均須由合格專業人士審閱。
