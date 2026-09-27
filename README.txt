SpinGo Photo Review v18

Critical fixes from the v17 screenshot:
1. v17 could remain on ANALIZĒJU because card OCR was awaited without a hard timeout.
2. v17 calculated the action before Hero/position/blinds/bets had been populated.

v18:
- card OCR is limited to ONE pass per card;
- each card has a 3.5-second hard timeout;
- the app always continues and completes even if card OCR fails;
- diagnostics updates during card reading;
- recommendation is calculated only AFTER all detected situation fields are assigned;
- if cards fail, result becomes PĀRBAUDI HANDU instead of hanging on ANALIZĒJU.

The already-correct table geometry remains unchanged.
