# Opportunity Hypotheses

The hypotheses below are designed for cheap behavioral tests; none recommends building software or running a paid pilot.

## H1 — 檢測報告 PDF→Excel 專業資料整理

- Target user: 台灣檢測／實驗室／品保團隊。
- Economic buyer: 專案主管或需要在期限前交付報表的公司負責人。
- Exact job/workflow: 把圖片型 PDF 中的數字、英文、表格欄位轉成 Excel，再做人工校正與格式整理。
- Observed pain: Tasker 2026-06 買方案件有 4–5 份 PDF、NT$6,000 預算與 52 個提案者；104 文件整理職缺證明內部人工存在。
- Current substitute: 內部行政、OCR＋人工校正、資料輸入外包。
- Measurable value: 每頁交付時間、錯誤欄位數、人工校正比例。
- Smallest testable offer: 一份真實 PDF 的 10 頁轉檔樣本＋錯誤標記，不做大規模系統。
- Evidence references: `taiwan_document_to_structured_data.json` E1, E3.
- Largest unknown: 同一格式是否可重複，以及客戶會不會每月再來。

## H2 — 工程估驗附件 PDF→公司模板

- Target user: 台灣營造／工程顧問公司的內業或估驗人員。
- Economic buyer: 工務主管或工程公司負責人。
- Exact job/workflow: 把施工照片、日報、數量表與 PDF 附件整理成公司／業主要求的 Word／Excel 包。
- Observed pain: 工程估驗是付薪工作；Tasker 有工程數量估算／外包案件；文件轉換是相鄰的買方需求。
- Current substitute: 內部估算／文件人員、工程估算師、營建 ERP。
- Measurable value: 文件退回次數、每期請款包整理時間、欄位錯誤。
- Smallest testable offer: 只做一個公開樣本的附件索引與格式重整，不簽章、不做工程判斷。
- Evidence references: `taiwan_document_to_structured_data.json` E1–E3; `taiwan_construction_external_demand_recent.json` E1–E3.
- Largest unknown: 工程公司是否願意把責任可分離的資料整理段外包。

## H3 — 多通路發票／對帳資料委外

- Target user: 官網＋蝦皮＋momo／PChome 的台灣品牌。
- Economic buyer: 品牌負責人或財務主管。
- Exact job/workflow: 收集各通路發票、退款／折讓、平台入帳與銀行資料，整理成每月交給會計師的資料包。
- Observed pain: 2026-08 Tasker 買方明確寫出取消內部財務職位、人工錯開／漏開與帳務延遲風險，並公開 NT$6,000 委外預算。
- Current substitute: 委外記帳／會計、Excel、ERP、平台報表。
- Measurable value: 月結完成日、缺件數、退款／折讓差異與重工時間。
- Smallest testable offer: 一個月去識別化資料包整理，不做記帳申報與稅務判斷。
- Evidence references: `taiwan_ecommerce_outsourced_reconciliation.json` E1–E3.
- Largest unknown: 是否續用第二個月與是否需要人工例外規則。

## H4 — 多店收入與帳戶對帳資料整理

- Target user: 有多店／多業務收入來源的台灣公司。
- Economic buyer: 公司負責人或財務主管。
- Exact job/workflow: 建立收入歸屬、店家帳戶往來與對帳結果表，整理漏帳與錯帳例外。
- Observed pain: Tasker 2026-08 買方公開 NT$24,000 案件，目標是降低人工彙整錯誤與漏帳。
- Current substitute: 內部會計、Excel、ERP 顧問。
- Measurable value: 未對帳項目、漏帳筆數、每月整理時間。
- Smallest testable offer: 只做一個月的對帳差異表，不做帳務簽證。
- Evidence references: `taiwan_ecommerce_outsourced_reconciliation.json` E2 and `taiwan_document_to_structured_data.json` E3.
- Largest unknown: 目標產業是否比電商更容易取得資料與續用。

## H5 — 標案文件完整性預檢

- Target user: 第一次／偶爾投標的台灣活動、顧問或 IT 服務公司。
- Economic buyer: 公司負責人或標案 PM。
- Exact job/workflow: 對照招標文件整理資格、附件、服務建議書章節與期限，輸出缺件清單。
- Observed pain: PRO360 近期客戶購買完整提案服務；104 顯示內部標案準備為付薪工作；台灣標案網近期內容反映格式／附件錯誤困擾新手。
- Current substitute: 老闆／行政、完整標案顧問、政府採購網人工搜尋。
- Measurable value: 讀案時間、缺件數、免費預檢後的正式報價請求。
- Smallest testable offer: 一案一頁預檢，不代寫、不保證得標。
- Evidence references: `taiwan_tender_external_demand_recent.json` E1–E4.
- Largest unknown: 窄版預檢是否可獨立收費。

## H6 — 活動標案的實績／附件資料夾整理

- Target user: 台灣小型活動／行銷公司。
- Economic buyer: 負責人或企劃主管。
- Exact job/workflow: 把歷年案例、團隊履歷、證照、附件與報價資料整理成可複用投標包。
- Observed pain: PRO360 評價顯示客戶將服務建議書與標案工作外包；104 顯示文件管理與標案流程為付薪工作。
- Current substitute: 每案複製 Word／雲端資料夾、外包企劃。
- Measurable value: 每案找資料時間、附件缺失與重複排版次數。
- Smallest testable offer: 一個實績資料夾模板＋真案缺件檢查。
- Evidence references: `taiwan_tender_external_demand_recent.json` E1–E3.
- Largest unknown: 活動標案文件是否足夠標準化。

## H7 — 小企業考勤薪資例外收集

- Target user: 台灣餐飲／零售／服務業兼任 HR／行政。
- Economic buyer: 10–50 人企業負責人。
- Exact job/workflow: 收集加班、跨夜、請假、獎金、到離職與勞健保異動，交給薪資計算者。
- Observed pain: Dcard 與 104 證明工作與人工公式問題；但近期買方外包證據不足。
- Current substitute: Excel、打卡系統、薪資 SaaS、薪資代辦。
- Measurable value: 待補資料件數、每月追資料時間、重算次數。
- Smallest testable offer: 匿名流程研究與例外清單，不收真實薪資資料。
- Evidence references: `taiwan_payroll_externalization_unproven.json` E1–E3.
- Largest unknown: 雇主是否真正想外包。
