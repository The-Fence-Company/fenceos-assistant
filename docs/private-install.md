# Use FenceOS with Claude, ChatGPT or Codex

Private installation · Early access · Updated October 31, 2026

You can install FenceOS directly without an official directory listing. Choose the product you need first. Installing one does not install or authorize the other.

## Choose your product

**FenceOS Assistant 0.2.0** helps you work through FenceOS screens. It covers getting started, catalog setup and bills of materials. You sign in yourself, confirm the company and approve each batch before changes are saved. You need a supported browser capability and your normal FenceOS permissions.

**FenceOS Intelligence** lets an AI client read approved business summaries through OAuth. It cannot edit records, send messages, schedule crews or process payments. Your company must be enabled and your user must have a personal Intelligence grant before connecting.

**Intelligence is invitation-only.** The last verified pilot configuration enables company 1 only. It is not open to all FenceOS companies. Contact [FenceOS support](mailto:support@thefencecompanyutah.com) to confirm eligibility. A plugin download does not grant access.

## Install the Assistant in Claude

Use a Claude plan and environment that allow custom plugins. For browser setup work, Claude Desktop with Cowork and its supported browser capability is the simplest documented route.

1. Open **Customize → Plugins → Add → Add marketplace**.
2. Enter [https://github.com/The-Fence-Company/fenceos-assistant](https://github.com/The-Fence-Company/fenceos-assistant).
3. Install **fenceos-assistant** from the **fenceos** marketplace. The reviewed package is version **0.2.0**.
4. Start a new browser-enabled task. Open FenceOS, sign in yourself and confirm your company.
5. Say: **“Help me get set up in FenceOS.”** Review and approve each proposed batch before saving.

Current Claude web and desktop clients can load custom plugins, but loading a skill does not provide browser control. Browser availability, plan and organization permissions still apply. Do not assume an organization's GitHub-sync route accepts the same public repository as an individual marketplace install.

For existing local Claude Code users, the public package documents:

```text
claude plugin marketplace add The-Fence-Company/fenceos-assistant
claude plugin install fenceos-assistant@fenceos
```

The skill is `/fenceos-assistant:fenceos-setup`. A local Code installation does not automatically install into a separate cloud session or provide a browser.

## Install the Assistant in Codex or a managed ChatGPT workspace

For an existing Codex desktop/CLI environment with plugin support, add the reviewed public marketplace revision:

```text
codex plugin marketplace add https://github.com/The-Fence-Company/fenceos-assistant --ref cf4e017b41a219a055ae15f483cce978502e6748
```

Open the Plugins browser, or use `/plugins` in Codex CLI. Select **fenceos**, install **fenceos-assistant**, then start a new session. Enable a supported browser capability, sign in to FenceOS yourself and use the same setup prompt above. The CLI alone does not provide browser control.

For a managed ChatGPT workspace, an administrator can use **Admin → Plugins → Add → Import marketplace**, enter the public repository, leave its root path empty and select the reviewed commit. Role availability, app authorization and browser support are separate checks. Imported plugins can be Desktop only.

These are specific marketplace routes. There is no verified universal one-click install link or ordinary Personal ChatGPT web ZIP installer. Do not paste a ZIP into a chat and assume it installed. This package's fresh install and browser workflows have not been qualified in every client, plan or region.

## Connect read-only Intelligence

**Check eligibility first.** Use your own approved FenceOS account and company. Keep an existing correct connection rather than creating duplicates.

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

## Know the current limits

- **Claude:** a fresh overview through the existing company 1 web connection passed on October 31. This is one current-release read, not proof of every tool or every desktop, Cowork, Code or mobile workflow.
- **ChatGPT:** all eight tools passed in the private test, but saved replies still failed to reopen in the latest check. The rendering issue is unresolved. Reconnecting or repeatedly regenerating is not a verified fix.
- **Assistant:** package files and install instructions were reviewed. A fresh customer install across all supported clients has not been completed.
- **Intelligence:** results contain bounded metrics and summaries. Booked quote margin is not realized profit or collected cash; handoff evidence is not an authoritative schedule; attribution is not proof of causation. Check important decisions in FenceOS.

## Data sharing, disconnect and support

Intelligence sends approved company metrics and bounded summaries to the AI provider when its tools run. The client sends the request arguments and context needed for those calls to FenceOS, subject to its notices. Connect only if your company permits that sharing. Never paste passwords, cookies, sign-in codes or tokens into a chat or support message.

To stop access, open [FenceOS Intelligence setup](https://estimate.thefencecompany.com/intelligence/connect) and disconnect the specific client connection. Disconnect it in that client's settings as well if needed. Claude and ChatGPT connections are separate. Disconnecting does not delete old conversations.

If installation or a call fails, send support your company name, the time and the visible error, without credentials or customer details. A missing browser needs a supported browser environment; a company denial needs an eligibility check; a rate limit needs its displayed retry time. Reinstalling does not change these permissions.

[Support](mailto:support@thefencecompanyutah.com) · [Privacy Policy](https://estimate.thefencecompany.com/legal/privacy) · [Terms of Use](https://estimate.thefencecompany.com/legal/eula) · [Existing Claude setup guide](https://estimate.thefencecompany.com/fenceos-intelligence.html)

## Installation references

[Claude custom plugins](https://claude.com/docs/plugins/overview) · [Claude custom connectors](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) · [Claude Code marketplaces](https://code.claude.com/docs/en/discover-plugins) · [OpenAI local marketplaces](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli) · [ChatGPT workspace import](https://learn.chatgpt.com/docs/enterprise/plugin-management) · [ChatGPT custom MCP setup](https://developers.openai.com/api/docs/guides/custom-mcp-server)

Direct distribution by FenceOS is private installation, not an official Claude or ChatGPT directory listing or endorsement. Client availability, company eligibility and individual consent remain required.
