# ADX Broadway 2027 Returning Registrant Page — Claude Rules

## DO NOT CHANGE unless explicitly asked:
- The "Additional deposits required" line must NOT appear in the step 1/2 live estimate payRows (calcAndRender). It was intentionally removed.
- "Deposits already paid" shows in green as negative
- Modal message color is gold (var(--gold))
- Confirmation label is "All Deposits Made"
- "Monthly payments begin July 1" copy is correct as-is
- Single button flow — no Option A/B choice cards

## Current architecture:
- Option A (addlDepositTotal > 0): backend uses mode:payment
- Option B (addlDepositTotal === 0): backend uses mode:setup
- Subscription schedule created in webhook after payment
