## 2025-02-23 - Interactive elements styled as spans
**Learning:** The application occasionally uses `<span>` tags with `cursor: "pointer"` for interactive text links (like "Forgot password?" or "Sign up"). These are inaccessible via keyboard navigation.
**Action:** Always convert interactive `<span>` elements to semantic `<button type="button">` or `<a>` tags. Use a CSS style reset (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain their visual appearance while enabling keyboard focus and interaction.
