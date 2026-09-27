SpinGo Photo Review v22

AUDIT FIX:
v21 still had a serious mobile performance issue. Its Promise timeouts did not cancel
the Tesseract.recognize calls already running in the background. A single photo could
launch dozens of OCR recognitions.

v22:
- creates ONE reusable Tesseract worker;
- runs ONE OCR pass per normal field, sequentially;
- uses only TWO targeted OCR attempts per card;
- no Promise.all OCR fan-out;
- no orphaned OCR jobs from timeout races;
- Hero hand remains the only manually editable field;
- JS syntax verified with node --check;
- checked that old voteOCR/Promise.all fan-out is absent.

Note: this is a static/code-path audit. Browser OCR accuracy still depends on the actual
photo and device; no claim is made that a browser-only OCR model is a full vision model.
