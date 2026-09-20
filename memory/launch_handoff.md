# Launch Handoff

## 1. 使用哪份 listing copy

使用 `memory/marketplace_listing_copy.md` 的標題與內文。發布前由創辦人自行確認平台規則、帳號身份、服務條款與文案是否通過專業審查；不要把「資料整理」改寫成記帳、報稅或稅務服務。

## 2. 附上／展示哪些 demo 檔案

只展示 `memory/demo/README.md`、`memory/demo/normalized_demo.csv`、`memory/demo/exceptions_demo.csv` 與 `memory/demo/accountant_handoff_demo.md`。它們全部是虛構資料，展示來源追溯、matched item、手續費／退款／缺件例外與未決交接；不得替換成真實買方資料。

## 3. 傳送哪份 intake asset

收到符合條件的詢問後，傳送 `memory/intake_form.md`；同時提供 `memory/data_handling_notice.md`。只接受去識別化小樣本，不接受密碼、OTP、後台登入或完整個資。

## 4. 什麼算 commitment

填表或詢價不算。較強訊號是符合目標 segment 的買方提供去識別化月份樣本、接受書面固定範圍報價、排定開始日，並明確承諾提供真實但已去識別化的檔案。付款或訂金才記為 `paid_commitment`／`paid_transaction`，未發生前不得宣稱。

## 5. 什麼 NOT 要承諾

不得承諾稅務申報、稅務建議、正式記帳、傳票入帳、收入／費用認列、發票或退款／折讓的專業結論、簽證／簽章、法律意見、合規保證、一定找回金額、一定不漏開發票、代登入後台或固定三日必定完成。超出固定範圍就停止並重新確認，不默默擴張。

## 6. 哪裡需要人類／外部帳戶行動

Codex 不會登入或操作 Tasker、PRO360、LINE／FB 社群或買方帳戶，也不會發布 listing、發訊息或接收回覆。創辦人必須自行完成外部發布、回覆、報價、檔案收件、專業人士審閱與任何付款安排；以上標記為 `EXTERNAL_ACTION_REQUIRED`。在專業邊界審查前：`posting_state: READY_TO_POST`；`delivery_state: DELIVERY_BLOCKED_PENDING_PRO_REVIEW`。

## 7. 如何記錄 responses

每個詢問在 `memory/measurement_log.csv` 新增一列，填入 timestamp、channel、listing/version、inbound case ID、segment match、commercial stage、是否提供去識別化樣本、固定範圍報價是否接受、排定開始日、是否付款、例外類型、人工時數、是否需要專業審閱、停止／拒絕原因與 month-two continuation。只記錄實際發生的行為；瀏覽、按讚、稱讚與提案數不算 commitment。

`posting_state: READY_TO_POST`

`delivery_state: DELIVERY_BLOCKED_PENDING_PRO_REVIEW`

`WAITING_FOR_EXTERNAL_BEHAVIOR`
