## 2024-05-15 - Interactive SPAN elements used as links
**Learning:** The application commonly uses `<span>` elements with `cursor: pointer` for interactive actions (like "Forgot password?" and "Sign up") which breaks native keyboard accessibility and screen reader interaction.
**Action:** Always convert these `<span>` elements to `<button type="button">` with a CSS style reset (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain visual design while fully enabling native accessibility features.
