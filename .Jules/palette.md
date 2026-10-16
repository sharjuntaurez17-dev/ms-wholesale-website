## 2024-06-16 - Interactive Spans
**Learning:** Interactive UI text elements (like "Forgot password?" and "Sign up") are sometimes implemented as `<span>` tags with `cursor: pointer`, breaking keyboard navigation and screen reader support.
**Action:** Always convert interactive `<span>`s to native `<button type="button">` or `<a>` elements and apply inline style resets (`background: 'none'`, `border: 'none'`, `padding: 0`, `font: 'inherit'`) to retain design parity while gaining accessibility.
