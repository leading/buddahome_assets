# Homepage ritual interactions — 2026-09-27

Complete React Native UI on an isolated iPhone 17 Pro simulator clone (402 × 874 pt), using the shared Three.js WebView comparison renderer. The actual phone remains on native Expo GL. The clone uses a guest scene copy; no production scene or account was changed by these interaction checks.

## Current captures: -v2.jpg

The first PNG review (commit 8783d59) exposed the general Tools button covering Stop. The revised images hide general Tools during cup selection/pouring, center the status control, and use smaller action popovers below ordinary objects. Teapot selection hints stay above to keep cups available. German mixed actions share a compact row. Original PNGs remain in that earlier commit.

## Captures

- 01–02: light and extinguish a candle through its holder.
- 03–04: clear a cup and display the resulting empty-cup state.
- 05–06: select a teapot, highlight eligible scene cups, and retain cup-selection mode while orbiting.
- 07: tea-pouring interaction and stop control.
- 08–09: editing has no ritual actions; structural ash fill remains available.
- 10: German mixed-incense actions.

Capture files are bound to SHA-256 hashes in image-manifest.json. These are native controls and the shared renderer, not standalone mockups. DOM PointerEvents and native control callbacks drove the flow; this is not physical finger-latency measurement. Grey Expo controls are development overlays.

## Validation

See verification.json for actual event replay, conservative transfer, periodic durable tea saves, clean editor history/drafts, unchanged arrangement/camera, and repeated highlight resource counts. Draw-completion timings describe this simulator WebView only, not physical iPhone GPU time.

Images are published to the authorized GitHub repository before HTTPS visual review. No image base64 is sent to the chat. The accepted states 01–10 have been reviewed through their immutable HTTPS images. Stop is unobstructed, ordinary actions sit below the hit, teapot hints keep the cup row clear, and editing contains no ritual controls. The setup-only 00 capture is excluded from acceptance.

Source implementation: 4fe89ee; final navigation compatibility: 5c959578dfb5ea05f4eba8cd77f20df57f04091f. Native type checks, workspace type checks (8/8), workspace lint (9/9), and formatting passed. Supplemental checks explicitly distinguish diagnostics, simulator UI, and non-mutating physical-device checks.
