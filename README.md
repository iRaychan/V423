# KeySuite V4.23.05 FULL CLEAN

V4.23.05 aligns BFI Product/Curve behavior with CHC and completes the requested BFI PDF/UI consistency changes.

## V4.23.05

- Product > BFI model rows now use the same row layout as CHC: model + Curve / Assembly / Quote on one row.
- Product > BFI > Curve now uses the same shared inline Product Curve route as CHC instead of the old BFI popup dialog path.
- BFI PDF Page 2 Type is HMS Pump.
- BFI PDF Page 3 family drawing is rendered at 80% of the previous size while retaining the supplied family-specific drawing mapping.
- BFI Currency & Multipliers is now an expandable/collapsible Price List panel, matching the global Price List pattern.
- BFI now supports the Enhanced tick in Dashboard Quick Selection Brand / Series Settings, with the Enhanced state passed end-to-end into BFI selection and selected-model opening.
- BFI Enhanced results are identified the same way as CHC Enhanced results.
- BFI product phase selection is preserved when opening an exact product curve.
- KeyBot/Telegram BFI PDF receives the same HMS Pump and 80% Page 3 drawing updates.

## Deployment

- No database migration is included.
- Deploy/overwrite the GitHub Pages web files.
- Redeploy `telegram-webhook` because `curve-pdf.ts` changed.
