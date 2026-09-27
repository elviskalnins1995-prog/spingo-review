SpinGo Photo Review v9

v9 is calibrated around the supplied OlyBet/GG four-colour screenshot layout.

Fixes:
- Hero cards use separate tight OCR regions.
- Dealer position uses yellow-pixel detection around the D button instead of text OCR alone.
- Empty third seat is used to distinguish heads-up from 3-max.
- Current blinds are reconstructed from visible posted chips / call amount.
- 'Next Blinds' is parsed separately and never used as current blinds.
- Stack, pot and posted-bet regions are OCR'd separately.
- Debug view draws the exact regions used by the detector.

For completed-hand/training review.
