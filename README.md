# KeySuite V4.23.09 FULL CLEAN

V4.23.09 fixes Product > Curve Enhanced state continuity for CHC C4/C6 and the live Enhanced model identity for BFI.

## V4.23.09

- BFI Product curve now updates the visible model identity immediately when Enhanced is toggled: standard 3Ph `T` becomes Enhanced `E` (for example `BFI 10-3T` → `BFI 10-3E`).
- CHC C6 Product curve keeps the exact Product model when switching from the standard Product selector to the Enhanced selector.
- CHC C4 Product curve now uses the C4 Enhanced selector and keeps the exact Product model/duty point when Enhanced is toggled.
- Product curve runtime re-arms the exact model whenever an iframe document is replaced during an Enhanced/Standard switch, preventing the empty `Enter Required Duty Flow and Head` state.
- No database migration and no Supabase function deployment are required for V4.23.09.
