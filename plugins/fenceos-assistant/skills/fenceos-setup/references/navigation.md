# Company context and setup navigation

Use this reference at entry, during the read-only look-around, and before every setup batch and write.

- Confirm the signed-in user, effective role and company with the owner. For a Super Admin, the selected organization must remain visible in **Viewing as**, with **Working Inside** on Products/Locations where shown. Never work from the platform template view for a company task. An ordinary Org Admin need not have a Super Admin banner; confirm its own company context instead. Missing or changed expected context stops work.
- **Org Admin:** open **Organization → Products → BOM Setup**. Advanced BOM access depends on the existing company rollout and permissions.
- **Super Admin:** open **Org Settings → Manage Products & BOM** for the selected company. Do not require a Products **BOM Setup** button for this role. A Super Admin explicitly in Account Admin Mode uses Org Admin navigation and its restricted permissions; do not switch modes or enable rollouts to bypass a missing control.
- The destination is **Product BOM Setup**; use **Advanced BOM Catalog** only when available. A missing control after a successful load is unavailable access, not permission to improvise. Ask the company's administrator/support to confirm eligibility; this skill never changes permissions or feature flags.

An empty or partial list may be a failed load. On a 429, honor its displayed retry time; otherwise allow about ten seconds before one reload. Reload at most once, only when it will not discard an unsaved draft, then recheck company context and successful loading. If loading or context remains uncertain, stop and report unavailable evidence, not an empty catalog or missing permission. No reload loops.

Never click **Reset organization BOM** or **Backfill Default BOM Catalog**, including during practice or after batch approval. These are not the draft-only **Reset to Stored Version** control.
