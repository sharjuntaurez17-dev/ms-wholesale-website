## 2024-05-24 - Convert interactive spans to buttons
**Learning:** This application makes heavy use of inline styles, which sometimes leads to interactive elements (like "Forgot password?" and "Sign up" links) being incorrectly implemented as inaccessible `<span>` tags.
**Action:** When making these interactive elements keyboard accessible, convert them to native `<button type="button">` or `<a>` elements and apply the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain the existing visual appearance while enabling keyboard accessibility.
