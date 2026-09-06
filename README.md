# KeySuite V4.23.10 FULL CLEAN

V4.23.10 adds BFI to Customer Brand / Series authorization and removes the Coupling Type placeholder from KeyBot CHC/BFI PDF Page 2.

## V4.23.10

- Customer → Brand / Series Price Preference now lists **BFI** under **B.G.Reich**, alongside CHC C4, CHC C6, End Suction and Motor.
- B.G.Reich brand-level **All Series** now includes BFI, and BFI can still be enabled/disabled individually.
- BFI Customer authorization uses the same saved Price + Selection preference keys as the global Product / Quick Selection authority flow.
- Non-master brands mapped to BFI now use the correct BFI authorization family instead of being treated as CHC.
- KeyBot PDF Page 2 removes **Coupling Type** completely for CHC and BFI; the Length row remains, with the right-hand coupling cells empty. ES keeps `Coupling Type · Flexible`.
- No database migration is required for V4.23.10.
- Because `telegram-webhook/curve-pdf.ts` changed, redeploy the `telegram-webhook` Supabase Edge Function after updating the files.
