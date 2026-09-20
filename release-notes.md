# BlurCut - Video Censor Editor — Release Notes

---

## Version 1.0.3 (Multi-Video Timeline Streams)

Multi-video timeline stream support, seamless multi-clip preview, and single-stream export.

**Multi-Video Streams & Editing**
- Added Top Bar append button (`+`) to quickly add additional video clips into a continuous timeline stream
- Multi-clip timeline rendering with high-contrast boundary separators
- Seamless ExoPlayer multi-item playback across clip transitions
- Inspector-based clip management displaying clip resolution, duration, and metadata
- Conditional **Delete Clip** button in Inspector (visible when 2 or more clips are present), shifting subsequent timeline items cleanly
- Dynamic full-duration effect adaptation: filters, color grades, and full-span FX automatically stretch to match the combined duration
- Safe auto-censor invalidation: adding or deleting clips resets tracking caches cleanly to allow accurate re-tracking

**Export**
- Multi-clip concatenation into a single high-quality MP4 export via Media3 Transformer `EditedMediaItemSequence`
- Per-clip trim and clipping configurations with segment-local effect shifting

---


Editor navigation rework, censor rendering fixes, and export stability.

**Export**
- Fixed exports hanging near completion on sources with no audio track: the composition declared an audio track the source did not have, so Media3 synthesised a silent track that never ended and the muxer never received end-of-stream
- Same fault also affected every export with "suppress audio" enabled, on any source
- Stalled exports now fail in ~30s instead of hanging; a truncated/corrupt source no longer blocks the pipeline indefinitely
- Transformer now runs on its own Looper so UI work cannot starve the export pipeline
- Debug builds record a Media3 pipeline trace and log it if export progress stops advancing for 30s

**Censoring**
- Fixed manual censor tracks rendering as a grid of blocks on export: they fell back to a legacy 9-tap kernel with `radius/4` sample spacing instead of the separable two-pass Gaussian used by automatic tracking
- Manual censor start frame can now be moved earlier — scrubbing before the first keyframe keeps the box visible so it can be dropped there, becoming the new start
- Manual keyframes are stored sorted by time
- Larger manual keyframe rows and delete buttons

**Editor navigation**
- Edit, Insert, Effects, Censor/Tracking, Audio, Filters, Colors, Special FX, Help and Export are now real full-screen pages instead of overlays nested inside the player container, where they could never cover the screen
- Page headers share the Help page style: back arrow plus 24sp title
- System back button pops the open page instead of prompting to close the project
- Rename and delete project confirmations restored to modal dialogs

**Watermarks and Pro**
- Free exports of 20.5s or shorter skip the diagonal censor watermark
- Corner watermark scales proportionally at every export resolution; size clamps that inflated it on sub-720p exports removed
- Corner watermark enlarged to 7.5% of the frame short side and uses "BlurCut" brand casing
- Editor Pro button opens the same upgrade page as the Projects Hub, with Pro benefits and the free watermark allowance documented on it

**Other**
- Timeline time/frame label updates live during playback instead of only on pause
- Text outline renders as a true centred glyph stroke instead of stamped offset copies
- Text shadow and outline default to visible amounts
- Help docs reworded from "modal" to "page" across all 10 locales

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
