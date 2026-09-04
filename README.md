# KeySuite V4.23.01 FULL CLEAN

V4.23.01 is a clean full package rolled forward from the verified V4.22.11 state.

## Included current state

- CHC C4 / C6 generation handling and Product/Quick Selection assignment rules retained.
- Selling Brand / Selling Sub Series handling retained for customer-facing Product, curve and PDF output.
- O.K.Pump C4 customer-facing naming uses VMS / VMSS / VMSN while CHC / CHCS / CHCN remain internal hydraulic identities.
- CHC / CHCS / CHCN PDF filename material mapping retained.
- C4 generation-aware Product curve routing/stability fixes retained.
- CHC C4/G1 Price List V1.2 master retained with 412 price models.
- Existing user-entered C4/G1 prices are not overwritten by source workbook zero values.

## Supabase migration normalization

The V4.22.11 pricelist migrations are included with the exact timestamp names already applied to the linked Supabase project:

- `20260904125637_v42211_chc_g1_pricelist_v12.sql`
- `20260904125639_v42211_verify_chc_g1_pricelist_v12.sql`

The KeyPLC migration already present in the full package remains:

- `20260901213000_v42113_keyplc_3kw_37kw.sql`

V4.23.01 itself does not add a new database migration. If the V4.22.11 migration was already pushed successfully, no additional `db push` is required just for the V4.23.01 version roll-forward.

## Full Clean packaging

Historical per-version README / upgrade-note files were removed from this Full Clean package. Production code, selector engines, assets, Supabase functions and database files are retained.

## V4.23.01
- Removed the special MOS → Motor hard-code from Role Brand / Series Assigned, Customer Brand / Series pricing, and Product navigation.
- MOS now follows the same saved Brand / Series master mapping as other selling brands. Motor will appear under MOS only when a real MOTOR mapping exists.
- No Supabase migration is required for this release.
