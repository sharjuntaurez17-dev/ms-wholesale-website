## 2024-07-15 - Interactive Spans in Inline-Styled Codebase
**Learning:** Found multiple instances where interactive elements ("Forgot password?", "Sign up") were built using `<span>` tags rather than semantic buttons, causing major accessibility barriers for keyboard/screen reader users.
**Action:** When updating these legacy elements, use semantic `<button type="button">` with the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to flawlessly match the original inline visual design while restoring native accessibility.
