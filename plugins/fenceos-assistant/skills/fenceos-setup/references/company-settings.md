# Company and quote settings

Hand-written. Steps 1, 3, 4, and 6 of the setup path live on **Org Settings** and **Locations**. This page says what is there, in what order to do it, and what you may and may not touch. The screens and the Learning Center win when they disagree with this page.

## The page

**Org Settings** is one long page with a **Settings Map** and a **Search settings** box. Selecting a group heading or a setting scrolls to it. **Save Settings** sits in the page header and beside the map; one save writes every edited section. The expandable **Setup checklist** shows which items FenceOS counts as complete; only some sections earn a **Configured** badge, so open the others and read the fields.

Org Admins see four groups. Super Admins also see **Platform setup**.

| Group | Settings |
|---|---|
| **Essentials** | Company information (name, logo), Brand colors, Product catalog, Locations, Setup checklist |
| **Quote Experience** | Quote Tax Rates, Deposit settings, Quote validity, Customer reminders, Google rating, Scope, payment terms & warranty, Financing settings, Email settings, Terms of Sale, Company documents, Customer reviews |
| **Pricing & Guardrails** | Wood fence stain, Fence removal, Warranty settings, Commission guardrails |
| **Integrations** | CompanyCam, Slack job channels when enabled |
| **Platform setup** (Super Admin) | Feature rollouts, Payment processor, Operator, HighLevel, API keys |

## Step 1. Company basics

1. **Company information:** legal or trading name as it should print on quotes, logo. Ask for the logo file; do not use another company's image or a stock mark.
2. **Brand colors:** the accent color. Ask for their brand color or read it from their logo and confirm.
3. **Locations:** each physical location exists with its address. Products and the online estimator attach to a location, so this comes before products.

## Step 3. Quote Experience

Work down the group in this order. Draft text from what the owner tells you and from their existing documents; never invent warranty terms, ratings, or claims. Present the whole group as one batch table, get one yes, save once, reload, and read every field back.

1. **Deposit settings.** Whether a deposit is required and either a percentage or minimum, or the structured payment schedule with its milestones. The preview shows the schedule a customer will see; read it back to the owner in plain words ("25% at acceptance, the balance on completion").
2. **Quote Tax Rates.** Named rates by jurisdiction when they charge sales tax. Ask; do not guess rates. Each rate saves on its own with **Add rate** or **Save changes** on its row; the page's **Save Settings** does not save tax rates. Save and read back each rate inside the same approved batch.
3. **Quote validity.** Days a newly sent quote stays open. Off by default; it applies only when a quote is first sent.
4. **Customer reminders.** Two separate switches, both off by default: quote and deposit reminders, and final invoice reminders. Explain the cadence from the field help before turning either on.
5. **Scope, payment terms & warranty.** Three optional customer-facing blocks shown on quote pages and PDFs until acceptance. **Draft from my Terms of Sale** can prefill them from the saved Terms of Sale; the owner reads every line before Save.
6. **Terms of Sale.** The contract text. Paste the owner's own terms; if they have none, say so and leave it for their attorney rather than drafting legal terms.
7. **Company documents.** Reusable PDFs and images reps can attach to quotes, such as a company guarantee. Upload only files the owner gives you; read each one back by its title in the list.
8. **Customer reviews and Google rating.** Up to two review quotes, and the Google listing import by Maps link or Place ID. The rating numbers are imported, never typed. **As Seen on HGTV** is Super Admin only.
9. **Email settings.** From name and address, and **Notify reps on first quote view**.
10. **Financing settings.** Only if they offer financing: the offer text, term, dealer fee, application link, and disclosure.
11. **Lifetime Warranty and Old Fence Removal labels**, if they want different customer-facing names.

Then **Pricing & Guardrails**: Wood fence stain price and cost per section, Fence removal price and cost per section, Warranty settings, Commission guardrails. These feed quotes directly, so they go in the pricing decision sheet in [catalog setup](../catalog-setup.md) with the products.

Mismatches between sections are common and easy to miss: a deposit percentage in Deposit settings that differs from the one written in Payment Terms, a review source on the quote page that differs from the saved reviews, a warranty length in the Warranty block that differs from the warranty document. Read the group as a customer would and list every disagreement for the owner before the batch.

## Step 4. Payments

The **Payment processor** is under **Platform setup**, visible to Super Admins only, and uses a payment provider with a merchant account behind it. Read what the Setup checklist and that section show and report it: not configured, configured, or configured with location payment accounts. **Configured** means credentials were saved, not that the provider or bank funding has been verified.

You do not connect it. Say who does: the company's administrator with FenceOS, through the provider's merchant onboarding. Never type, request, or relay merchant credentials, terminal numbers, or account numbers, and never add or change a payment account. Put the step on the board as blocked, with the owner, and continue with everything that does not depend on it. A company is not ready to sell from Estimator until this is live, so the board keeps saying so until it is.

## Step 6. Online estimator

On **Locations**, for each location that takes online estimates: the estimate link is present, a notification email is set so phone-only estimates reach someone, and the right products are enabled. On **Products**, every fence type shown online has its **Single gate product** and **Double gate product** set under Online estimator gate pricing; an unmapped gate shows the customer **Price confirmed onsite** and adds $0. Use the gate products whose default width is the common one, normally 4 ft single and 8 ft double, unless the owner wants otherwise. Open the location's estimate link in a new tab and walk through one estimate without submitting it; read back the prices it shows against the catalog.

## Rules on this page

- One batch per group, one yes, then save, reload, and read back every field. **Save Settings** writes all edited form sections at once, so a batch must list every field it will change, including ones in other groups that were touched. Some controls save through their own buttons and are not covered by Save Settings: Quote Tax Rates (**Add rate**, **Save changes**), Google rating (**Import from Google**, **Apply**, **Refresh**, **Remove**), Company documents (upload and remove), and the commission policy under Commission guardrails. Save each of those where it lives, inside the same approved batch, and read it back before moving on.
- Never change **Feature rollouts**, **Operator**, **HighLevel**, **API keys**, or anything under Platform setup. Read them and report.
- Never change roles or permissions on **Team**, and never work around a missing permission.
- Text you draft for the customer is a proposal until the owner reads it. Keep warranty, guarantee, and terms wording to what they gave you.
- Most of this page is read live by customer quote pages. Company name, logo and colors, financing text, Google rating, and customer reviews show on every quote page the moment you save, accepted quotes included. The scope, payment terms, and warranty blocks show on quotes still awaiting acceptance and are hidden once a quote is accepted. So an edit here changes quotes the company has already sent. Say that before the batch, and name the open quotes it will touch. Only a few things are frozen onto a quote when it is created or sent: add-on names and descriptions, copies of attached company documents, and the validity window applied at first send. When unsure which kind a field is, read its help text and say so rather than promising either way.
