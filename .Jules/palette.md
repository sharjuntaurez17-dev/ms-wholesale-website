## 2025-03-02 - Keyboard accessibility issues with styled spans
**Learning:** The application's extensive use of inline styles occasionally leads to interactive elements (like "Forgot password?" and "Sign up" links) being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">` or `<a>`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
