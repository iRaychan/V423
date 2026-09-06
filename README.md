# KeySuite V4.23.07 FULL CLEAN

V4.23.07 aligns Product curve Enhanced behavior and BFI motor phase identity.

## V4.23.07
- Product > CHC C6 > Curve now exposes Enhanced and switches the exact Product model into the CHC Enhanced hydraulic engine. Standard mode retains the Product impeller-adjustment editor.
- Product > BFI > Curve Enhanced now recalculates the exact BFI model instead of only changing the tick state.
- BFI model identity is phase-specific: no T = 1 Phase / IE1 data; T = 3 Phase / IE2 data.
- BFI Product, quotation payloads, selector display and PDF motor data follow the phase-specific naming/data rule.
- Exact-model Product auto duty keeps the design Flow and floors only the automatically generated Head to a whole metre (for example 13.4 m -> 13 m). Manual duty points are unchanged.
- CHC C4/C6 and BFI Product auto-duty Head use the same floor rule.

No database migration is required. The Telegram/KeyBot function changed for BFI phase-specific PDF/model handling and should be redeployed.
