
## 2024-06-27 - Semantic Elements Provide Native Accessibility
**Learning:** In codebases heavily reliant on inline styles, interactive elements are sometimes implemented as `<span>` or `<div>` tags with `cursor: pointer` rather than semantic elements. This completely removes keyboard accessibility and screen reader support without manual ARIA handling.
**Action:** Always identify interactive non-semantic elements and convert them to native `<button type="button">` or `<a>` elements using the CSS reset pattern `background: "none", border: "none", padding: 0` to preserve the visual design while restoring native accessibility features.
