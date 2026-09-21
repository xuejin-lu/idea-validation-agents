# Test Launch Checklist

狀態：`EXTERNAL_ACTION_REQUIRED`

Codex 沒有被授權登入或操作 Tasker、PRO360、LINE/FB 社群或任何外部買方帳戶；本 checklist 不代表已上架、已發訊息或已取得客戶。

## Launch channels

依順序使用已有需求訊號的管道：

1. Tasker 電商/會計相關案件頁：回應明確需求或刊登固定範圍服務。
2. PRO360 電商代營運/記帳相關需求頁：使用不誇大、不冒用資格的 listing copy。
3. 台灣電商營運/記帳社群：只在允許服務貼文的社團發布，遵守版規。
4. 轉介夥伴：詢問買方既有記帳士/會計師是否願意轉介資料整理需求；不把未持有資格寫成記帳服務。

不使用購買名單、群發冷信、冷電話或付費廣告作為第一個管道。

## Exact manual steps

### Before posting

- [ ] 審閱 `behavioral_test_package.md` 的 scope/exclusions。
- [ ] 用 synthetic data 產出 sample deliverable。
- [ ] 確認 listing 不含虛構 credentials、案例、結果或 compliance guarantee。
- [ ] 準備 intake form 和 privacy notice。
- [ ] 設定一個可記錄案件編號的測量表。

### After an inbound inquiry

- [ ] 確認對方是在台灣，且使用官網加多個通路。
- [ ] 確認需求是資料準備/差異清單，而不是正式記帳、申報或稅務建議。
- [ ] 發 intake form，不先要求完整帳務或登入權限。
- [ ] 要求去識別化小樣本；拒絕密碼、OTP、未遮蔽個資和銀行登入。
- [ ] 以同一 fixed-scope template 回覆，不為了成交承諾未定義的例外處理。
- [ ] 若要進一步，提供書面範圍/交付/限制/開始日；由買方決定是否接受。
- [ ] 記錄 commercial stage：interest / buyer_request / commitment / paid_transaction。

## What can be automated later

只有在真實測試中確認輸入/輸出穩定後，才考慮：

- 本地 spreadsheet formulas 做欄位標準化與筆數/加總檢查；
- 固定格式 CSV/XLSX 的欄位 mapping；
- exception taxonomy 的篩選、排序與狀態欄；
- 交付 checklist 的版本控制。

本階段不建 SaaS、不串接平台 API、不做瀏覽器自動化、不上傳原始檔到未審核的第三方 AI。

## External account/browser access

- Tasker/PRO360 發布需要創辦人自己的外部帳戶與權限；Codex 不代為登入或發布。
- 不要求買方提供電商、銀行、發票、金流帳密或 OTP。
- 若買方只允許後台登入而不提供匯出檔，停止本測試，改由合格資訊安全/帳務流程另行評估。

## Data/privacy precautions

- 先用 demo/synthetic data 驗證格式。
- 要求遮蔽姓名、地址、電話、統編、完整訂單號、信用卡/銀行帳號、token、OTP。
- 使用最小必要資料；檔案以案件代號命名，不用公司真名。
- 事先約定保存期限、可接觸人員、傳輸方式和刪除確認。
- 不把原始檔案拿去做公開案例、訓練資料或作品集。
- 差異清單只描述觀察到的資料，不作稅務/會計結論。
- 涉及正式記帳、申報、折讓/發票法定處理或稅務判斷時，交給買方合格專業人員。

## Stop conditions

- 買方要求未授權的記帳、申報、稅務 advice、簽證或 compliance guarantee。
- 買方要求帳密、OTP、未遮蔽敏感資料或直接操作支付/銀行後台。
- 樣本過大、格式過於客製，超出 fixed scope 卻不接受重新報價。
- 交付物會被當作正式帳冊/申報依據而沒有專業人士審閱。
- 沒有人願意提供去識別化樣本或接受書面範圍；不要用免費完整服務換取模糊興趣。

## Measurement log fields

- timestamp
- channel
- listing/version
- inbound case ID
- Taiwan segment match: yes/no/unknown
- requested platforms and file types
- commercial stage
- redacted sample offered: yes/no
- fixed-scope quote accepted: yes/no
- scheduled start date
- paid commitment: yes/no
- exception categories
- estimated operator hours
- professional review required: yes/no
- reason for rejection/stop
- month-two continuation: yes/no/unknown

## Completion rule

本 checklist 完成只代表資產準備好；未經創辦人實際在授權外部管道發布並記錄 buyer behavior，不得宣稱 test launched、demand validated 或已有付款。
