# Coverage check: does the BOM cover what you sell?

Hand-written. Owners ask this in plain words ("how's my BOM doing compared to my products?"). The answer is a gap list, product by product. Run it read-only at the start of any run on a company that already has products, after each publish, and whenever the owner asks.

## Why

The Products catalog and the BOM catalog are edited separately and nothing warns when they drift. A fence type can be sold at a height no recipe covers, a gate product can list a width with no gate recipe, and a disabled product can keep recipes nobody uses. A quote on an uncovered cell produces a **Mixed** or **Failed** material list in Operator, which the crew finds out about on order day.

## Steps

1. On **Organization → Products**, list every **enabled** fence type with its heights and variants (colors), and every enabled gate product with its type (single or double), widths, and heights. Note which gate products each fence type uses online.
2. In **BOM Setup → Advanced Editor → Fence Type Mappings**, record which fence types are linked, and to which system, style, and default variant.
3. For each linked fence type, open its style and check, for every height it sells and every variant it offers:
   - a section recipe;
   - line, end, corner, and gate post recipes (a shared, unscoped post recipe counts);
   - a gate recipe for every gate type, width, and height a matching gate product offers.
4. List what is in the BOM but no longer sold: styles no enabled fence type maps to, recipes for heights the product no longer offers. These are harmless to quotes but clutter the catalog. Ask the owner whether to keep them or delete them; some owners want only active products to keep build material.
5. Look for leftovers that confuse later work:
   - two Fence Systems for the same family (for example a custom one and an older starter one whose products have blank costs). Build on one; ask the owner which, and whether to retire the other;
   - a disabled product still mapped to a live style in **Fence Type Mappings**;
   - gate products that exist but do not show on **Products**, or show under a slightly different name. Report them; do not map to them.
6. Spot-check suspicious recipes: a 4 ft recipe with the same picket or post count as the 6 ft one, a section with a quantity far from its neighbors, or a recipe copied from another color still pointing at the old color's parts.

## Table

| Product | Linked to | Height | Variant | Section | Posts | Gates covered | Gap |
|---|---|---|---|---|---|---|---|

Under the table list:

- fence types with no BOM link at all;
- heights and variants offered with no recipe;
- gate widths and heights offered with no gate recipe (these show as **Mixed** in Operator);
- BOM content nothing sells, with the owner's keep or delete decision;
- recipes that look wrong, and why.

Rank gaps by how often the product sells. Fix nothing from this table without a batch and a yes; each fix is Phase C, D, or E work.

## Common fixes

- **Height sold, no recipe:** build it (Phase C), or remove that height from the product if it should be quoted another way (see "Heights and per-section pricing" in [field lessons](field-lessons.md)).
- **Gate width sold, no recipe:** build the recipe, or remove the width from the gate product. One gate product with many widths shares one price, so check the price still fits the widest width.
- **Fence type with no link:** link it (Phase E), or note that it quotes without a material list.
