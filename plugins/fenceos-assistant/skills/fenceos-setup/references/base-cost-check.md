# Base cost check

Hand-written reference. FenceOS does not perform this comparison today, so it is done from the screens.

## Why

A fence type's **Base Cost per Section** is a typed number. Quote line cost is sections times that number, the Estimator margin is built on it, and commission math uses it. The BOM is a separate recipe that produces a material list and a material cost in Operator after the sale. Nothing flows from the BOM back to the fence type, and nothing warns when the two drift apart. A company can keep an accurate BOM and still quote off a cost typed a year ago. Gate products and gate recipes have the same gap.

## When

In Phase D, before the fence type or gate form is saved, for every product in the run. Also when the user asks to review pricing or margins on existing products, and after a material cost import that changed costs under existing recipes. When BOM Setup is not available to the signed-in user, say the check cannot be done and move on.

## What a typical section is

One section recipe plus one line post recipe, at the fence type's default variant, for each height the fence type offers. A straight run uses one line post per section, so this is the lowest material cost a section can have. Corner, end, and gate posts, package round-up, waste, delivery, and labor all sit on top of it.

## Steps

1. On the fence type form read **Base Cost per Section**, **Price per Section**, and the **Margin (%)** FenceOS shows. In an organization catalog the form shows the effective value, override included.
2. Find the system, style, and variant to check against. For a product that already exists, read its saved **Fence System**, **BOM Style**, and default variant from the product. For a product this run is creating, there is no saved link yet, because Phase E saves it after the product; use the Fence System, BOM Style, and default variant approved for that product in Phase C. An existing product with no link and no Phase C approval cannot be checked; report that instead. In Phase E, after the link is saved, confirm it is the same system, style, and variant the check used, and rerun the check if it differs.
3. In **BOM Setup → Guided Builder** open **Edit an existing recipe** for that style. For each height the fence type offers, at the default variant, list every line of the section recipe: product, quantity per section, and the recipe's unit. Then list every line of the **line post** recipe the same way. Recipes show quantities only.
   Guided Builder shows **1** for a line whose quantity is a formula, with nothing to say so. Lines this run built in Guided Builder are plain numbers. For every line that existed before this run, confirm the quantity in **BOM Setup → Advanced Editor → Recipe Lines**: choose **Edit recipe line** and read **Quantity Formula**. A plain constant is the quantity. Anything else is a formula the takeoff evaluates per job; hold that line, mark the product's comparison **unavailable** in the table, and say which line, unless the user states the per-section quantity in writing. Never use the displayed 1.
4. In **BOM Setup → Advanced Editor → BOM Products** read each listed product's **Unit Cost ($)** and its unit. A blank cost is unknown, not zero; hold that row and name the product. If the recipe unit and the price unit differ, hold the row and ask. Do not convert on your own.
5. Multiply each line's quantity by its unit cost, ignoring **Round up to package**, and add the section lines and the line post lines. That sum is the BOM materials per typical section.
6. Compare:
   - Implied labor allowance = Base Cost minus BOM materials.
   - Margin on materials alone = (Price minus BOM materials) divided by Price. This is a ceiling; the real margin is lower once labor is in.
   - **Flag** the product when Base Cost is below BOM materials. Its labor allowance is negative and the margin FenceOS shows cannot be right.
   - If the user gave a labor per section figure in section 2 of [catalog setup](../catalog-setup.md), also flag when Base Cost is below BOM materials plus that labor.
7. Gates: do the same with the gate recipe for each type, width, and height the gate product offers, plus the **gate post** recipe multiplied by the number of posts the user says one opening adds. Ask; do not assume. Compare with the gate product's cost field.
8. Present the table below inside the Phase D batch. For each flagged row the user chooses one: raise Base Cost together with the price or margin that goes with it, fix the recipe or the product cost, or accept as is with a note. Record the choice in the receipt. Only a chosen Base Cost change goes into the save, and only after the normal batch yes.

## Table

| Product | Height | Variant | Base Cost | BOM materials | Labor allowance | Margin shown | Margin on materials | Flag | Decision |
|---|---|---|---|---|---|---|---|---|---|

All money figures are dollars per section. Under the table list every product line whose cost was blank or whose unit did not match, every line held because its quantity is a formula, and every recipe cell that was missing. A product with a held line shows **unavailable** in the BOM materials column, not a partial sum.

## Limits to state in the receipt

- The figure is a hand estimate from recipe lines and product costs as shown that day. It is not what Operator will report for a real job.
- It excludes corner, end, and gate posts, package round-up, waste, delivery, stain, add-ons, and labor.
- A fence type has one Base Cost for all its heights. Report the check per height and flag on the costliest.
- Material prices move. Repeat the check after each material cost import that touches the family.

## Until FenceOS does this itself

The workaround is what the check produces: copy the BOM materials per section into the Base Cost by hand, add labor, and set price or margin from there. Rerun the check whenever material costs change.
