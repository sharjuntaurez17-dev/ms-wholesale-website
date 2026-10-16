## 2024-07-23 - Convert styled spans to native buttons
**Learning:** Due to the application's extensive use of inline styles, interactive elements (like the "Forgot password?" link) are sometimes implemented as inaccessible `<span>` tags rather than native buttons or links.
**Action:** Always convert these `<span>` elements to native semantic elements (like `<button type="button">`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
