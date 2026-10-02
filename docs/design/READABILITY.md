# Dashboard readability standard

Updated October 2, 2026 from the user request to favor legibility over density.

- Inter throughout; reading text 16px/1.6, labels and controls 14px/1.5, exhibit headings 20px, section headings 24px. Key values retain larger sizes.
- Replace inherited 8–13px declarations with a shared 14px label token. Chart canvas labels use 14px. Footnotes and injected market-size styles follow the same minimum.
- Put chart interpretations below the main chart, in two reading columns on desktop and one on mobile. Give macro exhibits two columns on desktop and one below 1100px. Stack mobile status summaries and fiscal-flow blocks.
- Preserve SVG view-box label size with internally scrollable charts on small screens; allow fiscal labels to wrap. No smaller mobile typography.
- Keep existing light/dark surfaces, yellow accents, data and model calculations.

Verification: all seven macro tabs opened in both themes at 1440, 1024 and 390px without page-level horizontal overflow. DOM text-size audit caught injected market-size styles and superscript references, which were corrected. Mobile status-summary grid was visually inspected and corrected to stack. Dense SVG charts and tables deliberately scroll within their exhibit. This is a readability check, not a full accessibility certification.
