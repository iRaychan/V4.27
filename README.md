# KeySuite V4.27.02 FULL CLEAN

Baseline: V4.27.01.

Changes:
- OEM PDF popup pages now contain the assigned Brand name and logo before their first visible render.
- ES exports, including VEC and other assigned OEM Brands, no longer show the native B.G.Reich logo briefly before changing.
- Page 1, Page 2 and Page 3 Brand-logo elements are rewritten before `document.write()` completes.
- The pre-render OEM rewrite survives popup `document.open()` document resets.
- Printing still waits for the final Brand image and fonts to finish loading.

This is a web-only upgrade. No Supabase database push or Edge Function deployment is required.

Deployment:
1. Upload/deploy the V4.27.02 web files.
