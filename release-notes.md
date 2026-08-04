# BlurCut - Video Censor Editor — Release Notes

---

## Version 1.0.2 (Testing / Internal)

Stability and parity update for tracking/export workflows.

- Automatic Censoring now includes optional Post AI Analysis for on-device tracking refinement
- Post AI Analysis can augment baseline detections and improve subject continuity in difficult sections
- Export reuses saved tracking analysis cache when source/trim/settings match
- Export skips face-analysis phase when cache is valid (faster repeat exports)
- Export pre-gap behavior aligned with preview (full forward scan inside pre-gap window)
- Export post-gap now honors configured gap value from Tracking settings
- Improved tracking object ON/OFF parity for export
- Fixed export completion handling when output file was deleted externally
- Fixed timeline labels with dynamic time formatting (`50s`, `1:05`, `01:02:03`)
- Improved export dialog/progress text contrast in dark mode
- CPU tracked export overlay fixed to avoid frame accumulation artifacts

---

## Version 1.0 (Initial Release)

First public release of BlurCut.

- Automatic face censoring with on-device ML Kit face detection
- Optional on-device Post AI Analysis to refine automatic censor tracking after baseline detection
- Manual tracking: draw a censor box on any region and it follows it through the clip
- Censor modes: blur and pixelate
- Adjustable censor intensity, size, and shape (box or oval)
- VHS effect with scanlines, chromatic aberration, and controllable roll band (roll speed and roll position sliders)
- Glitch effect with band travel and wobble controls
- Film Grain, Shadow, Dream, B&W, Sepia, Inverse filters
- Cinematic colour grading with multiple looks
- Brightness and contrast adjustment
- Rotate and flip video in any direction
- Trim to select the exact segment you want
- Crop to reframe the shot
- Text overlays with custom fonts, colours, outlines, and shadows
- Emoji overlays with sizing and timing
- Sticker overlays (import your own images)
- All overlays support custom start and end times
- Full-quality export to device gallery using Media3 Transformer
- No watermark, no subscription, no account required
- All processing — including AI face detection and optional Post AI Analysis — runs entirely on-device
