## 2024-05-15 - Missing form semantic elements
**Learning:** Found that custom inline styles in this app result in clickable `<span>` elements instead of semantic `<button>` elements, breaking keyboard accessibility.
**Action:** When finding clickable `<span>` tags, always convert them to `<button type="button">` using style resets (`background: "none", border: "none", padding: 0`) to preserve the visual appearance while adding accessibility.
