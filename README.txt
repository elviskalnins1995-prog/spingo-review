SpinGo Photo Review v12

Fixes based on the user's v11 screenshot:
- v11 was not actually isolating the poker client; the normalized canvas still contained most of the phone photograph.
- v12 detects a large dark poker-client rectangle and scores candidates by dark-content fraction.
- Aspect-ratio acceptance is widened for photographed/windowed clients.
- JS fallback now searches dark horizontal/vertical bands instead of percentile bounds.
- Classic white-card rank ROIs are tightened to the upper-left rank glyphs.
- Current blind parser tolerates OCR variants of 'Blinds 10 | 20'.
- If the detected crop is nearly the whole photo, v12 warns instead of silently treating it as a good crop.

Reference target from the supplied classic-deck photo:
K♠ J♥, 3-max, BTN, Hero 300, opponents 290/280, current blinds 10/20,
next blinds 15/30, pot 30, posted bets 10/20.

This remains browser-side heuristic CV/OCR, not a trained custom vision model.
For completed-hand/training review.
