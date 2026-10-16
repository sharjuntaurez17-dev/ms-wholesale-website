## 2026-06-12 - Interactive Elements and Inline Styles
**Learning:** The application's extensive use of inline styles occasionally leads to interactive elements being incorrectly implemented as inaccessible `<span>` tags.
**Action:** Always convert these to native semantic elements (like `<button type="button">`) with reset inline styles (`background: 'none', border: 'none', padding: 0`) to maintain the existing visual appearance while improving keyboard navigability and screen reader support.
