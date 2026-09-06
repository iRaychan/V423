# KeySuite V4.23.11 FULL CLEAN

V4.23.11 fixes BFI source-price diagnosis/resolution and aligns the BFI Currency & Multipliers controls.

## V4.23.11

- BFI T/E identities normalize to the base product and use the 3 Phase price bucket.
- If a BFI source price exists but its currency is not enabled in the customer BFI Category Pricing rule, KeySuite now says so instead of falsely reporting that no source price exists.
- BFI Price List Currency Selection, USD → MYR and RMB → MYR labels align on one row, with their select/input controls aligned on one row below.
- No database migration is required for V4.23.11.
- No Telegram/KeyBot function redeploy is required for V4.23.11.
