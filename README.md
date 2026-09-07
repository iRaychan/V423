# KeySuite V4.23.14 FULL CLEAN

V4.23.14 makes BFI Product Assembly enter the complete System flow directly, matching CHC.

## V4.23.14

- Product > BFI > Assembly now routes directly to the System builder.
- Default BFI System starts with 2 pumps (1 Duty + 1 On Demand).
- The KeyPLC control panel is auto-selected at Qty 1 from the BFI motor rating and pump quantity.
- The manifold is auto-selected at Qty 1 from the BFI suction/discharge connection size and pump quantity.
- The GWS tank is auto-selected at Qty 1 from BFI series and shut-off head.
- BFI threaded connections are translated to the DN sizes used by the shared System sizing engine.
- BFI base / T / E model identity is retained in the System BOM.
- No database migration is required for V4.23.14.
- No Telegram/KeyBot function change is required for V4.23.14.
