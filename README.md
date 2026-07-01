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
