# Material Design 3 — Implementation Reference

> Source: m3.material.io + material-web.dev. Use this when building any MD3-influenced UI.

---

## 1. Color System

### Core Concept
MD3 uses **color roles** (not raw hex values). Every color in your theme maps to a semantic token.

### CSS Custom Properties (Full Color Scheme)

```css
:root {
  /* === PRIMARY === */
  --md-sys-color-primary: #6750A4;
  --md-sys-color-on-primary: #FFFFFF;
  --md-sys-color-primary-container: #EADDFF;
  --md-sys-color-on-primary-container: #21005D;

  /* === SECONDARY === */
  --md-sys-color-secondary: #625B71;
  --md-sys-color-on-secondary: #FFFFFF;
  --md-sys-color-secondary-container: #E8DEF8;
  --md-sys-color-on-secondary-container: #1D192B;

  /* === TERTIARY === */
  --md-sys-color-tertiary: #7D5260;
  --md-sys-color-on-tertiary: #FFFFFF;
  --md-sys-color-tertiary-container: #FFD8E4;
  --md-sys-color-on-tertiary-container: #31111D;

  /* === ERROR === */
  --md-sys-color-error: #B3261E;
  --md-sys-color-on-error: #FFFFFF;
  --md-sys-color-error-container: #F9DEDC;
  --md-sys-color-on-error-container: #410E0B;

  /* === SURFACE === */
  --md-sys-color-background: #FFFBFE;
  --md-sys-color-on-background: #1C1B1F;
  --md-sys-color-surface: #FFFBFE;
  --md-sys-color-on-surface: #1C1B1F;
  --md-sys-color-surface-variant: #E7E0EC;
  --md-sys-color-on-surface-variant: #49454F;
  --md-sys-color-surface-container-lowest: #FFFFFF;
  --md-sys-color-surface-container-low: #F7F2FA;
  --md-sys-color-surface-container: #F3EDF7;
  --md-sys-color-surface-container-high: #ECE6F0;
  --md-sys-color-surface-container-highest: #E6E0E9;

  /* === OUTLINE === */
  --md-sys-color-outline: #79747E;
  --md-sys-color-outline-variant: #CAC4D0;

  /* === INVERSE === */
  --md-sys-color-inverse-surface: #313033;
  --md-sys-color-inverse-on-surface: #F4EFF4;
  --md-sys-color-inverse-primary: #D0BCFF;
  --md-sys-color-shadow: #000000;
  --md-sys-color-scrim: #000000;
}

/* DARK THEME */
@media (prefers-color-scheme: dark) {
  :root {
    --md-sys-color-primary: #D0BCFF;
    --md-sys-color-on-primary: #381E72;
    --md-sys-color-primary-container: #4F378B;
    --md-sys-color-on-primary-container: #EADDFF;
    --md-sys-color-secondary: #CCC2DC;
    --md-sys-color-on-secondary: #332D41;
    --md-sys-color-secondary-container: #4A4458;
    --md-sys-color-on-secondary-container: #E8DEF8;
    --md-sys-color-background: #1C1B1F;
    --md-sys-color-on-background: #E6E1E5;
    --md-sys-color-surface: #1C1B1F;
    --md-sys-color-on-surface: #E6E1E5;
    --md-sys-color-surface-container: #211F26;
    --md-sys-color-outline: #938F99;
    --md-sys-color-outline-variant: #49454F;
  }
}
```

### Color Usage Rules
- **Primary** → interactive elements (buttons, links, selected states)
- **Secondary** → supporting UI (chips, secondary buttons)
- **Tertiary** → contrasting accent (call-to-action pops)
- **Surface** → card backgrounds, sheets, dialogs
- **On-[X]** → text/icons placed ON top of [X]
- **Container** → softer version of role for filled containers

---

## 2. Typography Scale

### Type Scale (15 Roles)

| Role | Size | Line Height | Weight | Usage |
|------|------|-------------|--------|-------|
| Display Large | 57sp/px | 64px | 400 | Hero headlines, landing pages |
| Display Medium | 45sp/px | 52px | 400 | Section headlines |
| Display Small | 36sp/px | 44px | 400 | Feature headlines |
| Headline Large | 32px | 40px | 400 | Page titles |
| Headline Medium | 28px | 36px | 400 | Card titles |
| Headline Small | 24px | 32px | 400 | Section titles |
| Title Large | 22px | 28px | 400 | List items, dialogs |
| Title Medium | 16px | 24px | 500 | App bars |
| Title Small | 14px | 20px | 500 | Subtitles |
| Body Large | 16px | 24px | 400 | Body copy |
| Body Medium | 14px | 20px | 400 | Smaller body copy |
| Body Small | 12px | 16px | 400 | Supporting text |
| Label Large | 14px | 20px | 500 | Buttons |
| Label Medium | 12px | 16px | 500 | Chips, tabs |
| Label Small | 11px | 16px | 500 | Captions, overlines |

### CSS Token Implementation

```css
:root {
  /* Typefaces */
  --md-ref-typeface-brand: 'Google Sans', 'Roboto', sans-serif;
  --md-ref-typeface-plain: 'Roboto', system-ui, sans-serif;

  /* Display */
  --md-sys-typescale-display-large-size: 3.5625rem;   /* 57px */
  --md-sys-typescale-display-large-line-height: 4rem; /* 64px */
  --md-sys-typescale-display-large-weight: 400;

  --md-sys-typescale-display-medium-size: 2.8125rem;  /* 45px */
  --md-sys-typescale-display-medium-line-height: 3.25rem;
  --md-sys-typescale-display-medium-weight: 400;

  --md-sys-typescale-display-small-size: 2.25rem;     /* 36px */
  --md-sys-typescale-display-small-line-height: 2.75rem;
  --md-sys-typescale-display-small-weight: 400;

  /* Headlines */
  --md-sys-typescale-headline-large-size: 2rem;       /* 32px */
  --md-sys-typescale-headline-large-line-height: 2.5rem;
  --md-sys-typescale-headline-medium-size: 1.75rem;   /* 28px */
  --md-sys-typescale-headline-medium-line-height: 2.25rem;
  --md-sys-typescale-headline-small-size: 1.5rem;     /* 24px */
  --md-sys-typescale-headline-small-line-height: 2rem;

  /* Body */
  --md-sys-typescale-body-large-size: 1rem;           /* 16px */
  --md-sys-typescale-body-large-line-height: 1.5rem;
  --md-sys-typescale-body-medium-size: 0.875rem;      /* 14px */
  --md-sys-typescale-body-medium-line-height: 1.25rem;
}

/* Apply typescale */
.display-large {
  font-size: var(--md-sys-typescale-display-large-size);
  line-height: var(--md-sys-typescale-display-large-line-height);
  font-weight: var(--md-sys-typescale-display-large-weight);
  font-family: var(--md-ref-typeface-brand);
  letter-spacing: -0.015625rem;
}
```

---

## 3. Elevation System

### Levels (0–5)

| Level | dp | Box Shadow CSS | Usage |
|-------|-----|----------------|-------|
| 0 | 0dp | none | Flat surfaces, body |
| 1 | 1dp | `0 1px 2px rgba(0,0,0,.3), 0 1px 3px 1px rgba(0,0,0,.15)` | Cards at rest |
| 2 | 3dp | `0 1px 2px rgba(0,0,0,.3), 0 2px 6px 2px rgba(0,0,0,.15)` | Filled buttons, FAB |
| 3 | 6dp | `0 4px 8px 3px rgba(0,0,0,.15), 0 1px 3px rgba(0,0,0,.3)` | Navigation drawer |
| 4 | 8dp | `0 6px 10px 4px rgba(0,0,0,.15), 0 2px 3px rgba(0,0,0,.3)` | Modal sheets |
| 5 | 12dp | `0 8px 12px 6px rgba(0,0,0,.15), 0 4px 4px rgba(0,0,0,.3)` | Dialogs, tooltips |

### CSS Elevation Tokens

```css
:root {
  --md-sys-elevation-0: none;
  --md-sys-elevation-1: 0 1px 2px rgba(0,0,0,.3), 0 1px 3px 1px rgba(0,0,0,.15);
  --md-sys-elevation-2: 0 1px 2px rgba(0,0,0,.3), 0 2px 6px 2px rgba(0,0,0,.15);
  --md-sys-elevation-3: 0 4px 8px 3px rgba(0,0,0,.15), 0 1px 3px rgba(0,0,0,.3);
  --md-sys-elevation-4: 0 6px 10px 4px rgba(0,0,0,.15), 0 2px 3px rgba(0,0,0,.3);
  --md-sys-elevation-5: 0 8px 12px 6px rgba(0,0,0,.15), 0 4px 4px rgba(0,0,0,.3);
}

/* Surface tint adds color at each elevation in dark mode */
.card-elevated {
  background: var(--md-sys-color-surface-container);
  box-shadow: var(--md-sys-elevation-1);
  transition: box-shadow 200ms cubic-bezier(0.2, 0, 0, 1);
}
.card-elevated:hover {
  box-shadow: var(--md-sys-elevation-2);
}
```

---

## 4. Motion System

### Easing Curves

| Name | CSS Value | Usage |
|------|-----------|-------|
| Standard | `cubic-bezier(0.2, 0, 0, 1)` | Elements moving within screen bounds |
| Standard Decelerate | `cubic-bezier(0, 0, 0, 1)` | Elements entering the screen |
| Standard Accelerate | `cubic-bezier(0.3, 0, 1, 1)` | Elements leaving the screen |
| Emphasized | `cubic-bezier(0.2, 0, 0, 1)` | Key hero animations |
| Emphasized Decelerate | `cubic-bezier(0.05, 0.7, 0.1, 1)` | Elements entering prominently |
| Emphasized Accelerate | `cubic-bezier(0.3, 0, 0.8, 0.15)` | Elements leaving prominently |

### Duration Tokens

| Token | Duration | Usage |
|-------|----------|-------|
| Short1 | 50ms | Micro animations |
| Short2 | 100ms | Icon transitions |
| Short3 | 150ms | Fade, chip expand |
| Short4 | 200ms | Button state changes |
| Medium1 | 250ms | List items |
| Medium2 | 300ms | Tabs, chips |
| Medium3 | 350ms | Dialogs enter |
| Medium4 | 400ms | Navigation transitions |
| Long1 | 450ms | Page transitions |
| Long2 | 500ms | Complex layouts |
| Long3 | 550ms | Persistent elements |
| Long4 | 600ms | Full-screen transitions |

### CSS Motion Tokens

```css
:root {
  /* Easings */
  --md-sys-motion-easing-standard: cubic-bezier(0.2, 0, 0, 1);
  --md-sys-motion-easing-standard-decelerate: cubic-bezier(0, 0, 0, 1);
  --md-sys-motion-easing-standard-accelerate: cubic-bezier(0.3, 0, 1, 1);
  --md-sys-motion-easing-emphasized: cubic-bezier(0.2, 0, 0, 1);
  --md-sys-motion-easing-emphasized-decelerate: cubic-bezier(0.05, 0.7, 0.1, 1);
  --md-sys-motion-easing-emphasized-accelerate: cubic-bezier(0.3, 0, 0.8, 0.15);

  /* Durations */
  --md-sys-motion-duration-short-4: 200ms;
  --md-sys-motion-duration-medium-2: 300ms;
  --md-sys-motion-duration-medium-4: 400ms;
  --md-sys-motion-duration-long-2: 500ms;
}

/* Scroll-reveal pattern */
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition:
    opacity var(--md-sys-motion-duration-medium-4) var(--md-sys-motion-easing-emphasized-decelerate),
    transform var(--md-sys-motion-duration-medium-4) var(--md-sys-motion-easing-emphasized-decelerate);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

---

## 5. Layout System

### Breakpoints

| Breakpoint | Min Width | Columns | Margin | Gutter |
|-----------|-----------|---------|--------|--------|
| Compact | 0px | 4 | 16px | 16px |
| Medium | 600px | 12 | 24px | 24px |
| Expanded | 840px | 12 | 24px | 24px |
| Large | 1240px | 12 | 24px | 24px |
| Extra-large | 1440px | 12 | 24px | 24px |

### CSS Grid Layout

```css
.layout-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  padding-inline: 16px;
}

@media (min-width: 600px) {
  .layout-grid {
    grid-template-columns: repeat(12, 1fr);
    gap: 24px;
    padding-inline: 24px;
  }
}

@media (min-width: 1240px) {
  .layout-grid {
    max-width: 1440px;
    margin-inline: auto;
  }
}
```

### Spacing Scale (4px base unit)
```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;
}
```

---

## 6. Shape System

```css
:root {
  --md-sys-shape-corner-none: 0px;
  --md-sys-shape-corner-extra-small: 4px;
  --md-sys-shape-corner-small: 8px;
  --md-sys-shape-corner-medium: 12px;
  --md-sys-shape-corner-large: 16px;
  --md-sys-shape-corner-extra-large: 28px;
  --md-sys-shape-corner-full: 9999px;
}

/* Shape usage: */
/* Buttons: full (pill) */
/* Cards: medium (12px) */
/* Dialogs: extra-large (28px) */
/* FAB: large (16px) or extra-large (28px) */
/* Chips: small (8px) */
/* Text fields: extra-small top (4px), none bottom */
```

---

## 7. Key Implementation Principles

1. **Never hard-code colors** — always use semantic tokens (`--md-sys-color-primary`, not `#6750A4`)
2. **State layers** — hover = 8% opacity overlay, focus = 12%, pressed = 12%, dragged = 16%
3. **Minimum touch target** = 48×48px (even if visual is smaller)
4. **Motion respects user preferences** — always add `@media (prefers-reduced-motion: reduce)`
5. **Elevation = depth signal** — don't use elevation decoratively; use it to signal interactivity
6. **Color contrast** — primary on surface must pass WCAG 4.5:1 (text) or 3:1 (large text)
