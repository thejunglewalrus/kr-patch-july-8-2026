# KR Lost Ark Patch Digest — July 8, 2026

English translation of the Korean Lost Ark July 8, 2026 update, built as a single
scrollable dark-themed page combining **four** official Korean sources.

**Live page (once deployed):** https://thejunglewalrus.github.io/kr-patch-july-8-2026/patch-2026-07-08.html

## Contents

- **Update Notice** ([Notice #13484](https://lostark.game.onstove.com/News/Notice/Views/13484)) —
  the July 8 regular maintenance notes: the new **Chronomancer** class launch, its
  growth-support events (exclusive jumping ticket + Accelerated Growth event),
  Maharaka Summer Camp co-op quest tuning, per-Ark-Passive card deck presets for
  support classes, and the usual bug-fix sweep.
- **Chronomancer Class Reveal** ([companion page](https://lostark.game.onstove.com/Event/Update/260708/DIMENSIONMASTER)) —
  the class's own landing page: full growth-event reward table (1660→1720) and
  the class-intro flavor text / Identity ("Dimension Clock") description not
  present in the notice body.
- **Chronomancer Open Avatar Package** ([cash-shop page](https://lostark.game.onstove.com/Event/Package/260708v2)) —
  the launch avatar/weapon selection chests and the Legendary "Eternity" avatar
  line (via Yoz's Jar).
- **Deep Wave Package** ([cash-shop page](https://lostark.game.onstove.com/Event/Package/260708)) —
  the 2026 summer swimwear cash-shop package: avatar/weapon/instrument lines,
  mounts, pets, wallpaper, and Prestige-tier items.

→ [`patch-2026-07-08.html`](patch-2026-07-08.html)

## Translation conventions

Direct translation only — no commentary, analysis, or extrapolation. The only
added material is the **Translation Notes** section (KR↔EN term cross-reference)
and the source/footer links. Class and mode names use the published Western
(NA/EU) client localization.

**Notable term choice:** 차원술사 is translated as **Chronomancer** — the official
Western client name revealed at LOA ON Summer — not the KR promotional page's own
stylized English wordmark "Dimension Master" (see Translation Notes for detail;
that wordmark is left untouched where it's baked into the source art, since it's
already in English).

## Structure

- `patch-2026-07-08.html` — the translation page (all 4 sources combined into one
  scrollable page with a collapsible table of contents; no separate index page).
- `images/` — downloaded banner/UI images from all 4 sources, surfaced via
  per-image Translation/Original toggle figures (decorative images with no baked
  text, like the Deep Wave hero shot, are shown plainly with no toggle).
- `style.css` — shared dark theme (shared with the rest of the `kr-patch-*` series).
- `assets/` — mascot, palm kicker icon, favicon.

## Notes for future updates to this page

- The Deep Wave package's `bg_event1`–`bg_event9` CSS background banners are pure
  decorative textures (pool deck, library, curtain, etc.) with no baked-in text —
  confirmed by inspection, not skipped by assumption. Only `bg_index` was kept.
- The Chronomancer companion/package pages are JS-rendered SPA shells; `curl`
  returns an empty shell. Use Playwright, read `document.body.innerText` for
  real DOM text and scan `getComputedStyle(el).backgroundImage` across all
  elements for the actual banner art (these pages render entirely via CSS
  background-image, not `<img>` tags — `document.querySelectorAll('img')` alone
  returns nothing useful here).
