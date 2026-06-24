## 2024-05-18 - Semantic HTML in Form Components

**Learning:** When improving accessibility in heavily-styled UI components, it's common to find interactive elements like links or buttons mistakenly implemented as `<span>` tags.

**Action:** Always convert interactive elements to native, semantic HTML elements (like `<button type="button">` or `<a>`) to guarantee proper keyboard navigation and screen reader support. Use a CSS style reset (`background: "none", border: "none", padding: 0`) to seamlessly integrate semantic elements while preserving the original visual design. Also, ensure `htmlFor` and `id` pair explicit connections between labels and form fields.
