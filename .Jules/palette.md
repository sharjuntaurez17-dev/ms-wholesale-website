## 2024-09-28 - Avoid <span> for interactive elements
**Learning:** Found interactive elements (like "Forgot password?" and "Sign up") implemented as `<span>` tags with `cursor: "pointer"`. This pattern prevents keyboard navigation and screen reader accessibility, hurting overall UX.
**Action:** Always convert these `<span>` elements to native semantic elements (like `<button type="button">`) with a CSS reset (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain the exact visual design while automatically providing native focus states and keyboard interactability.
