# Dayfold — Design System

A calm Mac (and iOS) productivity app for shaping your day around habits, time, tasks,
the people you care about, and the gentle rhythm of roles. Dayfold is **not** a generic task
manager — it is a *soft daily operating space* for people who want structure without the
hustle. The whole system exists to keep that feeling: **clear, warm, intentional, quietly
premium.**

> Three words it must feel like: **calm · grounded · clear.**
> Two it must never feel like: **hustle · corporate.**

---

## Sources we were given

This system was built from a small but rich set of brand inputs. No production codebase or
Figma file was provided; if you have access to either, prefer them as the source of truth and
update the UI kits accordingly.

| Source | Path | Notes |
|---|---|---|
| Accent palette reference | `assets/reference-palette.png` | The 10 named accents, "pulled exactly from app screenshots." |
| App icon / logo | `assets/dayfold-icon.png` | The cream-gold **fold** mark on dark warm-brown. Treated as the canonical mark. |
| App screenshot — Today | `assets/app-today.png` | Real "Today" screen: habits row + schedule timeline. |
| App screenshot — Habit gallery | `assets/app-habits.png` | Real habit-gallery sheet. |

GitHub is connected — if Dayfold's repo gets shared, import the real screens/components and
re-derive the UI kits from code rather than from these screenshots.

### ⚠️ Open flags (please confirm)
- **Fonts are substitutes.** No original Dayfold font files were supplied. The app itself uses
  a bold rounded humanist sans (system-like). We stand in with **Hanken Grotesk** for UI/body.
  The "Impact headers" request is served by **Anton** (a web-quality Impact stand-in), used for
  marketing/brand moments only — never in-app. Swap in the real faces when available
  (`tokens/fonts.css`).
- **The Anton display face is loud by nature.** It reads confident on the warm palette, but if
  it ever feels too "shouty" for *calm/grounded*, say so and we'll dial the hero type back to a
  heavy weight of Hanken instead.
- The app UI kit is reconstructed from **two screenshots**, not source — pixel details
  (exact paddings, the Calendar/Projects/Hub screens) are interpreted.

---

## Content fundamentals — how Dayfold talks

The voice is **human, concrete, and quiet.** It speaks like a thoughtful friend, never like a
productivity coach or a SaaS landing page.

- **Person & address:** Second person — *"your day," "the view you'll open first."* Warm and
  direct. Occasional gentle imperative (*"Pick a few that matter."*).
- **Case:** Sentence case everywhere in product and prose. UPPERCASE is reserved for the Anton
  display headlines and small eyebrow labels (with wide tracking).
- **Tone:** Reassuring, unhurried, lightly poetic but always understandable. Concrete nouns
  (*habits, hours, birthdays, the studio email*) over abstractions (*workflows, productivity,
  optimization*).
- **What it avoids:** streaks/guilt language, "10x", "crush your goals," dashboards, metrics
  worship, AI hype, exclamation-mark energy. Calm, never mystical or foggy.
- **Signature lines (use as a yardstick):**
  - "Shape your day."
  - "A soft daily operating space — not another productivity machine."
  - "No streaks to defend. No dashboards to feed."
  - "Miss a day; the next day is still there waiting, no penalty attached."
  - "It's a mirror you can glance at, then close."
- **Emoji:** none. The brand does not use emoji.

---

## Visual foundations

### Color — warm paper + 10 earthy accents
Backgrounds read like **daylight on paper** (warm off-whites, `--paper-50` … `--paper-200`).
Ink is a **warm brown-charcoal**, never pure black (`--ink` `#3D372F`, headings `#2D2823`). The
darkest tone, `--ink-900` `#2A2420`, is the *fold-ink* lifted straight from the logo ground.

The **primary action color is camel** `#C2A079` (`--brand`) — the tan of the selected date,
the "Create a new habit" button, the active tab. **Clay taupe** `#7E6656` (`--brand-strong`) is
the deeper accent for links and emphasis. **Burnt ochre** `#D3A26D` (`--brand-gold`) echoes the
fold's highlight.

Ten accents drive everything categorical (roles, habits, schedule blocks). Each ships as a raw
value, a `-soft` wash (chip/icon backgrounds) and a `-deep` readable ink:
Clay · Terra rose · Burnt ochre · Sandstone · Olive earth · Sage moss · Dusty steel ·
Sky mineral · Muted lavender · Neutral gray. **Status stays muted** (olive = positive, ochre =
attention, terra = critical) — calm, never alarming. **Energy** is expressed indirectly through
free time, roles and rhythm; the `--energy-*` scale (sky → sage → ochre) is the softest hint, not
a loud meter.

### Type
- **Display / hero — Anton** (`--font-display`): heavy condensed, UPPERCASE, tight. Marketing
  covers and posters only. Never inside the app.
- **UI & body — Hanken Grotesk** (`--font-sans`): warm humanist grotesque. **700** for titles,
  **600** for section heads, **400** for body. Headings carry `-0.02em` tracking.
- **Numerals / time — JetBrains Mono** (`--font-mono`): clock, dates, durations (`30m`, `9:04`),
  percentages — anything that benefits from tabular alignment.
- Gentle ~1.26 scale, `12 → 62px`. In-app text never below ~13px; slide text never below 24px.

### Space, radius, shadow, motion
- **Spacing:** 4px base, generous. Cards breathe; lists have air.
- **Radii:** soft but not bubbly — `sm 8` (controls), `md 12` (chips), `lg 16` (cards),
  `xl 22`–`2xl 28` (panels/sheets), pill for date chips, toggles, segmented controls and the FAB.
- **Shadows:** warm brown-tinted, low and diffuse (`rgba(42,36,32,…)`) — *light on paper*, never
  hard drops. Many surfaces (the app's cream cards) use **no shadow at all**, just a tint shift.
- **Borders:** hairline and warm (`--border-subtle` / `--border-default`). The app leans on
  **fill contrast** (cream card on white) more than borders.
- **Motion:** quick and gentle — `120–320ms`, ease-out. Toggles slide, sheets rise, rings fill.
  **Nothing bounces.** No infinite decorative loops.

### Surfaces & imagery
- App pattern: a near-**white page** with **soft cream cards** (`--surface-sunken`), large
  rounded corners, and soft-tinted inner elements (habit bubbles, schedule blocks) that carry a
  colored left bar or ring.
- Imagery = **real product screenshots**, shown in soft device frames with a gentle shadow.
  We don't draw fake dashboards or invent UI. Photos/illustrations, if added later, should be
  warm-toned and calm.
- No gradients-as-decoration (one barely-there radial wash on marketing backgrounds is the
  ceiling), no glassmorphism, no neon, no left-border-accent cards.

---

## Iconography

Dayfold uses **clean line icons** — even stroke (~1.75px), rounded caps, no fill. This matches
the app's tab bar and habit glyphs almost exactly. We standardize on **[Lucide](https://lucide.dev)**,
loaded from CDN (`unpkg.com/lucide`), used via `<i data-lucide="name"></i>` + `lucide.createIcons()`.

> **Substitution flag:** the app's own icons (likely SF Symbols / a custom set) were not
> provided. Lucide is the closest match. If the real icon set surfaces, drop the SVGs into
> `assets/icons/` and document the swap here.

Common mappings: tabs → `square-check-big` (Tasks), `calendar`, `layout-list` (Today), `kanban`
(Projects), `layout-grid` (Hub). Habits → `glass-water`, `moon`, `sunrise`, `footprints`,
`book-open`, `flower-2`, `heart`, `croissant`, `wine-off`. Actions → `plus`, `ellipsis`, `clock`,
`repeat`, `zap`, `list-checks`. **No emoji. No unicode glyphs as icons.** Color icons with the
accent `-deep` tones on their `-soft` backgrounds.

---

## Index / manifest

**Root**
- `styles.css` — the single entry point consumers link. `@import`s only.
- `tokens/` — `colors.css`, `typography.css`, `spacing.css`, `fonts.css`, `base.css`.
- `assets/` — `dayfold-icon.png`, `reference-palette.png`, `app-today.png`, `app-habits.png`.
- `readme.md` (this file) · `SKILL.md` (Agent Skill wrapper).

**Foundation cards** (`guidelines/cards/`) — Design System tab specimens for Colors, Type,
Spacing and Brand (brand colors, accents, paper, ink, tints, status/energy; display/headings/
body/mono/scale; spacing/radii/shadows; app icon, wordmark, iconography).

**Components** (`components/`)
- `core/` — **Button, IconButton, Badge, SegmentedControl, Avatar, Switch, Checkbox, Input, Card**.
- `dayfold/` — product primitives: **HabitBubble, DateChip, ScheduleBlock, TaskRow**.
- Each has `<Name>.jsx`, `<Name>.d.ts`, `<Name>.prompt.md`; one `@dsCard` HTML per directory.
  Mount via `const { X } = window.DayfoldDesignSystem_cc912d` after loading `_ds_bundle.js`.

**UI kits** (`ui_kits/`)
- `app/` — the **Dayfold iOS/Mac app**, click-through: Today (habits + schedule timeline),
  Tasks (sections + FAB), Roles (time-by-role), and the Habit Gallery sheet. Composes the
  components inside an iPhone frame.
- `website/` — **marketing site** (`index.html`) + **welcome / onboarding guide**
  (`welcome.html`). Static HTML using the tokens + real screenshots.
- `deck/` — **release presentation** (`index.html`): cover, the idea, five spaces, Today &
  Habits highlights, a big statement, and a close. `<deck-stage>` shell.

---

## Using this system

For throwaway artifacts (slides, mocks, prototypes), copy the assets you need and build static
HTML — link `styles.css` for tokens and use Lucide for icons. For production work, read the
rules above and reference the components. Keep one primary (camel) action per view, lean on warm
fills over borders, and let the day breathe.
