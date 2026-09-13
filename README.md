# KeySuite V4.26.10 FULL CLEAN

Baseline: V4.26.09.

Changes:
- Enhanced PDF page 2 shows `Max 3500 rpm` for both Pump Speed and Motor Speed. Frequency remains a separate field.
- Standard Pump Speed uses hydraulic curve rpm; Motor Speed uses motor-master rpm.
- KeyBot accepts `OK`, `O.K.`, `OKPump`, `OK Pump`, and `O.K.Pump` as O.K.Pump. Standalone `OK` starts a Brand-scoped duty request.
- `VMS` is a pump-type input. The output preserves the assigned selling series, including B.G.Reich `CHC` and M.O.S `MVC`.
- `MOS` plus `VMS 20-4` resolves to `M.O.S - MVC 20-4` with Type `VMS Pump`.
- `HMS` is the BFI pump-type alias for duty sizing and exact models, such as `HMS 20-3` resolving to `BFI 20-3`.
- PDF type labels use VMS Pump for CHC/MVC, SVM Pump for TESK, and HMS Pump for BFI.

No new Supabase database migration is required.

Deployment order:
1. Upload/deploy the V4.26.10 web files.
2. Redeploy the `telegram-webhook` Edge Function.
