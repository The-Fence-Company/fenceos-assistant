# Existing BOM failure: read-only handoff

Hand-written. Read this only when the user reports an existing failed historical-job material list, a generic BOM 409, or an old snapshot that stayed failed after catalog publication. Ordinary setup does not require a historical-job audit.

## What the evidence means

Publishing changes the catalog and mappings; it does not rebuild saved historical snapshots. Assembly/component counts and preserved-mapping counts prove publication only. Takeoff uses the quote's organization and exact saved fence-type IDs for all relevant lines. A similarly named product, including a new organization-owned copy of an inherited product, may have a different ID.

A protected 409 can refuse regeneration and preserve prior output when current BOM setup is incomplete. If `bom_setup_required` is visible, record it as a setup refusal. A generic 409 alone does not establish that code or the root cause. Do not infer a `useGlobalCatalog` defect or prescribe removing the protection.

Only `ready` is order-ready. `mixed` and `failed` need review even when they contain material rows. Identical successful output can reuse a snapshot/hash, so a new timestamp is not required proof; compare identity, source, status and expected quantities when visible. Neither a publish nor a successful fresh test proves that an old job was repaired.

## Read only what the reported failure needs

Use visible details in the user's signed-in browser for the already confirmed company. Keep the existing company-change stop rule. Read existing detail views without editing; do not reproduce the error by clicking Rebuild, Generate, Regenerate, retry, or replay. If reaching a detail requires a write or a missing control, stop there and mark the evidence unavailable.

Capture the following only when exposed in the existing screens or visible internal links. Do not search other companies or unrelated records. Missing fields are **unavailable**, not guessed from labels, defaults, memory, or the currently selected company.

| Evidence | Minimum to retain |
|---|---|
| Tenant and record identity | Company name and organization ID when shown, including the quote's organization; exact internal quote ID and job ID, keeping display numbers separate |
| Saved lines | Each relevant saved line's ID, fence-type/product ID, height, variant and gate type/width/height when shown; include secondary line types, not just the primary product |
| Mapping identity | The selected product's exact ID, inherited or organization-owned copy when shown, and its system/style/default-variant mapping |
| Production source | Selected production source and revision ID/version when shown; do not select a different source to investigate |
| Catalog provenance | Published catalog revision/generation and publication time when shown; distinguish reported counts from counts actually read back |
| Snapshot provenance | Snapshot ID, quote version/source revision, source hash, status, and creation/update time when shown |
| Failure | Visible HTTP status, failure code and short safe message, failure time/timezone and request ID when shown; distinguish the old snapshot's failure from the latest refused attempt |

Keep this a compact field summary. Redact customer names/contact details, addresses, bearer links, credentials, session data and any private values embedded in a message. Do not copy raw customer/provider payloads, full network responses, screenshots containing unrelated records, or browser network archives. Do not use console scripts, scripted fetch, direct API/provider calls, database access, or a new endpoint to fill gaps. The approved fresh-test read in [test quote](test-quote.md) does not authorize probing historical-job APIs.

## Hand off and stop before mutation

Give the user a support/engineering handoff containing the observed symptom, the available fields above, unavailable fields, and the separately verified setup outcomes from the [catalog receipt](../catalog-setup.md#6-receipt-template). Label user-reported facts as reported and hypotheses as unconfirmed. Write the handoff yourself and offer to send it to FenceOS support; send it only on the owner's instruction. Do not hand the owner a list of instructions to relay.

Ask support/engineering to trace the exact same-organization quote lines and selected production source against the catalog revision, determine the structured refusal code, and review the protected snapshot state. Leave recovery to a separately authorized workflow. Do not auto rebuild, replay integrations, re-save accepted quotes, modify sold jobs or production sources, toggle global catalog settings, or touch payments/manual supplements. Keep all existing setup approval and test-customer rules. If normal catalog work continues within the approved setup scope, its receipt must still leave historical-job recovery unverified.
