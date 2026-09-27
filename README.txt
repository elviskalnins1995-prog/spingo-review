SpinGo Photo Review v15

Based on the v14 test screenshot:
WORKING: poker-window crop, 3-max, BTN, Hero 300, opponents 290/280,
10/20, next 15/30, pot 30, posts 10/20.
BROKEN IN v14: Hero hand was blank although K♠ J♥ is clearly visible.

Root cause addressed:
v14 cropped a fixed fraction of each card and could cut through the rank glyph.
v15 takes a larger full-card region, finds the dark/red printed ink inside the
upper-left quadrant, builds a rank crop from the actual pixels, and then OCRs that
crop with multiple segmentation modes plus 8 threshold passes.

v15 no longer blanks a rank just because consensus is imperfect; it reports low
confidence instead. Different red/black card colors yield offsuit automatically.

Reference target: KJo.
For completed-hand/training review.
