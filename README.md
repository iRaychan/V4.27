# KeySuite V4.27.01 FULL CLEAN

Baseline: V4.26.11.

Changes:
- KeyBot accepts an exact pump model followed by a duty point and plots that entered duty on the specified model curve.
- Duty text preserves the user's entered flow unit and shows the converted m3/hr value in brackets, for example `1663 Lpm (99.8 m3/hr) @ 45 mtr`.
- Brand, series and pump-type routing recognizes B.G.Reich, MOS/M.O.S, OK/O.K.Pump, CHC/VMS/SVM and BFI/HMS without treating the Brand as a Customer name.
- A duty without a Brand searches the pump series assigned to the user; Brand or series input restricts the search to that scope.
- KeySuite BFI and KeyBot prioritize models with a filled pricelist value. Unpriced models are shown as Cold Item only when no priced suitable model is available.
- OEM PDF windows now wait for the assigned Brand name and logo to finish loading before becoming visible or opening Print, eliminating the B.G.Reich logo flash and refresh requirement.

No new Supabase database migration is required.

Deployment order:
1. Upload/deploy the V4.27.01 web files.
2. Redeploy the `telegram-webhook` Edge Function.
