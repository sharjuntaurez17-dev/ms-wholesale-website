## 2026-06-14 - Interactive elements incorrectly styled as spans
**Learning:** The application's extensive use of inline styles occasionally leads to interactive elements like 'Sign up' or 'Forgot password' being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">`) with reset inline styles (e.g. `background: "none", border: "none", padding: 0`) to ensure proper screen reader support and keyboard focusability, without affecting the existing visual design.
