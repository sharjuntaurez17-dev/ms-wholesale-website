## 2026-07-27 - Interactive Element Accessibility
**Learning:** The application's extensive use of inline styles occasionally leads to interactive elements like 'Forgot Password' and 'Sign Up' links being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
