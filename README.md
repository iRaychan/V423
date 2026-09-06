# KeySuite V4.23.02 FULL CLEAN

V4.23.02 adds B.G.Reich BFI as a global hydraulic pump family, independent from CHC C4/C6.

## BFI scope
- Product and Quick Selection integration
- CHC-style BFI hydraulic selection and curve presentation
- Head, efficiency, shaft power and NPSHr curves
- BFI model technical data, dimensions, 1Ph/3Ph availability and reduced-impeller handling
- Brand/Series role and customer assignment support
- Category pricing and independent MYR/USD/RMB BFI price list
- Quotation and Assembly routing
- KeyBot / Telegram direct model, duty selection and curve PDF support

## Supabase
Run the new migration after deploying the files:

`supabase db push`

The V4.23.02 migration is `supabase/migrations/V42302_BFI_GLOBAL.sql`.
It creates the independent BFI price table/RPCs, settings multipliers, BFI product-group mapping and seeds all 63 supplied BFI SKUs.

## Source workbooks
- `004 - BFI - 260905 - V1.0.xlsx`
- `010 - BFI - (Pricelist) - 260906 - V1.0.xlsx`

Source BFI prices are preserved exactly as supplied. Current V1.0 MYR/USD/RMB values are 0.00 and therefore remain non-quotable until prices are entered in Key → Price List → BFI.
