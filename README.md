# KeySuite V4.23.13 FULL CLEAN

V4.23.13 refines BFI KeyBot phase handling and aligns BFI quotation wording with the CHC quotation style.

## V4.23.13

- KeyBot BFI exact-model phase handling:
  - If both 1Ph and 3Ph are available, KeyBot asks the user to choose.
  - If only one phase is valid, KeyBot auto-selects it and continues without an unnecessary phase prompt.
  - BFI base / T / E identity remains: 1Ph = base, 3Ph = T, 3Ph Enhanced = E.
- KeySuite quotation:
  - CHC frequency displays 50Hz instead of 50.0Hz.
  - BFI uses CHC-style compact quotation wording.
  - Default BFI material/seal line: Material: SS304 / Mechanical Seal.
  - SiC/SiC: Material: SS304 / Mechanical Seal-SiC SiC Viton.
  - Removed separate BFI Motor, Impellers, Mechanical Seal and Maximum Operating Pressure description rows.
- No database migration is required for V4.23.13.
- Redeploy `telegram-webhook` because KeyBot phase routing changed.
