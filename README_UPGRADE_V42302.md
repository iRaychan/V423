# KeySuite V4.23.02 Upgrade

Upgrade target: V4.23.01 → V4.23.02.

This patch adds B.G.Reich BFI globally while leaving CHC C4/C6 independent and unchanged.

## Required deployment
1. Copy all files/folders from this upgrade package over the existing KeySuite deployment.
2. From the project root run `supabase db push`.
3. Deploy the updated Telegram webhook / Supabase functions using your normal KeySuite deployment command.
4. Refresh KeySuite so the V4.23.02 service-worker cache replaces V4.23.01.

## Database migration
`supabase/migrations/20260906160000_v42302_bfi_global.sql`

The migration creates BFI pricing/settings/RPC support and seeds 63 BFI product SKUs using the supplied V1.0 source prices (currently 0.00).

## Telegram / KeyBot deployment dependency fix
This upgrade package includes the complete local dependency closure required by `supabase functions deploy telegram-webhook`, including unchanged CHC C4/C6, ES, motor/baseplate, dimensions and report-assets files. This allows the V4.23.02 upgrade to be deployed from a clean extracted upgrade folder without missing-module bundling errors.
