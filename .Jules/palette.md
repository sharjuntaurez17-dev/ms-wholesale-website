## 2026-07-11 - Interactive text elements implemented as `<span>`
**Learning:** Due to heavy inline-styling workflows in this repository, developers frequently implement interactive text (like 'Sign up' or 'Forgot password?') as `<span>` tags with `cursor: pointer` rather than native semantic interactive elements.
**Action:** Actively scan for and convert interactive `<span>` and `<div>` elements into native `<button>` or `<a>` tags, utilizing a style reset (`background: none`, `border: none`, `padding: 0`, `font: inherit`) to ensure keyboard accessibility without breaking the visual design.
