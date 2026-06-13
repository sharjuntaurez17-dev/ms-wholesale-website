## 2024-06-13 - Replace Interactive Spans with Semantic Buttons
**Learning:** The application's heavy reliance on inline styles sometimes leads to implementing interactive UI components (such as "Forgot password" or "Sign up" links) as `<span>` tags. This creates keyboard accessibility and screen reader issues.
**Action:** Always replace interactive `<span>` tags with semantic `<button type="button">` or `<a>` elements and apply reset inline styles (`background: "none", border: "none", padding: 0`) to preserve the visual appearance without compromising accessibility.
