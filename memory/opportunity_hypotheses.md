# Opportunity Hypotheses

All hypotheses are Taiwan-specific and intentionally framed as tests, not build recommendations. Evidence references point to the records in `memory/problem_evidence/`.

## H1 — IT／專業服務商的標案文件預檢包

- Target user: 5–50 人台灣 IT、顧問或專業服務公司負責標案的行政／PM。
- Economic buyer: 公司負責人。
- Exact job/workflow: 從政府採購網下載一案，判斷資格、整理必備文件與期限，檢查服務建議書是否缺章節或附件。
- Observed pain: 官方投標須知呈現多文件、多階段要求；104 職缺與 PRO360 顯示相鄰工作被付費雇用／外包。
- Current substitute: 老闆／行政人工讀 PDF、重用舊標書、外包顧問。
- Measurable value: 預檢交付時間、缺件數、被排除的不可投案件數。
- Smallest testable offer: 一頁檢查表＋收到一份公開招標文件後 24 小時內輸出「適投／不適投／缺件」範例；不提供法律意見。
- Evidence references: `taiwan_tender_bid_readiness.json` E1–E5.
- Largest unknown: 目標垂直的案量與預檢付費意願。

## H2 — 標案機會「適投清單」訂閱／轉介

- Target user: 沒有標案專員但想嘗試政府勞務案的台灣小公司。
- Economic buyer: 負責接案的老闆。
- Exact job/workflow: 每週從公告中篩選符合公司登記範圍、實績、地區、期限與預算的案件。
- Observed pain: CITYGLOW 已將標案推播與初判商品化，說明「找對案」是被包裝的工作；104 職缺也顯示標案資料蒐集是付費勞動。
- Current substitute: 人工盯政府電子採購網、平台推播、熟人顧問。
- Measurable value: 每週收到的案件中，符合資格且能在期限內準備的比例。
- Smallest testable offer: 一個垂直的公開週報，要求申請者填公司類型與過去實績，以量測精準度；不先做爬蟲或軟體。
- Evidence references: `taiwan_tender_bid_readiness.json` E2–E5.
- Largest unknown: 免費推播已有競品，使用者是否願意留下足夠資料或轉成高價預檢。

## H3 — 食品包裝標示「印刷前風險分流」

- Target user: 台灣微型食品品牌、進口商與食品包裝設計公司。
- Economic buyer: 品牌負責人／設計案 PM。
- Exact job/workflow: 上傳去識別化標示稿與配方資料，先分出「資料缺漏／需食品技師審查／可進一步人工核對」三類。
- Observed pain: TFDA 官方列出多個法定欄位與罰則；在地服務按件定價。
- Current substitute: 自行查規定、照舊稿、找食品技師或報驗行。
- Measurable value: 來回補件次數、印刷前發現的問題數、從稿件到可送專業審查的時間。
- Smallest testable offer: 自檢清單＋合格食品技師轉介表單；創辦人不給正式法規結論。
- Evidence references: `taiwan_food_label_preflight.json` E1–E5.
- Largest unknown: 客戶是否願意在線上提供配方與外文資料，以及技師合作供給。

## H4 — 進口食品中文標示資料完整性包

- Target user: 少量進口食品／零食／保健品的台灣小型進口商。
- Economic buyer: 進口商負責人或採購／報關窗口。
- Exact job/workflow: 在報關／印刷前彙整外文成分、營養資料、進口商資訊、原產地與中文標示所需附件。
- Observed pain: 官方說明指出進口食品可能缺中文標示；報驗行按件收費且要求多項文件。
- Current substitute: 報關行／報驗行一次性處理、人工翻譯與 Excel 文件夾。
- Measurable value: 缺件補件回合、每件 SKU 整理時間、送審前退回次數。
- Smallest testable offer: 文件需求清單與資料完整性檢查，不碰法規判斷；從進口商社群與報驗行合作頁取得有意願者。
- Evidence references: `taiwan_food_label_preflight.json` E1, E5 plus the official source note.
- Largest unknown: 與報驗行／報關行既有合作的轉換摩擦。

## H5 — 電商月結差異清單（食品／保健垂直）

- Target user: 在蝦皮、momo、官網同時賣貨的台灣品牌營運／會計。
- Economic buyer: 品牌負責人或記帳士事務所。
- Exact job/workflow: 匯入各平台月報與銀行／發票資料，列出退款、平台費、物流、入帳與商品銷售額的異常。
- Observed pain: 台灣在地服務商直接拆解該對帳流程；電子發票系統與多通路記帳已成付費類別。
- Current substitute: Excel 手工對帳、兼任會計、ERP／電子發票整合。
- Measurable value: 月結完成日、未解釋差異金額、人工核對行數。
- Smallest testable offer: 一個月的人工差異報告範例，不串 API；要求客戶提供去識別化 CSV。
- Evidence references: `taiwan_multichannel_ecommerce_reconciliation.json` E1–E5.
- Largest unknown: 垂直特有的例外是否足以避開通用整合競爭。

## H6 — 電商退款／平台費毛利異常週報

- Target user: 月交易量中等、跨平台且 SKU 較多的台灣 D2C 品牌。
- Economic buyer: 品牌主或營運主管。
- Exact job/workflow: 將退款、折扣、物流與平台費映射到 SKU／通路，找出毛利低於門檻的例外。
- Observed pain: 在地文章把平台費、退款與物流列為對帳拆解項；本地服務有按月外包價格。
- Current substitute: 月底一次性人工整理，或只看平台總額。
- Measurable value: 發現的異常筆數、可能追回／修正的金額、每週報告閱讀／處置率。
- Smallest testable offer: 對一個月匿名資料做一頁例外報告；不做即時監控、不連接平台。
- Evidence references: `taiwan_multichannel_ecommerce_reconciliation.json` E1–E4.
- Largest unknown: 品牌是否願意每週採取行動，而不是只想要月結帳。
