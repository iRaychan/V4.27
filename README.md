# KeySuite V4.27.03 FULL CLEAN

Baseline: V4.27.02.

Changes:
- Quick Pump Selection adds a **Cold Item** checkbox beside **Check Pumps**.
- With Cold Item unticked, models with a filled price remain the priority and unpriced alternatives stay hidden when priced models are available.
- With Cold Item ticked, suitable unpriced CHC C4/C6, BFI and ES models are included and labelled **Cold Item**.
- KeyBot first shows priced recommended and alternative models, followed by a **Cold Item** button.
- Pressing **Cold Item** opens the suitable unpriced-model list without rerunning the duty selection.
- A selected cold model keeps its **Cold Item** status through the model summary and curve generation.

No Supabase database migration is required. The `telegram-webhook` Edge Function must be redeployed for the KeyBot changes.

Deployment:
1. Upload/deploy the V4.27.03 web files.
2. Link Supabase project `skidqdixnnnuhvarekxp` and deploy the `telegram-webhook` function.
