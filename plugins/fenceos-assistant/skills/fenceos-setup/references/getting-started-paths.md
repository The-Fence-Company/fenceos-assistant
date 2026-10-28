# Getting started: pick a path

Hand-written. The front page ([SKILL.md](../SKILL.md)) asks the package and path questions once and keeps the answers in the session notes. Use this page for what each answer means and how to run each path; ask again only if the notes do not have the answer.

## Before you begin: checklist to share

Tell the user up front what helps, so there is no back-and-forth later:

- FenceOS open and signed in (they sign in; never ask for a password or code).
- Their email, only if they want you to find supplier prices in invoices and quotes.
- One recent quote they sent a customer. It is the fastest way to see what they sell and charge.
- Photos of their own installs, their logo and brand colors.
- Warranty terms in their own words, so descriptions never invent any.
- Which products sell most, to set order and the popular flag.

## First question: which package do they have?

Ask: "Do you use Estimator only, or Estimator and Operator?"

- **Estimator only:** they quote with basic pricing and do not get build-of-material lists. Run the product setup only: fence types, gates, add-ons, finishes, descriptions, photos, price and cost (with "Help me price it" if needed). Skip the BOM pass, supplier cost imports and BOM mappings. Do not call prices provisional for lack of a BOM; they are final once the owner approves them. Cost still matters for margin and commission, so get a real number.
- **Estimator and Operator:** they get material lists. Offer the two paths below.

If unsure, check the screens (for example whether **BOM Setup** is offered on Products), but confirm with the user instead of assuming; a missing button can also mean the feature is not switched on.

Ask the user which way they want to start; do not choose for them. Explain both in plain words, then let them pick.

> "We can start two ways. **Fast track:** you tell me what you sell and roughly what you charge and what it costs you, and I set up all your products today so you can quote right away. We add the material lists later. **Full build:** we work out exactly what goes into each fence first, then price from that. It takes longer but every number has a source. Which fits you better?"

Most new companies should take the fast track. Recommend the full build when they already know their materials well or say their prices are guesses.

## Fast track: products first, BOMs later

Goal: every fence type and gate they sell exists, with a price, cost, description and photo, so they can quote the same day.

1. **List what they sell.** For each fence type: name, material, style, color, heights, section length. For gates: single and double, widths, which fence types they go with. Group them the way they talk about them.
2. **Price and cost.** Ask for their retail price per section (or per foot, and convert) and what one section costs them, materials plus labor. If they know only the price, ask for their usual margin and work the cost back; if they know only the cost, do the reverse. Show the margin on every row so they can sanity-check it.
3. **Descriptions.** Draft a short customer-facing description for each product from what they told you (material, look, benefit, warranty if they mention one). Keep it plain and specific, two sentences at most. Offer it; they edit or approve. Never invent warranties, ratings or claims.
4. **Photos.** Ask for one photo per fence type and gate, ideally of their own installs. Suggest what makes a good one: the full run in daylight, straight on, no clutter. If they have none yet, note it as open and move on; do not use stock or other companies' photos.
5. **Gates.** For each gate product: single or double, the widths it covers (one product can list `3, 4, 5`), heights, which fence types use it, price and cost, and a short description. Check every fence type has the gate sizes it actually sells, and map the exact single and double gate for each fence type shown online. Price as in "Help me price it" below.
6. **Add-ons.** Ask which extras they sell, and suggest the common ones for them to confirm: old fence removal, haul-away, permits, private line protection, warranty upgrades, rush scheduling. For each: how it is charged (flat, per section, or per square foot), price, cost, sold labor hours per unit, and a description. The reserved **Old Fence Removal** and **Premium Protection** add-ons always need a price, and Premium Protection also a cost. Stain is not an add-on; it belongs under Finishes.
7. **Finishes, groups and order.** Stain or color options and their pricing per fence type, product groups the way they talk about them, sort order, and the popular flag on best sellers.
8. **Everything else on the form.** Online estimator visibility and location availability. Propose sensible defaults and confirm.
9. **Batch, approve, save, read back.** One table for all products, gates and add-ons (section 5 of [catalog setup](../catalog-setup.md)), their yes, save, then reopen each and compare.
10. **Mark every price as provisional.** In the receipt, list each product as "priced by owner estimate, no BOM yet." This is the to-do list for the BOM pass.

## Help me price it (when they don't know)

Many owners know more about cost than they think. Work from cost to price:

1. **Materials per section.** What do they pay for the materials in a typical section? If they don't know, use a recent invoice or quote, or a rough supplier list.
2. **Labor per section.** How many sections does a crew finish in a day, how many people, and what does each cost per hour with taxes and comp? Labor per section = hourly cost / sections per man-hour.
3. **Margin, in plain words.** "Out of every $100 you charge, how much should be left after materials and labor to cover trucks, the office and profit?" Many installers aim for about 40 to 55 percent; let them pick. Price = cost / (1 - margin).
4. **Sanity check.** Show price per section and per foot, and ask if it matches what they have quoted before or what competitors charge. Adjust together.
5. **Gates.** Price from gate materials plus labor at their margin; a common labor starting point is 2 times the section hours. If materials are unknown, start from a rule of thumb they confirm, such as a multiple of the section price, and mark it provisional.
6. **Add-ons.** Price at what it costs them (crew time, dump fees, permit fees) plus their margin, or at their going rate.

Say plainly what the method leaves out (end, corner and gate posts; taller heights share one price per section) and mark everything provisional until the BOM pass.

## Then: the BOM pass, one family at a time

Start with their highest-volume fence type.

1. Intake for that family: posts (size, wall, length per height, driven or concreted and how many bags), spacing, infill spec and count, rails and hardware, gates (kit or parts), labor in sections per man-hour, target margin.
2. Supplier prices with dates and sources; estimates labeled.
3. Build one height, run a sample job (for example 100 ft, two corners, one gate) and have them compare the material list with what the crew would load.
4. Copy to other heights, colors and gates.
5. Run the base cost check: their fast-track cost versus BOM materials plus labor. Show the gap and let them choose the new price and cost. Expect surprises in both directions.
6. Link the fence type to the recipes, then, with the owner's yes, save a labeled test quote and check its material list ([test quote](test-quote.md)).
7. Check the margin at every height the fence type offers; one price per section covers them all.

## Full build: BOM first

Same BOM pass as above, then create each product with cost and price calculated from it, then descriptions and photos as in fast-track steps 3 to 5.

## Be helpful along the way

- Offer defaults they confirm instead of open questions ("Most installers drive chain-link posts. True for you?").
- Record every confirmed rule (post spec, labor rate, margin) so you never ask twice.
- After each family, say what is done, what is provisional, and what is next.
