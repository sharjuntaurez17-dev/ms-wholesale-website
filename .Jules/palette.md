## 2026-08-04 - Inaccessible inline styles interactive elements
**Learning:** The application's extensive use of inline styles often leads to interactive elements (like 'Forgot password?' and 'Sign up' buttons) being incorrectly implemented as inaccessible `<span>` tags, failing keyboard accessibility constraints.
**Action:** Always convert these `<span>` tags to native semantic elements (like `<button type="button">`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
