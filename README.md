# KeySuite V4.23.12 FULL CLEAN

V4.23.12 makes KeyBot confirm BFI motor phase before finalising an exact BFI model identity.

## V4.23.12

- Direct BFI model requests now ask **1 Phase / 3 Phase** before the model is finalised.
- 1 Phase resolves to the base model with no suffix, for example `BFI 10-3`.
- 3 Phase resolves to the `T` suffix model, for example `BFI 10-3T`.
- If an Enhanced BFI request is explicitly carried into the phase step, Enhanced remains 3 Phase only and resolves to the `E` suffix.
- The same phase-confirmation rule is used for KeyBot Product exact-model selection and direct BFI price requests.
- No database migration is required for V4.23.12.
- `telegram-webhook` must be redeployed because KeyBot routing changed.
