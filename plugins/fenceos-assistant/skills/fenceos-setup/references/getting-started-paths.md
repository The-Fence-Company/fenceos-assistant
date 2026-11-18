# Getting started: pick a path

Scope: account work. In paper work (SKILL.md, "Two kinds of work") use only the facts and screen names here; no step that opens, saves or reads back a screen applies.

Hand-written. The front page ([SKILL.md](../SKILL.md)) asks the package and path questions once and keeps the answers in the session notes. Use this page for what each answer means and how to run each path; ask again only if the notes do not have the answer.

## The setup path, step by step

The front page lists the nine steps and keeps the rules for done, provisional and blocked. This is what each step covers and which reference runs it.

**Sales-ready (every company)**

1. **Company basics.** **Org Settings → Essentials**: Company information (name, logo), Brand colors. **Locations**: each physical location exists with its address. Reference: company settings (`references/company-settings.md`).
2. **Products and pricing.** Every fence type, gate, and add-on they sell, with price, cost, description, and photo; finishes and groups; location availability. On the fast track prices are owner estimates, marked provisional. On the full build no price is entered until that family's material list and base cost check (step 7) are done. Online gate links are step 6; they never hold up step 3. Reference: catalog setup (`catalog-setup.md`) Phases D and F, and the fast track and full build on this page.
3. **Quote Experience.** **Org Settings → Quote Experience** and **Pricing & Guardrails**: deposit settings or payment schedule, quote validity, customer reminders, scope, payment terms and warranty text, Terms of Sale, company documents, customer reviews and Google rating, email settings, tax rates, financing, stain and removal defaults, warranty settings, commission guardrails. Reference: company settings (`references/company-settings.md`).
4. **Payments.** The payment processor sits under **Org Settings → Platform setup**, which only a Super Admin sees. Read whether it shows as configured and report it. Connecting it, and the merchant account behind it, is the company administrator's and FenceOS's job (SKILL.md, section 6). A company is not ready to sell from Estimator until this is done, so it stays on the board as blocked, with the owner, until it is.
5. **Sales test.** One labeled test quote on a test customer, with the owner's yes: price, documents, deposit schedule, and the customer quote page, read back and archived. Reference: test quote (`references/test-quote.md`). Do this after step 3 even when step 4 is still blocked; the deposit payment itself is not tested until the processor is live.
6. **Online estimator.** Each location that takes online estimates has its estimate link, a notification email, the right products enabled, and the **Single gate product** and **Double gate product** links on every online fence type; an unlinked gate shows **Price confirmed onsite** and adds $0. Use the gate products whose default width is the common one, normally the 4 ft single and the 8 ft double, unless the owner says otherwise.

**Operator-ready (Estimator and Operator)**

7. **First family's material list.** Pick the family they sell most. Supplier costs, BOM products, recipes, mapping, the base cost check, the margin at every height, guided quantities against expected counts, and a saved test quote whose material list is read back. Reference: catalog setup (`catalog-setup.md`) Phases A to G.
8. **Remaining families**, one at a time, the same way.
9. **Coverage check and final receipt.** Everything Products sells has a recipe, and the receipt separates published, coverage checked, quantities verified, and test-quote BOM verified.

## Before you begin: checklist to share

FenceOS open and signed in by them; one recent quote they sent a customer; photos of their own installs, logo and brand colors; warranty terms in their own words; which products sell most. Their email only if they want supplier prices found in invoices.

## First question: which package do they have?

Ask: "Do you use Estimator only, or Estimator and Operator?"

- **Estimator only:** they quote with basic pricing and do not get build-of-material lists. Run the product setup only: fence types, gates, add-ons, finishes, descriptions, photos, price and cost (with "Help me price it" if needed). Skip the BOM pass, supplier cost imports and BOM mappings. Do not call prices provisional for lack of a BOM; they are final once the owner approves them. Cost still matters for margin and commission, so get a real number.
- **Estimator and Operator:** they get material lists. Offer the two paths below.

If unsure, follow company context and navigation (`references/navigation.md`) for the effective role, then confirm with the user. A missing button or failed load alone does not establish access or feature availability.

Ask the user which way they want to start; do not choose for them. Explain both in plain words, then let them pick.

> "We can start two ways. **Fast track:** you tell me what you sell and roughly what you charge and what it costs you, and I set up all your products today so you can quote right away. We add the material lists later. **Full build:** we work out exactly what goes into each fence first, then price from that. It takes longer but every number has a source. Which fits you better?"

Most new companies should take the fast track. Recommend the full build when they already know their materials well or say their prices are guesses.

## Fast track: products first, BOMs later

Goal: every fence type and gate they sell exists, with a price, cost, description and photo, so they can quote the same day.

1. **List what they sell.** For each fence type: name, material, style, color, heights, section length. For gates: single and double, widths, which fence types they go with.
2. **Price and cost.** Their retail price per section and what one section costs them, materials plus labor. FenceOS needs both; with only one, get their usual margin and work out the other. Show the margin on every row.
3. **Descriptions and photos.** Two plain sentences per product from what they told you; they edit or approve. Never invent warranties, ratings or claims; leave the claim out and list it as open. One photo per product from their own installs; with none, note it as open. Do not use stock or other companies' photos.
4. **Gates.** For each gate product: single or double, the widths it covers (one product can list `3, 4, 5`), heights, which fence types use it, price and cost. Check every fence type has the gate sizes it sells.
5. **Add-ons.** For each: how it is charged (flat, per section, or per square foot), price, cost, sold labor hours per unit, and a description. The reserved **Old Fence Removal** and **Premium Protection** add-ons always need a price, and Premium Protection also a cost. Stain is not an add-on; it belongs under Finishes.
6. **Finishes, groups and order.** Stain or color options and their pricing per fence type, product groups, sort order, the popular flag, online estimator visibility and location availability.
7. **Batch, approve, save, read back.** One table for all products, gates and add-ons (section 5 of catalog setup (`catalog-setup.md`)), their yes, save, then reopen each and compare.
8. **Mark every price as provisional.** In the receipt, list each product as "priced by owner estimate, no BOM yet." This is the to-do list for the BOM pass.

## Help me price it (when they don't know)

Work from cost to price with the owner's own numbers: materials per section from a recent invoice, labor per section from sections per man-hour and hourly cost, then their margin. Gates: materials plus labor at the family margin; many owners start gate labor at 2 times the section hours. Say what this leaves out in FenceOS (end, corner and gate posts; taller heights share one price per section) and mark everything provisional until the BOM pass.

## Then: the BOM pass, one family at a time

Start with their highest-volume fence type.

1. Intake for that family: posts (size, wall, length per height, driven or concreted and how many bags), spacing, infill spec and count, rails and hardware, gates (kit or parts), labor in sections per man-hour, target margin.
2. Supplier prices with dates and sources; estimates labeled.
3. Build one height, run a sample job (for example 100 ft, two corners, one gate) and have them compare the material list with what the crew would load.
4. Copy to other heights, colors and gates.
5. Run the base cost check: their fast-track cost versus BOM materials plus labor. Show the gap and let them choose the new price and cost. Expect surprises in both directions.
6. Link the fence type to the recipes, then, with the owner's yes, save a labeled test quote and check its material list (test quote (`references/test-quote.md`)).
7. Check the margin at every height the fence type offers; one price per section covers them all.

## Full build: BOM first

Same BOM pass as above, then create each product with cost and price calculated from it, then descriptions and photos as in fast-track step 3.
