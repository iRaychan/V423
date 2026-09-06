# KeySuite V4.23.04 FULL CLEAN

V4.23.04 completes BFI PDF engineering data/dimensions and repairs Product > CHC > Curve routing.

## BFI PDF

- Casing / Impeller / Shaft: Stainless Steel 304.
- Suction and discharge are shown independently.
- Motor efficiency class: IE2.
- Page 2: L = maximum L1-L6; W = maximum Dimension-sheet W/B1/B2; H = maximum Dimension-sheet H/H2/H.
- Page 3: supplied BFI dimension drawing is selected by BFI family and blank dimension rows are omitted.

## Product

- Product > CHC > Curve now has shared-runtime and native fallback routing for CHC C4/C6.

## Deployment

No database migration is required. Deploy the web build, then redeploy the `telegram-webhook` function for the matching KeyBot PDF output.
