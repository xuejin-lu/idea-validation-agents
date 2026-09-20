# Opportunity Shortlist

## Research constraints

- Market: Taiwan-first; online discovery and inbound/community/marketplace channels preferred.
- Founder default: 1–3 people, low capital, manual-first, NT$0–5,000 validation budget, up to 3 months.
- This run does not recommend building software or running a paid pilot.
- Evidence labels: Observed, Inferred, Estimated, Unknown. Evidence roles are kept separate: pain, paid_labor, transaction, competition, regulatory_context, market_context.
- Prior run preserved at `memory/discovery_runs/run-9281428/`; this is a fresh synthesis, not a deletion of prior evidence.

## Top Startup Opportunities

### Candidate A — 台灣中小電商的多通路月結、發票與退款差異處理

- Startup classification: `startup-ready-to-test`
- Target user: 以官網＋蝦皮/momo/PChome 等多通路銷售的台灣中小品牌、代理商與電商營運者。
- Economic buyer: 品牌負責人、營運主管或財務負責人。
- Problem: 每月要從多個平台、金流、ERP、銀行與發票流程彙整銷售資料，處理對帳差異、退款/折讓與月結交付；錯漏會造成漏開/錯開、延遲結帳或會計交接成本。
- Current workaround: 內部兼職/正職會計、Excel/ERP 匯出後人工核對、外部會計師或記帳單位接手申報前資料。
- Strongest evidence:
  - **Observed / transaction + pain / Tier A-B, 2026-08-28:** 台灣 Tasker buyer explicitly requested long-term outsourcing after cancelling an internal finance role; scope includes multi-channel invoices, sales aggregation, reconciliation, refunds/allowances, monthly reports and handoff to accountants. Budget shown as NT$6,000 and 15 proposals. [Source](https://www.tasker.com.tw/cases?selected_tags=250%2C60%2C64)
  - **Observed / paid_labor / Tier A, 2026-06/07:** 104 listings for Taiwan e-commerce accounting include per-channel settlement, bank/platform reconciliation, invoices, refunds/allowances and monthly close; listed salaries include NT$30,000–33,000 and NT$45,000–60,000/month. [Source](https://www.104.com.tw/jobs/search/?jobcat=2003001000&keyword=%E5%B0%8D%E5%B8%B3%E5%96%AE)
  - **Observed / paid_labor / Tier A, 2026-06/07:** another 104 listing describes platform account reconciliation, e-invoice documents and tax-document preparation. [Source](https://www.104.com.tw/jobs/search/?jobcat=2003001000&keyword=%E9%9B%BB%E5%95%86%E5%B9%B3%E5%8F%B0&page=1)
- Evidence quality: A/B mix; recent Taiwan buyer-side externalization plus repeated paid labor. Strongest commercial signal is one explicit external request, so demand breadth remains Unknown.
- Value mechanism: measurable monthly hours avoided, fewer reconciliation exceptions, faster month close, and reduced leakage/error risk. Do not claim a numeric saving before observing a customer’s files.
- Why now: multi-channel workflows are visibly fragmented across platforms and the buyer is already replacing internal labor with outsourcing.
- Repeatability: recurrence trigger = monthly close, refunds/allowances and tax/accounting handoff. Expected recurrence type = `same-customer` and `cross-customer`.
- Standardizable unit: channel-to-ledger intake schema, exception taxonomy, monthly checklist, evidence pack and accountant handoff.
- Leverage path: reusable templates/rules, standardized intake, trained operator QA, then selective automation. Founder-labor scaling risk = `medium` until month-two volume and exception rate are measured.
- Main contradiction: existing accountants/ERP integrations may already cover the buyer; the Tasker listing may represent a narrow segment and not a scalable product wedge.
- Biggest unknown: whether buyers will repeat the same narrow reconciliation package for at least two monthly cycles and accept a standardized scope without bespoke bookkeeping.
- Cheapest behavioral test: publish a fixed-scope “one monthly close / one platform bundle” offer through a Taiwan marketplace or relevant e-commerce/accounting community; request a redacted sample and a second-month commitment before any integration. Success signal: 3 qualified requests, 1 real payment or firm scheduled follow-up, and the same exception fields recurring across 2 customers.
- Kill criterion: no qualified buyer will share a sample or pay for a fixed-scope close; every request requires unrelated bookkeeping/tax work; or month-two work is not repeated.

### Candidate B — 特定產業的政府標案投標前文件健檢與公司資料包整理

- Startup classification: `startup-ready-to-test` (low-confidence; specific preflight wedge still unproven)
- Target user: 台灣中小工程、專業服務、設備與活動供應商，尤其第一次或低頻參與政府/法人標案的團隊。
- Economic buyer: 公司負責人、投標/業務主管或標案專員。
- Problem: 投標前需快速判讀招標須知、資格門檻、格式、附件與評分要求；文件/頁碼/附件錯誤可能造成失分或不予開標。完整服務建議書代寫已有外包，但輕量的 go/no-go 與格式健檢 wedge 尚未被單獨驗證。
- Current workaround: 內部標案專員、顧問/寫手、公司既有履歷與資格文件資料夾，加上人工逐份檢查。
- Strongest evidence:
  - **Observed / transaction + pain / Tier A-B, 2026-06-22:** PRO360 Taiwan government-tender consultant page shows a customer review praising a consultant for completing a service proposal within a limited time; this is buyer-side purchase/review evidence for external help, not merely vendor marketing. [Source](https://www.pro360.com.tw/category/tender_proposal)
  - **Observed / pain / Tier B, 2026-07-10:** Taiwan Tender guide identifies repeated pre-bid work: read exclusion conditions, profitability/contract risks, and avoid document/format mistakes. [Source](https://twbuying.org/guide/tender-doc-reading)
  - **Observed / paid_labor / Tier A, 2026-06:** 104 “備標” listings specify collecting/analyzing tender data, reading tender documents, preparing bid meetings, proposal presentations, formatting and data integration. [Source](https://www.104.com.tw/jobs/search/?keyword=%E5%82%99%E6%A8%99)
  - **Observed / transaction + paid_labor / Tier A-B, 2026-05-21:** Tasker request seeks external government proposal writing, explicitly asks for long-term cooperation and offers a staged fee/award structure. [Source](https://www.tasker.com.tw/cases?selected_tags=442%2C88)
- Evidence quality: B plus A/B external buying evidence for full proposal work; the preflight-only scope is an inference, not directly purchased yet.
- Value mechanism: fewer avoidable disqualifications, faster go/no-go decisions, and reusable company-document preparation. Exact win-rate or hours saved are Unknown.
- Why now: recent buyer reviews and job listings show a live external labor market, while the proposed narrow wedge can be tested without writing a whole proposal.
- Repeatability: recurrence trigger = each bid opportunity; expected recurrence type = `same-customer` for active bidders and `cross-customer` for a vertical. Frequency by target vertical is Unknown.
- Standardizable unit: bid-readiness checklist, common document profile, qualification matrix, attachment/version checklist and red-flag report.
- Leverage path: reusable company profile/templates, vertical-specific rules and delegated document QA. Founder-labor scaling risk = `medium-high` because bid-specific interpretation remains expert work.
- Main contradiction: most observed buyers may want full proposal strategy/writing, not a standalone preflight; procurement trust and domain credentials may be required.
- Biggest unknown: whether a narrow vertical has enough bids per customer and whether buyers pay for a preflight before asking for full proposal support.
- Cheapest behavioral test: offer a single paid-or-committed “投標前 30 分鐘資料健檢＋一頁紅旗清單” through PRO360/Tasker or a relevant industry group, with no bid writing. Success signal: 3 requests from one vertical and at least 1 paid or scheduled repeat review.
- Kill criterion: prospects only ask for free bid searches or full proposal writing; no one shares the tender pack/company profile; or repeat trigger cannot be observed.

## Service-ready-to-test (commercially real, startup repeatability not yet strong enough)

### Candidate C — PDF/掃描報表/對帳單轉 Excel 與統計清理

- Startup classification: `service-ready-to-test`
- Target user/buyer: Taiwan SMEs, researchers, accountants and operations teams with scanned or inconsistent tables.
- Problem/current workaround: manual key-in and spreadsheet cleaning are slow/error-prone; they use freelancers, internal staff or scripts.
- Evidence: Tasker buyer requests from 2026-06/07 included PDF/image-to-Excel work with multiple files; a current Taiwan provider lists batch extraction, consistency checks and NT$3,000+ per-job pricing. [Service source](https://www.tasker.com.tw/workroom/tinobrief/service-detail/47337)
- Why not Top Startup: external demand and standardizable processing are plausible, but repeated same-customer volume and a shared document family are not demonstrated. Most visible demand is project-by-project.
- Repeatability: trigger = unknown; expected recurrence = `cross-customer` only; standardizable unit = extraction/QA pipeline; leverage = scripts/templates; founder-labor scaling risk = `medium-high`.
- Cheapest test: ask for a sample from one narrow document family and quote one batch; only promote if two buyers have recurring monthly/quarterly files.

### Candidate D — 工程/營造的數量計算、估算與請款資料整理

- Startup classification: `service-ready-to-test`
- Target user/buyer: Taiwan small contractors, subcontractors and owners.
- Problem/current workaround: measurement, quantity takeoff, initial estimates, progress quantities and subcontractor billing require expert manual work across plans/photos/spreadsheets.
- Evidence: 2026 Tasker requests show buyers seeking remote quantity/initial estimates and longer cooperation; 104 listings show paid duties for periodic subcontractor billing, invoices, evidence and progress/quantity records. [Tasker category](https://www.tasker.com.tw/cases?selected_tags=49%2C58%2C472) · [104 search](https://www.104.com.tw/jobs/search?isnew=3&keyword=%E4%BC%B0%E9%A9%97%E8%A8%88%E5%83%B9)
- Why not Top Startup: externalization is real, but scope is professional and project-specific; labor may scale 1:1 unless one narrow sub-workflow is isolated.
- Repeatability: trigger = project phases and periodic billing; expected recurrence = `same-customer` plausible; standardizable unit = quantity/billing checklist; leverage = templates and QA; founder-labor scaling risk = `high`.
- Cheapest test: target one trade and one billing package, then measure whether the same customer sends a second phase.

## Research-more / insufficient gates

### Candidate E — 例行公開資料監測與提醒（特定垂直，不做泛爬蟲）

- Startup classification: `research-more`
- Evidence: Tasker lists recent Taiwan buyer requests for twice-monthly collection of around 150 items and for periodic city-government contact data updates. [Source](https://www.tasker.com.tw/cases/top?selected_tags=120)
- Why interesting: recurrence and standardized inputs/outputs are visible, and the first version could be a report/alert service.
- Gate failure: requests are heterogeneous; buyer identity, willingness to pay for a productized niche, and a repeatable vertical are not yet established. One marketplace category cannot prove a market.
- Next evidence: find three Taiwan buyers with the same source, same fields and same alert trigger; otherwise treat as custom scraping service.

### Candidate F — 薪資計算/出勤與勞健保資料外包

- Startup classification: `research-more`
- Gate failure: Taiwan paid labor exists, but recent independent buyer-side externalization for a narrow standardized package was not refreshed in this run. Regulation and vendor pages are not enough.

### Candidate G — 食品標示資料整理/法規變更協作

- Startup classification: `research-more`
- Gate failure: regulatory burden and vendor/consultant supply are visible, but recent Taiwan buyer-side external purchase/outsourcing and repeatable scope were not sufficiently demonstrated.

## Not recommended now

- Generic “AI document-to-data” platform: real jobs exist, but without a repeated document family the opportunity collapses into custom service work.
- Generic construction estimation platform: buyer pain exists, but trust, professional judgment and custom scope create high founder-labor risk.
- Payroll or food-label software as a first build: evidence currently proves obligation or internal labor, not enough external buying for a narrow initial wedge.

## Decision

The strongest problem worth testing is **monthly multi-channel e-commerce reconciliation as a fixed-scope recurring service**, with tender preflight as the second test only after narrowing to one vertical. Both are test candidates, not build recommendations. The e-commerce candidate has the clearest combination of recent external demand, repeated paid labor, monthly recurrence and reusable processing units.
