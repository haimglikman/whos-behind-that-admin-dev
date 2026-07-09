### v2.13.14 (admin-dev) | Server: v1.19.3 | Client: v1.15.9
- Fixed posts array always being empty when saving clusters — now built from the basket (in-memory) instead of getHistory() which could miss posts not in current localStorage session

### v2.13.13 (admin-dev) | Server: v1.19.3 | Client: v1.15.8
- Fixed P-number mismatch when viewing client clusters in admin — timeline and legend now preserve postIds order when reconstructing from cluster history (presorted=true), instead of re-sorting by scan timestamp which caused scrambled P-numbers and future dates

### v2.13.12 — DISCAREDED (duplicate of v2.13.10)

### v2.13.11 — bug fix (admin-dev) | Server: v1.19.3 | Client: v1.15.6
- Fixed P-number scrambling — timeline and legend now assign P-numbers from the original postIds order, not the ts-sorted display order. P1/P2/P3/P4 are now identical between client and admin for the same cluster.

### v2.13.10 (admin-dev) | Server: v1.19.3 | Client: v1.15.5
- Clusters history: now uses saved posts data to reconstruct client clusters — P-numbers, entities and URLs now match what the client showed
- Clusters history: cluster ID moved above timeline in live investigation view
- Clusters history: frame and event now shown as prominent labeled cards in live investigation view
- Tab title changed to "WBT - Admin DEV"

### v2.13.9 (admin-dev) | Server: v1.19.2 | Client: v1.15.4
- Clusters history: client-originated clusters now display gracefully — posts not in admin's local history get placeholder timestamps spread 1 day apart so they don't all stack on top of each other
- Clusters history: cluster ID moved above timeline (prominent, at top of view)
- Clusters history: frame and event shown as prominent labeled cards, not tiny bottom text
- Clusters history: omitted posts now show their one-liner summary in legend, same as included posts
- Investigate (live): cluster IDs now shown above timeline before running
- Investigate (live): frame and event shown as prominent labeled cards throughout

### v2.13.8 — bug fix (admin-dev) | Server: v1.19.1
- Fixed "clearInvestigationBasket is not defined" error when running investigation

### v2.13.7 (admin-dev) | Server: v1.19.1
- Post history: app/server version filters are now dropdowns populated from actual versions in history — only versions with real data appear
- Post history: blank version filter = no limit on that side (from/up to work independently)
- Post history: pending banner expanded — shows each basket post with primary entity, secondary entity, date, scan ID, and × remove button
- Post history: "Run investigation →" button auto-navigates to Investigate tab and runs immediately
- Investigate: results persist while tab is active, survive navigation away and back
- All dates: switched to DD/MM/YYYY format throughout
- Bottom bar: app version now always reads from APP_VERSION constant — fixes stale version occasionally showing

### v2.13.6 (admin-dev) | Server: v1.19.1
- Timeline: label column reduced to 120px — timeline now starts at ~18% of SVG width
- Timeline: entity label font reduced to 8px, wrap at 16 chars — cleaner and less wide
- Timeline: hover popup now flips left when near the right edge of the screen
- Post history: version filter labels shortened to "App version — from" / "up to"
- Investigate: pending banner auto-clears after running investigation

### v2.13.5 — bug fix (admin-dev) | Server: v1.19.1
- Timeline: rebuilt hover popup using clean global functions (wbtShowTlPopup/wbtHideTlPopup) — no more inline quote-escaping that was breaking the SVG
- Timeline: popup shows P number, primary entity + score, secondary entity (if exists), date, post summary — each on its own line, collapses on mouseout
- Timeline: secondary entity removed from below circles
- Timeline: label column 160px, 2px buffer, labels wrap at ~20 chars
- Post history: version filters split into "starting from" / "up to" with semver range comparison

### v2.13.4 — bug fix (admin-dev) | Server: v1.19.1 - BAD VERSION, REVERTED!!! 2.13.5 was based on 2.13.3
- Timeline: label column 160px, 2px buffer — timeline starts further left matching card edge
- Timeline: secondary entity removed from below circles — shown in hover popup and legend instead
- Timeline: hover popup on each circle — shows P number, primary entity + score, secondary entity (if exists), date, post summary; collapses on mouseout
- Legend: secondary entity shown between primary entity and post summary (if exists)
- Post history filters: app version and server version split into "starting from" / "up to" range fields with semver comparison

### v2.13.3 — bug fix (admin-dev) | Server: v1.19.1
- Timeline: label column 160px, 2px buffer — timeline starts further left matching card edge
- Timeline: secondary entity removed from below circles — shown in hover popup and legend instead
- Timeline: hover popup on each circle — shows P number, primary entity + score, secondary entity (if exists), date, post summary; collapses on mouseout
- Legend: secondary entity shown between primary entity and post summary (if exists)
- Post history filters: app version and server version split into "starting from" / "up to" range fields with semver comparison

### v2.13.3 — bug fix (admin-dev) | Server: v1.19.1
- Timeline: label column narrowed to 140px (from 180px) — more room for the timeline
- Timeline: buffer between labels and first post reduced to 2px
- Timeline: entity labels left-aligned from x=6, wrap to second line at ~18 chars
- Timeline: no annotation lines in output

### v2.13.2 — bug fix (admin-dev) | Server: v1.19.1
- Timeline: hard 180px label column — entity names left-aligned from x=6, wrap to second/third line if long
- Timeline: 4px buffer between label column and first post (down from 12px)
- Timeline: posts start exactly at the first date position, no overlap with labels
- Timeline: nodeR reduced from 18 to 15 — cleaner, less dominant circles
- Timeline: lane height increased to 70px to accommodate wrapped 2-line entity labels

### v2.13.1 — bug fix (admin-dev) | Server: v1.19.1
- Investigate basket: removed individual × remove buttons — use the reversible + Investigate button to add/remove instead
- Timeline Y axis: entity labels reduced to font-size 9px, allowing more characters to fit cleanly
- Legend: each post now shows a "↗ Go to post" link — both included and omitted posts
- FAQ tab: seeded with all 32 existing FAQs from client, now loaded dynamically from server DB

### v2.13.0 (admin-dev) | Server: v1.19.0
- Sidebar replaced with horizontal top nav bar — same style as client (Analyze left, Stats right)
- New FAQ tab — fully editable: add, edit, delete FAQ items; stored on server DB; grouped by category
- Timeline visualization: Y axis now shows entity lanes — posts sit at the height of their primary entity; secondary entity shown in brackets below the circle; no more label collisions
- Bug fix: connection lines now preserved and restored when reopening a cluster from history
- Bug fix: cluster history card now shows total post count including isolated posts
- + Investigate button is now reversible — clicking again removes the post from the basket

### v2.12.4 — bug fix (admin-dev) | Server: v1.18.3 | Client: v1.14.4
- Entity match: now filters by prefix (startsWith) not substring — typing "i" shows Iran and Itamar Ben Gvir, not all entities containing "i"
- Timeline: entity name labels now clamp to frame edges — leftmost posts no longer escape the SVG boundary
- Timeline: long entity names now truncated with ellipsis (…), full name shown on hover via SVG tooltip
- Cluster cards: cluster ID shown prominently at top in blue monospace badge
- Cluster cards: editable name field with Save button — renames cluster in server DB, default is AI-generated name
- Same rename field shown when reopening a cluster from history

### v2.12.3 — bug fix (admin-dev) | Server: v1.18.2 | Client: v1.14.3
- Timeline: same-date posts now stack entity labels vertically (Iran on top, Turkey below)
- Timeline: removed textLength/lengthAdjust from labels — crisp font rendering restored
- Cluster history: omitted posts now shown identically to live investigation view
- Entity match filter: fixed — typing now filters results immediately without rebuilding the dropdown

### v2.12.2 — bug fix (admin-dev) | Server: v1.18.1 | Client: v1.14.2
- Timeline: close-proximity date labels now skip rendering when within 52px of previous label, preventing overlap
- Timeline: entity titles below nodes now constrained to node width using SVG textLength — no bleed into adjacent nodes
- Clusters history: view button now works — fixed double JSON.stringify bug that broke inline onclick handler
- Entity match filter: now filters results on every keystroke immediately, not just after first population

### v2.12.1 (admin-dev) | Server: v1.18.1 | Client: v1.14.1
- Timeline: same-date posts now sit side by side with horizontal offset, smaller circles
- Timeline: date label shown once per date, each post gets its own narrative title below
- Basket: hovering a post shows tooltip with entity, score and post excerpt
- Legend: each included post shows its one-liner narrative summary below the metadata row
- Clusters history: each cluster is clickable — opens full investigate view reconstructed from saved data
- Investigate: buttons auto-clear after Run investigation is pressed

### v2.12.0 (admin-dev) | Server: v1.18.0 | Client: v1.14.0
- New Clusters history tab (below Investigate) — shows all previous cluster analyses from server DB
- Investigation: clusters now saved to server DB after synthesis with auto-generated cluster ID (WBT-CLU-...)
- Timeline fix: same-date posts now show the date label only once; entities stack vertically below

### v2.11.1 — bug fix (admin-dev) | Server: v1.17.2 | Client: v1.13.0
- History filters: combined Platform and News site into single "Source" dropdown — social platforms at top, individual news sites populated dynamically below
- Entity match: now only shows entities that appear in at least one history entry
- Entity match: dropdown populates on first keystroke (lazy init)

### v2.11.0 (admin) | Server: v1.17.1 | Client: v1.13.0

- New Investigate tab — full one-pager with timeline, legend, synopsis, technical details, excluded posts
- + Investigate button on every history card
- Pending investigation banner in Post History tab
- History filters: added Actor handle, News site (dynamic, shows display names)
- DOMAIN_NAMES lookup shared across admin# whos-behind-that-admin-dev
