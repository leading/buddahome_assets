# Altar editor comparison

ui-reference-edit.png: approved UI reference.
iphone-gl-before-floating-editor.png: physical iPhone 11 Expo GL render, captured before the floating editor update. It includes the 3D layer only; it is not a full UI screenshot.

simulator-editor-expanded.png: complete React Native editor UI on iPhone 17 Pro simulator. Uses the isolated WebView comparison renderer on port 8083 for layout checks; the physical iPhone app keeps Expo GL. Shows the preserved existing draft, not a reset theme. Captured 2026-09-25.

Additional complete simulator UI states: collapsed, moved to the upper-right safe area and expanded, scene-view mode. Native React handlers / PanResponder events were invoked by the inspector. These captures verify layout, not real-finger performance. Existing draft preserved; no model transforms were edited.
