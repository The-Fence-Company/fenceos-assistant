# Review packet and action receipt

For each meaningful financial batch/import/conversion, maintain one private receipt before and after execution:

| Field | Record |
| --- | --- |
| Identity | Local batch label, business/host, selected plan and dates |
| Input | Source file/version and hash when available, exact fields/rows and exclusions |
| Before | Relevant existing values, source ownership, record IDs when exposed, backup/recovery |
| Approval | User authorization basis/date or message reference, exact data/destination/write set, unresolved sections and any tool-required action-time approval |
| Expected | Counts, amounts, dates and totals, including intentional differences |
| Outcome | Not started / Entered / Persisted / Reconciled / Partial / Uncertain / Blocked; reload time and readback IDs/counts/totals and discrepancies. Applied means persisted and read back, never merely entered |
| Dependencies | Which downstream goals, costs or forecasts require this result |
| Resume | Next safe action and what must be revalidated |

A local label or hash is an audit aid, not server idempotency. Do not invent hidden API IDs. After uncertain saves inspect records/history before retrying. If partial success cannot be distinguished from failure, stop that write and seek a supported reconciliation route. Do not resubmit an entire file because its toast was lost.

Compare affected live state with the approved before-state immediately before resumed writes. Human edits or new sources require revising the affected proposal, not resetting everything or reusing stale approval. Reconcile expected versus saved amounts/dates/counts, then assess readiness separately. Only independently reconciled downstream fields may proceed around a discrepancy.

Exports should identify the business/plan, export date, schema/build when available and file integrity. A successful export does not prove restore or sync. Restore rehearsals require a safe authorized target; never overwrite a customer budget merely to test recovery.
