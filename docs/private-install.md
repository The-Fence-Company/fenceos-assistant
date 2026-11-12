# Use FenceOS Assistant with ChatGPT or Claude

Package guide: Assistant **0.3.2**, FenceOS setup **0.7.3**, optional Matrix / Cash Copilot setup **3.3**. Verify the installed versions before starting. Client documentation reviewed November 4, 2026; source compatibility is not proof of a fresh install or browser session.

For GitHub installation, choose the reviewed public commit carrying the versions above. OpenAI directory availability and Windows acceptance are separately qualified; this guide is not proof of either.

## Choose your product

**FenceOS Assistant** uses your authorized browser for FenceOS catalog/BOM setup. Its second, optional skill handles explicit Matrix budget and Cash Copilot planning requests. Installation does not start either workflow or grant browser, account or financial permissions.

**FenceOS Intelligence** is a separate read-only OAuth integration for business summaries. It cannot perform browser setup, edit records, send messages, schedule crews or process payments. As of the October 31, 2026 pilot check, company 1 was enabled; this dated observation is not current eligibility proof. Confirm company eligibility and your personal grant with [FenceOS support](mailto:support@thefencecompanyutah.com).

## Install for ChatGPT desktop Work

Use a ChatGPT desktop Work environment that offers custom plugins and a supported interactive browser capability. A local marketplace is a desktop setup route. Registering it with Codex CLI is an administrator/setup step toward desktop plugin use, **not installation into ordinary ChatGPT chat**. [OpenAI's package guide](https://developers.openai.com/plugins/build/plugins) documents Git/local marketplaces and ref selection; [plugin guidance](https://learn.chatgpt.com/docs/plugins) describes the separate plugin and app authorizations.

1. Obtain the reviewed `fenceos-assistant.zip` and extract it into a retained local folder. The extracted `fenceos-assistant` folder contains both marketplace manifests and `plugins/`.
2. An administrator or local setup operator with an existing supported Codex CLI can register that extracted marketplace root. This example uses a local input, not a promised public release SHA:

   ```text
   codex plugin marketplace add /path/to/reviewed/fenceos-assistant
   ```

3. Open the desktop Plugins interface, select **fenceos**, and install **fenceos-assistant** where available. `/plugins` is the Codex CLI plugin interface; its presence alone does not prove ChatGPT desktop loading. Confirm the installed package and both skills in the intended desktop session.
4. Start a new Work task with supported browser control. Sign in to FenceOS yourself in that controlled browser, confirm the company and use the setup prompt below. A phone or another browser's login does not authenticate this session.

If the desktop cannot discover the registered marketplace, stop and have the workspace administrator check the supported import route. Do not copy caches, move cookies or assume a CLI success proves desktop access.

## Managed ChatGPT workspace import

A workspace administrator with repository access can use **Admin → Plugins → Add → Import marketplace**, enter `The-Fence-Company/fenceos-assistant`, leave the repository root path empty, and select the actual reviewed available public commit from its release receipt. Confirm that commit contains the intended versions. Imported plugins may be Desktop only; role availability, app authorization and browser support remain separate. See [workspace plugin management](https://learn.chatgpt.com/docs/enterprise/plugin-management).

There is no verified universal ZIP installer for this browser assistant in ordinary personal ChatGPT web. Web clients can load supported plugins, but loading does not create browser automation. Use a qualified ChatGPT desktop Work session or Claude Desktop Cowork with its supported browser capability when the ordinary chat lacks it. Do not substitute the Intelligence MCP connector for the browser assistant.

## Install in Claude Cowork or Code

Use a Claude plan/workspace that allows custom plugins. In Claude Desktop, open **Cowork** first, then **Customize → Plugins → Add → Add marketplace**. Enter [The-Fence-Company/fenceos-assistant](https://github.com/The-Fence-Company/fenceos-assistant), install **fenceos-assistant** from **fenceos**, and verify the installed versions. Start a new task with supported browser control, sign in yourself in that session and confirm the company. [Claude plugin overview](https://claude.com/docs/plugins/overview) and [using plugins in Claude](https://support.claude.com/en/articles/13837440-use-plugins-in-claude) describe these routes.

For existing Claude Code users, register the reviewed local marketplace folder or use the public repository after confirming its release version:

```text
claude plugin marketplace add /path/to/reviewed/fenceos-assistant
claude plugin install fenceos-assistant@fenceos
```

The skills are `/fenceos-assistant:fenceos-setup` and `/fenceos-assistant:matrix-cash-copilot-setup`. See the [Claude Code plugin CLI reference](https://code.claude.com/docs/en/plugins/cli-reference). Account-installed plugins can be available across chat, Cowork and Code, but a local Code installation does not prove installation in a different session. Web plugin loading is distinct from browser automation; confirm the actual browser tool and signed-in session before promising actions.

## Connect read-only Intelligence

**Check eligibility first.** Use your own approved FenceOS account and company. Keep an existing correct connection rather than creating duplicates.

A copy installed from OpenAI's plugin directory, once it is listed there, already lists this connector with the plugin, so connect it when prompted instead of adding a custom server. Only an Org Admin or Super Admin of an enabled company can complete the sign-in.

Server URL:

```text
https://estimate.thefencecompany.com/api/mcp/fenceos-intelligence
```

### In Claude

1. Open **Customize → Connectors → Add custom connector** and enter the server URL.
2. Use OAuth with **Claude's published identity / CIMD** where offered.
3. Complete normal FenceOS sign-in yourself. Inspect the client, your company and the read-only consent before accepting.
4. Enable the connector in a chat. Ask: **“Give me a business overview for the last 30 days. Include the reporting window and missing evidence.”**

A private custom connector does not require a directory listing or the Assistant package. Organization owners or administrators may need to make the connector available first; every user still completes their own authorization.

### In ChatGPT on the web

1. Open [ChatGPT Plugins](https://chatgpt.com/plugins), select **+ → Add custom MCP server**, and name it **FenceOS Intelligence**.
2. Enter the server URL. Choose OAuth and **Client ID Metadata Documents / CIMD** where offered. Leave static client ID and client secret fields unset.
3. Review the risk and data-sharing notice. Create the private plugin only if you approve, then complete FenceOS sign-in and your company's read-only consent.
4. Install the resulting plugin. Start a new chat, type **@**, select **FenceOS Intelligence** and use the overview prompt above.

Your plan and workspace must allow custom MCP creation. No Free or Go availability is promised here. If the control is missing, access is denied, or an unexpected secret or client identity is required, stop and contact support. Do not switch to unauthenticated access, share a key or change registration settings to force a connection.

## Historical evidence and unresolved limits (October 31, 2026)

- **Claude:** a fresh overview through the existing company 1 web connection passed on October 31. This was one then-current-release read, not proof of every tool or every desktop, Cowork, Code or mobile workflow.
- **ChatGPT:** all eight tools passed in the private test, but saved replies still failed to reopen in the latest check. The rendering issue is unresolved. Reconnecting or repeatedly regenerating is not a verified fix.
- **Assistant:** package files and install instructions were reviewed. A fresh customer install across all supported clients has not been completed.
- **Intelligence:** results contain bounded metrics and summaries. Booked quote margin is not realized profit or collected cash; handoff evidence is not an authoritative schedule; attribution is not proof of causation. Check important decisions in FenceOS.

## Data sharing, disconnect and support

Intelligence sends approved company metrics and bounded summaries to the AI provider when its tools run. Its three conversation tools also send contact display names and message text from recent customer conversations, with phone numbers and email addresses masked where the connector detects them. The client sends the request arguments and context needed for those calls to FenceOS, subject to its notices. Connect only if your company permits that sharing. Never paste passwords, cookies, sign-in codes or tokens into a chat or support message.

To stop access, open [FenceOS Intelligence setup](https://estimate.thefencecompany.com/intelligence/connect) and disconnect the specific client connection. Disconnect it in that client's settings as well if needed. Claude and ChatGPT connections are separate. Disconnecting does not delete old conversations.

If installation or a call fails, send support your company name, the time and the visible error, without credentials or customer details. A missing browser needs a supported browser environment; a company denial needs an eligibility check; a rate limit needs its displayed retry time. Reinstalling does not change these permissions.

[Support](mailto:support@thefencecompanyutah.com) · [Privacy Policy](https://estimate.thefencecompany.com/legal/privacy) · [Terms of Use](https://estimate.thefencecompany.com/legal/eula) · [Existing Claude setup guide](https://estimate.thefencecompany.com/fenceos-intelligence.html)

## Updates, packages and rollback

When either skill starts, the assistant checks once whether a newer FenceOS Assistant has been published. It reads only the version number from the public plugin file on GitHub and sends nothing about you or your company. If a newer version is out, it tells you which version you have, which is available and how to update in your app, then keeps working unless you ask it to wait. If the check cannot run, it says nothing and carries on. It never installs an update without your yes.

Use the supported marketplace update control, start a new session, and verify **Assistant 0.3.2 / setup 0.7.3 / finance 3.3** in the installed copy. A publisher records the actual public commit in the release receipt; only pin a Git route to that reviewed available commit. A local folder or copied skill does not acquire an update URL or automatic refresh: replace the complete reviewed folder/package through its supported route and retain the private checkpoint separately.

`fenceos-assistant.zip` contains the marketplace folder and both marketplace formats. Extract it before registering a local marketplace. `fenceos-assistant-plugin.zip` contains only the plugin, both manifests at the archive root and both skills, for clients that actually offer plugin upload. A GitHub source archive or a ZIP attached to chat is not evidence of installation.

Availability history, checked offline November 4, 2026: public commit `63cc63da51fe274fa84ccbd5857af56c224d0c72` carried Assistant 0.2.0 / setup 0.6.0. It is a known rollback baseline, not a pin for this package. To roll back, select that reviewed version through a supported reinstall/version-selection route or use a retained verified archive. The old package has **no finance module**. Plugin rollback neither deletes private checkpoints nor rolls back saved business or financial data; those need their own reviewed recovery workflow.

## First run and troubleshooting

For FenceOS setup, say **“Help me get set up in FenceOS. Start with a read-only look around.”** Confirm the company and role in the controlled browser. If browser control is absent, the assistant can explain steps while you click, but cannot claim to have performed them.

Expect one yes per exact batch, then a readback. Organization BOM reset/backfill, sold jobs, accepted terms, automatic recomputation and payments remain outside setup. Published catalog, coverage, guided quantities and saved test-quote BOM are separate results; a new test does not prove an old job recovered.

For finance only when requested, say **“Use Matrix and Cash Copilot setup to help me plan next year's budget. Confirm the business, planning period and records, and prepare the proposed changes before entering live fields.”** The assistant supplies the Matrix sign-in destination, checks actual account capabilities and obtains exact business/host/plan/period, source and account/email scope. It needs batch approval before the first autosaving keystroke. It cannot enable Cash, provision accounts, mark paid/received, change real due dates or authorize rate publication as part of setup. Saved, Reconciled and Ready are separate finance results and never substitute for catalog/BOM proof. The 8 to 10 hour planning target is not a tested universal promise. General FenceOS setup does not prompt for or start finance.

For a 429 or stale/empty FenceOS page, honor its retry time and reload at most once when no unsaved draft would be lost. Confirm the company again. If it still fails, stop with the time and safe visible error. Use the skill's role-specific navigation; do not infer an empty catalog or missing access. Financial guides and enabled controls must be checked in an authorized session before financial capabilities are treated as available.

Direct distribution is not an official directory listing or endorsement. Fresh ChatGPT and Claude installation, browser control, correct-company navigation and financial save/reconciliation remain separate qualification steps; package tests prove none of them.
