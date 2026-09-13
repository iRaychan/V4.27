# KeySuite V4.26.11 FULL CLEAN

Baseline: V4.26.10.

Changes:
- CHC and BFI pump prices now respond to motor IE-class changes.
- Formula: pump quoted price minus the included motor raw cost, plus the replacement motor quoted price.
- Included motor defaults: CHC C4 IE2; CHC C6 IE3; BFI 1-phase IE1; BFI 3-phase IE2.
- Motor matching uses the same pole and closest priced HP, preferring the higher HP when equally close.
- BFI 3-phase selection now allows IE2, IE3, IE4 and IE5. BFI 1-phase remains IE1.
- KeyBot no longer resets an explicitly selected BFI motor class to its phase default.
- KeyBot accepts Product details first, one blank row, then the Customer name.
- `BG` resolves to B.G.Reich; standalone `OK` and `M.O.S` are treated as Brand aliases before Customer matching.

No new Supabase database migration is required.

Deployment order:
1. Upload/deploy the V4.26.11 web files.
2. Redeploy the `telegram-webhook` Edge Function.
