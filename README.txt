SpinGo Photo Review v14

Built from the v13 test result:
Correct in v13: 3-max, BTN, Hero 300, opponents 290/280, blinds 10/20,
next 15/30, pot 30 and left blind 10.
Remaining observed error: K♠ J♥ was read as 7J.

v14 focuses only on card recognition:
- larger classic-card rank crop;
- seven threshold passes;
- removed the unsafe I/L -> J substitution;
- rejects weak one-off OCR guesses;
- adds glyph geometry as a K-vs-7 cross-check for the observed deck font;
- detects red vs black separately;
- when card colors differ, automatically appends 'o' (offsuit);
- when both cards have the same red/black class, v14 does NOT falsely assume suited,
  because hearts/diamonds and spades/clubs still require exact suit-symbol recognition.

Reference target for supplied image: KJo.
For completed-hand/training review.
