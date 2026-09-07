## 2024-10-24 - Interactive inline-styled spans
**Learning:** Interactive elements are occasionally incorrectly implemented as `<span>` tags due to the extensive use of inline styles.
**Action:** Convert these pseudo-interactive `<span>` tags to native semantic elements like `<button type="button">` or `<a>` using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
