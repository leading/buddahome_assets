# Local arrangement UI review — 2026-09-27

Source code baseline: 4221635 with a scoped select-all repair.
Device: iPhone 17 Pro simulator, 402 × 874 pt; complete React Native controls with the shared Three.js WebView comparison renderer on isolated Metro 8083. Physical iPhone remains on native Expo GL / Metro 8081.

01 entry, 02 local arrangement, 03 local select-all, 04 collapsed card, 05 whole-scene comparison, 06 return with card and selection preserved, 07 moved expanded card, 08 exit local. Images prefixed 00 are connection diagnostics, not acceptance evidence.

The existing simulator draft was restored for observation only. Object transforms and saved scene were not changed. UI states are driven through actual React callbacks; they do not establish physical finger latency or native GPU performance.

Native iPhone callback checks independently cover fruit plate, flower vase, nested group, global select-all and clear selection. Original scene, saved record and draft remain unchanged.

Images are published first and inspected through immutable GitHub HTTPS URLs. No image base64 is sent to the chat.
