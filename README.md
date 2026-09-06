# KeySuite V4.23.03 FULL CLEAN

V4.23.03 standardises the BFI selector display to the CHC master selector style.

## V4.23.03 — BFI / CHC display consistency
- BFI Selection now uses the CHC selector as the master visual shell.
- Same header, spacing, typography, cards, duty-point input layout and result hierarchy.
- Same Required Duty / Multiple Duty Points / Operating Speed / Motor controls.
- Same Display Settings, parallel-curve controls, system-curve and orifice sections.
- Same selection hero, summary KPI cards, large Head curve plus Efficiency / Power / NPSHr side curves.
- Same Alternative Models card treatment and responsive/mobile behaviour.
- BFI remains hydraulically independent: its 63-model master data and BFI curve engine are unchanged.
- No database migration is required for V4.23.03.
- No Supabase Edge Function redeploy is required for this UI-only release.

## Existing V4.23.02 BFI database
The V4.23.02 BFI migration and database RPCs remain unchanged and should not be pushed again.

---

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

The V4.23.02 migration is `supabase/migrations/20260906160000_v42302_bfi_global.sql`.
It creates the independent BFI price table/RPCs, settings multipliers, BFI product-group mapping and seeds all 63 supplied BFI SKUs.

## Source workbooks
- `004 - BFI - 260905 - V1.0.xlsx`
- `010 - BFI - (Pricelist) - 260906 - V1.0.xlsx`

Source BFI prices are preserved exactly as supplied. Current V1.0 MYR/USD/RMB values are 0.00 and therefore remain non-quotable until prices are entered in Key → Price List → BFI.

### V4.23.02 BFI exact-model curve correction
- Exact BFI model curve generation now resolves the BFI rated point through the BFI hydraulic engine instead of the CHC resolver.
- BFI duty-point Fast Search now remains scoped to the BFI product group.
- No additional database migration is required for this correction; redeploy `telegram-webhook`.
