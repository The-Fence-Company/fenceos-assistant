# Company context and setup navigation

Scope: account work. In paper work (SKILL.md, "Two kinds of work") use only the facts and screen names here; no step that opens, saves or reads back a screen applies.

Use this reference at entry, during the read-only look-around, and before every setup batch and write.

- Confirm the signed-in user, effective role and company with the owner. For a Super Admin, the selected organization must remain visible in **Viewing as**, with **Working Inside** on Products/Locations where shown. Never work from the platform template view for a company task. An ordinary Org Admin need not have a Super Admin banner; confirm its own company context instead. Missing or changed expected context is a hard stop (SKILL.md, section 6): tell the user and wait.
- **Org Admin:** open **Organization → Products → BOM Setup**. Advanced BOM access is standard for Org Admins; it depends only on permissions.
- **Super Admin:** open **Org Settings → Manage Products & BOM** for the selected company. Do not require a Products **BOM Setup** button for this role. A Super Admin explicitly in Account Admin Mode uses Org Admin navigation and its restricted permissions; do not switch modes or enable rollouts to bypass a missing control.
- The destination is **Product BOM Setup**; use **Advanced BOM Catalog** only when available. A missing control after a successful load is unavailable access, not permission to improvise. Tell the user the control is not on screen and that their company administrator, or FenceOS support, can confirm access (SKILL.md, section 6); this skill never changes permissions or feature flags.

An empty or partial list may be a failed load. On a 429, honor its displayed retry time; otherwise allow about ten seconds before one reload. Reload at most once, only when it will not discard an unsaved draft, then recheck company context and successful loading. If loading or context remains uncertain, that is a hard stop (SKILL.md, section 6): tell the user the page did not load, report unavailable evidence, not an empty catalog or missing permission, and wait for them. No reload loops.

Never click **Reset organization BOM** or **Backfill Default BOM Catalog**, including during practice or after batch approval (SKILL.md, section 6). These are not the draft-only **Reset to Stored Version** control.

Browser connection: section 0 of [SKILL.md](../SKILL.md) covers the first check, and its Troubleshooting table covers the one recovery path. After any reconnect, reload, or tab change, re-read the signed-in user, role, company and the open record before the next write; a difference is a hard stop (SKILL.md, section 6); values read before the interruption may be stale.
