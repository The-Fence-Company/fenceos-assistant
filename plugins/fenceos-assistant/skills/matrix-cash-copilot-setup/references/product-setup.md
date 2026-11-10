# Product-specific setup and verification

This packaged reference is a navigation aid. At every start, follow [Current deployed product knowledge](live-product-knowledge.md); current guide/build identity and enabled account controls determine which instructions apply. Never use a source feature as proof it is deployed.

These are source-grounded navigation hints, not proof of the currently deployed UI. Reinspect live labels, active business, capabilities, and save behavior before acting. Do not needlessly inspect source code during a customer onboarding session.

## Entry and existing data

CashOS hosts Cash Copilot plus an embedded Matrix. The default customer sign-in is `https://matrix.thefencecompany.com/login`. Supply and open this address yourself after orientation/public-guide refresh; honor an already verified organization-specific deployment. Do not ask a first-time user to identify a "login host." Ask for an invitation/link only when the known destination fails or points to the wrong business. The signed-in launchpad `/` has Matrix and Cash Copilot cards. `/matrix` is the embedded budget, `/dashboard` the cash timeline, and `/settings` the cash configuration. Use the embedded Matrix under the confirmed CashOS account; a standalone or local-only Matrix page may not share saved goals with Cash Copilot. The login page offers work-email/password and Google; Google email must match an existing CashOS account. Google sign-in to CashOS does not connect Gmail for financial-record discovery. Signed-in sessions expire; when the login page reappears mid-session, say so, ask the owner to sign in again in the same browser, and re-read business, plan and the change ledger before any write.

Cash Copilot exposes a five-step initial dashboard tour and a persistent **Learning guide** with ten topics: weekly routine, dashboard definitions, week management, forecasts/overrides, AP planning, QuickBooks AP export/upload, recurring/debt, goals/payroll, weekly close, and outflow definitions. Read the relevant topics through visible navigation. Matrix ships Setup Guide and Migration Guide links; use the current product links rather than guessing remote standalone URLs.

Current Matrix source groups the workspace into **Overview**, **Build Budget**, **Track**, and **Plan Scenarios**. Build Budget has Budget, Cost Structure, Revenue History, COGs, Overhead, Revenue Plan, Loans, and Profit Allocation tabs. Track has Actuals and Quarterly Review. Settings provides Import P&L, Import Excel Matrix, Export Budget (JSON), and Import Budget (JSON). Older embedded bundles can still show earlier labels. Use the visible UI and do not assume the remote Matrix build and CashOS fallback are identical.

Earlier guide copies contained browser-only storage claims, Command Center guarantees, inconsistent Magic Number definitions, and loose reconciliation tolerances. Corrected guides distinguish standalone storage from CashOS sync and define Magic Number as total direct COGs, with overhead separate. Still verify actual storage and formulas, reconcile money to the source or explained rounding, and never accept an unexplained variance. Overhead percentage and crew-based labor are derived from approved inputs.

Verify whether data already exists. Matrix imports can overwrite budget sections. Use its supported Settings > Export Budget/backup controls, when available, before import. Do not clear browser storage, accept an old local restore, or reset a budget to make onboarding appear new. A business switch requires a fresh identity and data check before any write.

## Annual bonuses and independent plans

The public Matrix guide refreshed October 28, 2026 describes **Build Budget > COGs > Installation Performance Bonuses** as an annual dollar amount and **Settings > Saved budgets > Create separate budget copy** for independent plans. Verify both in the signed-in business; guide availability is not a completed edit test.

For an approved annual installation-bonus amount, inspect existing crew costs, direct labor and overhead before using the dedicated field, so it is included once. Leave ordinary crew rates/hours unchanged. The field does not calculate eligibility or individual awards. Separately inspect Cash Copilot payroll/recurring sources; adding a Matrix budget amount does not authorize a second cash payment or schedule.

For another year, export the selected plan, inspect the supported separate-copy action and approve its target period/name. Verify the original remains intact and the copy is selected. Review copied actuals, revenue history, loan dates and monthly assumptions before using it. The current guide describes JSON import/restore as creating separate copies; verify live semantics before any restore. Matrix exports exclude Cash Copilot goals/payroll settings. Export each required plan separately. Do not infer successful restoration, independent-year persistence or server sync from a visible selector.

## Matrix

In maintainer-reviewed Matrix source (`ec18535ffa199229236d6672d2e56ea59b075cab`, `packages/budget-ui/src/App.tsx`), budget and planning edits autosave after about 300 milliseconds. This is source evidence, not a live-client guarantee; customers do not need repository access. Establish or reuse approval for the exact business, plan, fields and values before the first keystroke or selection. Do not draft unapproved values in live controls or wait for a Save click to obtain approval. Check the current save status and persisted readback after the approved batch.

### Units, currency and percentage controls

Read the unit label beside each control before typing: dollars, thousands, cents, percent as 15 or as 0.15, annual or monthly. Enter one approved value, leave the field, wait for the save status, reload and read it back before entering the rest of the batch. If the control reformats or rescales the value, or a documented control is absent, stop: the live control wins over the guide, the unit is unknown until a read-back shows it, and the gap is recorded for support. Never type the whole batch into a field whose unit has not been proved once.

1. **Choose the import path.** Use P&L import for monthly QuickBooks `.xlsx` reports. Use Import Matrix for a legacy Fence Matrix Excel workbook; it can replace the current budget, including year, history, crew, cost, and overhead data. JSON budget restore is another distinct action. Do not run these imports consecutively without determining which overlapping fields should win.
2. **Preview and reconcile.** Review years, completeness, revenue, COGS, net income, and account mappings. Prefer the most recent representative complete year as the overhead baseline, subject to owner confirmation. Complete calendar years supply seasonal history. Partial-year annualization, if offered, is an explicit projection with approved assumptions, not completed historical data. Generic P&L PDFs are not direct workbook imports.
3. **Review mapping manually.** Account names alone do not establish whether payroll, loans, transfers, depreciation, or owner payments belong in overhead. Mark excluded rows and explain why. The P&L import fills history/overhead; it does not finish the crew/direct-cost model. AI mapping or CFO Advisor may transmit account data to another service or incur cost; leave it unused unless separately authorized and its destination is understood.
4. **Historic Revenue.** Confirm monthly values and annual sums against the source. Keep actuals and projections separate. If no compatible import exists, enter reviewed values via the UI rather than pretending a generic spreadsheet is supported.
5. **COGs/direct costs.** Review material/subcontractor/equipment percentages, crew count and roles, hourly rates, annual hours, and relevant non-field production staff. Resolve labor burden and overlap with overhead. Use this business's data, not examples from the setup guide.
6. **Overhead.** Review imported categories and known future changes. Verify each displayed input's annual/monthly unit. Check office payroll, insurance, leases, taxes, and owner compensation against the agreed classification.
7. **Revenue plan.** Set the budget year and approved annual target or projection. Where present, configure Revenue Strategy sales mix, capacity and close-rate assumptions. Check Cost Structure and budget totals for consistency. Existing strategy rows may take precedence over a Quick Budget Projection in downstream goal imports.
8. **Optional pages.** Loans, Profit Allocation, Actuals, and Quarterly Checkup are useful only within the requested scope. Do not invent a missing Command Center button: CashOS can intentionally hide it.
9. **Persist and verify.** Wait for save/sync status, reload in the same org, and compare history, overhead, crews, and target; only then do the ledger rows move from entered to persisted and the owner hears "saved". A save-error banner or a value that reverts after reload is not saved, whatever the field showed before the reload. Distinguish browser-local persistence from confirmed CashOS sync. A successful goal read/import in Cash Copilot is additional evidence that the saved Matrix state is available to CashOS, but still check the transferred values.

## Cash Copilot

| Screen | Setup action | What to verify |
| --- | --- | --- |
| Settings `/settings` | Fallback starting cash, cash floor, deposit/commission/labor rates, payroll, salaries | Units, date, approved rates and payroll cadence; successful save and reload |
| Settings monthly goals | Choose year/window and **Pull from Matrix**, or explicitly enter approved goals | Imported month count, overwritten values, sales and production timing, weekly overrides |
| AP CSV `/ap-upload` | Preview/map current open AP CSV | Vendor, Amount, Due date; Document number recommended; row counts and remaining balance total |
| Recurring `/recurring` | Where deployed: Payment schedules, Create schedule, Payroll schedule, and Convert legacy rules; legacy rules remain separate | Native/legacy ownership, periods, cents versus USD, calendar coverage, reviewed preview, saved forecast and absence of duplicate cash |
| Recurring CSV `/recurring-upload` | Preview/map recurring outflow CSV | Vendor, Amount, Frequency, Next due date required; optional Category, Payment method, Active, Memo |
| Debt Service `/debt-service` | Add itemized lender payments | Debt name, lender, monthly payment, next date, active state; no duplicate forecast entry |
| Dashboard `/dashboard` | Review current and future weeks | Beginning cash, inflows, outflows, payroll dates, ending cash and cash-floor warnings |

### Settings and goals are not interchangeable numbers

- Fallback starting cash seeds a timeline only when no saved weekly balance takes precedence. Saved weekly beginning cash can anchor later weeks. For an existing workspace, inspect the current week's source before deciding whether to change Settings or an approved dated beginning-cash override. Do not paste today's balance into Monday without reconciling intervening transactions.
- Monthly sales and production goals are full-ticket dollar values. Weekly cash-in uses the deposit/remaining-collection logic. Internal field names containing `Units` do not make the visible production goal a fence-footage field. Confirm the UI labels and values; do not enter cents in dollar fields or decimals in percentage fields.
- CashOS goal import uses Matrix revenue strategy totals when configured, then saved projection targets as fallback. It derives sales goals from the following Matrix production month. For example, January sales use February's production target. December sales stay at their existing value because the saved year's Matrix targets do not include next January; the import reports that caveat. Existing weekly overrides are preserved and can still control the displayed cash forecast. Do not shift a second time or invent next January. Verify an ordinary month, December, and the selected year/window; ask if the product's lead-time assumption fits the business.
- **Pull from Matrix** is a write. Review the chosen year/window, existing goals and weekly overrides before using it. Confirm imported months and any warning about months outside the window. Do not overwrite the owner's deliberate manual goals without approval.
- Legacy Settings payroll uses two paydays per month. The newer native Payment schedules implementation adds weekly, every-other-week, twice-monthly and monthly payroll, including last-weekday selectors and separate work-period mapping. Check deployment and visible controls before treating weekly payroll as unsupported. Existing Settings estimates remain active until reviewed conversion transfers their exact labor/salary cohorts. Do not merely add a native schedule on top of them.
- Check whether labor estimates and salaried employees cover different people. Inspect taxes/benefits and any recurring payroll entries for overlap. Debt service weekly (unallocated) is added to itemized debt, so confirm zero when all debts are already itemized.

For exact native payroll controls, amount bases, month/year semantics, one-time payments and reviewed source replacement, read [Native payroll schedules and legacy conversion](payroll-calendars.md). Native fixed one-time payments do not implement Matrix performance-bonus eligibility formulas.

### AP and recurring imports

First confirm the actual unpaid-bill system of record. An empty connected accounting-app screen is not proof of no unpaid obligations when the owner manages bills elsewhere.

AP accepts CSV, not raw P&L workbooks. Use a current open-payables detail report, preserving the raw export. Prefer the remaining open balance over an original invoice total when they differ. Remove report headers/totals only in a checked import copy. Preview and reconcile counts and amounts before committing.

**Import AP rows** appends and skips recognized duplicates. It is not a guarantee that a changed bill will update or that every existing bill matches. Resolve changed amounts/dates against existing records, and never assume another upload is harmless.

**Replace open AP bills** removes the current open set and replaces it with the file. Use only for an owner-approved complete snapshot, after explaining any loss of current edits and establishing recovery. No AP export/restore workflow was verified during skill authoring: do not invent an Undo button or call screenshots a restorable backup. Inspect supported controls, preserve the relevant source/saved changes, and if recovery cannot be established, leave replacement blocked and prepare a targeted update plan. If removal is irreversible through normal product controls, obtain action-time confirmation required by the browser tool. Never choose replacement for an incomplete or uncertain report.

Read imported/duplicate/invalid counts. Investigate rejected rows and unmatched totals before calling AP current. After a timeout or ambiguous result, inspect the changed records before retrying.

Legacy recurring rules and their CSV path support weekly, biweekly, monthly, and quarterly schedules. The newer native editor has richer calendars and reviewed conversion; do not assume the legacy CSV can encode native payroll, holiday calendars, exceptions or payment history. The inspected CSV mapping has no inflow/outflow type field. Use the visible Create rule type control for inflows; do not assume CSV supports them. Bank and Credit card have distinct forecast groupings, so verify whether a source amount is a card charge or the later card payment before creating it.

### Forecast caveats and final readback

- Some legacy Recurring and Debt reads can normalize due dates and persist changes. Opening a view is not necessarily read-only. For a no-change review or smoke check, first use a supported, authorized read-only preflight to establish that no rows would change, or use an authorized isolated environment. If that preflight is unavailable, route the affected check to support and continue independent preparation. Do not probe customer pages as a no-write test or change due dates without the required exact authorization.

- The inspected AP calculation includes open AP plus a gap up to a 35% material target based on full-ticket sales. This can make AP forecast exceed imported bills. Explain the difference; do not enter that gap again as a manual expense or silently treat it as the business's measured material ratio. Verify the live behavior because this rule can change.
- Forecast overrides replace a calculated value for a week; manual lines add to it. Use neither just to force a green chart. Preserve existing deliberate overrides unless the approved setup changes them.
- Pay this week is a planning selection. Mark paid/received changes recorded state and can advance schedules. Neither is a necessary setup action. Do not claim a provider payment or collection occurred from a planning checkbox.
- Recalculate a representative week independently: beginning cash plus inflows minus outflows equals ending cash. Verify all configured obligations are counted once and the next week's beginning cash follows correctly unless an approved override applies.
- Inspect an ordinary week, a payroll/debt-heavy week, a month transition, and a goal year boundary. Compare Base with Conservative if visible, explaining that these are scenarios. List missing data that prevents reliance on the forecast.
- Give the owner the weekly routine: refresh open AP, review recurring/debt/payroll and expected collections, reconcile beginning cash, and inspect forecast warnings. Monthly, update Matrix actuals and compare with budget. Actual payments/receipts require their normal separate workflow.

## Optional FenceOS and Operator connections

Only when requested, use Settings > Command Center Connections if available. FenceOS is the sales/pipeline source; Operator is the operations/completed-work source. Confirm the exact source organization and URL for each. Have the user enter keys privately in the product UI, review sensitive access at action time, and inspect the product's test/readback result. Never copy keys into chat, the skill, URLs, screenshots, or browser scripts. Account provisioning, org mapping, and missing server-side feature flags are admin work, not customer browser onboarding. Report them as blockers for that connection while preserving the completed manual budget.

## Capability limits and financial discrepancies

Native payroll capability must come from the current public index and the selected business's enabled controls. Older availability observations do not establish current access. The conditional payroll reference explains how to use it only after verification; do not promise conversion or attempt deployment or activation during setup. Ordinary native activation is broader than calendar access and can enable settlements/reversals, reconciliation, imports, bulk edits and named backups. Conversion and recovery remain separate capabilities and require their own applicable authorization. Account activation is admin work, never implied by a budgeting request.

Earlier pilot reports described missing annual bonus/separate-budget paths. The newer public Matrix guide and later narrow user test report expose those controls. Neither proves bonus formulas, a complete separate-year workflow, full financial reconciliation, restore or cross-browser sync. Preserve reported observations with their date and tested scope rather than carrying an old blocker forward as a universal feature fact.

For differing displayed totals or margins, trace the definition and input dependencies. Preserve source/export and displayed totals separately, record variance and possible scope differences, and block affected reliance or goal/cost transfer until explained. Do not alter correct source values to force agreement. Independently reconciled, unaffected sections may proceed. Compare proposed and saved amounts, dates, counts and totals in the action receipt.
