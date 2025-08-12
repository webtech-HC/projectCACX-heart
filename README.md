# CACX Kit v0.2 — Culturally Adaptive, Cognitively eXpressive UX

A single-file playground that demonstrates culturally adaptive (locale, direction, writing mode, numerals) and cognitively expressive (tone, verbosity, density, guided mode) UX patterns. Built accessibility-first with high contrast, strong focus styles, keyboard navigation, and `prefers-reduced-motion` support.

---

## Live Demo (GitHub Pages)

1. Create a new repo and add these files at the **repo root**:
   - `index.html` (the demo)
   - `.nojekyll` (empty file; disables Jekyll and serves files as-is)
   - `README.md` (this file)

2. Push to GitHub, then open **Settings → Pages**:
   - **Source:** *Deploy from a branch*
   - **Branch:** `main` (or `master`) / **Root**
   - Click **Save**.
   - After ~1–2 minutes, your site will be available at  
     `https://<your-username>.github.io/<your-repo>/`

> Using a custom domain? Add it in **Settings → Pages** and create a `CNAME` record at your DNS host.

---

## What’s Inside

- **Communication-style switcher**  
  Toggle **Tone** (casual/formal), **Verbosity** (brief/detailed), **Density** (cozy/compact), and **Emoji** (off/minimal/full). Choices persist via `localStorage`.

- **Internationalization (i18n) with cultural signals**  
  Languages: **English (EN)**, **Español (ES)**, **Français (FR)**, **日本語 (JA)**, **中文 (ZH)**.  
  Locale switches update UI labels and font stacks (Noto Sans JP/SC).  
  **Optional vertical writing** for JA/ZH via toolbar (**Writing → Vertical**) using
  `writing-mode: vertical-rl; text-orientation: mixed;`.

- **Guided Mode stepper**  
  Chunk tasks into small steps with `aria-live` announcements to reduce cognitive load.

- **Container Queries**  
  Components adapt to the **space of their container**, not just the viewport.

- **Wide-gamut color**  
  Uses `lch()` (with graceful fallback) for perceptually uniform color.

- **Icons via CDN**  
  Font Awesome (Free) is linked from a CDN—no asset pipeline required.

---

## Accessibility (starter checklist)

- Keyboard navigation (Tab/Shift+Tab) reaches all interactive controls.  
- High-contrast text, visible focus outlines.  
- Honors `prefers-reduced-motion`.  
- No color-only state communication (icons/labels used).  
- RTL/vertical writing supported where applicable.  
- Live updates use `aria-live="polite"`.

> Note: This kit is a demo; run your own audits (e.g., Axe/ARC/Pa11y) and manual checks.

---

## Customize

- **Colors / spacing / motion**: Edit CSS variables at the top of `index.html`.
- **Locales / copy**: Update the `COPY` and `LOCALES` objects in the inline script.
- **Writing mode (JA/ZH)**: Toggle in the toolbar; class `vwrite` scopes vertical typesetting.
- **Patterns**: Extend the stepper, add forms, or wire real auth (e.g., WebAuthn/Passkeys).

---

## Local Preview

Just open `index.html` in a modern browser. No build step is needed.

---

## Roadmap (v0.3 ideas)

- **Disability-first toggles**:
  - *Readable Text*: larger line-height/word-spacing + dyslexia-friendly option.
  - *Numbers-friendly*: tabular figures, clear grouping, disambiguated glyphs.
  - *Larger Targets*: meet WCAG pointer target guidelines.
  - *Visual Alerts API*: toast/banners that never rely on sound alone.
  - *Landmarks & Skip Link*: nav/region semantics, skip to content.
  - *Passkeys flow*: real WebAuthn UI states (success/fallback/recovery).

---

## Files

- `index.html` – the entire demo (HTML/CSS/JS inline)  
- `.nojekyll` – empty file to disable Jekyll on GitHub Pages  
- `README.md` – this file  
- *(optional)* `cacx-kit-v0.1.html` – earlier single-file version

---

## Credits

- **Icons**: [Font Awesome Free (CDN)](https://fontawesome.com/)  
- **Fonts**: [Noto Sans JP](https://fonts.google.com/specimen/Noto+Sans+JP), [Noto Sans SC](https://fonts.google.com/specimen/Noto+Sans+SC)

---

## License

No license is included. If you plan to reuse/modify, consider adding a license (MIT/Apache-2.0/etc.) to your repository.

---

### Changelog

**v0.2**
- Added locales: **EN, ES, FR, JA, ZH**.
- Locale-aware font stacks (Noto Sans JP/SC).
- Optional **vertical writing** demo for JA/ZH.
- Internationalized UI labels in the toolbar.

**v0.1**
- Initial release with tone/verbosity/density/emoji, EN/FR/AR, guided mode, container queries, LCH colors.

