# Verification

Verification is done on screen, in the same signed-in FenceOS browser tab the work was done in. Nothing outside the browser is needed.

## Before each batch and again before each save, publish, or import

- The company name shown in FenceOS is still the company being set up. A Super Admin is still in **Viewing as** for that organization.
- The signed-in user has not changed and the **BOM Setup** button is still present when the batch needs it.
- Only one BOM Builder draft is open, and it is the one this run created.

If any of these has changed, stop and tell the user before continuing.

## After each save

Reopen the saved record on screen and compare every field with the approved batch:

- **Material cost import:** open **Recent imports** and the affected materials; compare cost, unit, and package conversion.
- **BOM products, systems, styles, recipes:** after publish, reopen the system, style, and each recipe cell in Guided Builder; confirm no cell still says **needs materials**; note the row counts and the "mappings preserved or dropped" line from the publish confirmation.
- **Fence type and gate products:** reopen the product form; compare heights, base cost, price or margin, gate mappings, and the Fence System and BOM Style link. Confirm the saved base cost matches the decision recorded in the base cost check table, and that every flagged row carries a decision.
- **Location availability:** reopen each location; confirm the products are enabled only where approved.

Static recipe presence does not prove quantities. Run the guided review's labeled sample drawing and compare its post, rail, picket, and concrete counts with the quantities the customer said to expect. A difference is a blocker. Do not create a quote or job just to produce evidence, with one exception: after a large publish or a pricing change, the owner may approve a labeled test quote on a test customer, saved and never sent, to prove prices and the saved material list. Follow [test quote](test-quote.md). Never create a job.

If a saved value differs from the batch, or FenceOS reports that another editor changed the catalog, report it and prepare a new batch for the user. Do not retry on your own.

## Receipt

Return the receipt in section 6 of [catalog setup](../catalog-setup.md). It lists what was requested, what was saved and reopened, what was held or conflicted, the sample output result, the publication counts, the recovery references captured before each write, and anything not reopened and compared. No passwords, raw supplier files, or unrelated records.

## Practice run

Before the first real run at a company, the customer may choose to rehearse on a disposable test organization or a throwaway fence family that will be deleted or reset afterward. A practice run exercises package-unit conversion, an ambiguous material match, a known zero versus an unknown cost, and a wrong-company stop. Never rehearse against live customer records, accepted quotes, sold jobs, payments, or messages.
