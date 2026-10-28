# Test quote: prove it the way a rep would

Hand-written. The guided review's sample drawing checks recipes in isolation. It does not prove that a rep picking the product in Field Estimator gets the right price and the right material list. A saved test quote does. Use it only when the owner asks for it or says yes to it, after a publish or a pricing change.

## Rules

- **Owner's yes first.** Name the quotes you will save and the test customer you will use.
- **Test customer only.** One clearly labeled customer, such as `QA TEST <date>`, with **no phone number and no email** so nothing can be texted or emailed. Use the company's own shop address, never a real customer's.
- If saving would sync the customer to a CRM, send, or notify anyone, and there is no way to turn that off, stop and ask.
- Save only. Never send, present, share, accept, sign, take a deposit, mark sold, or schedule.
- When done, archive the test quotes. If only Delete is offered, leave them and give the owner the quote numbers.

## Pick the tests

One quote per family changed, at the heights that changed. Vary the drawing so every recipe gets used:

- a straight run (2 end posts, line posts);
- a run with a turn (adds a corner post);
- a single gate on one family and a double gate on another;
- at least one short height (4 ft) and one tall one.

Write the expected result before you draw: section count (feet / section width), fence price (sections x price per section), gate price, and the per-unit recipe for each section, post type, and gate.

## Read the saved material list

FenceOS builds a material list a few seconds after each save. Field Estimator does not show it, but the same signed-in tab can read it:

1. Find the quote's internal id. It is the `id` in the save response in the browser's network panel (not the quote number), or the `quoteId=` in the quote's link on **Admin → Field Quotes**.
2. Open `<the FenceOS address>/api/field/quotes/<id>/bom` in the same tab. It shows the saved material list as text and changes nothing.
3. Read `status` (`ready` is good; `mixed` or `failed` is a fail, with `failureCode` and `failureReason`), the counts in `summary` (sections, line, end, corner, and gate posts, gates), and every entry in `lineItems`.
4. If it says the snapshot was not found, wait 30 seconds and reload once.

For Operator customers, the same list appears in Operator once a quote becomes a job. Do not create a job to see it.

## Check the amounts

For each part:

> expected = sections x per-section qty + line posts x per-line-post qty + end posts x per-end qty + corner posts x per-corner qty + gate posts x per-gate-post qty + gates x per-gate qty

Use the counts from `summary`. A quantity slightly above the math is fine when it rounds up to a whole roll, box, or bag. A missing part, an extra part, the wrong color or length, or a gap bigger than rounding is a fail. Also check the counts make sense for what was drawn.

## Report

Per quote: what was drawn, the price lines and total as shown, the material list status and counts, and a table of part, quantity FenceOS made, quantity expected, pass or fail. Keep the raw material list text so someone else can redo the math. End with what was archived.

## Handing this to a second agent

A second agent (for example Codex in its own browser) can run the tests while you check the results. Give it: the rules above, the exact drawings, the expected price and per-unit recipe for each, where to read the material list, and a results file to write with the raw material lists pasted in. Then redo the math yourself from the raw data; do not take its pass or fail on trust.
