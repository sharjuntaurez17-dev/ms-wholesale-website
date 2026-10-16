## 2026-07-05 - Inline Styles Leading to Inaccessible Spans
**Learning:** The application's extensive use of inline styles occasionally leads to interactive elements (like 'Forgot password?' and 'Sign up' links) being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">`) using the CSS style reset `background: "none", border: "none", padding: 0` to maintain existing visual appearance while ensuring keyboard accessibility.
