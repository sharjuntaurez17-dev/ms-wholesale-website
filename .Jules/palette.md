## 2024-10-07 - Interactive Spans to Buttons
**Learning:** The application extensively uses inline styles, leading to interactive elements like "Forgot password?" or "Sign up" links being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these `<span>` elements to native semantic elements (like `<button type="button">` or `<a>`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
