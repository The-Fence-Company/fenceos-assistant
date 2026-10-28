# Getting started mode

Read this file when the user is new, asks what the assistant can do or where to begin, or the request is unclear. The front page ([SKILL.md](SKILL.md)) has already signed the user in, confirmed the company, and recorded the session notes. This mode changes nothing. It looks at the account, reports what is there, suggests the next step, and moves straight into [catalog setup](catalog-setup.md) when the user picks one.

## 1. Look around, read-only

Open each of these and note what you see. Read them in a tab of your own, not the one the user signed in on, so neither of you moves the other's page. Do not click Save, Publish, Import, Sync, Enable, Retry, Replay, or Send anywhere in this mode.

| Where | What to note |
|---|---|
| **Launch Pad** | The **Estimates & sales** numbers (quotes sent, acceptance rate, dollars won this month, and the monthly goal), **Today in Operator** (jobs today, crews out, unscheduled), and **Recent quote activity**. |
| **Organization → Products** | The counts on the **Fence Types**, **Gates**, **Add-ons**, **Groups**, and **Finishes** tabs. A **Custom** badge means the organization owns the product; a **Template** badge means it comes from the platform library. Note fence types with no cost (their margin shows 100%), archived items, and names that look like duplicates. Is the **BOM Setup** button present? |
| **BOM Setup** | Only when the company has Operator and the button is present: how many fence types are linked to a BOM, and whether any recipe cells say **needs materials**. For a full picture, run the [coverage check](references/coverage-check.md). |
| **Locations** | How many locations, how many products each has enabled ("19 enabled"), its online-estimate link, and its notification emails. Note name typos, and locations that look like tests or demos but have a live estimate link. |
| **Quotes** | The total in "Showing N of N quotes." A customer row can show an accepted quote with other options "still pending." Those are usually alternatives to the accepted one, not open quotes to chase. |
| **Org Settings** | **Configuration progress** and **Setup checklist (N need attention)**. Only some sections earn a **Configured** badge; Wood fence stain, Fence removal, Quote validity, Customer reminders, Financing, and Commission guardrails never show one, so open those sections and read the fields. Read only. |
| **Sidebar** | Which sections are visible (Core, Organization, Platform) and the role shown under the account name at the bottom. If Products or Locations are missing, the user is a standard User, not an Org Admin, and setup work needs an admin. |

If a page will not open or a control is missing, note it and move on.

## 2. Report what you found

Keep it short. Put anything the user said did not work at the top. Then a table: area, what is there now, suggested next step. Then one line on how long the suggested path should take.

**What the assistant can do in this version**

- **Set up the catalog.** Fence types, gates, add-ons, prices, descriptions, and photos; supplier material costs from a price sheet or from supplier invoices in their email; BOM recipes; the fence type mapping; location availability. One fence family at a time, with the user approving each batch before it is saved. It checks base costs and the margin at every height against the BOM, finds what the BOM does not cover, and can prove the work with a test quote.
- **Tidy settings and turn on the online estimator** by following the screens, with the user approving each change.
- **Answer questions about any screen** using the **Learning Center** and the question-mark help on each page.

**What it does not do in this version**

- Communicator (HighLevel) setup, importing customers, and the daily sales review of leads, messages, and calls. Say these are coming later.
- Importing past jobs. In FenceOS a job is an accepted quote; there is no bulk import on screen.
- Changing roles or permissions, accepting quotes, taking payments, or working around a missing permission.
- Signing in for the user or storing a password.

## 3. Suggest an order

For a company starting from an empty or template-only catalog:

1. **Locations.** Confirm each physical location exists, because products and the online estimator attach to a location.
2. **Products.** On the fast track, every fence type, gate, and add-on with a price, cost, description, and photo, so they can quote today. On the full build, start with step 3.
3. **One fence family's material list**, if they have Operator. Pick the family they sell most, then check it with a test quote before the next family.
4. **Remaining families**, one at a time.
5. **Online estimator.** Needs the catalog, a location, and a notification email for phone-only estimates.

For a company that already has a catalog, start at whichever step the look-around showed is incomplete. Recommend one step and ask whether to start there.

## 4. Move into the work

When the user says yes to a step, or names something to do, open [catalog setup](catalog-setup.md) and continue in the same conversation. Carry over what this mode found so the user is not asked again. Do not tell the user to start anything else.

If the user is not sure what to ask, offer two or three of these:

- "Set up all our fence types and gates so we can start quoting."
- "Set up our 6 foot cedar privacy fence from this supplier price sheet."
- "Find our current material prices in our supplier invoices."
- "How does our material list compare with what we sell?"
- "Walk me through turning on the online estimator for our Ogden location."
