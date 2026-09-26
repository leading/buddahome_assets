# Tea rendering review — 2026-09-26

Current implementation:
- tea-native-absorption-55.jpg: physical iPhone / Expo GL, newest tea absorption shader. Original glass transmission remains 1, opacity remains 1; duplicate liquid sidewall is hidden.
- tea-web-glass-0/55/100.jpg: isolated browser scene copy, transparent cup empty/half/full.
- tea-web-opaque-55.jpg: same calibrated geometry with an opaque ceramic material to verify shared shading and depth occlusion. This is a renderer comparison, not a newly published asset.

Earlier experiments (not the final renderer): tea-iphone-*.png, tea-original-glass.jpg and tea-depth-glass.jpg. The obsolete tea-volume-final.jpg was captured before the shader update and has been removed to avoid misidentification.

Captured scene layout and stored user data were preserved. Browser images do not represent native GPU performance; the native capture is labeled separately. Teapots keep authored geometry and materials and have no generated internal liquid.
