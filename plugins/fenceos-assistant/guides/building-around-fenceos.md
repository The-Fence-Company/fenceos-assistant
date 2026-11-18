# Building around FenceOS

Version 1, 2026-11-17. The newest version is always at https://github.com/The-Fence-Company/fenceos-assistant/blob/main/plugins/fenceos-assistant/guides/building-around-fenceos.md

Give this file to your AI tool (Claude, ChatGPT, or any other) before you ask it to build something for your fence company. It tells the tool what FenceOS already does, so it does not rebuild it.

## The short version

Use FenceOS as intended first. Live in the house before you knock down walls. Then add things on top, in the tools below, instead of building your own app.

## What each tool is for

| Tool | What it is for | What does not belong there |
|---|---|---|
| **FenceOS Estimator** | Drawings, quotes, prices, deposits and payments, sales numbers. This is the record of every quote. | Chatting with customers. Team chatter. |
| **FenceOS Operator** | The schedule, crews, time clock, material lists, job progress. This is the record of every job in production. | Leads that have no accepted quote yet. |
| **Communicator (HighLevel)** | Your company phone number. Calls, texts, chat and lead forms. The lead board, up to the point a quote is sent. | Pricing. Job records. Running the job after the quote is accepted. FenceOS still sends updates to Communicator after that, so your tags and follow-ups keep working. |
| **Slack** | Your team talking about a job. If your company has the FenceOS Slack connection set up and tested, a private channel is made for each job when the quote is accepted. Photos, walkthrough videos, checklists. | Customer conversations. The official record of the job. |
| **Your AI helper or bot** | A helper that watches things and tells you what to act on. Think of it as a virtual assistant you train. | Being the record of anything. If the bot goes away, nothing should be lost. |

## How a job moves

1. A lead calls, texts or fills out a form. It lands in **Communicator**.
2. You qualify the lead in Communicator. You can start a drawing in **Estimator** in a side tab while you talk.
3. You send the quote from Estimator. FenceOS tells Communicator the quote was sent. If your Communicator is set up for it, the lead then moves to your quoted stage.
4. The customer accepts. From here the job lives in FenceOS (the quote and money in Estimator, the work in Operator), not in the lead board.
5. The job shows in **Operator** so production knows it is coming. It shows even before the deposit is paid. Whether you schedule before the deposit is your call.
6. If the Slack connection is set up and tested, a **Slack** channel is made for the job. The team posts there.
7. Crews run the job in Operator. Payments are recorded in FenceOS.

## Rules for your AI tool

Read these as instructions.

1. **FenceOS is the source of truth.** Never keep a second copy of prices, quotes, payments, schedules or customer records in another app, a spreadsheet or a database of your own.
2. **Before you build anything, check this list in order.** Can FenceOS already do it? Can a Communicator stage or workflow do it? Can a Slack workflow, checklist or bot do it? Only if all three are no should you suggest something new.
3. **Do not build a separate hosted app.** No new website, no new server, no new database. A hosted app is something the owner then has to keep running, fix and pay for. Suggest a Slack bot or workflow instead.
4. **Keep Communicator simple.** Start from the standard setup. Add one automation at a time. The more rules you stack, the more they collide and break.
5. **Test every automation before trusting it.** Use a made-up customer. Check that nothing sends a customer the same text twice. Plan on more time testing than building.
6. **A person approves anything a customer or the public will see.** Texts, emails, social posts, review replies.
7. **Never move money, change a price, or record a payment from a bot.** People do those in FenceOS.
8. **Ask before you automate.** If the owner has not run the step by hand a few times, it is too early to automate it.

## Good things to build on top

- A morning message in Slack: missed calls, new leads, who needs a follow-up.
- A bot that reads call notes and lists the things someone promised to do.
- A bot that picks the best job photos of the day and asks before posting them.
- A receipts channel: post a photo of a receipt and it gets sent to your bookkeeping.
- A Slack checklist for the pre-job walkthrough.

## Things not to build

- Your own photo app, task app or job tracker.
- A second lead board outside Communicator.
- Anything that copies FenceOS data somewhere and then edits the copy.
- Anything that needs you to host code.

## Handing a job from sales to production

These steps are for your people, not for an AI tool.

- Put the notes production needs on the quote in Estimator: dogs, gates, where to knock, utility locate details.
- If it matters, also call or message the production lead. Do not rely on the note alone.
- A site video is worth it on tricky jobs. Post it in the job's Slack channel once the job is accepted.
- If you use CompanyCam and have it turned on in FenceOS: when you add a customer, FenceOS links them to the CompanyCam project at that address, or makes a new project if there is none. After the quote is accepted, the drawing and the documents included with the quote are added to it.

## What FenceOS support will and will not help with

- Yes: how FenceOS works, how the pieces fit, which tool to use for an idea.
- No: reviewing or fixing code for an app you built yourself.

## Versions

- Version 1, 2026-11-17: first version.
