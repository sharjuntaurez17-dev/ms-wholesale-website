## 2024-05-24 - Interactive Elements as Spans
**Learning:** Due to the application's heavy reliance on inline styles, many interactive elements (like text links or "forgot password" buttons) were implemented as inaccessible `<span>` tags.
**Action:** Always convert these `<span>` elements into semantic `<button type="button">` elements with reset inline styles (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain design while ensuring proper keyboard focusability and accessibility.
