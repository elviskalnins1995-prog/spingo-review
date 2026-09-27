SpinGo Photo Review v13

This revision is based on the user's v12 result screenshot.

What v12 proved:
- poker-client detection/cropping now works correctly;
- title/current blinds and Hero 300 can be read;
- dealer marker can be found.

What was wrong:
- opponent stack ROIs were vertically too high/low relative to the normalized client, so seat occupancy failed and 3-max was incorrectly classified as heads-up;
- card rank ROIs were too small, causing blank Hero hand.

v13 changes:
- recalibrated left/right stack, bet, pot, card, dealer and Hero-stack regions against the correctly cropped classic-deck client;
- card OCR now starts from the full card ROI and internally crops its upper-left rank corner;
- six threshold passes for each rank;
- opponent stacks are kept separate from posted blind amounts;
- 3-max requires two plausible opponent stack reads;
- missing ranks remain blank instead of being guessed.

Reference target:
K♠ J♥, 3-max, BTN, Hero 300, left 290, right 280,
current blinds 10/20, next 15/30, pot 30, posts 10/20.

Browser-side heuristic CV/OCR; not a trained custom vision model.
For completed-hand/training review.
