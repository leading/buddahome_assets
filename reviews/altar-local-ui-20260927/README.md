# Local arrangement UI review — 2026-09-27

Source code baseline: 4221635 with a scoped select-all repair.
Device: iPhone 17 Pro simulator, 402 × 874 pt; complete React Native controls with the shared Three.js WebView comparison renderer on isolated Metro 8083. Physical iPhone remains on native Expo GL / Metro 8081.

01 entry, 02 local arrangement, 03 local select-all, 04 collapsed card, 05 whole-scene comparison, 06 return with card and selection preserved, 07 moved expanded card, 08 exit local. Images prefixed 00 are connection diagnostics, not acceptance evidence.

The existing simulator draft was restored for observation only. Object transforms and saved scene were not changed. UI states are driven through actual React callbacks; they do not establish physical finger latency or native GPU performance.

Native iPhone callback checks independently cover fruit plate, flower vase, nested group, global select-all and clear selection. Original scene, saved record and draft remain unchanged.

Images are published first and inspected through immutable GitHub HTTPS URLs. No image base64 is sent to the chat.

## HTTPS review outcome

Reviewed the published complete UI states through immutable GitHub HTTPS URLs. Default local framing keeps the plate visible between the local header and lower card; overview hides edit marks and the card; return preserves selection and collapsed state. A manually moved card may intentionally cover the object; camera auto-follow for card dragging was not introduced.

The German sample revealed a single trailing letter wrapping in the Move label. `09-german.jpg` is the before image; `09-german-v2.jpg` is the accepted fitted-label result, published in image commit `59b15c8f6a516f54afa2edd98aa92f70b4199b4e`. Full accessibility labels are preserved. The two-line local header remains clear of action icons. This is one language sample, not all-language approval.

Validation: native TypeScript, scoped lint and formatting, 27 existing numeric camera/surface/placement checks; actual iPhone callbacks exercise scoped/global select-all, clear selection and overview return. Physical-phone scene/saved/draft and simulator scene/draft/recovery records remain unchanged. Physical finger latency and all small-screen states remain outside this review.

Source repair and handoff commit: `27163cf` in the authorized BuddhaHome source repository.
