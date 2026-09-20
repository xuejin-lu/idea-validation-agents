# Opportunity Hypotheses

All hypotheses are tests, not software build recommendations. Evidence roles follow the stricter control spec.

## H1 — 室內裝修公司的圖說數量清單外包

- Target user: 5–30 人室內裝修／機電工程公司的估算或工務人員。
- Economic buyer: 負責人或工務主管。
- Exact job/workflow: 從 PDF／CAD 圖說整理工程數量、材料與發包前估算表。
- Observed pain: Tasker 有公開的遠端工程數量計算需求與 NT$100,000 預算；Tasker 服務商也把「案件多、人手不足、不想慢慢算」列為外包理由。
- Current substitute: 內部估算人員、Excel、外包工程估算師。
- Measurable value: 每張圖／每案整理工時、返工次數、發包前錯誤項目。
- Smallest testable offer: 只處理一個工種的一份去識別化圖說，交付數量表範例；工程責任由合作估算師承擔。
- Evidence references: `taiwan_construction_quantity_billing.json` E1, E2, E5.
- Largest unknown: 創辦人能否取得具工程專業的協作者。

## H2 — 公共工程估驗資料包預檢

- Target user: 有公共工程但內業人手不足的台灣小型營造廠。
- Economic buyer: 工務經理／營造廠負責人。
- Exact job/workflow: 對照契約、施工日誌、照片、數量與請款資料，檢查本期估驗包缺件。
- Observed pain: 台灣研究與官方程序描述多種文件、數量核對與分期請款；104 職缺明確付薪處理估驗與請款資料。
- Current substitute: 內部工務／估算員逐件整理、ERP。
- Measurable value: 退件次數、文件完整時間、請款提送延誤天數。
- Smallest testable offer: 契約附件＋一個月文件的人工缺件表，不簽章、不取代技師／監造。
- Evidence references: `taiwan_construction_quantity_billing.json` E2–E4.
- Largest unknown: 外部預檢能否接觸工程資料且不觸及法定簽核。

## H3 — IT 服務商標案適投／缺件檢查

- Target user: 5–50 人台灣 IT／系統整合／顧問服務公司。
- Economic buyer: 負責接案的老闆或 PM。
- Exact job/workflow: 閱讀招標文件、確認公司資格、列出缺件與期限。
- Observed pain: 104 付薪職缺、PRO360 客戶評價／需求與官方投標文件共同支持。
- Current substitute: 行政人工閱讀、標案顧問、標案平台。
- Measurable value: 讀案時間、發現缺件數、放棄不適投案件數。
- Smallest testable offer: 一案一頁預檢報告＋文件來源索引，不代寫、不保證得標。
- Evidence references: `taiwan_tender_readiness_strict.json` E1–E4.
- Largest unknown: 預檢是否有獨立付費價值。

## H4 — 活動／行銷公司提案附件資料夾整理

- Target user: 常投政府活動／宣傳／教育訓練標案的台灣小型公司。
- Economic buyer: 負責人或企劃主管。
- Exact job/workflow: 從歷年實績、團隊履歷、證照、報價與附件建立可重用的投標資料夾。
- Observed pain: PRO360 頁面有活動／勞務類標案需求與多筆客戶評價；104 標案職缺顯示文件管理為付費工作。
- Current substitute: 每案複製 Word／雲端資料夾、外包企劃。
- Measurable value: 每案尋找資料時間、缺附件數、重複改稿次數。
- Smallest testable offer: 用一個公開案例做資料夾模板與附件索引，邀請公司提交一案文件需求；不碰投標策略。
- Evidence references: `taiwan_tender_readiness_strict.json` E1–E2.
- Largest unknown: 活動公司的文件是否足夠相似可重用。

## H5 — 食品／保健品牌通路對帳差異包

- Target user: 同時經營蝦皮、momo、官網的台灣食品／保健品牌。
- Economic buyer: 品牌負責人或財務主管。
- Exact job/workflow: 對照平台銷售、退款、平台費、物流、發票與銀行入帳，列出異常。
- Observed pain: 104 職缺把該流程列為付薪工作，PTT 賣家描述對帳麻煩並長期延後。
- Current substitute: Excel、電商會計、記帳士、ERP。
- Measurable value: 異常金額、異常筆數、月結完成時間。
- Smallest testable offer: 一個月 CSV 的人工差異報告，不做申報、不串 API。
- Evidence references: `taiwan_ecommerce_reconciliation_strict.json` E1–E4.
- Largest unknown: 垂直內的重複異常規則。

## H6 — 電商退貨／平台費毛利週報

- Target user: SKU 多、退貨頻率高的台灣多平台賣家。
- Economic buyer: 品牌主或營運主管。
- Exact job/workflow: 將退款、運費、抽成與折扣對應到 SKU／平台，找出毛利異常。
- Observed pain: 賣家討論描述退款運費與抽成侵蝕利潤；職缺要求平台對帳與退款處理。
- Current substitute: 月底一次性對帳，或容忍差異。
- Measurable value: 發現的異常金額、可追回／修正的款項、週報處置率。
- Smallest testable offer: 手工一頁異常週報範例，要求去識別化資料。
- Evidence references: `taiwan_ecommerce_reconciliation_strict.json` E1–E3.
- Largest unknown: 品牌是否每週採取動作，而非只要稅務帳。

## H7 — 小企業薪資例外資料收集器

- Target user: 台灣餐飲、零售、服務業的兼任人資／行政。
- Economic buyer: 10–50 人企業負責人。
- Exact job/workflow: 收集跨夜班、加班、請假、獎金、到離職與勞健保異動，整理給薪資計算者。
- Observed pain: Dcard 直接描述 Excel／手算容易錯；104 顯示此流程是付薪職責。
- Current substitute: Excel、打卡系統、薪資 SaaS、記帳士。
- Measurable value: 每月追資料時間、待補資料件數、重算次數。
- Smallest testable offer: 匿名化例外清單與流程範本，不接觸真實薪資、不提供勞法意見。
- Evidence references: `taiwan_payroll_exception_strict.json` E1–E4.
- Largest unknown: 雇主端是否願意付費，現有工具是否已足夠。
