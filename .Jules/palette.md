## 2024-07-07 - Interactive Spans in Splitwork

**Learning:** This application heavily utilizes inline styles, and interactive text elements (like "Forgot password?" or "Sign up") were implemented as inaccessible `<span>` tags.
**Action:** When adding keyboard navigation and screen reader support, always convert these spans to native `<button type="button">` or `<a>` tags. Crucially, apply the CSS reset `background: "none", border: "none", padding: 0` to maintain the existing visual appearance perfectly.
