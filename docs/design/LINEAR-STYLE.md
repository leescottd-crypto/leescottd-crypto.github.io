# Multi-asset dashboard visual refresh · October 2, 2026

Applies the user-approved Hexxy / Linear-inspired styling to `/dashboard/` in the GitHub Pages repository. Keeps the Multi-Asset dashboard identity, data, calculations, asset list, four key moving averages and existing workflows.

## Design

Locally bundled Inter, compact type, charcoal/neutral light surfaces, thin dividers, rounded controls and outlined panels. Yellow `#FFC83D` accents, charcoal foreground on yellow, golden light-theme focus/text for contrast. Green/red retain financial state meaning; chart-series colors remain distinct and labelled. No Hexxy rebranding of the dashboard.

`dashboard/linear.css` contains semantic tokens and the shared styling adaptation. `dashboard/src/theme.js` handles theme persistence and chart appearance; the initial head script avoids a theme flash. Theme changes update existing chart options without changing the asset, range or data. SVG chart backgrounds and text follow theme tokens. A dashboard-scoped reserve chart module preserves the root application's existing presentation.

## Scope

The target site is `https://leescottd-crypto.github.io/dashboard/`, served by `leescottd-crypto/leescottd-crypto.github.io`, branch main. Other local desktop, iPhone and Sites variants were not modified. Market-data files and financial calculations are unchanged. This is a styling update, not a fresh-data fetch; the existing main snapshot is September 29, 2026, and older individual observation dates remain visible.

## Verification

- JavaScript syntax checks passed for app, theme and reserve modules; git diff whitespace checks passed.
- Browser inspected both themes at 1440, 1024 and 390px, without page-level horizontal overflow. Dense chart/tab/data areas retain internal scrolling.
- All 11 assets and four chart tabs opened. All seven macro tabs opened.
- Price/chart backgrounds and reserve comparison adapt to both themes. Theme persistence and selected chart controls were checked in the browser.
- Console inspected with no errors or warnings returned. Existing JSON export handler preserved and source-reviewed; browser download completion was not confirmed.
- Browser checks are recorded in evidence/browser-evidence.json and paired screenshots. These checks do not constitute an exhaustive financial-model or accessibility audit.

## Run and rollback

Run `python3 -m http.server 5182 --bind 127.0.0.1` from the repository root and open `/dashboard/`. GitHub Pages serves static files directly; no npm build is required. Roll back by reverting the styling commit; do not roll back market-data files or alter the separate upstream dashboards.
