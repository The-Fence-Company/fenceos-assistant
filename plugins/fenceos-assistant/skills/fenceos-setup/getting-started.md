# Getting started mode

Read this file when the user is new, asks what the assistant can do or where to begin, or the request is unclear. The front page ([SKILL.md](SKILL.md)) has already signed the user in, confirmed the company, and recorded the session notes. This mode changes nothing. It looks at the account, reports what is there, places the company on the setup path (section 3 of [SKILL.md](SKILL.md)), and starts the first incomplete step in the same conversation.

## 1. Look around, read-only

Open each of these and note what you see. Read them in a tab of your own, not the one the user signed in on, so neither of you moves the other's page. Do not click Save, Publish, Import, Sync, Enable, Retry, Replay, or Send anywhere in this mode.

| Where | What to note |
|---|---|
| **Launch Pad** | The **Estimates & sales** numbers (quotes sent, acceptance rate, dollars won this month, and the monthly goal), **Today in Operator** (jobs today, crews out, unscheduled), and **Recent quote activity**. |
| **Organization → Products** | The counts on the **Fence Types**, **Gates**, **Add-ons**, **Groups**, and **Finishes** tabs. A **Custom** badge means the organization owns the product; a **Template** badge means it comes from the platform library. Note fence types with no cost (their margin shows 100%), archived items, and names that look like duplicates. Use [role-specific navigation](references/navigation.md) to reach BOM Setup. |
| **BOM Setup** | Only when the company has Operator and the page opens (titled **Product BOM Setup**): the **Products linked** count against the fence type count, which fence types say **No BOM Link**, and, inside **Advanced BOM Catalog**, whether any recipe cells say **needs materials**. For a full picture, run the [coverage check](references/coverage-check.md). Never click **Reset organization BOM** or **Backfill Default BOM Catalog**. |
| **Locations** | How many locations, how many products each has enabled ("19 enabled"), its online-estimate link, and its notification emails. Note name typos, and locations that look like tests or demos but have a live estimate link. |
| **Quotes** | The total in "Showing N of N quotes." A customer row can show an accepted quote with other options "still pending." Those are usually alternatives to the accepted one, not open quotes to chase. |
| **Org Settings** | **Configuration progress** and **Setup checklist (N need attention)**. Only some sections earn a **Configured** badge; Wood fence stain, Fence removal, Quote validity, Customer reminders, Financing, and Commission guardrails never show one, so open those sections and read the fields. Read only. |
| **Sidebar** | Which sections are visible (Core, Organization, Platform) and the role shown under the account name at the bottom. Confirm the visible role; missing controls alone do not establish role or permissions. |

If a page will not open or a control is missing, note it and move on.

Follow [company context and navigation](references/navigation.md), including its one-reload limit and rate-limit handling, before reporting missing access or an empty catalog.

## 2. Report what you found

Keep it short. Put anything the user said did not work at the top. Then a table: area, what is there now, suggested next step. Then one line on how long the suggested path should take.

**What the assistant can do in this version**

- **Set up the catalog.** Fence types, gates, add-ons, prices, descriptions, and photos; supplier material costs from a price sheet or from supplier invoices in their email; BOM recipes; the fence type mapping; location availability. One fence family at a time, with the user approving each batch before it is saved. It checks base costs and the margin at every height against the BOM, finds what the BOM does not cover, and can prove the work with a test quote.
- **Set up the company and quote settings** on Org Settings: branding, locations, deposit schedule, terms, scope and warranty text, company documents, reviews and Google rating, email settings, tax rates, financing, stain and removal defaults. It reads the payment processor status and says who connects it. Reference: [company settings](references/company-settings.md).
- **Turn on the online estimator** per location, with the gate links checked, and walk through one estimate without submitting it.
- **Answer questions about any screen** using the **Learning Center** and the question-mark help on each page.

**What it does not do in this version**

- Communicator (HighLevel) setup, importing customers, and the daily sales review of leads, messages, and calls. Say these are coming later.
- Importing past jobs. In FenceOS a job is an accepted quote; there is no bulk import on screen.
- Changing roles or permissions, accepting quotes, taking payments, or working around a missing permission.
- Signing in for the user or storing a password.

## 3. Place them on the path

Use the setup path in section 3 of [SKILL.md](SKILL.md). From the look-around, mark each step done, provisional, blocked, or not started, show the setup board, and name the first incomplete step as next with a time estimate. Do not ask which step they would like. Say which one is next and why, and start it unless they object. A company starting from an empty or template-only catalog begins at step 1; a company that already has a catalog usually resumes at step 3, 5, or 7. On the full build, step 2's prices come after step 7's material list; say so on the board.

## 4. Move into the work

Start the next step at once: open [catalog setup](catalog-setup.md) or [company settings](references/company-settings.md) and continue in the same conversation. Carry over what this mode found so the user is not asked again. Do not tell the user to start anything else, and do not end the turn with an offer; end it with the step under way.

If the user is not sure what to ask, offer two or three of these:

- "Set up all our fence types and gates so we can start quoting."
- "Set up our 6 foot cedar privacy fence from this supplier price sheet."
- "Find our current material prices in our supplier invoices."
- "How does our material list compare with what we sell?"
- "Walk me through turning on the online estimator for our Ogden location."
