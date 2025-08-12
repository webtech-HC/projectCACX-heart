# CACX Kit v0.3 — Culturally Adaptive, Cognitively eXpressive UX

A single-file playground that demonstrates culturally adaptive (locale, direction, **optional vertical writing**, numerals) and cognitively expressive (tone, verbosity, density, guided mode) UX patterns — built **accessibility-first** with high contrast, strong focus styles, keyboard navigation, and `prefers-reduced-motion` support.

---

## Live Demo (GitHub Pages)

1. Create a new repo and add these at the **repo root**:
   - `index.html` (the demo)
   - `.nojekyll` (empty file; disables Jekyll and serves files as-is)
   - `README.md` (this file)

2. Push to GitHub, then open **Settings → Pages**:
   - **Source:** *Deploy from a branch*
   - **Branch:** `main` (or `master`) / **Root**
   - Click **Save**.
   - After ~1–2 minutes:  
     `https://<your-username>.github.io/<your-repo>/`

> Custom domain? Add it in **Settings → Pages** and create a `CNAME` at your DNS host.

---

## What’s Inside

- **Communication-style switcher**  
  Toggle **Tone** (casual/formal), **Verbosity** (brief/detailed), **Density** (cozy/compact), and **Emoji** (off/minimal/full). Choices persist via `localStorage`.

- **Internationalization (i18n) with cultural signals**  
  Languages: **English (EN)**, **Español (ES)**, **Français (FR)**, **日本語 (JA)**, **中文 (ZH)**.  
  Locale switches update UI labels and font stacks (Noto Sans JP/SC).  
  **Optional vertical writing** (JA/ZH) via toolbar (**Writing → Vertical**) using
  `writing-mode: vertical-rl; text-orientation: mixed;`.

- **Guided Mode stepper**  
  Chunk tasks into small steps with `aria-live` announcements to reduce cognitive load.

- **Container Queries**  
  Components adapt to the **space of their container**, not just the viewport.

- **Wide-gamut color**  
  Uses `lch()` (with graceful fallback) for perceptually uniform color.

- **Icons via CDN**  
  Font Awesome Free (CDN) — no asset pipeline required.

---

## Accessibility (starter checklist)

- Keyboard navigation (Tab/Shift+Tab) reaches all interactive controls.  
- High-contrast text, visible focus outlines.  
- Honors `prefers-reduced-motion`.  
- No color-only state communication (icons/labels used).  
- RTL/vertical writing supported where applicable.  
- Live updates use `aria-live="polite"`.

> This kit is a demo; run your own audits (Axe/ARC/Pa11y) and manual checks.

---

## Customize

- **Colors / spacing / motion** — Edit CSS variables at the top of `index.html`.  
- **Locales / copy** — Update the `COPY` and `LOCALES` objects in the inline script.  
- **Writing mode (JA/ZH)** — Toggle in the toolbar (`vwrite` scope).  
- **Patterns** — Extend the stepper, add forms, or wire real auth (WebAuthn/Passkeys).

---

## Local Preview

Open `index.html` in any modern browser. No build step is needed.

---

## v0.3 Updates (Disability-first)

New **Accessibility** toolbar with:

- **Readable Text** — dyslexia-friendly spacing/line-height.  
- **Numbers-friendly** — tabular figures; numeric formatting demo.  
- **High Contrast** — stronger tokens; targets ≥3:1 for UI elements.  
- **Larger Targets** — comfort mode at ~44×44 CSS px (aligns with WCAG 2.5.8 guidance).

Plus:

- **Tint overlay** (adjustable hue/opacity) — emulate “yellow paper” style reading aids.  
- **Skip link** and **live regions** (`aria-live="polite"` and `role="alert"`).  
- **Dwell-to-activate** demo button (eye-tracking friendly).  
- Kept **vertical writing** demo (JA/ZH), i18n for EN/ES/FR/JA/ZH.

---

## Roadmap (v0.4 ideas)

- **Scan Mode** (one-switch sequential focus) for switch/eye users.  
- **Media component** with captions, transcript, and an optional **sign-language slot**.  
- **Form patterns** with explicit labels, errors (`role="alert"`), and undo-instead-of-error flows.  
- **Design tokens build** (DTCG → CSS vars & TS types) and theme packs.  
- **Color-blind safe states** + designer-side CVD simulator filters (for QA).

---

## Files

- `index.html` — the entire demo (HTML/CSS/JS inline)  
- `.nojekyll` — empty file to disable Jekyll on GitHub Pages  
- `README.md` — this file

---

## Credits

- **Icons**: [Font Awesome Free](https://fontawesome.com/) (CDN)  
- **Fonts**: [Noto Sans JP](https://fonts.google.com/specimen/Noto+Sans+JP), [Noto Sans SC](https://fonts.google.com/specimen/Noto+Sans+SC)

---

## License

No license is included. If you plan to reuse/modify, consider adding a license (MIT/Apache-2.0/etc.) to your repository.
