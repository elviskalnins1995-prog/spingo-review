SpinGo Photo Review v11

Main change:
The OCR regions are no longer tied to the full phone photograph.

Pipeline:
1. Detect a large poker/application window in the photo.
2. Crop it.
3. Normalize the crop to 1200x760.
4. Read cards, title/blinds, stacks, bets, pot and dealer button from normalized coordinates.
5. Use multiple threshold passes and majority voting.
6. Do not guess fields that fail confidence checks.

Calibrated for the classic white 2-colour card style shown in the supplied reference photo.

Important:
- OpenCV.js and Tesseract.js are loaded from HTTPS CDNs, so the GitHub Pages site needs internet access.
- This is a browser-side heuristic reader, not a trained custom computer-vision model.
- If a field cannot be read reliably, v11 leaves it for manual correction instead of fabricating a value.
- Intended for completed-hand / training review.
