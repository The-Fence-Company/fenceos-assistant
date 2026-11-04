# Native payroll schedules and legacy conversion

This packaged reference is a navigation aid. At every start, follow [Current deployed product knowledge](live-product-knowledge.md); current guide/build identity and enabled account controls determine which instructions apply. Never use a source feature as proof it is deployed.

Read this before configuring payroll or proposing recurring-rule workarounds. Prefer native payroll schedules when the current deployment exposes them. Keep a legacy fallback only for a confirmed missing capability, not because an older pilot needed many rules.

## Check availability before using this reference

These are conditional native-scheduler instructions, not proof the customer has the feature. Do not carry an older build's availability observation forward as a current feature fact. At each session refresh the public index, then inspect the selected business's enabled controls if the feature is present in that build. If absent, skip the native procedures and use the bounded fallback at the end. Customers do not need repository access or release diagnosis.

Ordinary native access, customer conversion and recovery are separate capabilities. Ordinary native-write activation can also enable payment history changes, reconciliation, imports and bulk edits; it is broader than calendar access. Budgeting never authorizes changing those permissions or deploying a feature. Keep a missing capability as an admin/support dependency rather than bypassing it to finish setup.

## Configure a native payroll schedule

For a genuinely new obligation, open **Recurring > Payment schedules > Create schedule** and enable **Payroll schedule**. If replacing existing payroll rules or legacy labor/salary estimates, start with **Convert legacy rules** instead; saving an ordinary new schedule does not retire the existing sources.

1. Confirm the business, covered workers/roles, gross or net treatment, requested calendar, first covered period, first payday and amount basis. Set the effective start and anchor payday from evidence. Changing payday does not establish the correct work period automatically.
2. Choose the payroll cadence and period fields below. Verify every auto-filled default against the owner decision table.
3. Choose the amount basis and source, plus weekend/holiday behavior. Match the units shown beside each field.
4. Use **Preview schedule**. Review the next scheduled payments, nominal versus scheduled dates, work periods, source month, and 13/52-week dates/counts/totals. Resolve incomplete calendar coverage and unexplained differences before **Save schedule**. A stale preview requires a fresh review, not repeated saves.
5. Reload and verify the saved schedule and representative dashboard weeks, including a five-payday month and December/January. Ordinary schedule creation is forecasting, not recording that payroll was paid.

| Requirement | Native controls and checks |
| --- | --- |
| Every Friday | **Payroll cadence: Weekly**, **Payday weekday: Friday**, a real **Anchor payday**, and **First period start/end** covering exactly seven contiguous days. One schedule can cover the series; do not create separate monthly payroll rules. |
| Every other Friday | **Every other week**, the actual first Friday anchor, and a fourteen-day first work period. Confirm which alternating Friday applies. Biweekly is not twice monthly. |
| Two fixed paydays per month | **Twice per month**, first/second monthly paydays, first/second period end selectors and **Period month lag**. Verify distinct ordered period ends and short-month behavior. |
| Last Friday each month | **Monthly > Monthly payday selector: Relative weekday > Payday ordinal: Last > Payday weekday: Friday**. Set the period end selector and month lag independently. Last Friday is not the last business day. No fixed-day or every-four-weeks workaround is needed when this control is present. |
| One fixed monthly payday | **Monthly > Day of month**, approved monthly payday and period end selector. Choose the invalid-payday policy explicitly. |
| A single known bonus/payment | A regular **Create schedule** with **Recurrence: One-time payment**, approved single payment date and fixed amount. Leave **Payroll schedule** off for this one-time calendar. This schedules a known cash amount; it does not calculate performance eligibility or implement Matrix performance-pay formulas. |

For monthly periods, **Period month lag: 1** pairs January paydays with December period ends. Period dates, nominal payday and adjusted cash date are separate facts. The displayed amount **Source month** follows the nominal payday month, which can differ from the work-period month. Confirm that this budget allocation matches the owner's intent.

## Amount basis and units

- **Fixed amount per run:** the same approved amount for each generated payday.
- **Allocate monthly labor and salary budget:** allocate the monthly budget over that month's nominal paydays, so four- and five-payday months need not have the same per-run amount. Choose **Labor**, **Salary**, or **Labor and salary** as the exact source cohort.
- **Allocate annual salary over actual paydays:** allocate over the actual nominal payday count; a year can have 53 weekly or 27 biweekly slots. Do not divide by a hardcoded 52 or 26.

Budgets can use **Manually entered budget** or **Organization salary, labor rate and production goals**. Organization-funded payroll requires reviewed conversion of the exact legacy cohorts it replaces. The backend blocks conflicting ownership. Do not substitute a manual amount to bypass that protection.

The inspected payroll editor labels manual amounts **(cents)**, including amount per run and monthly/annual budgets. The ordinary non-payroll editor labels fixed payments **(USD)**. Read the current label and verify the preview in dollars: a synthetic $1,000 is 100000 in a cents field, 1000.00 in a USD field. Never assume all fields use the same unit.

Allocation preserves cents, assigning remainders to the earliest nominal slots. Pauses and skips retain their original allocation; do not assume the missed amount is redistributed. Monthly-budget allocation needs a nominal payday in every source month, so month-end clamping is required where skipping an invalid date would leave no payday. Fixed and annual bases also support skip policies where valid.

## Calendar and payment semantics

The general scheduler supports daily, weekly, every-other-week, twice-monthly, monthly, quarterly, annual, relative weekday of month, custom week/month intervals, and one-time payments. Relative weekdays support first, second, third, fourth and last. Do not infer a fifth-weekday selector.

Schedules preserve an anchor and an effective start. End conditions are no end, an inclusive nominal end date, or a scheduled occurrence count. Count/end boundaries refer to scheduled slots, not a count of successful bank payments. Monthly/annual invalid dates use the selected clamp-to-month-end or skip policy. These native calendars replace annual date lists when the requested pattern is supported.

**Business-day adjustment** is none, previous business day, or next business day. **Weekends only** does not include public holidays. **Versioned holiday dates** requires an explicit supplied date list, version and coverage dates; there is no automatic holiday feed. Do not invent a jurisdiction's holidays or claim coverage beyond that calendar. Check adjustments crossing months and years. The dashboard's legacy Sunday-to-upcoming-Monday grouping still needs readback against the intended cash week.

Use **Payments and history** for separately authorized single-payment changes, partial actuals and reversals; dated pauses and future series revisions are distinct actions. Setup alone does not authorize marking paid, moving actual obligations, recording payments or editing financial history. Unknown legacy payment history stays unknown.

## Replace existing workarounds through reviewed conversion

1. Inventory exact legacy rule IDs, native schedules, labor/salary estimates, AP, debt, manual adjustments, overrides and any FenceOS-owned sources for the covered obligations. Record dated inputs and existing payment history. Identify each source being replaced before making changes.
2. On **Convert legacy rules**, select the actual legacy rules and, when applicable, the **Labor** and/or **Salary** cohorts. Select an effective cutover date, then **Configure replacement** with the native calendar and amount basis. Preparing a draft does not create an obligation.
3. Use **Review replacement** and inspect every before/after payment and **Weekly cash comparison**. Include the actual 13/52-week windows, December/January boundary, remaining finite payments and long-interval coverage. Record and obtain approval for each intentional difference. A 52-week preview is not automatically a full calendar-year comparison. Stop on incomplete, stale or ambiguous coverage.
4. With the exact conversion authorized, approve its displayed differences and use **Apply reviewed conversion**. Cutover retains source records/history, records dated ownership and creates a before-change backup transactionally. Do not also zero payroll settings, delete source rules, or manually disable retained sources as a second cutover. Conflicting FenceOS ownership must be resolved through its supported owner workflow, not bypassed.
5. Reload the new schedule, **Conversion history**, retained source ownership and dashboard weeks. Verify that the covered cash is counted once, including AP/debt/manual-linked payments and any dashboard overrides. Retained source rows are protected from direct mutation. Known actuals must remain known, and unpaid balances must remain visible.

**Consolidation suggestions** can prefill an evidenced conversion, for example complementary monthly dates or alternating biweekly phases. Suggestions alone do not merge, delete or activate anything; matching names/amounts alone are insufficient. Review the complete comparison before applying. Bulk edits have their own review and future effective boundaries; they are not a shortcut around source conversion.

**Conversion history > Review rollback** offers a forward-effective rollback with payment mapping and cash comparison. It preserves actuals and may require resolving ambiguous mappings. Use it only with specific approval; do not undo a conversion by deleting schedules or restoring an old application binary. Native schedule backups/restore are separate from Matrix budget exports. A successful native backup does not prove Matrix restoration or cross-browser synchronization.

Before converting a customer's large legacy setup, obtain a sanitized fixture of their actual sources and expected dates/amounts, rehearse the comparison in an authorized safe environment, and obtain approval of intentional differences. Generic synthetic tests or another customer's result do not establish that this customer's conversion is correct. Do not impose this migration rehearsal on a genuinely new setup with no legacy sources to replace.

## If native controls are unavailable

Preserve current data and explain the precise missing control/version. Ask support about availability and continue independent setup. Only propose a small, explicitly approved legacy workaround if the owner wants it and its amount/date/coverage can be verified. Prove one representative rule before expansion; avoid silently creating dozens of rules. Do not use twice-monthly settings to represent weekly payroll or a fixed monthly date to represent last Friday.

Carry forward the decision table's gross/net, employee-withholding, employer-tax, card and debt distinctions. Assign each cash component to one source. Gross payroll already includes employee withholding; adding withheld amounts on top of gross would double count them. Confirm bookkeeper treatment and remittance timing rather than inventing tax calculations.

Use native date controls if typed text fails to persist, within the cumulative retry budget. Record the first/last covered dates, calendar coverage, source replacements, temporary override expiration, maintenance owner and next review. Amounts outside verified coverage remain unverified.

Use the [Action receipt](action-receipt.md) for conversion. After a lost response, inspect Conversion history and ownership before retrying Apply.
