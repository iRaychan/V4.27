# KeySuite V4.26.09 FULL CLEAN

Baseline: V4.26.08.

Changes:
- Exact BFI model plus duty input keeps the exact hydraulic model and plots the entered duty point on its generated curve.
- Bare Flow @ Head searches all curve-enabled Brand / Series assigned to the KeySuite user.
- Broad assigned-product results keep only Common models with an input price and the closest suitable model per Brand / Series.
- KeyBot accepts `MOS`, `Mos`, and `M.O.S` for the configured M.O.S brand, and `OK`, `OK Pump`, and `O.K.Pump` for O.K.Pump.
- PDF page 2 shows OEM CHC-family products as VMS Pump and TESK products as SVM Pump instead of exposing the internal CHC generation.
- PDF Pump Speed comes from hydraulic data and Motor Speed comes independently from motor master data; both are shown in rpm only while Frequency remains a separate Hz field.

No new Supabase database migration is required.

Deployment order:
1. Upload/deploy the V4.26.09 web files.
2. Redeploy the `telegram-webhook` Edge Function.
