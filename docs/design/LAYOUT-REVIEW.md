# Dashboard alignment review — October 2, 2026

The research readout had a full-width label column beside a 148px value/context column, separating related content and forcing excessive wrapping. It now uses semantic grouped definition rows with proportional columns, left-aligned values and readable context. Research and source notes share two desktop columns and stack below 1100px.

The site review also corrected fixed-width asset ticker tracks that overlapped enlarged cards; cycles now wrap or stack; metric notes have consistent two-column desktop and one-column phone layouts; macro interpretations use a single reading column within each card; holders span one column with local table scrolling; annual M2 cells wrap; headings and fiscal row labels can wrap without pushing values out of alignment.

Verification: 88 layout cases covering four chart tabs and seven macro tabs, light/dark, and 1920/1440/1024/390px. No page-level horizontal overflow or clipped paragraphs, headings, definition terms/values, or asset buttons in the DOM geometry audit. Intentional chart/table scroll areas remain. Research desktop/mobile and fiscal desktop were visually inspected. Console returned no errors/warnings. Financial data and calculations were not changed.
