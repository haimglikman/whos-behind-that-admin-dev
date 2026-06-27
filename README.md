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
