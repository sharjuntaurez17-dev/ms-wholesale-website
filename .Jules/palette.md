## 2026-07-25 - Interactive elements accessibility
**Learning:** Some standard interactive elements (like 'Forgot password?' or 'Sign up' triggers) are built using inline styles on non-interactive semantic tags (e.g., `<span>`), which breaks screen reader and keyboard accessibility on mobile designs.
**Action:** Always convert these elements into semantically appropriate `<button type="button">`, or `<a>` when they act as a link, using CSS resets like `background: 'none', border: 'none', padding: 0, font: 'inherit'` to preserve visual integrity while gaining accessibility.
