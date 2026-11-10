# Verification

Verification is done on screen, in the same signed-in FenceOS browser tab the work was done in. Nothing outside the browser is needed.

## Before each batch and again before each save, publish, or import

- The company, signed-in user and effective role still match [company context and navigation](navigation.md).
- The required setup page is accessible by that role's route; a Super Admin does not need a Products **BOM Setup** button. Failed loads are unavailable evidence.
- Only one BOM Builder draft is open, and it is the one this run created.

If any of these has changed, stop and tell the user before continuing.

## After each save

Reopen the saved record on screen and compare every field with the approved batch. A change is **entered** when typed, **saved** only once the reopen shows it, and **verified** when it matches the batch. Say "saved" only after the reopen.

- **Material cost import:** open **Recent imports** and the affected materials; compare cost, unit, and package conversion.
- **BOM products, systems, styles, recipes:** after publish, reopen the system, style, and each recipe cell in Guided Builder; confirm no cell still says **needs materials**; note the row counts and the "mappings preserved or dropped" line from the publish confirmation.
- **Fence type and gate products:** reopen the product form; compare heights, base cost, price or margin, gate mappings, and the Fence System and BOM Style link. Confirm the saved base cost matches the decision recorded in the base cost check table, and that every flagged row carries a decision.
- **Location availability:** reopen each location; confirm the products are enabled only where approved.

Static recipe presence does not prove quantities. Run the guided review's labeled sample drawing and compare its post, rail, picket, and concrete counts with the quantities the customer said to expect. A difference is a blocker. Do not create a quote or job just to produce evidence, with one exception: after a large publish or a pricing change, the owner may approve a labeled test quote on a test customer, saved and never sent, to prove prices and the saved material list. Follow [test quote](test-quote.md). Never create a job.

If a saved value differs from the batch, or FenceOS reports that another editor changed the catalog, report it and prepare a new batch for the user. Do not retry on your own.

## Publishing and revisions

One statement, so the other pages do not disagree. Where another page in this skill says otherwise, this one wins.

- The guided publish previews the catalog and the mapping set together under one captured catalog revision. If the stored catalog or the reviewed payload changes after the preview, FenceOS refuses the publish, stores neither half, keeps the local draft, and asks for **Re-run Preview**. Nothing is replaced in that case.
- **Re-run Preview** builds a new preview from the local draft, and the draft is a full copy of the catalog as it stood when the page loaded. Confirming after a re-run replaces the stored catalog with that draft, so another editor's changes since the load would be lost. That is why a re-run request is a stop: reload, rebuild the approved batch on the newer revision, preview again, then publish.
- Mappings: the guided publish stores catalog and mappings in one transaction and its confirmation reports how many mappings were preserved or dropped. Advanced Editor's **Review & Publish** stores the catalog only and preserves saved product BOM links only while the referenced system and style IDs still exist; a renamed or removed ID drops the link. Read the preserved-or-dropped line after every publish and remap anything dropped before the receipt.
- Publication changes nothing already saved. Historical quote snapshots and saved job material lists keep their numbers; a failed historical job is not repaired by a publish.
- Evidence stays in four separate statuses: **published**, **coverage checked**, **guided quantities verified**, and **saved test-quote BOM verified**. A publication count never passes any of the other three.

## Receipt

Return the receipt in section 6 of [catalog setup](../catalog-setup.md). It lists what was requested, what was saved and reopened, what was held or conflicted, the sample output result, the publication counts, the recovery references captured before each write, and anything not reopened and compared. No passwords, raw supplier files, or unrelated records.

Report four outcomes separately: **published**, **coverage checked**, **guided quantities verified**, and **saved test-quote BOM verified**. Each needs its own evidence; publication counts cannot stand in for the other three. Without owner-supplied expectations, the sample only ran and its quantities remain unverified. A declined, blocked, or unrun optional test stays unverified. Only `ready` is order-ready; `mixed` and `failed` require review, even with partial rows. A ready status still needs the expected-versus-actual comparison to pass the test.

If an existing historical job still fails or shows a generic 409, follow the [BOM failure handoff](bom-failure-handoff.md). Fresh test success does not establish historical-job recovery.

## Practice run

Before the first real run at a company, the customer may choose to rehearse on an already authorized disposable test organization or an isolated test family. Cleanup is a separate exact approved batch using supported record controls; leave records and report them if safe cleanup is unavailable. Never use organization BOM reset/backfill for practice cleanup. A practice run exercises package-unit conversion, an ambiguous material match, a known zero versus an unknown cost, and a wrong-company stop. Never rehearse against live customer records, accepted quotes, sold jobs, payments, or messages.
