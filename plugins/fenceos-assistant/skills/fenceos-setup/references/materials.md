<!-- Generated from USER_GUIDE.md; do not edit.
Sections: material-cost-import, material-records
Revision: sha256:50b4916495d9d7c17659e70aa56196a367ae130d8a3f6d9d43cd386e5af9ba00
Regenerate with scripts/package-fenceos-setup-skill.py. -->

#### Import supplier material costs

Use **Import material costs** in BOM Builder to update product costs or create missing materials. Publish or reset any current catalog or mapping draft first. The same BOM access permissions apply.

1. Enter the supplier and drop CSV or XLSX spreadsheets into the form. You can use up to 3 files, 5 MB each, with 500 material rows total. Costs must be in USD. Each worksheet can have its own column layout.
2. Check the detected description, SKU, cost, unit, pack size and quantity columns. Choose whether the price is for one unit/package or the entire ordered line. Optional **Suggest columns with AI** uses column headings and cell types; spreadsheet row contents stay in FenceOS. Manual mapping works if AI is unavailable.
3. Review material matches. Compatible supplier/SKU and remembered matches can be selected for you. Similar descriptions require your choice. **Select all usable rows** includes new material drafts but leaves ambiguous matches unselected. Choose only one supplier price per material.
4. Open **Change material or pricing units** when needed. For an $80 box containing 20 brackets, choose **Each piece** and enter **20**. The review shows **$4.00 / ea**. A box price initially stays a price per box. Changing units requires checking the count; line-total prices also divide by ordered quantity.
5. Review new material names and component types, then review old and new costs and select **Save material costs**. New materials work even when the catalog has no products. If the supplier has no SKU, review shows the internal material code FenceOS will assign. Add materials to recipes separately when you know the required piece counts. Existing accepted quotes keep their recorded snapshots.

**Recent imports** shows saved imports and **Undo import**. Undo restores unchanged costs and removes unused new materials. It keeps later edits and materials now used in recipes or rules, and reports how many were kept. A fresh upload can be imported again after undo.

Formula prices or quantities must be replaced with verified values in the source spreadsheet and uploaded again. Missing package counts, conflicting specifications, duplicate selected prices and a catalog changed by another editor block saving. Source review expires after two hours; upload again if it expires. Matching recognizes common material abbreviations and specifications, but it does not understand every supplier description. Remembered matches include the reviewed pricing units, so a new upload may require confirming a package conversion again.

#### Edit material records

- In **BOM Setup → Advanced Editor → BOM Products**, enter **Unit Cost ($)** in dollars and cents, such as `4.78` for $4.78 per unit. You can type the decimal normally. Zero means a known $0 cost; clearing the field leaves the cost unset. Use **Review & Publish** to save the catalog changes.
- Adding a BOM product, style, or assembly places the unsaved draft at the top and opens it. New BOM products also inherit the active category and Fence System filters, so the draft cannot disappear behind the filters that were active when **Add BOM Product** was clicked.
- Fence System and fence-style relationships use searchable checkbox selectors. After one or more Fence Systems are selected for a BOM product, its style selector shows only compatible styles. Existing mismatched or missing relationships remain visible and removable with a review warning until an authorized catalog admin deliberately corrects them.
- Product links inside an assembly use a searchable selector. Type any part of a product name or ID to narrow the list; selecting a result closes the picker and updates that one product link.
- Deleting an assembly also removes its linked component rows from the unsaved draft, so the catalog does not retain product formulas that point to a missing assembly. Use **Reset to Stored Version** before saving if the deletion was accidental.
