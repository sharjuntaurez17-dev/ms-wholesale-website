## 2023-10-25 - Inaccessible span elements for buttons
**Learning:** The applications extensive use of inline styles occasionally leads to interactive elements being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">` or `<a>`) using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility.
