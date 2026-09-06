# KeySuite V4.23.08 FULL CLEAN

V4.23.08 completes the pending Enhanced/phase and BFI Category-pricing corrections on top of V4.23.07.

## V4.23.08
- BFI Enhanced is available for 3 Phase only.
  - Standard 1 Phase: `BFI 10-3` -> IE1 data.
  - Standard 3 Phase: `BFI 10-3T` -> IE2 data.
  - Enhanced 3 Phase: `BFI 10-3E` -> IE2 data + Enhanced curve.
  - Selecting 1 Phase automatically disables/unticks Enhanced.
- BFI Product/Selector/quotation identity carries the `E` / `T` / base suffix consistently. KeyBot direct-model handling and BFI curve PDF also recognize the `E` identity.
- Product > CHC C4 > Curve now exposes the Enhanced tick like CHC C6, and the C4 Product selector can enter the existing C4 Enhanced hydraulic mode. Quick Selection Brand / Series Settings also treats CHC C4 and C6 as Enhanced-capable.
- BFI pricing-category save no longer falls through to the legacy category RPC that rejects BFI. Category Compare uses the same BFI-safe save RPC.
- Removed the misleading blanket `Run V41511_CATEGORY_CURRENCY_SELECTION.sql first` error suffix; the actual database error is shown.
- Existing V4.23.07 exact-model auto-duty rule remains: automatic Head is floored to a whole metre while manually entered duty points are unchanged.

## Deployment
This release includes a new Supabase migration. After replacing the web files, run:

```powershell
npx.cmd supabase db push
npx.cmd supabase functions deploy telegram-webhook
```

Then deploy/update GitHub Pages and hard-refresh KeySuite.
