# SS WIN Black Bag — Scroll-Driven Landing Page Design

Date: 2026-05-27
Status: Approved (pending spec review)

## Goal

A cinematic, single-page brand showcase for **MUTHU WIN · SS · KANGAYAM** premium Ponni Sortex Rice (black 26kg bag), inspired by the scroll-driven feel of eathungrytiger.com. The product commercial MP4 acts as the "flow": as the user scrolls, the video timeline scrubs forward/back.

Reference site analysis: eathungrytiger.com is a Webflow build using **Lenis** (smooth scroll) + **GSAP ScrollTrigger** + a pinned canvas animation. We reproduce the same *feel* with a native React + Vite stack.

## Decisions (locked)

- **Location:** Clone `github.com/sharjuntaurez17-dev/sswinblacklanding-page-` into a new sibling folder and build/push there.
- **Scroll technique:** Scrub the MP4 by scroll position (video pinned full-screen).
- **Scope:** Brand showcase only — no checkout, no enquiry form.
- **Theme:** Black + gold cinematic; green/red (from the SS logo) as small accents.
- **Language:** Tamil + English (mirrors the bag).
- **Scrub implementation:** Native `<video>` + `currentTime` driven by scroll (Approach A). No ffmpeg/frame-sequence.

## Stack

- Vite + React 19 (matches the user's other repo)
- GSAP 3 + ScrollTrigger (scroll-pinning + progress)
- Lenis (smooth scroll, like the reference)
- Plain CSS with design tokens (no UI framework needed)

## Assets

Copied into `public/`:
- `public/ss-win-commercial.mp4` — from `Downloads/SS_WIN_rice_commercial_animation_202605271207.mp4`
- `public/ss-win-bag.png` — the 26kg black bag product render (provided image)

## Theme tokens

```
--bg:        #0a0a0a   (matte black)
--gold:      #d4af37   (metallic gold — headings, rules)
--gold-soft: #e8d488
--green:     #1e8f3e   (SS logo green — accent)
--red:       #d12027   (SS logo red — accent)
--text:      #f2ede1   (warm off-white body)
--muted:     #9a948a
```
Headings: an elegant serif (e.g. "Cormorant Garamond" / "Playfair Display" via Google Fonts). Body: a clean sans (Inter). Tamil: "Noto Sans Tamil".

## Page flow (single page, top → bottom)

1. **Hero** — full black screen. Gold serif wordmark "MUTHU WIN · SS · KANGAYAM", subline "27 Years of Excellence · 27 ஆண்டுகால சிறப்பு", scroll-down cue. Video first frame frozen/blurred behind, low opacity.
2. **Scrub stage (pinned, ~300vh scroll length)** — the commercial video fills the viewport. Scroll progress (0→1) maps to `video.currentTime` (0→duration). Overlaid captions fade in/out at progress milestones:
   - ~0.15: "Premium Quality Sortex Rice"
   - ~0.45: "நெய் கிச்சடி பொன்னி அரிசி" / "Ney Kichadi Ponni Rice"
   - ~0.75: "Naturally Rich · இயற்கையாக சத்தானது"
3. **Product highlights** — the 26kg bag image floats in; spec chips animate in: `26kg`, `Sortex Rice`, `Ponni`, `100% Customer Satisfaction`, `Natural Rich`.
4. **Brand story** — short narrative: 27 years of milling excellence, Kangayam roots, premium Ponni. Tamil + English paragraph pair.
5. **Footer** — brand mark, tagline, simple contact line (brand name / generic line — no form).

## Component structure (small, single-purpose files)

```
src/
  main.jsx              # React entry
  App.jsx               # composes sections, mounts Lenis
  hooks/
    useLenis.js         # init Lenis + GSAP ScrollTrigger ticker sync
  components/
    ScrubVideo.jsx      # pinned <video>, maps scroll progress -> currentTime
    Caption.jsx         # progress-driven fade caption overlay
    ScrollCue.jsx       # animated scroll-down indicator
  sections/
    Hero.jsx
    ScrubStory.jsx      # wraps ScrubVideo + Captions, owns the pinned scroll length
    Highlights.jsx
    Story.jsx
    Footer.jsx
  styles/
    tokens.css          # theme variables + font imports
    base.css            # reset + base typography
```

### Scrub logic (ScrubVideo.jsx)

- On mount: wait for `loadedmetadata` to read `video.duration`.
- ScrollTrigger pins the stage for a scroll distance (e.g. `+=300%`), `scrub: true`.
- On scroll progress `p` (0→1): set a *target* time = `p * duration`; ease the actual `currentTime` toward target each frame (lag smoothing) and use `requestVideoFrameCallback` when available for smoother seeking.
- `video` is `muted`, `playsInline`, `preload="auto"`, never `autoplay` (scroll controls it). `poster` = first frame.
- Mobile: same behavior; if seeking is too heavy on a device, fall back to letting it loop-play (progressive enhancement, not a hard requirement for v1).

## Error / edge handling (only what's real)

- If video metadata fails to load, show the bag image as a static hero backdrop (no crash).
- `prefers-reduced-motion`: disable scrubbing/pinning, show video poster + content statically.

## Out of scope (YAGNI)

- No checkout, cart, payments, enquiry form, CMS, analytics, multi-page routing, or backend.

## Success criteria

- `npm run dev` serves the page; scrolling smoothly scrubs the commercial video forward and reverse.
- Captions appear at the right scroll milestones; sections animate in.
- Black/gold theme matches the bag; Tamil + English render correctly.
- Builds clean with `npm run build`; pushed to the `sswinblacklanding-page-` repo.
