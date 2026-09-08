# KeySuite V4.25 Upgrade

Apply over V4.23.20.

## Changes
1. BFI USD/RMB multiplier save now updates only `ks_app_settings.id = default`, satisfying Supabase safe-update protection.
2. Price List Currency & Multipliers uses the shared 3-second hold-to-unlock behavior, including BFI.
3. BFI Price List price inputs now display the active source currency beside each 1 Phase / 3 Phase price, matching CHC style.
4. Quotation deletion now removes the quotation from both local quotation caches before/after the Supabase delete and refreshes secure history, preventing deleted quotations from being re-imported after page refresh.

## Deployment
Run `supabase db push` because V4.25 includes `20260908003500_v425_bfi_multiplier_safe_update.sql`.
No Telegram/KeyBot function redeploy is required.
