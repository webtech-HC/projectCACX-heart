# CACX Kit v0.1 — Culturally Adaptive, Cognitively eXpressive UX

Single‑file playground that demonstrates culturally adaptive (locale, direction, numerals) and cognitively expressive (tone, verbosity, density, guided mode) UX patterns. Built accessibility‑first with high contrast, strong focus styles, keyboard navigation, and `prefers-reduced-motion` support.

## What’s inside

- **Communication‑style switcher:** toggles **Tone** (casual/formal), **Verbosity** (brief/detailed), **Density** (cozy/compact), and **Emoji** (off/minimal/full). Choices persist in `localStorage`.- **Internationalization demo:** languages **English**, **Français**, **العربية** with direction (`ltr`/`rtl`) and numeral systems (Latin / Arabic‑Indic) reflected across UI.- **Guided Mode stepper:** chunked steps with live announcements to reduce cognitive load.- **Container Queries:** components adapt to their **container** width, not just the viewport.- **Wide‑gamut color:** uses `lch()` with graceful fallback in modern browsers.- **Icons:** Font Awesome (CDN).

## Customize

- **Colors / spacing / motion:** edit CSS variables at the top of `index.html`.- **Locales / copy:** update the `COPY` and `LOCALES` objects in the inline script.- **Patterns:** extend the stepper, add forms, or wire real auth (e.g., WebAuthn Passkeys).

## Accessibility checklist (starter)

- Keyboard navigation (Tab/Shift+Tab) reaches all interactive controls.- Focus styles are clearly visible.- Reduced‑motion users see minimal animation.- Color contrast meets or exceeds WCAG 2.2 AA.- RTL users get correct reading order and alignment.- Live region announcements use `aria-live` for changing content.

## Local preview

Just open `index.html` in any modern browser. No build step is needed.

---

*Made for experimentation and teaching. Consider this public‑domain for now unless you add a license.*
