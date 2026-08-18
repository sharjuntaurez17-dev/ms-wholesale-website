## 2025-02-19 - Semantic Accessibility in React Inline Styles
**Learning:** High reliance on inline styles in this React app occasionally leads to interactive elements (like "Forgot password?" and "Sign up") being incorrectly implemented as `<span>` tags.
**Action:** Always convert these `<span>` elements to native semantic `<button type="button">` or `<a>` elements using the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain existing visual appearance while enabling keyboard accessibility and screen reader support.
