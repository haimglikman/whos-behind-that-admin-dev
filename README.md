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
