# Opportunity Hypotheses

Fresh run date: 2026-09-20. All hypotheses are Taiwan-first and remain hypotheses until behavioral validation.

| ID | Target user / buyer | Job to be done | Observed pain / workaround | Smallest testable offer | Evidence refs | Largest unknown | Classification |
|---|---|---|---|---|---|---|---|
| H1 | Multi-channel Taiwan e-commerce brand owner / finance lead | Close one month of platform, bank, invoice and refund data | Internal role removed; manual reconciliation and monthly handoff remain | Fixed-scope one-month reconciliation + exception report | Tasker 2026-08-28; 104 e-commerce accounting 2026 | Month-two repeat and willingness to accept standardized scope | startup-ready-to-test |
| H2 | Taiwan tender-active SME owner / bid lead | Decide go/no-go and check required files before bidding | Manual reading of tender docs, attachment/version/format risk | One tender preflight: red flags + missing-document checklist | PRO360 review 2026-06-22; Taiwan Tender guide 2026-07-10; 104備標 | Buyers pay for preflight alone vs full proposal writing | startup-ready-to-test, low confidence |
| H3 | Taiwan ops/accounting team with recurring scanned reports | Convert one narrow document family into validated Excel | Manual key-in and cleanup; freelancer or script | One batch conversion with reconciliation/QA note | Tasker conversion service 2026-09-18; prior Tasker requests archived | Same buyer/monthly volume and shared schema | service-ready-to-test |
| H4 | Taiwan contractor/subcontractor | Prepare one trade-specific quantity/progress billing packet | Expert manual measurement, spreadsheets, evidence collection | One standardized billing packet for one phase | Tasker construction category; 104 estimate/billing jobs | Can expertise be delegated without losing trust | service-ready-to-test |
| H5 | Taiwan operator needing recurring public-data updates | Receive a scheduled, structured update from a specific source | Manual searching/collection; custom scripts | Monthly report + change alert for one source and field set | Tasker recurring scraping requests 2026-08/09 | Same vertical repeats enough to productize | research-more |
| H6 | Taiwan small employer / accountant | Reconcile attendance, payroll and statutory inputs | Excel/manual calculator and paid payroll labor | Manual audit of one payroll cycle, not filing | archived prior evidence; current 104 payroll search | Recent external buyer request for standardized outsourcing | research-more |
| H7 | Taiwan food brand / importer | Keep label source data and change log consistent | Internal QA/consultant/regulatory checking | One SKU label data intake + change checklist | archived prior evidence; current regulatory context | External purchase and repeat frequency | research-more |

## Falsification order

1. H1: ask for a redacted month and a paid/committed second month.
2. H2: offer preflight-only to determine whether the wedge exists separate from proposal writing.
3. H5: interview only after identifying a single data source/vertical with at least three similar requests.

No hypothesis should be implemented as software before the stated unknown is resolved by behavior.
