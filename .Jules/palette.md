## 2025-03-01 - Interactive Element Implementations
**Learning:** This application heavily relies on inline styles and frequently implements interactive elements (like 'Forgot password' or 'Sign up' links) using non-interactive `<span>` tags, which breaks keyboard accessibility.
**Action:** Always scan for interactive `<span>` or `<div>` elements and convert them to semantic `<button type="button">`, applying the style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain visual consistency.
