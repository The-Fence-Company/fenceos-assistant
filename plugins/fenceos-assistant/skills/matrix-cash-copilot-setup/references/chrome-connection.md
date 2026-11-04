# Built-in browser first, Chrome only when needed

This reference covers desktop browser fallback. It does not connect a phone or cloud browser to a desktop profile; follow the [client adapter](client-adapter.md) for the current client's supported route and authentication boundary.

The agent is the browser operator. Use the chat app's built-in browser for website work by default. Do not ask the owner to click menus, enter reviewed business values, perform imports, or save settings when the tool can do those steps. Ask concise questions in chat for decisions and unclear facts, then carry out the authorized answer yourself. Prefer connected email search tools for discovery; this browser preference does not require replacing a working read-only connector with webmail.

## Default connection and handoffs

Initialize the documented browser-control tool and open the confirmed product URL in the built-in browser. Inspect the current page and follow the ordinary sign-in flow. No Chrome extension is needed unless a fallback is actually required. A signed-out page alone is not evidence that the built-in browser is blocked.

Ask the user to take over only for private credentials/MFA, sensitive access consent, legal acceptance, a chooser the tool cannot operate, or another mandatory tool handoff. Explain the single required action, wait for it, inspect the result, and resume control. Do not turn one handoff into a request for the user to complete the rest of setup manually. Respect the tool's action-time confirmation rules even when the intended workflow is hands-off.

A successful read of the intended signed-in business proves access. A permission toggle alone does not. Recheck the business after any account or browser change. Do not inspect unrelated tabs or browsing history.

## When to switch to Chrome

Use Chrome after a concrete built-in browser failure, such as an unsupported sign-in or upload flow, an explicit browser restriction, or an unavailable control capability. First use one supported diagnosis or corrective action if appropriate. Do not repeatedly retry a blocked flow. Tell the user the reason for switching, preserve completed saves and pending actions, and resume only after verifying the same account/business in Chrome. Never bypass browser security warnings, organizational restrictions, or site access controls.

## Connect Chrome only for the fallback

Use the current client's installed browser capability documentation and returned tools to identify the actual extension and connection flow. In Codex, use its installed browser plugin documentation; in ChatGPT or Claude, use that client's supported route. Do not direct a user to another client's Settings menus. Explain only the missing step and verify a read of the intended site after connection.

Have the user approve the extension's sensitive access themselves. Explain that it can operate signed-in pages and that financial content read during work may enter the chat context. Use site-specific access for the confirmed product domain. There is no need to enable all-site access or browser history for this task. Respect blocked sites and managed-browser restrictions.

Connection evidence is an actual successful read of the correct signed-in product page, not the user's report that a toggle is on. Confirm the displayed business/location and intended workspace. Have the user sign in privately and complete MFA. If a new account accepts terms or asks for new permissions, hand that step to the user.

## File access

Reading an attachment in the chat and uploading it into the product are separate steps. Identify the exact file and destination before uploading. Use only file-selection APIs documented by the active tool. If the built-in browser cannot complete the chooser, try the supported Chrome fallback. Ask the user to select a file only if the active tool cannot operate the chooser. Never invent a `setInputFiles` method or bypass a failed chooser with HTTP uploads.

Only if current diagnostics specifically require local file-URL permission, identify the actual installed extension and its documented permission path. The owner grants any expanded local-file access. Do not enable it merely because an ordinary upload failed.

Native computer control may separately request Accessibility or Screen Recording access. Only guide those permissions when the active tool explicitly requires them for a native step. Use the OS prompt's exact application name and settings destination, explain the purpose, and let the user grant access. Do not ask for Full Disk Access as a routine shortcut.

## If connection fails

Use the tool's supported diagnostics. Check the active Chrome profile, extension enabled state, app connection, and product-site access. Retry a lightweight read once after a concrete corrective action. Do not restart Chrome or close the user's work without agreement. If transport/native-host setup is broken, guide the user through reinstalling the browser plugin from the app; do not edit its manifest or weaken system controls.

If both supported browser routes are blocked or the user declines a required permission, continue document analysis and prepare the exact remaining setup packet. Explain the blocker and offer the smallest necessary manual step. A complete manual click-through is a last resort, not the default. Do not claim the product is configured. Follow the shared recovery limit: at most three unsuccessful cycles or about five minutes of diagnosis, then ask for help or prepare an FOS support handoff.

## Source and drift

The executing environment's current browser documentation and confirmation policy govern setup. Use visible control labels; no fixed extension/menu name is assumed here.
