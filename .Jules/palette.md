## 2024-08-26 - Semantic Interactive Elements in Inline Styled UIs
**Learning:** This application heavily relies on inline styles, which has led to interactive elements (like "Forgot password?" and "Sign up" links) being incorrectly implemented as inaccessible `<span>` tags.
**Action:** When converting these to semantic `<button type="button">` or `<a>` elements for keyboard accessibility, apply the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain the existing visual appearance while gaining native semantic and accessibility benefits.
