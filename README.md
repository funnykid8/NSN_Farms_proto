# NSN Farms — GitHub Pages web edition

A responsive, serverless farm management prototype built with HTML, CSS and vanilla JavaScript. No build tooling is required.

## Publish

1. Create a GitHub repository, e.g. `NSN-Farms`.
2. Upload `index.html`, `styles.css`, and `app.js` to the repository root.
3. Go to **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Select `main` and `/ (root)`; save.
5. Open `https://YOUR-USERNAME.github.io/NSN-Farms/` after deployment.

## Implemented

- Crop/cost-centre and worker master records.
- Paid expense and sale entry with balanced double-entry journals.
- Seasonal attendance with historical wage rate snapshots.
- Worker advances, FIFO recovery, and wage settlement with duplicate-attendance protection.
- Crop operating reports, transaction histories, and journal balancing check.
- Browser-local JSON backup and restore.

## Important limitations

**Not production-ready for sole use as a farm accounting system.** This is a professional-looking functional web prototype, not a certified ERP. The app has not undergone full browser-based end-to-end tests. In particular:

- Uses browser `localStorage`, not SQLite/IndexedDB. Storage is device/browser specific, has size limits, and can be cleared. No cross-device sync or guaranteed offline loading after cache eviction.
- No browser encryption for records or backups. Do not use on a shared device without appropriate safeguards.
- No staff monthly payroll, overtime, sales receipt follow-up, inventory, fixed asset depreciation, opening balances, full balance sheet, manual overhead allocations, or PDF/CSV export.
- Ledger postings exist for the implemented cash expenses, sales, advances and wage settlements; this is not a complete accounting ledger with all asset/liability workflows.
- Restore checks basic structure and journal balancing but does not perform comprehensive relational/schema validation. Preserve external backups.
- No immutable audit trail against users modifying browser storage; no deletion/editing workflows.
- Hosting is public on GitHub Pages; farm data is **not** uploaded to GitHub unless you manually commit backups. Do not commit private backups or credentials.

## Validation

`node --check app.js` checks JavaScript syntax. Manually test in Chrome, Firefox and mobile browsers before relying on any calculations. Keep an independent accounting record.
